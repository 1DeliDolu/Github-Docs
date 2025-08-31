## 📈 Runner ölçek kümeleri (Runner scale sets)

Bir runner ölçek kümesinin ne olduğunu ve Actions Runner Controller (ARC) ile nasıl etkileşim kurabileceğini öğrenin.

---

## 📌 Runner ölçek kümeleri hakkında (About runner scale sets)

Bir runner ölçek kümesi, GitHub Actions’tan işler (jobs) alabilen homojen runner’lardan oluşan bir gruptur. Bir runner ölçek kümesinin sahip olduğu aktif runner sayısı, Actions Runner Controller (ARC) gibi otomatik ölçeklendirme (auto-scaling) çözümleriyle kontrol edilebilir.

Runner gruplarını kullanarak runner ölçek kümelerini yönetebilirsiniz. Self-hosted runner’larda olduğu gibi, mevcut runner gruplarına runner ölçek kümeleri ekleyebilirsiniz. Ancak, runner ölçek kümeleri aynı anda yalnızca bir runner grubuna ait olabilir ve yalnızca bir etiket (label) alabilir.

Bir runner ölçek kümesine iş atamak için iş akışınızı, runner ölçek kümesinin adına referans verecek şekilde yapılandırmanız gerekir. Daha fazla bilgi için bkz. Using Actions Runner Controller runners in a workflow.

---

## ⚖️ Yasal bildirim (Legal notice)

Bu bölümün bazı kısımları [https://github.com/actions/actions-runner-controller/](https://github.com/actions/actions-runner-controller/) adresinden alınmış olup Apache-2.0 lisansı kapsamında uyarlanmıştır:

```
Copyright 2019 Moto Ishizawa

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

## ⏭️ Sonraki adımlar (Next steps)

* Actions Runner Controller kavramı hakkında daha fazla bilgi için bkz. Actions Runner Controller.
* Runner grupları hakkında bilgi edinmek için bkz. Managing access to self-hosted runners using groups.
