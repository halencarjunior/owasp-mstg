## Testando a Interação do Usuário

### Testando a Educação dos Usuários (MSTG-STORAGE-12)

Muitas coisas aconteceram ultimamente em termos de responsabilidades que os desenvolvedores têm no sentido de educar os usuários no quê eles necessitam saber.
Isso mudou especialmente com a introdução da [Regulação Geral de Proteção de Dados (General Data Protection Regulation - GDPR)](https://gdpr-info.eu/ "GDPR") na Europa. Desde então, é melhor educar os usuários no sentido do que está acontecendo com seus dados pessoais e porquê.
Além disso, é uma boa prática informar o usuário sobre como utilizar a aplicação de forma adequada. Isso deve garantir uma utilização e processamento seguros das informações do usuário.
Após isso, o usuário deve ser informado de que tipo de dado do dispositivo o aplicativo irá acessar, sejam eles Informações Pessoalmente Identificáveis (Personally Identifiable Information - PII) ou não.
Finalmente, você precisa compartilhar com o usuário informações relacionadas a software de código aberto (Open Source Software - OSS).
Todos os quatro itens serão cobertos aqui.

> Por favor note que esse é um projeto MSTG e não um manual legal. Portanto nós não vamos cobrir o GDPR e outras possíveis leis relevantes aqui.

#### Informando os usuários sobre suas informações pessoais

Quando você necessita informações pessoais do usuário para o seu processo de negócio, o usuário precisa ser informado sobre o que você faz com os dados e porquê precisa deles. Se existe um terceiro fazendo atualmente o processamento dos dados, você deve informar o usuário disso também. Finalmente, há três controles que você deve suportar:

- **O direito de ser esquecido**: Usuários devem conseguir solicitar a deleção dos seus dados, e ter uma explicação de como fazê-lo.
- **O direito de corrigir dados**: Usuários devem conseguir corrigir os seus dados pessoais a qualquer momento, e ter uma explicação de como fazê-lo.
- **O direito de acessar dados do usuário**: Usuários devem conseguir requisitar todas as informações que a aplicação possui sobre eles, e ter uma explicação de como conseguir essa informação.

A maioria disso pode ser coberto pela política de privacidade, mas tenha certeza que ela está entendível para o usuário.

Quando dados adicionais precisem ser processados, você deve pedir o consentimento do usuário novamente. Durante a requisição de consentimento precisa ser claro ao usuário como ele pode reverter a decisão de compartilhar dados adicionais. De forma semelhante, quando os bancos de dados existentes sobre um usuário precisarem ser conectados, você precisa solicitar o consentimento do usuário para isso também.

#### Informando o usuário das melhores práticas de segurança

Aqui há uma lista de melhores práticas das quais o usuário pode ser informado a respeito:

- **Uso de digital**: Quando um aplicativo utiliza as digitais do usuário para autenticação e essas provém acesso a informações/transações de alto risco, informe o usuário sobre os problemas que podem acontecer quando existem diversas digitais de outras pessoas também registradas no dispositivo.
- **Root/Jailbreak de dispositivo**: Quando um aplicativo detecta que o dispositivo sofreu root ou jailbreak, informe o usuário do fato que certas ações de alto risco terão riscos adicionais pelo fato do dispositivo estar nessa condição.
- **Credenciais específicas**: Quando um usuário solicita um código de recuperação, uma senha ou pin do aplicativo (ou define algum deles), ensine o usuário a nunca compartilhá-lo com ninguém mais e que apenas o próprio aplicativo irá requisitar o mesmo.
- **Distribuição do aplicativo**: Em caso de aplicativos de alto risco, é recomendado comunicar qual a forma oficial de distribuição do mesmo. De outra forma, os usuários podem utilizar outros canais nos quais eles podem fazer o download de versões comprometidas do aplicativo.

#### Acesso aos dados do dispositivo

Apesar de ser parcialmente coberto pelas lojas de aplicativos Google Play e Apple, ainda assim você precisa explicar para o usuário quais tipos de serviços o aplicativo consome e porquê. Por exemplo:

- O aplicativo necessita acesso a lista de contatos?
- O aplicativo necessita acesso aos serviços de localização do dispositivo?
- O aplicativo necessita acesso aos identificadores do dispositivo para poder identificá-lo?

Explique ao usuário porquê seu aplicativo necessita fazer esse tipo de coisas. Mais informações (em inglês) sobre esse assunto podem ser encontrados em [Orientações Apple para Interface Humana](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/requesting-permission/ "Apple Human Interface Guidelines") e [Melhores Práticas de Permissões para Aplicativos Android](https://developer.android.com/training/permissions/requesting.html#explain "Android App permissions best practices").

#### Outras informações que você precisa compartilhar (informações sobre software de código aberto)

Dadas as leis de direitos autorais, você precisa ter certeza que o usuário está sendo informado sobre quaisquer bibliotecas de terceiros que são utilizadas no aplicativo. Para cada biblioteca terceira você deve consultar a licença da mesma para verificar se determinadas informações (como direitos de cópia, modificação, autor original, etc.) devem ser apresentadas ao usuário. Para isso, é melhor solicitar conselhos legais de um especialista. Um exemplo (em inglês) pode ser encontrado na [postagem do blog Big Nerd Ranch](https://www.bignerdranch.com/blog/open-source-licenses-and-android/ "Example on license overview"). Além disso, o site [TL;DR - Legal](https://tldrlegal.com/ "TL;DR - Legal")

### Referências

#### OWASP MASVS

- MSTG-STORAGE-12: "O aplicativo ensina o usuário sobre os tipos de informações pessoais identificáveis processadas, assim como as melhores práticas de segurança que o usuário deve seguir no uso do aplicativo."

#### Examplo em como mencionar licenças de código aberto (em inglês)

- <https://www.bignerdranch.com/blog/open-source-licenses-and-android/>

#### Site para auxiliar a entender licenças (em inglês)

- <https://tldrlegal.com/>

#### Orientações sobre requisição de permissões (em inglês)

- Orientações Apple para Interface Humana - <https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/requesting-permission/>
- Melhores Práticas de Permissões para Aplicativos Android - <https://developer.android.com/training/permissions/requesting.html#explain>
