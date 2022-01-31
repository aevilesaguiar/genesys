## O que é GVP e como funcionam os aplicativos de voz

A Genesys Voice Platform (GVP) é um servidor de mídia baseado em VoiceXML para provedores de serviços de rede e clientes corporativos.

**O que é GVP?**
No nível mais básico, o Genesys Voice Platform (GVP) é um software Interactive Voice Response (soft IVR). Em um nível mais complexo, o GVP é um pacote de software que integra uma combinação de processamento de chamadas, relatórios, gerenciamento e servidores de aplicativos com redes de Voz sobre IP (VoIP), para fornecer diálogo orientado pela Web e serviços de controle de chamadas aos chamadores.

Usando recursos como Reconhecimento Automático de Fala (ASR) e Text-to-Speech (TTS), o GVP oferece uma maneira econômica de implementar interações de voz automatizadas de clientes que ligam para seu contact center. No nível de tecnologia, o GVP é um conjunto de componentes de software que complementam e funcionam com outros produtos da Genesys para fornecer uma solução completa de autoatendimento de voz.

Notas:

Enquanto o GVP é comumente usado em ambientes corporativos de autoatendimento, muitas outras aplicações do GVP — incluindo aquelas fora do contact center — são possíveis.

Uma máquina na qual os componentes do GVP estão instalados também é chamada de Servidor GVP em outros locais neste sistema de Ajuda.

## Caso de uso
Um exemplo de fluxo para um aplicativo de autoatendimento de voz GVP é apresentado abaixo:

- Um cliente que ligasse para um IVR receberia avisos/anúncios com uma mensagem de boas-vindas. Esses prompts podem ser específicos para uma região com base no número DNIS de entrada ou personalizados com base nas opções do usuário, como um prompt para selecionar um idioma.
- Os aplicativos podem ter lógica de controle de negócios, permitindo que os usuários de negócios definam horários de abertura e fechamento, definam anúncios e sinalizadores de emergência, definam dias especiais e assim por diante. Essas opções podem ser definidas no Genesys Administrator ou no Genesys Rules System.
- O aplicativo pode ter a capacidade de coletar a entrada do usuário com várias opções e repetibilidade para lidar com recursos sem entrada / sem correspondência.
- Depois que o aplicativo obtém a entrada do usuário, como o número da conta, essas informações podem ser verificadas em aplicativos de back office ou podem ter a capacidade de extrair dados de uma solução do Gerenciador de conversas
- As informações do cliente recuperadas podem ser anexadas à interação como dados do usuário e podem ser usadas para segmentação de clientes e, assim, determinar como um determinado cliente seria gerenciado no autoatendimento
- O aplicativo pode fornecer autoatendimento com opções de reconhecimento de voz e opções DTMF nos menus.
- O aplicativo pode ser configurado para permitir que os usuários desativem o autoatendimento por padrão ou dentro do fluxo predefinido do aplicativo.
- Quando os usuários optam por não participar do IVR, eles podem ser roteados para uma fonte externa ou para um Agente com base no ambiente conforme definido acima. Por exemplo, os clientes podem escolher ser roteados para “Último Agente Chamado” ou ser roteados para qualquer Agente pressionando o “0” repetitivo.
- Os clientes podem ter atividades definidas em todo o fluxo do autoatendimento e também podem definir marcos para definir critérios de sucesso/fracasso em cada segmento do fluxo.


## Como funcionam os aplicativos de voz?

Assim como se usa HTML para criar aplicativos visuais, VoiceXML é uma linguagem de marcação usada para criar aplicativos de voz. Com uma página da Web tradicional, um navegador da Web fará uma solicitação a um servidor da Web, que por sua vez enviará um documento HTML ao navegador para ser exibido visualmente ao usuário. Com um aplicativo de voz, é o interpretador VoiceXML que envia a solicitação ao servidor web, que retornará um documento VoiceXML para ser apresentado como um aplicativo de voz via telefone. O que torna o VoiceXML tão poderoso é que todas as ferramentas mais populares para criar páginas da Web estão disponíveis para criar aplicativos de voz. Os desenvolvedores podem usar tecnologias com as quais já estão familiarizados, como JavaScript, JSP e ASP.NET/C# para gerar novos aplicativos de voz empolgantes.

O Composer é uma ferramenta de desenvolvimento de aplicativos VXML com todos os recursos. Os usuários podem desenvolver, depurar e testar seus aplicativos em seu Ambiente de Desenvolvimento Integrado (IDE) que fornece recursos amigáveis ​​ao desenvolvedor para testar e depurar aplicativos VXML e páginas da Web do lado do servidor. Quando o aplicativo estiver pronto, ele poderá ser exportado ou implantado manualmente usando um pacote exportado em um servidor de aplicativos/servidor da Web como Tomcat ou Microsoft IIS. Uma vez implantado, o GVP pode acessar as páginas VXML do aplicativo de voz e qualquer página do lado do servidor (JSP/ASP.NET) usando HTTP.

Quando uma chamada chega ao GVP, o GVP determina a localização do aplicativo VXML por meio de seus dados de provisionamento. Em seguida, ele busca a(s) página(s) VXML e usa seu mecanismo VXML para executá-las. Os resultados são reproduzidos para o chamador em seu telefone. Quaisquer páginas do lado do servidor que acessam bancos de dados ou serviços da Web ou outras páginas do lado do servidor são executadas no servidor de aplicativos/servidor da Web por meio de construções do lado do servidor implementadas pelo Composer.

Durante o desenvolvimento, o Composer pode usar seu pacote Tomcat ou uma instalação local do Microsoft IIS como servidor web e fazer chamadas de teste para o aplicativo diretamente através do GVP de dentro do IDE. Esse recurso fornece uma maneira rápida de testar aplicativos, eliminando a necessidade de implantar aplicativos em outro servidor e, em seguida, apontar o GVP para esse local.

Depois que o aplicativo é implantado em produção, o Composer não aparece mais. O aplicativo geralmente é implantado em seu próprio servidor web dedicado e servidor de aplicativos de onde é acessado pelo GVP. O servidor web/aplicativo fornece acesso a todas as páginas e scripts que compõem o aplicativo e executa qualquer página do lado do servidor do aplicativo.

