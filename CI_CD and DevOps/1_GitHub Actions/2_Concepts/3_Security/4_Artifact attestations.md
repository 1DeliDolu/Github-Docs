## 📦 Artifact Attestations (eser beyanları)

Eser beyanlarının (artifact attestations) kullanımını ve güvenlik avantajlarını anlayın.

---

### 📖 Genel Bakış (overview)

Eser beyanları, oluşturduğunuz yazılım için değiştirilemez köken (provenance) ve bütünlük garantileri oluşturmanıza olanak tanır. Böylece yazılımınızı kullanan kişiler, yazılımınızın nerede ve nasıl oluşturulduğunu doğrulayabilir.

Yazılımınızla birlikte eser beyanları ürettiğinizde, derlemenizin kökenini belirleyen kriptografik olarak imzalanmış iddialar oluşturursunuz. Bu iddialar şunları içerir:

* Eserle ilişkili iş akışına bağlantı
* Eser için depo (repository), kuruluş (organization), ortam (environment), commit SHA ve tetikleyici olay (triggering event)
* Kökeni doğrulamak için kullanılan OIDC belirtecinden diğer bilgiler (daha fazla bilgi için bkz. **OpenID Connect**)

Ayrıca, ilişkili bir **SBOM (software bill of materials)** içeren eser beyanları da üretebilirsiniz. Derlemelerinizi kullanılan açık kaynak bağımlılıklarının bir listesiyle ilişkilendirmek şeffaflık sağlar ve kullanıcıların veri koruma standartlarına uymasını kolaylaştırır.

---

### 🏗️ SLSA Seviyeleri (SLSA levels for artifact attestations)

**SLSA (Supply-chain Levels for Software Artifacts)** çerçevesi, tedarik zinciri güvenliğini değerlendirmek için kullanılan endüstri standardıdır. Seviyeler halinde düzenlenmiştir ve her seviye yazılım tedarik zinciri için artan güvenlik ve güvenilirlik derecesini temsil eder.

* **Artifact attestations tek başına SLSA v1.0 Build Level 2 sağlar.**
  Bu, eserinizi oluşturma talimatlarıyla (build instructions) ilişkilendirir.

* Daha ileri bir adım olarak, yalnızca bilinen ve doğrulanmış oluşturma talimatlarını kullanacak şekilde derlemeleri zorunlu kılabilirsiniz.
  Bunun harika bir yolu, derlemeyi kuruluşunuzdaki birçok depo tarafından paylaşılan **yeniden kullanılabilir bir iş akışında (reusable workflow)** gerçekleştirmektir.

* Yeniden kullanılabilir iş akışları, derleme süreci ile çağıran iş akışı arasında izolasyon sağlayarak **SLSA v1.0 Build Level 3** gereksinimlerini karşılayabilir.

Daha fazla bilgi için bkz. **Using artifact attestations and reusable workflows to achieve SLSA v1 Build Level 3**.

---

### ⚙️ GitHub’un Eser Beyanlarını Nasıl Ürettiği (how GitHub generates artifact attestations)

Eser beyanlarını oluşturmak için GitHub, yazılım eserlerini imzalama ve doğrulama için kapsamlı bir çözüm sunan açık kaynak projesi **Sigstore**’u kullanır.

* **Genel depolar (public repositories):** Sigstore Public Good Instance kullanır.
  Üretilen Sigstore paketi GitHub’da saklanır ve ayrıca internette herkese açık okunabilen değiştirilemez bir şeffaflık günlüğüne yazılır.

* **Özel depolar (private repositories):** GitHub’un Sigstore örneğini kullanır.
  Bu örnek, Public Good Instance ile aynı kod tabanını kullanır, ancak bir şeffaflık günlüğü içermez ve yalnızca GitHub Actions ile federasyon sağlar.

---

### ⏱️ Ne Zaman Beyan Üretilmeli (when to generate attestations)

Beyanları üretmek tek başına bir güvenlik faydası sağlamaz; faydanın gerçekleşmesi için bu beyanların doğrulanması gerekir. İşte bazı yönergeler:

**İmzalanması gerekenler:**

* Yayınladığınız ve insanların `gh attestation verify ...` komutu ile doğrulamasını beklediğiniz yazılımlar
* İnsanların çalıştıracağı ikili dosyalar (binaries), indirilecek paketler veya ayrıntılı içeriklerin hash değerlerini içeren manifestler

**İmzalanmaması gerekenler:**

* Yalnızca otomatik test için yapılan sık derlemeler
* Kaynak kodu dosyaları, dokümantasyon dosyaları veya gömülü görseller gibi tekil dosyalar

---

### 🔍 Eser Beyanlarını Doğrulama (verifying artifact attestations)

Eser beyanları yayımlayan yazılımları kullanıyorsanız, bu beyanları **GitHub CLI** ile doğrulayabilirsiniz.

Beyanlar, yazılımın nerede ve nasıl oluşturulduğu hakkında bilgi verdiğinden, bu bilgileri tedarik zinciri güvenliğinizi artıracak güvenlik politikaları oluşturmak ve uygulamak için kullanabilirsiniz.

⚠️ **Uyarı:**
Eser beyanları, bir eserin güvenli olduğunun garantisi değildir. Bunun yerine, eseri üreten kaynak koda ve derleme talimatlarına bağlantı sağlar. Bir yazılımı kullanmadan önce kendi politika kriterlerinizi tanımlamanız, içeriği değerlendirmeniz ve bilinçli bir risk kararı vermeniz gerekir.

---

### 📌 Sonraki Adımlar (next steps)

Derlemeleriniz için eser beyanları üretmeye ve doğrulamaya başlamak için bkz. **Using artifact attestations to establish provenance for builds**.
