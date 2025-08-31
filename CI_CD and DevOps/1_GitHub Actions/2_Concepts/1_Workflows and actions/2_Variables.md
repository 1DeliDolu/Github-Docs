## 📦 Değişkenler (variables)

GitHub Actions iş akışlarında (workflows) değişkenler hakkında bilgi edinin.

## ℹ️ Hakkında (about)

Değişkenler (variables), hassas olmayan yapılandırma bilgilerini depolamak ve yeniden kullanmak için bir yol sağlar. Derleyici bayrakları (compiler flags), kullanıcı adları (usernames) veya sunucu adları (server names) gibi herhangi bir yapılandırma verisini değişken olarak saklayabilirsiniz. Değişkenler, iş akışınızı (workflow) çalıştıran koşucu (runner) makinesinde ara değerlerine yerleştirilir. İşlemler (actions) veya iş akışı adımlarında (workflow steps) çalışan komutlar değişkenler oluşturabilir, okuyabilir ve değiştirebilir.

Kendi özel değişkenlerinizi (custom variables) ayarlayabilir veya GitHub’ın otomatik olarak belirlediği varsayılan ortam değişkenlerini (default environment variables) kullanabilirsiniz.

Bir özel değişkeni (custom variable) iki şekilde ayarlayabilirsiniz.

* Bir iş akışında kullanılmak üzere ortam değişkeni (environment variable) tanımlamak için iş akışı dosyasında `env` anahtarını kullanabilirsiniz. Daha fazla bilgi için bkz. Tek bir iş akışı için ortam değişkenleri tanımlama (Defining environment variables for a single workflow).
* Birden fazla iş akışında kullanılacak bir yapılandırma değişkeni (configuration variable) tanımlamak için organizasyon, depo (repository) veya ortam (environment) düzeyinde tanımlama yapabilirsiniz. Bir organizasyonda değişken oluştururken, depo bazında erişimi sınırlamak için bir ilke (policy) kullanabilirsiniz. Örneğin, erişimi tüm depolara verebilir veya yalnızca özel depolar (private repositories) ya da belirtilen depo listesiyle sınırlandırabilirsiniz. Daha fazla bilgi için bkz. Birden fazla iş akışı için yapılandırma değişkenlerini tanımlama (Defining configuration variables for multiple workflows).

## ⚠️ Uyarı (warning)

Varsayılan olarak, değişkenler (variables) derleme çıktılarında (build outputs) maskelenmeden görüntülenir. Parolalar gibi hassas bilgiler için daha fazla güvenliğe ihtiyacınız varsa, bunun yerine sırları (secrets) kullanın. Daha fazla bilgi için bkz. Secrets.

## 📖 Başvuru (reference)

Ayrıntılı dokümantasyon için bkz. Değişkenler başvurusu (Variables reference).
