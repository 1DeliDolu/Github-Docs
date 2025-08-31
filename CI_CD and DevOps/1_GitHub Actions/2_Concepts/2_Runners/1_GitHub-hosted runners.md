## 🖥️ GitHub tarafından barındırılan runner’lar (GitHub-hosted runners)

GitHub, iş akışlarını (workflow) çalıştırmak için barındırılan sanal makineler (virtual machine - VM) sunar. Sanal makine, GitHub Actions tarafından kullanılabilen araçlar, paketler ve ayarlardan oluşan bir ortam içerir.

---

## 📌 GitHub tarafından barındırılan runner’lara genel bakış (Overview of GitHub-hosted runners)

Runner’lar, bir GitHub Actions iş akışındaki (workflow) işleri (job) çalıştıran makinelerdir. Örneğin, bir runner havuzunuzu yerel olarak klonlayabilir, test yazılımlarını yükleyebilir ve ardından kodunuzu değerlendiren komutları çalıştırabilir.

GitHub, işleri çalıştırmak için kullanabileceğiniz runner’lar sağlar veya kendi runner’ınızı barındırabilirsiniz. Her GitHub tarafından barındırılan runner, GitHub tarafından barındırılan ve önceden yüklenmiş runner uygulaması ile diğer araçları içeren yeni bir sanal makinedir. Ubuntu Linux, Windows veya macOS işletim sistemleriyle kullanılabilir. GitHub tarafından barındırılan bir runner kullandığınızda, makine bakımı ve yükseltmeleri sizin için yapılır.

Standart GitHub-hosted runner seçeneklerinden birini seçebilir veya GitHub Team ya da GitHub Enterprise Cloud planında iseniz daha fazla çekirdekli ya da GPU işlemciyle güçlendirilmiş bir runner kullanabilirsiniz. Bu makineler “daha büyük runner (larger runner)” olarak adlandırılır. Daha fazla bilgi için bkz. Larger runners.

GitHub-hosted runner kullanımı için en az 70 kilobit/saniye yükleme ve indirme hızına sahip ağ erişimi gereklidir.

---

## 🖼️ Runner görüntüleri (Runner Images)

GitHub, standart barındırılan runner’larımız için kendi VM görüntü setimizi (images) yönetir. Buna macOS, x64 Linux ve Windows görüntüleri dahildir. Görüntülerin listesi ve içerdiği araçlar `actions/runner-images` deposunda yönetilir. Arm64 görüntülerimiz ise partner görüntülerdir ve `actions/partner-runner-images` deposunda yönetilir.

---

## 🛠️ GitHub’a ait görüntülerde önceden yüklenmiş yazılımlar (Preinstalled software for GitHub-owned images)

GitHub’a ait görüntülere dahil edilen yazılım araçları haftalık olarak güncellenir. Güncelleme süreci birkaç gün sürer ve ana dal (main branch) üzerindeki önceden yüklenmiş yazılım listesi dağıtım tamamlandıktan sonra güncellenir.

İş akışı günlüklerinde (workflow logs), tam olarak kullanılan runner üzerindeki önceden yüklenmiş araçlara bağlantı bulunur. Bu bilgiyi görmek için günlükte `Set up job` bölümünü genişletin. Bu bölümün altında `Runner Image` kısmını genişletin. `Included Software` bağlantısı, iş akışını çalıştıran runner’daki önceden yüklenmiş araçları gösterir.

Daha fazla bilgi için bkz. Viewing workflow run history.

GitHub-hosted runner’lar, yukarıda belirtilen paketlerin yanı sıra işletim sisteminin varsayılan yerleşik araçlarını da içerir. Örneğin, Ubuntu ve macOS runner’ları `grep`, `find` ve `which` gibi araçları içerir.

Ayrıca, Windows ve Ubuntu runner görüntülerinin her derlemesi için bir yazılım malzeme listesi (SBOM) görüntüleyebilirsiniz. Daha fazla bilgi için bkz. Secure use reference.

Yüklenen yazılımlarla etkileşim için actions kullanmanızı öneririz. Bunun birkaç avantajı vardır:

* Genellikle actions, sürüm seçimi, argüman ve parametre geçirme gibi daha esnek işlevler sağlar.
* İş akışınızda kullanılan araç sürümlerinin yazılım güncellemelerinden bağımsız olarak aynı kalmasını sağlar.

İstediğiniz bir aracı talep etmek için `actions/runner-images` deposunda bir konu (issue) açabilirsiniz. Bu depo ayrıca runner’lar üzerindeki tüm büyük yazılım güncellemeleri hakkında duyuruları da içerir.

Not:
GitHub-hosted runner’lara ek yazılımlar da kurabilirsiniz. Bkz. Customizing GitHub-hosted runners.

---

## ☁️ GitHub-hosted runner’ların kullandığı bulut sağlayıcılar (Cloud hosts used by GitHub-hosted runners)

GitHub, Linux ve Windows runner’ları Microsoft Azure üzerindeki sanal makinelerde, yüklenmiş GitHub Actions runner uygulamasıyla barındırır. GitHub-hosted runner uygulaması, Azure Pipelines Agent’in bir çatallanmış sürümüdür (fork). Tüm Azure sanal makineleri için gelen ICMP paketleri engellenmiştir, bu nedenle `ping` veya `traceroute` komutları çalışmayabilir. GitHub, macOS runner’larını da Azure veri merkezlerinde barındırır.

---

## 🔄 İş akışı sürekliliği (Workflow continuity)

GitHub Actions servisleri geçici olarak kullanılamazsa, tetiklendikten sonraki 30 dakika içinde kuyruğa alınmayan iş akışı çalıştırmaları iptal edilir. Örneğin, bir iş akışı tetiklenirse ve GitHub Actions servisleri 31 dakika veya daha uzun süre kullanılamazsa, bu iş akışı çalıştırması işlenmez.

Ayrıca, iş akışı kuyruğa başarıyla alınmış, ancak 45 dakika içinde bir GitHub-hosted runner tarafından işlenmemişse, bu bekleyen iş akışı çalıştırması iptal edilir.

---

## 📂 etc/hosts dosyası (The etc/hosts file)

GitHub-hosted runner’lar, çeşitli kripto para madenciliği havuzlarına ve kötü amaçlı sitelere ağ erişimini engelleyen bir `etc/hosts` dosyasıyla sağlanır. Örneğin, `MiningMadness.com` ve `cpu-pool.com` gibi adresler localhost’a yönlendirilir, böylece önemli bir güvenlik riski oluşturmazlar.
