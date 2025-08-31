## 🔒 GitHub tarafından barındırılan runner’larla özel ağ kullanımı (Private networking with GitHub-hosted runners)

GitHub tarafından barındırılan runner’ları, paket kayıt defterleri (package registries), gizli anahtar yöneticileri (secret managers) ve diğer şirket içi (on-premises) servisler dahil olmak üzere özel bir ağa bağlayabilirsiniz.

---

## 🌐 GitHub-hosted runner’ların ağ kullanımı hakkında (About GitHub-hosted runners networking)

Varsayılan olarak, GitHub-hosted runner’lar genel internete erişime sahiptir. Ancak, bu runner’ların özel ağınızdaki bir paket kayıt defterine, gizli anahtar yöneticisine veya diğer şirket içi hizmetlere erişmesini de isteyebilirsiniz.

GitHub-hosted runner’lar tüm GitHub müşterileri arasında paylaşılır. Ancak özel ağ kullanımıyla, bu runner’ları yalnızca iş akışlarınız çalışırken özel ağınıza ve kaynaklarınıza bağlanacak şekilde yapılandırabilirsiniz.

Bu erişimi yapılandırmak için farklı yaklaşımlar kullanabilirsiniz. Her yaklaşımın kendine özgü avantajları ve dezavantajları vardır.

---

## 🔑 OIDC ile bir API Gateway kullanma (Using an API Gateway with OIDC)

GitHub Actions ile, iş akışınızı GitHub Actions dışında kimlik doğrulamak için OpenID Connect (OIDC) jetonlarını kullanabilirsiniz. Daha fazla bilgi için bkz. Using an API gateway with OIDC.

---

## 🛜 WireGuard ile ağ kaplaması oluşturma (Using WireGuard to create a network overlay)

Bir API Gateway için ayrı altyapıyı sürdürmek istemiyorsanız, WireGuard’ı hem runner’da hem de özel ağınızdaki bir serviste çalıştırarak runner ile servisiniz arasında bir ağ kaplaması (overlay network) oluşturabilirsiniz. Daha fazla bilgi için bkz. Using WireGuard to create a network overlay.

---

## ☁️ Azure Sanal Ağı (VNET) kullanma (Using an Azure Virtual Network - VNET)

GitHub-hosted runner’ları bir Azure VNET içinde kullanabilirsiniz. Bu, CI/CD için GitHub tarafından yönetilen altyapıyı kullanırken runner’larınızın ağ politikaları üzerinde tam kontrol sağlamanıza imkan tanır. Azure VNET hakkında daha fazla bilgi için bkz. Azure belgelerindeki *What is Azure Virtual Network?*

GitHub Team planını kullanan organizasyon sahipleri, GitHub-hosted runner’lar için organizasyon düzeyinde Azure özel ağ yapılandırması yapabilir. Daha fazla bilgi için bkz. About Azure private networking for GitHub-hosted runners in your organization.
