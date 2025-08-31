## ⚖️ GitHub Actions ve GitHub Apps Karşılaştırması (GitHub Actions vs GitHub Apps)

GitHub Actions ve GitHub Apps arasındaki temel farkları öğrenerek kullanım senaryolarınıza en uygun olanı seçebilirsiniz.

GitHub Marketplace hem GitHub Actions hem de GitHub Apps sunar; her ikisi de değerli otomasyon ve iş akışı (workflow) araçlarıdır. Farklılıkları ve her seçeneğin avantajlarını anlamak, işiniz için en uygun olanı seçmenize yardımcı olacaktır.

---

## 🔧 GitHub Apps

* Sürekli çalışır (persistently run) ve olaylara hızlı tepki verebilir.
* Kalıcı veri gerektiğinde çok iyi çalışır.
* Zaman alıcı olmayan API istekleri ile en iyi şekilde çalışır.
* Sağladığınız bir sunucu veya işlem altyapısında çalışır.

---

## 🔄 GitHub Actions

* Sürekli entegrasyon (continuous integration) ve sürekli dağıtım (continuous deployment) gerçekleştirebilen otomasyon sağlar.
* Doğrudan `runner` makinelerinde veya `Docker` konteynerlerinde çalışabilir.
* Deponuzun bir kopyasına erişim sağlayabilir, bu sayede dağıtım ve yayınlama araçları, kod biçimlendiriciler ve komut satırı araçları kodunuza erişebilir.
* Kod dağıtımı yapmanızı veya bir uygulama sunmanızı gerektirmez.
* `secrets` oluşturmak ve kullanmak için basit bir arayüz sunar; bu sayede actions, üçüncü taraf hizmetlerle etkileşime geçebilir ve eylemi kullanan kişinin kimlik bilgilerini saklamanıza gerek kalmaz.
