## ⚡ Daha büyük runner’lar (Larger runners)

GitHub tarafından barındırılan daha büyük runner türleri ve kullanım alanları hakkında bilgi edinin.

---

## 👥 Bu özelliği kimler kullanabilir? (Who can use this feature?)

Daha büyük runner’lar yalnızca GitHub Team veya GitHub Enterprise Cloud planlarını kullanan kuruluşlar ve işletmeler için kullanılabilir.

---

## 📌 Daha büyük runner’lar hakkında (About larger runners)

GitHub Team ve GitHub Enterprise Cloud planlarındaki müşteriler, standart GitHub-hosted runner’lardan daha fazla kaynağa sahip yönetilen sanal makinelerden seçim yapabilir. Bu makineler “daha büyük runner (larger runners)” olarak adlandırılır. Aşağıdaki gelişmiş özellikleri sunarlar:

* Daha fazla RAM, CPU ve disk alanı
* Statik IP adresleri
* Azure özel ağ (private networking)
* Runner’ları gruplama yeteneği
* Eşzamanlı iş akışlarını desteklemek için otomatik ölçeklendirme (autoscaling)
* GPU destekli runner’lar

Bu daha büyük runner’lar GitHub tarafından barındırılır ve önceden yüklenmiş runner uygulaması ile diğer araçları içerir.

GitHub, macOS, Ubuntu veya Windows işletim sistemleriyle daha büyük runner’lar sunar. Kullanılan işletim sistemine bağlı olarak farklı özellikler ve boyutlar mevcuttur.

---

## 🐧🪟 Ubuntu ve Windows daha büyük runner’lar hakkında (About Ubuntu and Windows larger runners)

Ubuntu veya Windows işletim sistemine sahip daha büyük runner’lar, kuruluşunuzda veya işletmenizde yapılandırılır. Daha büyük bir runner eklediğinizde, mevcut donanım özellikleri ve işletim sistemi görüntülerinden bir makine türü tanımlamış olursunuz.

Ubuntu ve Windows daha büyük runner’lar ile şunları yapabilirsiniz:

* Belirli bir aralıktan statik IP adresleri atayabilir ve bu aralığı güvenlik duvarı izin listesi (firewall allowlist) yapılandırmasında kullanabilirsiniz.
* Runner’ları runner gruplarına atayarak kaynaklarınıza erişimi kontrol edebilirsiniz.
* Runner yönetimini basitleştirmek ve maliyetlerinizi kontrol etmek için otomatik ölçeklendirme kullanabilirsiniz.
* Runner’larınızı Azure özel ağ (private networking) ile kullanabilirsiniz.

---

## 🍏 macOS daha büyük runner’lar hakkında (About macOS larger runners)

macOS işletim sistemine sahip daha büyük runner’lar kuruluşunuza veya işletmenize manuel olarak eklenmez. Bunun yerine, bir iş akışı dosyasındaki `runs-on` anahtarını GitHub tarafından tanımlanmış macOS daha büyük runner etiketlerinden birine güncelleyerek kullanılır.

macOS daha büyük runner’lar önceden yapılandırılmadığından, Ubuntu ve Windows daha büyük runner’larda olmayan sınırlamalara sahiptir. Daha fazla bilgi için bkz. Larger runners reference.

---

## 💰 Faturalandırma (Billing)

Not:
Daha büyük runner’lar özel havuzlarda (private repositories) dahil edilen dakikalar için uygun değildir. Hem özel hem de genel havuzlarda (public repositories) daha büyük runner kullanıldığında, her zaman dakika başına ücretlendirilir.

Standart GitHub-hosted runner’lara kıyasla, daha büyük runner’lar farklı şekilde faturalandırılır. Daha büyük runner’lar yalnızca iş akışlarının üzerinde çalıştığı süre boyunca dakika başına ücretlendirilir. Bir iş akışı tarafından kullanılmayan daha büyük runner oluşturmanın herhangi bir maliyeti yoktur. Daha fazla bilgi için bkz. Actions minute multiplier reference.

---

## ⏭️ Sonraki adımlar (Next steps)

* Windows veya Ubuntu daha büyük runner’ları kullanmaya başlamak için bkz. Managing larger runners.
* macOS daha büyük runner’ları kullanmaya başlamak için bkz. Running jobs on larger runners.
* Daha büyük runner’ların kullanımıyla ilgili başvuru bilgileri için bkz. Larger runners reference.
