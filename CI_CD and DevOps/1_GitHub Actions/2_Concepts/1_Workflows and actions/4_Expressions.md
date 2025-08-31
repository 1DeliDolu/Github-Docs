## 🧮 İfadeler (expressions)

İş akışlarında (workflows) ve işlemlerde (actions) ifadeleri değerlendirebilirsiniz.

## ℹ️ İfadeler hakkında (about expressions)

İfadeleri (expressions), iş akışı dosyalarında ortam değişkenlerini (environment variables) programatik olarak ayarlamak ve bağlamlara (contexts) erişmek için kullanabilirsiniz. Bir ifade, sabit değerlerin (literal values), bir bağlama (context) yapılan başvuruların veya işlevlerin (functions) herhangi bir kombinasyonu olabilir. Sabitleri, bağlam başvurularını ve işlevleri operatörler (operators) kullanarak birleştirebilirsiniz. Bağlamlar hakkında daha fazla bilgi için bkz. Bağlamlar başvurusu (Contexts reference).

İfadeler genellikle, bir adımın çalıştırılıp çalıştırılmayacağını belirlemek için iş akışı dosyasında koşullu `if` anahtar sözcüğüyle birlikte kullanılır. Bir `if` koşulu doğru olduğunda, adım çalıştırılır.

Bir ifadeyi dizge (string) olarak değil de GitHub tarafından değerlendirilmesi gereken bir ifade olarak belirtmek için özel sözdizimi kullanmanız gerekir.

```
${{ <expression> }}
```

## 📝 Not (note)

Bu kurala istisna, ifadeleri bir `if` koşulunda kullanırken ortaya çıkar; burada genellikle ` ${{` ve `}}` yazımını isteğe bağlı olarak atlayabilirsiniz. `if` koşulları hakkında daha fazla bilgi için bkz. GitHub Actions için iş akışı sözdizimi (Workflow syntax for GitHub Actions).

## ⚠️ Uyarı (warning)

İş akışları (workflows) ve işlemler (actions) oluştururken, kodunuzun olası saldırganlardan gelen güvenilmeyen girdileri çalıştırıp çalıştırmayacağını her zaman göz önünde bulundurmalısınız. Belirli bağlamlar güvenilmeyen girdi olarak değerlendirilmelidir; çünkü bir saldırgan kendi kötü amaçlı içeriğini ekleyebilir. Daha fazla bilgi için bkz. Güvenli kullanım başvurusu (Secure use reference).

## 🛠️ Ortam değişkeni ayarlama örneği (example setting an environment variable)

```yaml
env:
  MY_ENV_VAR: ${{ <expression> }}
```

👉 Bu örnekte, `MY_ENV_VAR` adlı ortam değişkeni bir ifade (expression) kullanılarak ayarlanmaktadır.

## 📖 Daha fazla okuma (further reading)

İş akışlarında (workflows) ve işlemlerde (actions) kullanabileceğiniz ifadeler hakkında teknik başvuru bilgisi için bkz. İfadeleri değerlendirme (Evaluate expressions in workflows and actions).
