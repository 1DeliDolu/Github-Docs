## 🔄 Sürekli Entegrasyon (continuous integration)

GitHub Actions ile doğrudan GitHub deposunda özel sürekli entegrasyon (continuous integration, CI) iş akışları (workflow) oluşturabilirsiniz.

### 📋 Bu makalede

* Sürekli entegrasyon hakkında
* GitHub Actions kullanarak sürekli entegrasyon hakkında
* Sonraki adımlar

---

## ℹ️ Sürekli Entegrasyon Hakkında (about continuous integration)

Sürekli entegrasyon (continuous integration, CI), kodun sık sık paylaşılan bir depoya (repository) işlenmesini gerektiren bir yazılım pratiğidir. Daha sık kod işlemek, hataları daha erken tespit etmeyi sağlar ve geliştiricinin bir hatanın kaynağını bulurken hata ayıklaması gereken kod miktarını azaltır. Sık yapılan kod güncellemeleri ayrıca bir yazılım geliştirme ekibindeki farklı üyelerin yaptığı değişikliklerin birleştirilmesini de kolaylaştırır. Bu durum geliştiriciler için faydalıdır, çünkü daha fazla zamanı kod yazmaya, daha az zamanı hata ayıklamaya veya birleştirme (merge) çakışmalarını çözmeye ayırabilirler.

Kodunuzu deponuza işlediğinizde, bu işlemin hatalara yol açmadığından emin olmak için kodu sürekli olarak derleyip (build) test edebilirsiniz. Testleriniz; kod biçimlendirmesini kontrol eden `linter` araçlarını, güvenlik kontrollerini, kod kapsamı (code coverage), fonksiyonel testler ve diğer özel kontrolleri içerebilir.

Kodunuzu derlemek ve test etmek bir sunucu gerektirir. Kod güncellemelerini bir depoya göndermeden önce yerel olarak derleyip test edebilir veya depoya yapılan yeni kod işlemlerini kontrol eden bir CI sunucusu kullanabilirsiniz.

---

## ⚙️ GitHub Actions Kullanarak Sürekli Entegrasyon (about continuous integration using GitHub Actions)

GitHub Actions kullanarak CI, deponuzdaki kodu derleyebilen ve testlerinizi çalıştırabilen iş akışları (workflow) sunar. İş akışları, GitHub tarafından barındırılan sanal makinelerde (GitHub-hosted runners) veya sizin barındırdığınız makinelerde (self-hosted runners) çalıştırılabilir. Daha fazla bilgi için bkz. `GitHub-hosted runners` ve `Self-hosted runners`.

CI iş akışınızı, bir GitHub olayı (örneğin, deponuza yeni kod gönderildiğinde), belirli bir zamanlama ile veya `repository dispatch webhook` aracılığıyla meydana gelen harici bir olay gerçekleştiğinde çalışacak şekilde yapılandırabilirsiniz.

GitHub, CI testlerinizi çalıştırır ve her testin sonuçlarını pull request içinde sağlar, böylece dalınızdaki değişikliğin bir hata oluşturup oluşturmadığını görebilirsiniz. Bir iş akışındaki tüm CI testleri başarılı olduğunda, gönderdiğiniz değişiklikler bir ekip üyesi tarafından incelenmeye veya birleştirilmeye hazırdır. Bir test başarısız olduğunda, yaptığınız değişikliklerden biri bu başarısızlığa sebep olmuş olabilir.

Depoda CI kurduğunuzda, GitHub deponuzdaki kodu analiz eder ve kullandığınız dil ve çerçeveye (framework) göre CI iş akışları önerir. Örneğin, Node.js kullanıyorsanız, GitHub `Node.js` paketlerinizi yükleyen ve testlerinizi çalıştıran bir iş akışı şablonu önerir. GitHub’ın önerdiği CI iş akışı şablonunu kullanabilir, önerilen şablonu özelleştirebilir veya CI testlerinizi çalıştırmak için kendi özel iş akışı dosyanızı oluşturabilirsiniz.

Projeniz için CI iş akışları kurmanıza yardımcı olmanın yanı sıra, GitHub Actions yazılım geliştirme yaşam döngüsünün tamamında iş akışları oluşturmanıza da imkân tanır. Örneğin, projenizi dağıtmak (deploy), paketlemek veya yayımlamak (release) için actions kullanabilirsiniz. Daha fazla bilgi için bkz. `Writing workflows`.

Sık kullanılan terimlerin tanımı için bkz. `Understanding GitHub Actions`.

---

## 🚀 Sonraki Adımlar (next steps)

GitHub, çeşitli diller ve çerçeveler için CI iş akışı şablonları sunar. Bu şablonlarla sürekli entegrasyonu kurma konusunda öğreticiler için bkz. `Building and testing your code`.
