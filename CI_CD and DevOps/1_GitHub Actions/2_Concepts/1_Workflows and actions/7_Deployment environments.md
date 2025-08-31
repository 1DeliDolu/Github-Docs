## 🌍 Dağıtım Ortamları (deployment environments)

Farklı ortamlar oluşturabilir ve bu ortamlara dağıtım yapabilirsiniz.

## ℹ️ Ortamlar hakkında (about environments)

Ortamlar (environments), üretim (production), hazırlık (staging) veya geliştirme (development) gibi genel bir dağıtım hedefini tanımlamak için kullanılır. Bir GitHub Actions iş akışı (workflow) bir ortama dağıtım yaptığında, bu ortam deponun (repository) ana sayfasında görüntülenir.

Ortamları şu amaçlarla kullanabilirsiniz:

* Bir işin devam etmesi için onay gerektirmek
* Hangi dalların (branches) bir iş akışını tetikleyebileceğini kısıtlamak
* Özel dağıtım koruma kuralları (custom deployment protection rules) ile dağıtımları kontrol altına almak
* Sırlara (secrets) erişimi sınırlamak

Daha fazla bilgi için bkz. Dağıtım için ortamları yönetme (Managing environments for deployment).

## 🛠️ İşlerde ortam kullanımı (environments in jobs)

Bir iş akışındaki (workflow) her iş (job) tek bir ortama referans verebilir. Ortam için yapılandırılmış tüm koruma kuralları (protection rules), bu ortama referans veren iş koşucuya (runner) gönderilmeden önce geçmek zorundadır. İş, yalnızca koşucuya gönderildikten sonra ortama ait sırları (secrets) kullanabilir.

Bir iş akışı bir ortama referans verdiğinde, bu ortam deponun dağıtımlarında (deployments) görünür. Geçerli ve önceki dağıtımları görüntülemek hakkında daha fazla bilgi için bkz. Dağıtım geçmişini görüntüleme (Viewing deployment history).
