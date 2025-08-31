## 🛠️ Actions Runner Controller desteği (Support for Actions Runner Controller)

GitHub Support’tan (destek) Actions Runner Controller (ARC) ile ilgili yardım almadan önce bilmeniz gerekenler.

---

## 📌 Genel bakış (Overview)

Actions Runner Controller (ARC) projesi, GitHub tarafından yeni bir GitHub ürünü olarak yayımlanmak üzere devralınmıştır. Bunun sonucu olarak, şu anda iki ARC sürümü vardır:

* Topluluk tarafından sürdürülen eski ARC (legacy ARC)
* GitHub’ın **Autoscaling Runner Sets** sürümü

GitHub yalnızca en son **Autoscaling Runner Sets** sürümünü destekler. Eski ARC için destek yalnızca topluluk tarafından **Actions Runner Controller deposunda** sağlanır.

---

## 🎯 Actions Runner Controller için destek kapsamı (Scope of support for Actions Runner Controller)

Destek talebiniz GitHub Support ekibinin yardımcı olabileceği kapsam dışında ise, sorununuzu GitHub dışındaki yollarla çözmeniz için sonraki adımlar önerilebilir. Aşağıdaki durumlarda destek kapsamı dışında kalabilirsiniz:

* Topluluk tarafından sürdürülen eski ARC sürümü
* Bağımlılıkların kurulumu, yapılandırılması veya bakımı
* Template spec özelleştirmesi
* Konteyner orkestrasyonu (ör. Kubernetes kurulumu, ağ yapılandırması, ARC’de imaj oluşturma (DinD) vb.)
* Kubernetes politikalarının uygulanması
* Yönetilen Kubernetes sağlayıcıları veya sağlayıcıya özel yapılandırmalar
* ARC’nin Kubernetes modunda Runner Container Hooks kullanımı
* Helm dışındaki kurulum araçları
* Depolama sağlayıcıları (storage provisioners) ve PersistentVolumeClaim (PVC) yönetimi
* En iyi uygulamalar (ör. metrics server yapılandırma, imaj önbellekleme vb.)

ARC, farklı araçlar ve yapılandırmalarla başarıyla dağıtılabilse de, aşağıdaki durumlarda da destek kapsamı dışında kalabilirsiniz:

* Helm dışındaki kurulum araçları ile dağıtım
* Service account ve/veya template spec özelleştirmesi

Daha fazla bilgi için bkz. **Contacting GitHub Support**.

---

## ⚠️ Notlar (Notes)

* **OpenShift kümeleri** şu anda **genel önizleme** (public preview) aşamasındadır. Yapılandırma önerileri için Red Hat yönergelerine bakın.
* ARC yalnızca **GitHub Enterprise Server 3.9 ve üstü sürümlerde** desteklenmektedir.

---

## 🤝 GitHub Support ile çalışma (Working with GitHub Support for Actions Runner Controller)

GitHub Support, sizden Actions Runner Controller dağıtımınız hakkında sorular sorabilir ve destek talebinize şu bilgileri eklemenizi isteyebilir:

* Controller günlükleri (logs)
* Listener günlükleri
* Runner günlükleri
* Helm chart dosyaları (`values.yaml`)

---

## 📚 Yardım ve destek (Help and support)

Daha fazla bilgi ve destek için bkz. **Contacting GitHub Support**.
