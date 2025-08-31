## 🔑 Secrets (gizli bilgiler)

GitHub Actions iş akışlarında (workflows) kullanılan gizli bilgiler hakkında bilgi edinin.

### ℹ️ Gizli Bilgiler Hakkında (about secrets)

Gizli bilgiler (secrets), kuruluşunuzda (organization), deponuzda (repository) veya depo ortamlarınızda (repository environments) hassas bilgileri saklamanıza olanak tanır. Gizli bilgiler, GitHub Actions iş akışlarında kullanılmak üzere oluşturduğunuz değişkenlerdir.

GitHub Actions yalnızca bir iş akışında açıkça dahil ettiğinizde bir gizli bilgiyi okuyabilir.

### ⚙️ Gizli Bilgiler Nasıl Çalışır (how secrets work)

Gizli bilgiler, GitHub’a ulaşmadan önce şifrelenmeleri için **Libsodium sealed boxes** kullanır. Bu, gizli bilgi kullanıcı arayüzü (UI) veya REST API aracılığıyla gönderildiğinde gerçekleşir. Bu istemci taraflı şifreleme, GitHub altyapısında oluşabilecek kazara günlükleme (örneğin, istisna günlükleri veya istek günlükleri) ile ilgili riskleri en aza indirmeye yardımcı olur. Gizli bilgi yüklendikten sonra GitHub, onu iş akışı çalışma zamanına (workflow runtime) enjekte edebilmek için çözebilir.

### 🏢 Kuruluş Düzeyinde Gizli Bilgiler (organization-level secrets)

Kuruluş düzeyindeki gizli bilgiler, aynı gizli bilgileri birden fazla depo arasında paylaşmanıza olanak tanır ve bu da yinelenen gizli bilgiler oluşturma ihtiyacını azaltır. Bir kuruluş gizlisini tek bir yerde güncellemek, bu gizliyi kullanan tüm depo iş akışlarında değişikliğin etkili olmasını sağlar.

Bir kuruluş için gizli bilgi oluştururken, erişimi depoya göre sınırlamak için bir politika kullanabilirsiniz. Örneğin, erişimi tüm depolara verebilir veya erişimi yalnızca özel depolara ya da belirli bir depo listesine sınırlayabilirsiniz.

Ortam (environment) gizlileri için, erişimi kontrol etmek amacıyla gerekli onaylayıcıları etkinleştirebilirsiniz. Bir iş akışı görevi (workflow job), gerekli onaylayıcılar tarafından onay verilene kadar ortam gizlilerine erişemez.

Bir gizli bilgiyi bir eyleme (action) kullanılabilir kılmak için, iş akışı dosyanızda gizli bilgiyi bir giriş (input) veya ortam değişkeni (environment variable) olarak ayarlamanız gerekir. Eylemin hangi girişleri ve ortam değişkenlerini beklediğini öğrenmek için README dosyasını inceleyin. Bkz. **Workflow syntax for GitHub Actions**.

### 🔐 Kimlik Bilgisi İzinlerini Sınırlama (limiting credential permissions)

Kimlik bilgileri (credentials) oluştururken, mümkün olan en az izni vermeniz önerilir. Örneğin, kişisel kimlik bilgileri yerine dağıtım anahtarları (deploy keys) veya hizmet hesabı (service account) kullanın. Yalnızca salt okunur erişim gerekiyorsa, salt okunur izinler vermeyi düşünün ve erişimi olabildiğince sınırlayın.

Kişisel erişim belirteci (personal access token – classic) oluştururken, yalnızca en az gerekli kapsamları seçin. İnce ayarlı (fine-grained) kişisel erişim belirteci oluştururken, minimum izinleri ve depo erişimlerini seçin.

Kişisel erişim belirteci kullanmak yerine, GitHub Uygulaması (GitHub App) kullanmayı düşünün. GitHub Uygulamaları, ince ayarlı izinler ve kısa ömürlü belirteçler kullanır. Ayrıca kişisel erişim belirteçlerinden farklı olarak, bir GitHub Uygulaması bir kullanıcıya bağlı değildir. Bu nedenle, uygulamayı yükleyen kullanıcı kuruluşunuzdan ayrılsa bile iş akışı çalışmaya devam eder. Daha fazla bilgi için bkz. **Making authenticated API requests with a GitHub App in a GitHub Actions workflow**.

### 🛡️ Otomatik Olarak Gizlenen Gizli Bilgiler (automatically redacted secrets)

GitHub Actions, iş akışı günlüklerine (workflow logs) yazdırılan tüm GitHub gizli bilgilerini otomatik olarak gizler.

GitHub Actions ayrıca gizli olarak tanımlanan ancak gizli bilgi olarak saklanmayan bilgileri de gizler. Otomatik olarak gizlenen gizli bilgilerin listesi için bkz. **Secrets reference**.

Bir gizli bilginin değeri birden fazla şekilde dönüştürülebileceği için, bu gizleme her zaman garanti edilemez. Ayrıca, çalıştırıcı (runner) yalnızca mevcut görevde (job) kullanılan gizli bilgileri gizleyebilir. Sonuç olarak, gizli bilgilerin gizlenmesini sağlamak ve gizli bilgilerle ilgili diğer riskleri sınırlamak için izlemeniz gereken bazı güvenlik adımları vardır. Gizli bilgilerle ilgili güvenlik en iyi uygulamaları listesi için bkz. **Secrets reference**.

### 📚 Daha Fazla Okuma (further reading)

* Using secrets in GitHub Actions
* REST API endpoints for GitHub Actions Secrets
