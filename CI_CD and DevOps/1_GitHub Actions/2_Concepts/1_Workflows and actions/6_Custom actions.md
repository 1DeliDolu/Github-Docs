## ⚙️ Özel İşlemler Hakkında (about custom actions)

İşlemler (actions), işleri (jobs) oluşturmak ve iş akışınızı (workflow) özelleştirmek için birleştirebileceğiniz bireysel görevlerdir. Kendi işlemlerinizi oluşturabilir veya GitHub topluluğu tarafından paylaşılan işlemleri kullanıp özelleştirebilirsiniz.

## ℹ️ Özel işlemler hakkında (about custom actions)

Depo (repository) ile etkileşime giren özel kod yazarak işlemler oluşturabilirsiniz. Bu, GitHub’ın API’leriyle veya herkese açık üçüncü taraf API’leriyle entegre olmayı da içerebilir. Örneğin, bir işlem npm modüllerini yayınlayabilir, acil sorunlar oluşturulduğunda SMS uyarıları gönderebilir veya üretime hazır kodu dağıtabilir.

Kendi işlemlerinizi yazabilir, iş akışınızda kullanabilir veya geliştirdiğiniz işlemleri GitHub topluluğuyla paylaşabilirsiniz. Geliştirdiğiniz işlemleri herkesle paylaşmak için deponuzun herkese açık olması gerekir.

İşlemler doğrudan bir makinede veya bir Docker konteynerinde çalıştırılabilir. Bir işlemin girdilerini (inputs), çıktıları (outputs) ve ortam değişkenlerini (environment variables) tanımlayabilirsiniz.

## 🛠️ İşlem Türleri (types of actions)

### 📝 Not (note)

Docker konteyner (Docker container), JavaScript ve bileşik işlemler (composite actions) oluşturabilirsiniz. İşlemler için, girdiler, çıktılar ve çalıştırma yapılandırmasını tanımlayan bir meta veri dosyası gerekir. İşlem meta veri dosyaları YAML sözdizimi kullanır ve dosya adı `action.yml` veya `action.yaml` olmalıdır. Tercih edilen format `action.yml`’dir.

| Tür (Type)        | Linux | macOS | Windows |
| ----------------- | ----- | ----- | ------- |
| Docker container  | ✅     | ❌     | ❌       |
| JavaScript        | ✅     | ✅     | ✅       |
| Composite Actions | ✅     | ✅     | ✅       |

### 🐳 Docker konteyner işlemleri (Docker container actions)

Docker konteynerleri, ortamı GitHub Actions kodu ile birlikte paketler. Bu, işlem tüketicisinin araçlar veya bağımlılıklar konusunda endişelenmesine gerek kalmayan daha tutarlı ve güvenilir bir çalışma birimi oluşturur.

Bir Docker konteyneri, belirli işletim sistemi sürümleri, bağımlılıklar, araçlar ve kodları kullanmanıza olanak tanır. Belirli bir ortam yapılandırmasında çalışması gereken işlemler için Docker ideal bir seçenektir çünkü işletim sistemini ve araçları özelleştirebilirsiniz. Ancak, konteyneri oluşturma ve alma gecikmesi nedeniyle Docker işlemleri, JavaScript işlemlerine göre daha yavaştır.

Docker işlemleri yalnızca Linux işletim sistemine sahip koşucularda (runners) çalıştırılabilir. Kendi barındırılan koşucular (self-hosted runners), Linux işletim sistemi kullanmalı ve Docker yüklü olmalıdır. Daha fazla bilgi için bkz. Self-hosted runners.

### 📜 JavaScript işlemleri (JavaScript actions)

JavaScript işlemleri doğrudan koşucu makinesinde çalıştırılabilir ve işlem kodunu çalıştırmak için kullanılan ortamdan ayırır. JavaScript işlemleri, Docker konteyner işlemlerine göre daha hızlı çalışır ve işlem kodunu basitleştirir.

JavaScript işlemlerinizin tüm GitHub barındırılan koşucularla (Ubuntu, Windows, macOS) uyumlu olmasını sağlamak için yazdığınız paketlenmiş JavaScript kodunun saf JavaScript olması ve başka ikili dosyalara (binaries) bağlı olmaması gerekir. JavaScript işlemleri doğrudan koşucuda çalışır ve koşucu imajında zaten mevcut olan ikilileri kullanır.

Node.js projesi geliştiriyorsanız, GitHub Actions Toolkit, projenizde kullanabileceğiniz paketler sunar. Daha fazla bilgi için bkz. `actions/toolkit` deposu.

### 🔗 Bileşik işlemler (composite actions)

Bileşik bir işlem, birden fazla iş akışı adımını tek bir işlemde birleştirmenizi sağlar. Örneğin, birden fazla `run` komutunu tek bir işlemde paketleyebilir ve ardından bu işlemi bir adım olarak çalıştıran bir iş akışı oluşturabilirsiniz. Örneğe bakmak için bkz. Bileşik işlem oluşturma (Creating a composite action).

## ⏭️ Sonraki adımlar (next steps)

Özel işlemlerinizi nasıl yöneteceğinizi öğrenmek için bkz. Özel işlemleri yönetme (Managing custom actions).
