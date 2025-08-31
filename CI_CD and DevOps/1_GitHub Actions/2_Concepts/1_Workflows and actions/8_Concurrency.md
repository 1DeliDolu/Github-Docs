## ⚡ Eşzamanlılık (concurrency)

İş akışlarını (workflows) ve işleri (jobs) aynı anda çalıştırma hakkında bilgi edinin.

## ℹ️ Genel Bakış (overview)

Varsayılan olarak GitHub Actions, aynı iş akışı içinde birden fazla işin, aynı depoda (repository) birden fazla iş akışı çalıştırmasının ve bir depo sahibinin hesabında birden fazla iş akışı çalıştırmasının eşzamanlı (concurrently) çalışmasına izin verir. Bu, aynı iş akışının veya işin birden çok örneğinin aynı anda çalışabileceği ve aynı adımları gerçekleştirebileceği anlamına gelir.

GitHub Actions ayrıca eşzamanlı yürütmeyi devre dışı bırakmanıza da olanak tanır. Bu, aynı anda birden fazla iş akışının veya işin çalıştırılmasının çakışmalara neden olabileceği ya da beklenenden daha fazla Actions dakikası ve depolama tüketebileceği durumlarda hesap veya organizasyon kaynaklarınızı kontrol etmek için yararlı olabilir.

Örneğin:

* Aynı anda birden fazla dağıtımın (deployments) çalışmasını önlemek isteyebilirsiniz.
* Eski commit’ler için çalışan lint kontrollerini iptal etmek isteyebilirsiniz.

## 🛠️ Eşzamanlılığı kontrol etme (controlling concurrency)

Kendi iş akışlarınızda eşzamanlılığı kontrol etmeye başlamak için `concurrency` anahtar sözcüğünü kullanabilirsiniz. Daha fazla bilgi için bkz. İş akışları ve işlerin eşzamanlılığını kontrol etme (Control the concurrency of workflows and jobs).

## 🆘 Yardım ve destek (help and support)

Daha fazla yardım için GitHub belgelerine ve destek kaynaklarına başvurabilirsiniz.
