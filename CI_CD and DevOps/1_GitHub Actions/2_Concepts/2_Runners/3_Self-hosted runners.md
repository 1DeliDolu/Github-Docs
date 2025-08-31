## 🏠 Kendi barındırdığınız runner’lar (Self-hosted runners)

Kendi runner’ınızı barındırabilir ve GitHub Actions iş akışlarınızdaki (workflows) işleri (jobs) çalıştırmak için kullanılan ortamı özelleştirebilirsiniz.

Kendi barındırdığınız runner (self-hosted runner), GitHub Actions’tan gelen işleri çalıştırmak için sizin kurup yönettiğiniz bir sistemdir.

---

## 📌 Kendi barındırdığınız runner’ların özellikleri (Self-hosted runners)

* GitHub-hosted runner’ların sağladığından daha fazla donanım, işletim sistemi ve yazılım aracı kontrolü sunar. Ancak işletim sistemini ve tüm diğer yazılımları güncel tutmaktan siz sorumlusunuz.
* GitHub Actions ile ücretsiz olarak kullanılabilir, ancak runner makinelerinizin bakım maliyetlerinden siz sorumlusunuz.
* Daha büyük işler (jobs) çalıştırmak için işlem gücü veya belleğe sahip özel donanım yapılandırmaları oluşturmanıza, yerel ağınızda bulunan yazılımları yüklemenize olanak tanır.
* Yalnızca self-hosted runner uygulaması için otomatik güncellemeler alır, ancak bu güncellemeleri devre dışı bırakabilirsiniz.
* Zaten ücretini ödediğiniz bulut servislerini veya yerel makineleri kullanabilir.
* Her iş yürütümü için temiz bir kopyaya (clean instance) ihtiyaç duymaz.
* Fiziksel, sanal, bir konteyner içinde, şirket içi (on-premises) veya bulutta olabilir.

Kendi barındırdığınız runner’ları yönetim hiyerarşisinin herhangi bir seviyesinde kullanabilirsiniz:

* Havuz (repository) düzeyindeki runner’lar tek bir havuza özeldir.
* Organizasyon (organization) düzeyindeki runner’lar bir organizasyondaki birden fazla havuz için işleri çalıştırabilir. Organizasyon sahipleri, hangi havuzların havuz düzeyinde self-hosted runner oluşturabileceğini seçebilir. Bkz. Disabling or limiting GitHub Actions for your organization.
* Son olarak, işletme (enterprise) düzeyindeki runner’lar bir işletme hesabındaki birden fazla organizasyona atanabilir.

---

## ⏭️ Sonraki adımlar (Next steps)

* Çalışma alanınızda bir self-hosted runner kurmak için bkz. Adding self-hosted runners.
* Self-hosted runner’lar için gereksinimler ile desteklenen yazılım ve donanım hakkında bilgi bulmak için bkz. Self-hosted runners reference.
