## 🚀 Sürekli Dağıtım (continuous deployment)

GitHub Actions ile doğrudan GitHub deponuzda özel sürekli dağıtım (continuous deployment, CD) iş akışları (workflow) oluşturabilirsiniz.

### 📋 Bu makalede

* Sürekli dağıtım hakkında
* GitHub Actions kullanarak sürekli dağıtım hakkında
* İş akışı şablonları ve üçüncü taraf actions
* Sonraki adımlar

---

## ℹ️ Sürekli Dağıtım Hakkında (about continuous deployment)

Sürekli dağıtım (continuous deployment, CD), yazılım güncellemelerini yayımlamak ve dağıtmak için otomasyonun kullanılmasını ifade eder. Tipik bir CD sürecinin parçası olarak, dağıtımdan önce kod otomatik olarak derlenir (build) ve test edilir.

Sürekli dağıtım genellikle sürekli entegrasyon (continuous integration) ile birlikte kullanılır. Sürekli entegrasyon hakkında daha fazla bilgi için bkz. `Continuous integration`.

---

## ⚙️ GitHub Actions Kullanarak Sürekli Dağıtım (about continuous deployment using GitHub Actions)

Yazılım ürününüzü dağıtmak için bir GitHub Actions iş akışı kurabilirsiniz. Ürününüzün beklendiği gibi çalıştığını doğrulamak için, iş akışınız deponuzdaki kodu derleyebilir ve dağıtımdan önce testlerinizi çalıştırabilir.

CD iş akışınızı bir olay meydana geldiğinde (örneğin, deponuzun varsayılan dalına yeni kod gönderildiğinde), belirli bir zamanlamayla, manuel olarak veya `repository dispatch webhook` kullanarak harici bir olay gerçekleştiğinde çalışacak şekilde yapılandırabilirsiniz. İş akışınızın ne zaman çalıştırılabileceği hakkında daha fazla bilgi için bkz. `Events that trigger workflows`.

GitHub Actions, dağıtımlar üzerinde size daha fazla kontrol sağlayan özellikler sunar. Örneğin:

* Bir işin devam edebilmesi için onay gerektirmek üzere `environments` kullanabilirsiniz.
* Hangi dalların (branch) bir iş akışını tetikleyebileceğini kısıtlayabilirsiniz.
* `secrets` erişimini sınırlayabilirsiniz.
* `concurrency` kullanarak CD hattınızı (pipeline) aynı anda en fazla bir devam eden dağıtım ve bir bekleyen dağıtımla sınırlayabilirsiniz.

Daha fazla bilgi için bkz. `Deploying with GitHub Actions` ve `Managing environments for deployment`.

---

## 📝 İş Akışı Şablonları ve Üçüncü Taraf Actions (workflow templates and third-party actions)

GitHub, Azure Web App gibi birçok popüler hizmet için dağıtım iş akışı şablonları sunar. Bir iş akışı şablonunu kullanmaya başlamak için bkz. `Using workflow templates` veya dağıtım iş akışı şablonlarının tam listesini inceleyin. Ayrıca belirli dağıtım iş akışlarına ilişkin daha ayrıntılı kılavuzlara göz atabilirsiniz, örneğin: `Deploying Node.js to Azure App Service`.

Birçok hizmet sağlayıcı ayrıca kendi hizmetlerine dağıtım için GitHub Marketplace üzerinde actions sunmaktadır. Tam liste için bkz. `GitHub Marketplace`.

---

## 🔑 Sonraki Adımlar (next steps)

GitHub Actions iş akışlarınız, OpenID Connect (OIDC) destekleyen bir bulut sağlayıcısındaki kaynaklara erişmesi gerektiğinde, iş akışlarınızı doğrudan bulut sağlayıcıya kimlik doğrulaması yapacak şekilde yapılandırabilirsiniz. Bu sayede bu kimlik bilgilerini uzun süreli `secret` olarak saklamayı bırakabilir ve ek güvenlik avantajları elde edebilirsiniz. Daha fazla bilgi için bkz. `OpenID Connect`.
