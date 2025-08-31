## 🔔 İş Akışı Çalıştırmaları için Bildirimler (notifications for workflow runs)

Tetiklediğiniz (trigger) iş akışı çalıştırmaları (workflow runs) hakkında bildirimlere abone olabilirsiniz.

## ℹ️ Genel Bakış (overview)

GitHub Actions için e-posta veya web bildirimlerini etkinleştirirseniz, tetiklediğiniz herhangi bir iş akışı çalıştırması tamamlandığında bir bildirim alırsınız. Bildirim, iş akışı çalıştırmasının durumunu içerir (başarılı, başarısız, nötr veya iptal edilmiş). Ayrıca yalnızca bir iş akışı çalıştırması başarısız olduğunda bildirim almayı seçebilirsiniz. Daha fazla bilgi için bkz. Bildirimler hakkında (About notifications).

Zamanlanmış iş akışlarının (scheduled workflows) bildirimleri, iş akışını ilk oluşturan kullanıcıya gönderilir.

* İş akışı dosyasındaki zamanlama (schedule) olayında `cron` sözdizimini farklı bir kullanıcı güncellerse, sonraki bildirimler bu kullanıcıya gönderilir.
* Bir zamanlanmış iş akışı devre dışı bırakılır ve ardından yeniden etkinleştirilirse, bildirimler `cron` sözdizimini en son değiştiren kullanıcıya değil, iş akışını yeniden etkinleştiren kullanıcıya gönderilir.

Bir deponun (repository) **Actions** sekmesinde de iş akışı çalıştırmalarının durumunu görebilirsiniz. Daha fazla bilgi için bkz. İş akışı çalıştırmalarını yönetme (Managing workflow runs).
