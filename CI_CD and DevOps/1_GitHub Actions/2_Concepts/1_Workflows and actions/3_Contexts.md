## 🧩 Bağlamlar (contexts)

GitHub Actions’daki bağlamlar hakkında bilgi edinin.

## ℹ️ Bağlamlar hakkında (about contexts)

Bağlamlar (contexts), iş akışı çalıştırmaları (workflow runs), değişkenler (variables), koşucu (runner) ortamları, işler (jobs) ve adımlar (steps) hakkında bilgilere erişmenin bir yoludur. Her bağlam, dize (string) veya diğer nesneler olabilen özellikler (properties) içeren bir nesnedir (object).

Bağlamlar, nesneler ve özellikler, farklı iş akışı çalıştırma koşullarında önemli ölçüde değişiklik gösterebilir. Örneğin, matris bağlamı (matrix context) yalnızca bir matris içindeki işler için doldurulur.

Bağlamlara ifade sözdizimi (expression syntax) kullanarak erişebilirsiniz. Daha fazla bilgi için bkz. İş akışlarında ve işlemlerde ifadeleri değerlendirme (Evaluate expressions in workflows and actions).

```
${{ <context> }}
```

## ⚠️ Uyarı (warning)

İş akışları (workflows) ve işlemler (actions) oluştururken, kodunuzun olası saldırganlardan gelen güvenilmeyen girdileri çalıştırıp çalıştırmayacağını her zaman göz önünde bulundurmalısınız. Belirli bağlamlar güvenilmeyen girdi olarak değerlendirilmelidir; çünkü bir saldırgan kendi kötü amaçlı içeriğini ekleyebilir. Daha fazla bilgi için bkz. Güvenli kullanım başvurusu (Secure use reference).

## 🛠️ Bağlamların ne zaman kullanılacağını belirleme (determining when to use contexts)

GitHub Actions, bağlamlar (contexts) adı verilen bir değişkenler koleksiyonunu ve varsayılan değişkenler (default variables) adı verilen benzer bir koleksiyonu içerir. Bu değişkenler, iş akışının farklı noktalarında kullanılmak üzere tasarlanmıştır:

* **Varsayılan ortam değişkenleri (default environment variables):** Bu ortam değişkenleri yalnızca işinizi çalıştıran koşucuda (runner) bulunur. Daha fazla bilgi için bkz. Değişkenlerde bilgi depolama (Store information in variables).
* **Bağlamlar (contexts):** Çoğu bağlamı iş akışınızın herhangi bir noktasında kullanabilirsiniz; bu, varsayılan değişkenlerin mevcut olmadığı durumlar da dahil. Örneğin, bağlamları koşucuya (runner) yönlendirilmeden önce ilk işlemleri gerçekleştirmek için ifadelerle (expressions) birlikte kullanabilirsiniz; bu, bir adımın çalışıp çalışmayacağını belirlemek için `if` anahtar sözcüğüyle bir bağlam kullanmanıza olanak tanır. İş çalışmaya başladığında, işi çalıştıran koşucudan bağlam değişkenlerini (context variables) da alabilirsiniz, örneğin `runner.os`. Bir iş akışı içinde çeşitli bağlamları nerede kullanabileceğiniz hakkında ayrıntılar için bkz. Bağlamlar başvurusu (Contexts reference).

Aşağıdaki örnek, bu farklı türde değişkenlerin bir işte nasıl birlikte kullanılabileceğini göstermektedir:

```yaml
name: CI
on: push
jobs:
  prod-check:
    if: ${{ github.ref == 'refs/heads/main' }}
    runs-on: ubuntu-latest
    steps:
      - run: echo "Deploying to production server on branch $GITHUB_REF"
```

👉 Bu örnekte, `if` ifadesi geçerli dal (branch) adını belirlemek için `github.ref` bağlamını kontrol eder; eğer ad `refs/heads/main` ise, sonraki adımlar çalıştırılır. `if` kontrolü GitHub Actions tarafından işlenir ve sonuç doğruysa iş yalnızca koşucuya (runner) gönderilir. İş koşucuya gönderildikten sonra adım çalıştırılır ve `runner` üzerindeki `$GITHUB_REF` değişkenine başvurur.
