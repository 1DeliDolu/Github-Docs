## 🔑 GITHUB\_TOKEN

GitHub Actions iş akışlarında (workflows) **GITHUB\_TOKEN**’ın ne olduğunu, nasıl çalıştığını ve güvenli otomasyon için neden önemli olduğunu öğrenin.

### ℹ️ GITHUB\_TOKEN Hakkında (about the GITHUB\_TOKEN)

Her iş akışı görevinin (workflow job) başında, GitHub iş akışınızda kullanmanız için otomatik olarak benzersiz bir **GITHUB\_TOKEN** gizlisi (secret) oluşturur. Bu belirteci (token) iş akışı görevinizde kimlik doğrulama için kullanabilirsiniz.

GitHub Actions’ı etkinleştirdiğinizde, GitHub deponuza bir GitHub Uygulaması (GitHub App) yükler. **GITHUB\_TOKEN** gizlisi, bu GitHub Uygulaması için bir **yükleme erişim belirtecidir** (installation access token). Bu belirteci, deponuza yüklenen GitHub Uygulaması adına kimlik doğrulama yapmak için kullanabilirsiniz. Belirtecin izinleri, iş akışınızı içeren depo ile sınırlıdır. Daha fazla bilgi için bkz. **Workflow syntax for GitHub Actions**.

Her görev başlamadan önce, GitHub görev için bir yükleme erişim belirteci alır. **GITHUB\_TOKEN**, görev bittiğinde veya en fazla 24 saat içinde sona erer.

Belirteç ayrıca `github.token` bağlamında (context) da kullanılabilir. Daha fazla bilgi için bkz. **Contexts reference**.

### ⚙️ GITHUB\_TOKEN İş Akışı Çalışmalarını Ne Zaman Tetikler (when GITHUB\_TOKEN triggers workflow runs)

Bir deponun **GITHUB\_TOKEN**’ını kullanarak görevler yürüttüğünüzde, **workflow\_dispatch** ve **repository\_dispatch** istisnaları dışında, **GITHUB\_TOKEN** tarafından tetiklenen olaylar yeni bir iş akışı çalıştırmaz. Bu, yanlışlıkla yinelemeli (recursive) iş akışlarının oluşturulmasını önler.

Örneğin, bir iş akışı çalışması, deponun **GITHUB\_TOKEN**’ını kullanarak kod gönderirse (push), depoda push olaylarında çalışacak şekilde yapılandırılmış bir iş akışı olsa bile yeni bir iş akışı çalışması tetiklenmez.

Ayrıca, **GITHUB\_TOKEN** kullanan bir GitHub Actions iş akışı tarafından gönderilen commit’ler bir **GitHub Pages** derlemesini tetiklemez.

### 📌 Sonraki Adımlar (next steps)

* Use GITHUB\_TOKEN for authentication in workflows
* Workflow syntax for GitHub Actions
