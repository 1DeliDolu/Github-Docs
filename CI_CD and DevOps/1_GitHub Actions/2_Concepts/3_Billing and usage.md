## 💰 Faturalandırma ve kullanım (Billing and usage)

GitHub Actions iş akışları (workflows) için kullanım sınırları vardır. Bir deponun ücretsiz dakika ve depolama miktarını aşması durumunda kullanım ücretleri uygulanır.

---

## 📄 GitHub Actions için faturalandırma hakkında (About billing for GitHub Actions)

* **Kamuya açık depolarda (public repositories)** standart GitHub tarafından barındırılan çalıştırıcıların (GitHub-hosted runners) ve kendi barındırdığınız çalıştırıcıların (self-hosted runners) kullanımı ücretsizdir. Bkz. *Choosing the runner for a job*.
* **Özel depolarda (private repositories)** her GitHub hesabı, hesabın planına bağlı olarak GitHub tarafından barındırılan çalıştırıcılarla kullanılmak üzere belirli bir ücretsiz dakika ve depolama kotası alır. Bu miktarın ötesindeki her kullanım hesabınıza faturalandırılır. Daha fazla bilgi için bkz. *GitHub Actions billing*.

---

## 🌍 Kullanılabilirlik (Availability)

GitHub Actions tüm GitHub ürünlerinde mevcuttur, ancak eski depo başına planları (legacy per-repository plans) kullanan hesaplara ait özel depolarda kullanılamaz. Daha fazla bilgi için bkz. *GitHub’s plans*.

---

## 📏 Kullanım sınırları ve politika (Usage limits and policy)

* GitHub tarafından barındırılan çalıştırıcıları (GitHub-hosted runners) kullanırken GitHub Actions kullanımı için çeşitli sınırlar vardır. Bkz. *Actions limits*.
* Kullanım sınırlarının yanı sıra, GitHub Actions'ı GitHub Hizmet Şartları (Terms of Service) kapsamında kullanmanız gerekir. GitHub Actions'a özgü şartlar için bkz. *GitHub Additional Product Terms*.

---

## 📊 GitHub Actions kullanım ölçümleri (GitHub Actions usage metrics)

* Organizasyon sahipleri ve **"View organization Actions metrics"** iznine sahip kullanıcılar, organizasyonları için GitHub Actions kullanım ölçümlerini görüntüleyebilir.
* Bu ölçümler, Actions dakikalarının nasıl ve nerede kullanıldığını anlamanıza yardımcı olur. Daha fazla bilgi için bkz. *Viewing GitHub Actions metrics for your organization*.

⚠️ Önemli: GitHub Actions kullanım ölçümlerinde, görüntülenen metriklere dakika çarpanları (minute multipliers) uygulanmaz. Bunlar faturayı anlamanıza yardımcı olabilir, ancak asıl amaçları organizasyonunuzda Actions dakikalarının nasıl ve nerede kullanıldığını göstermek içindir. Daha fazla bilgi için bkz. *GitHub Actions billing*.

---

## 🔄 Yeniden kullanılabilir iş akışları için faturalandırma (Billing for reusable workflows)

Bir iş akışını yeniden kullandığınızda, faturalandırma her zaman çağıran iş akışı (caller workflow) ile ilişkilidir.

* GitHub tarafından barındırılan çalıştırıcıların atanması yalnızca çağıranın bağlamına göre değerlendirilir.
* Çağıran iş akışı, çağrılan depodan (called repository) GitHub tarafından barındırılan çalıştırıcıları kullanamaz.

Daha fazla bilgi için bkz. *Reuse workflows*.

---

## 📌 Sonraki adımlar (Next steps)

GitHub Actions kullanımınızı ve saklama politikalarınızı (retention policies) deponuz, organizasyonunuz veya kurumsal hesabınız (enterprise account) için yönetebilirsiniz. Daha fazla bilgi için bkz.:

* *Managing GitHub Actions settings for a repository*
* *Configuring the retention period for GitHub Actions artifacts and logs in your organization*
* *Disabling or limiting GitHub Actions for your organization*
* *Enforcing policies for GitHub Actions in your enterprise*
