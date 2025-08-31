## ⚡ Bağımlılık Önbellekleme (dependency caching)

İş akışları (workflows) için hız ve verimlilik sağlamak amacıyla bağımlılık önbellekleme hakkında bilgi edinin.

## ℹ️ İş akışı bağımlılık önbellekleme hakkında (about workflow dependency caching)

İş akışı çalıştırmaları (workflow runs), çoğunlukla aynı çıktıları veya indirilen bağımlılıkları yeniden kullanır. Örneğin, Maven, Gradle, npm ve Yarn gibi paket ve bağımlılık yönetim araçları indirilen bağımlılıkların yerel bir önbelleğini tutar.

GitHub tarafından barındırılan koşucularda (GitHub-hosted runners) işler, temiz bir koşucu imajında başlar ve her seferinde bağımlılıkların indirilmesi gerekir. Bu durum ağ kullanımını artırır, çalışma süresini uzatır ve maliyeti yükseltir. GitHub, bağımlılıklar gibi sık kullanılan dosyaları iş akışlarında yeniden oluşturma süresini hızlandırmak için bu dosyaları önbelleğe alabilir.

### 📝 Not (note)

Kendi barındırılan koşucular (self-hosted runners) kullanıldığında, iş akışı çalıştırmalarından gelen önbellekler GitHub’a ait bulut depolamada saklanır. Müşteriye ait depolama çözümü yalnızca GitHub Enterprise Server ile kullanılabilir.

## ⚖️ Artifaktlar ve bağımlılık önbellekleme (artifacts versus dependency caching)

Artifaktlar (artifacts) ve önbellekleme (caching) benzer görünür çünkü ikisi de dosyaları GitHub’da depolamanıza olanak tanır, ancak farklı kullanım durumları vardır ve birbirinin yerine kullanılamazlar.

* **Önbellekleme kullanın (caching):** İşler veya iş akışı çalıştırmaları arasında sık değişmeyen dosyaları yeniden kullanmak istediğinizde, örneğin bir paket yönetim sisteminden gelen derleme bağımlılıkları (build dependencies).
* **Artifakt kullanın (artifacts):** Bir iş tarafından üretilen dosyaları, iş akışı tamamlandıktan sonra görüntülemek üzere saklamak istediğinizde, örneğin oluşturulmuş ikili dosyalar veya derleme günlükleri.

Daha fazla bilgi için bkz. İş akışı artifaktlarıyla veri depolama ve paylaşma (Store and share data with workflow artifacts).

## ⏭️ Sonraki adımlar (next steps)

İş akışlarınızda bağımlılık önbellekleme uygulamak için bkz. Bağımlılık önbellekleme başvurusu (Dependency caching reference).
