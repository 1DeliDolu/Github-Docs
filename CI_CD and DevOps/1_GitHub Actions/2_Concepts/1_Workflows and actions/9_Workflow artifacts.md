## 📦 İş Akışı Artifaktları (workflow artifacts)

GitHub Actions iş akışlarının (workflows) artifaktları olarak verileri depolama ve paylaşma hakkında bilgi edinin.

## ℹ️ İş akışı artifaktları hakkında (about workflow artifacts)

Bir artifakt (artifact), bir iş akışı çalıştırması (workflow run) sırasında üretilen bir dosya veya dosya koleksiyonudur. Artifaktlar, bir iş (job) tamamlandıktan sonra verileri kalıcı hale getirmenizi ve aynı iş akışındaki başka bir iş ile bu verileri paylaşmanızı sağlar. Örneğin, artifaktları bir iş akışı tamamlandıktan sonra derleme (build) ve test çıktılarını saklamak için kullanabilirsiniz.

GitHub, derleme artifaktlarını yüklemek ve indirmek için kullanabileceğiniz iki işlem sağlar: `upload-artifact` ve `download-artifact`.

Yaygın artifakt örnekleri:

* Günlük dosyaları (log files) ve çekirdek dökümleri (core dumps)
* Test sonuçları, hatalar ve ekran görüntüleri
* İkili (binary) veya sıkıştırılmış dosyalar
* Yük test performansı çıktısı ve kod kapsama (code coverage) sonuçları

## ⚖️ Artifaktlar ve bağımlılık önbellekleme (artifacts versus dependency caching)

Artifaktlar (artifacts) ve önbellekleme (caching) benzer görünebilir çünkü ikisi de dosyaları GitHub’da depolamanızı sağlar, ancak farklı kullanım alanları sunarlar ve birbirinin yerine kullanılamazlar.

* **Önbellekleme kullanın (caching):** İşler veya iş akışı çalıştırmaları arasında sık değişmeyen dosyaları yeniden kullanmak istediğinizde. Örneğin, paket yönetim sisteminden gelen derleme bağımlılıkları (build dependencies).
* **Artifakt kullanın (artifacts):** Bir iş tarafından üretilen dosyaları, iş akışı çalıştırması bittikten sonra görüntülemek için saklamak istediğinizde. Örneğin, oluşturulmuş ikili dosyalar veya derleme günlükleri.

Daha fazla bilgi için bkz. Bağımlılık önbellekleme başvurusu (Dependency caching reference).

## 🛡️ Derlemeler için artifakt beyanları oluşturma (generating artifact attestations for builds)

Artifakt beyanları (artifact attestations), oluşturduğunuz yazılım için sahteciliğe karşı korunan köken (provenance) ve bütünlük garantileri oluşturmanıza olanak tanır. Bu sayede yazılımınızı kullanan kişiler, yazılımınızın nerede ve nasıl oluşturulduğunu doğrulayabilir.

Bir yazılımınızla birlikte artifakt beyanları ürettiğinizde, derlemenizin kökenini kanıtlayan ve şunları içeren kriptografik olarak imzalanmış beyanlar oluşturursunuz:

* Artifakt ile ilişkili iş akışına bağlantı
* Artifakt için depo (repository), organizasyon (organization), ortam (environment), commit SHA ve tetikleyici olay (triggering event)
* Kökeni belirlemek için kullanılan OIDC belirtecinden (token) alınan diğer bilgiler. Daha fazla bilgi için bkz. OpenID Connect.

Ayrıca yazılım malzeme listesi (SBOM – Software Bill of Materials) içeren artifakt beyanları da üretebilirsiniz. Derlemelerinizi kullanılan açık kaynak bağımlılıkların listesiyle ilişkilendirmek, şeffaflık sağlar ve kullanıcıların veri koruma standartlarına uymasını mümkün kılar.

Derleme çalıştırması tamamlandıktan sonra, beyanlara oluşturulan artifaktların listesi altında erişebilirsiniz. Daha fazla bilgi için bkz. Derlemeler için köken oluşturmak amacıyla artifakt beyanlarını kullanma (Using artifact attestations to establish provenance for builds).

## 🗑️ Silinen iş akışı çalıştırmalarındaki artifaktlar (artifacts from deleted workflow runs)

Bir iş akışı çalıştırması silindiğinde, o çalıştırma ile ilişkili tüm artifaktlar da depolamadan silinir. Bir iş akışı çalıştırmasını GitHub Actions kullanıcı arayüzünü (UI), REST API’yi veya GitHub CLI’yı kullanarak silebilirsiniz. Bkz.:

* Bir iş akışı çalıştırmasını silme (Deleting a workflow run)
* `Delete a workflow run`
* `gh run delete`
