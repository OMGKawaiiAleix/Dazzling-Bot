# Política de Privacidade

**Última atualização: 18 de novembro de 2026**

*Este documento é uma tradução do Privacy Policy original em inglês, oferecida por conveniência. Em caso de qualquer divergência, prevalece a versão em inglês.*

Esta Política de Privacidade explica como a Dazzling ("Dazzling", "o bot", "nós") coleta, usa, armazena e protege informações quando você usa a Dazzling no Discord ou interage com sua documentação oficial.

A Dazzling é desenvolvida e operada por um desenvolvedor individual conhecido no Discord como **omgkawaiialeix** ("o Desenvolvedor"). Para qualquer dúvida sobre esta Política, entre em contato através do nosso servidor de suporte oficial no Discord: **https://discord.gg/R3AZpftXTm**.

Ao usar a Dazzling, você também concorda com a [Política de Privacidade](https://discord.com/privacy) e os [Termos de Serviço](https://discord.com/terms) próprios do Discord, já que a Dazzling opera inteiramente dentro da plataforma do Discord e não pode funcionar sem ela.

---

## 1. Informações que Coletamos

Coletamos apenas as informações estritamente necessárias para que as funcionalidades da Dazzling funcionem. Nós as agrupamos em quatro categorias:

### 1.1 Conteúdo que Você Cria Diretamente

Quando um administrador de servidor usa comandos como `/embed create`, `/embed edit`, `/config`, `/partner message`, ou `/autorole`, a Dazzling armazena o conteúdo que essa pessoa digita ou seleciona, incluindo:

- O texto e as configurações de embeds personalizados: título, descrição, cor, nome/ícone do autor, texto/ícone do footer, URLs de imagem e miniatura, texto de campos, rótulos e URLs de botões, e o nome interno/pasta usados para organizá-los.
- Qual embed e qual canal estão vinculados às funcionalidades de Boas-vindas, Boost, Despedida, ou Partner (alianças).
- Para a funcionalidade de auto-cargo (`/autorole`): o texto gatilho configurado, e a mensagem de confirmação própria que você configurar (seu próprio texto, ou uma referência a um dos seus embeds salvos).

Esse conteúdo é escrito voluntariamente pelo administrador do servidor para configurar o comportamento do bot. Nós não geramos, sugerimos, nem alteramos esse conteúdo.

### 1.2 Identificadores do Discord

Para que as funcionalidades acima funcionem por servidor e por usuário, armazenamos os identificadores próprios do Discord ("snowflakes"):

- O ID do servidor (guild) do Discord onde uma funcionalidade é configurada.
- O ID do usuário do Discord que criou ou é dono de um embed salvo, ou que configurou uma funcionalidade.
- O ID do canal do Discord escolhido para uma funcionalidade (ex: onde deve ser enviada uma mensagem de boas-vindas, um alerta de aliança, ou onde é detectado o texto gatilho do auto-cargo).
- O(s) ID(s) do(s) cargo(s) do Discord configurados para a funcionalidade de auto-cargo (o cargo a atribuir, e, se configurado, o cargo a remover).
- O idioma de resposta (espanhol ou português) que um servidor escolheu com `/language`.

Nós **não** armazenamos nomes reais, e-mails, números de telefone, nem endereços físicos. De início, não temos acesso a essa informação através da API do Discord.

### 1.3 Contadores de Uso Gerados Automaticamente

Alguns contadores numéricos são gerados e armazenados automaticamente, sem que ninguém digite nenhum texto:

- **Contador de alianças**: para cada usuário, mantemos uma contagem de quantas vezes ele já postou um link de convite válido de um servidor do Discord no canal de alianças configurado de um servidor. Essa contagem só é usada para o placeholder `{{partner.count}}` (ex: "esta é sua 5ª aliança!") e está vinculada a um ID de usuário e de servidor do Discord, não a nenhuma outra informação pessoal.

### 1.4 Informações Processadas Temporariamente (Não Armazenadas)

Algumas informações são lidas ou usadas por um momento para montar uma mensagem, e depois são descartadas — nunca são gravadas em nosso banco de dados:

- **Informações do membro no momento de um evento**: quando alguém entra em um servidor (Boas-vindas), dá boost nele (Boost), sai dele (Despedida), cola um link de convite em um canal de alianças configurado (Partner), ou escreve o texto gatilho configurado para a funcionalidade de auto-cargo, usamos brevemente o nome de usuário, tag, menção e URL do avatar dessa pessoa no Discord para preencher os placeholders (ex: `{{user.name}}`) da mensagem que o administrador do servidor projetou. Essa informação é usada só para montar essa mensagem e é descartada imediatamente depois.
- **Conteúdo de mensagens só nos canais de "Partner" e de auto-cargo**: se um administrador de servidor configurar um canal com `/partner channel` ou configurar o canal da funcionalidade de auto-cargo, a Dazzling lê o texto das mensagens postadas **somente nesses canais específicos**, apenas para detectar se uma mensagem contém um link de convite de servidor do Discord (Partner), ou se corresponde ao texto gatilho configurado (auto-cargo). Se nenhuma condição for atendida, nada acontece.
  - A Dazzling **não** lê, processa, nem armazena conteúdo de mensagens de nenhum outro canal, para nenhuma outra finalidade.
  - O texto dessas mensagens nunca é salvo em nosso banco de dados nem escrito em nenhum registro, exceto o texto gatilho que você mesmo configurou para a funcionalidade de auto-cargo (veja a Seção 1.1), que é diferente das mensagens que os membros escrevem depois para corresponder a ele.
- **Envio por Webhook**: se um administrador de servidor escolher enviar um embed com a opção de Webhook (para mostrar um nome e/ou avatar diferente do bot), a Dazzling cria ou reutiliza um webhook do Discord nesse canal para enviar a mensagem. Esse webhook é criado e gerenciado inteiramente pelo Discord; nós não armazenamos seu ID, token, nem nenhum dado relacionado em nosso banco de dados.

---

## 2. Como Usamos as Informações

Usamos as informações descritas acima exclusivamente para:

- Operar as funcionalidades que você ou os administradores do seu servidor configurarem (embeds personalizados, mensagens automáticas de Boas-vindas/Boost/Despedida, a detecção de links de aliança do Partner, e a funcionalidade de auto-cargo, incluindo atribuir ou remover um cargo do Discord quando configurado).
- Permitir que o dono de um embed o encontre, edite, renomeie, mova, transfira, ou apague.
- Manter, depurar e melhorar o funcionamento da Dazzling.

Não usamos suas informações para publicidade, geração de perfis, ou para qualquer finalidade que não seja operar as funcionalidades do bot.

---

## 3. Como Armazenamos as Informações

Todos os dados descritos nas Seções 1.1 e 1.2 são armazenados em um banco de dados SQLite na infraestrutura de hospedagem da Dazzling. O acesso à nossa conta de hospedagem é protegido por autenticação de dois fatores, e nosso provedor de hospedagem inclui proteção contra DDoS. Ainda assim, como qualquer serviço online, não podemos garantir segurança absoluta dos dados armazenados ou em trânsito.

O console do nosso provedor de hospedagem não mantém um histórico permanente de logs por padrão, e qualquer log técnico que possa existir temporariamente na infraestrutura não contém o conteúdo das suas mensagens do Discord. Nosso provedor de hospedagem pode apagar logs ou backups a seu próprio critério, principalmente se eles consumirem um espaço de armazenamento considerável.

---

## 4. Retenção e Exclusão de Dados

- Os dados vinculados a um servidor são mantidos enquanto a Dazzling continuar sendo membro desse servidor, sem data de expiração fixa.
- **Exclusão automática**: se a Dazzling for removida de um servidor (expulsa, ou o servidor for excluído), todos os dados associados a esse servidor — cada embed salvo, configuração de Boas-vindas/Boost/Despedida, configuração de Partner, configuração de auto-cargo, e contadores de alianças — são **excluídos automática e imediatamente** do nosso banco de dados. Isso não acontece se um servidor apenas sofrer uma queda temporária do Discord; a Dazzling só exclui dados quando realmente deixou o servidor.
- **Exclusão manual**: qualquer usuário pode excluir seus próprios embeds salvos a qualquer momento usando `/embed delete`, sem precisar remover o bot do servidor. Um administrador do servidor pode apagar a configuração de auto-cargo a qualquer momento usando `/autorole` com sua opção `disable`.
- O conteúdo de mensagens lido nos canais de alianças do Partner e de auto-cargo, e os dados de webhooks (Seção 1.4), nunca são armazenados, então não há nada para excluir ali.
- **Se a Dazzling for descontinuada permanentemente**, faremos um esforço razoável para excluir todos os dados restantes dentro de um prazo razoável após o Serviço ser encerrado.
- Se você quiser que excluamos algum dado específico e as ferramentas acima não cobrirem sua situação, você pode entrar em contato através do nosso servidor de suporte no Discord e atenderemos à sua solicitação.

---

## 5. Compartilhamento de Informações

Não vendemos, alugamos, nem compartilhamos suas informações com terceiros para fins de marketing ou qualquer outra finalidade. As informações só são trocadas com o próprio Discord, já que isso é inerentemente necessário para que a Dazzling funcione como um bot do Discord, e está sujeito à própria Política de Privacidade do Discord.

---

## 6. Privacidade de Menores

A Dazzling é destinada a ser usada de acordo com os próprios Termos de Serviço do Discord, que exigem que os usuários cumpram o requisito mínimo de idade do Discord. Não coletamos informações intencionalmente de pessoas que não atendam a esse requisito, e confiamos nos próprios mecanismos de verificação de idade do Discord.

---

## 7. Seus Direitos

Dependendo de onde você mora, você pode ter direitos sobre seus dados pessoais, incluindo o direito de acessar, corrigir, ou solicitar a exclusão de suas informações. Se você estiver na Colômbia, isso inclui os direitos reconhecidos pela **Lei 1581 de 2012 ("Habeas Data")** e seus decretos regulamentadores. Respeitamos esses direitos conforme descrito na Seção 4 (exclusão por conta própria via `/embed delete`, ou exclusão automática quando o bot sai do seu servidor). Para qualquer outra solicitação, entre em contato através do nosso servidor de suporte no Discord.

---

## 8. Doações

A Dazzling pode oferecer uma forma de apoiar voluntariamente seu desenvolvimento através do Patreon. As doações são processadas inteiramente pelo Patreon, e qualquer informação de pagamento ou cobrança que você fornecer é gerenciada pelo Patreon sob sua própria Política de Privacidade — nós não recebemos nem armazenamos seus dados de pagamento.

---

## 9. Uso Internacional

A Dazzling pode ser usada por servidores e usuários do mundo todo. Ao usar a Dazzling, você entende que suas informações podem ser armazenadas e processadas em infraestrutura localizada em um país diferente do seu, e que esta Política e os Termos de Serviço são regidos pelas leis da Colômbia (veja nossos Termos de Serviço).

---

## 10. Onde Estes Documentos São Publicados

Esta Política de Privacidade e nossos Termos de Serviço são publicados como documentos de texto simples (Markdown) em um repositório público do GitHub, não como um site dedicado. Se você os visualizar no GitHub, sua visita também está sujeita à [Declaração de Privacidade do GitHub](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement), que é independente e está fora do nosso controle.

---

## 11. Alterações a Esta Política

Podemos atualizar esta Política de Privacidade periodicamente, por exemplo para refletir novas funcionalidades ou exigências legais. Quando o fizermos, atualizaremos a data de "Última atualização" no topo desta página. Continuar usando a Dazzling após as alterações entrarem em vigor significa que você aceita a Política atualizada.

---

## 12. Contato

Se você tiver alguma dúvida sobre esta Política de Privacidade ou sobre como suas informações são tratadas, entre em contato com **omgkawaiialeix** através do nosso servidor de suporte oficial no Discord: **https://discord.gg/R3AZpftXTm**.
