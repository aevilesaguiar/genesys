# Composer

Composer fornece um ambiente de desenvolvimento integrado (IDE), que permite que usuários técnicos e não técnicos criem:

- Aplicativos de Roteamento

O que é o Genesys Customer Experience Routing?
 Genesys Customer Experience Routing é um software de computador que ajuda as organizações a gerenciar melhor as jornadas dos clientes. O roteamento prioriza e combina a interação certa com o recurso certo no momento certo. Nossa abordagem é única no setor porque é:  

- SIMPLES para suportar 80% das interações com clientes que são rotineiras
- DYNAMIC para se adaptar automaticamente às flutuações dentro dos 80% (para que essa variabilidade não consuma 100% dos recursos)
- PODEROSA para impulsionar os 20% de interações que não são rotineiras, mas são as mais valiosas (ao longo do tempo, canais, multimídia, front e back office)
## O que é um aplicativo de roteamento?  e quais seus elementos basicos?

O roteamento forncece instruções sobre como lidar e para onde direcionar as interações em diferentes circunstancias. Um aplicativo de roteamento é como uma série de instruções priorizadas que levam em considerações vários fatores para determinar o destino do roteamentoideal e o que fazer a seguir se essa ação não for possível dentro das restrições especificadas.

Os aplicativos de roteamento são compostos de vários elementos diferentes:
- Os dados podem vir de várias fontes e podem incluir dados de clientes, contextuais, operacionais ou análiticos. Dados anexados que estão inclusos nas mensagens de chamada , os dados anexados podem ser adicionados e atualizados ao longo da vida da interação, por exemplo a edida que uma chamada flui pelo o IVR, roteamento, desktop do agente e relatórios.
- Skills (habilidade)  é o que vc sabe sobre o agente , para identificar o melhor recurso disponível para lidar com uma interação específica , o roteamento procura as combinações desejadas de habilidades no nível individual(por agente), no nível da equipe (por grupo de habilidades ou fila) ou em um pool virtual de recursos(fila virtual).


A lógica fornece as decisões ou instruções gerais de roteamento. A lógica especifica as condições sob as quais o roteamento se aplica e o método de seleção de destino. A lógica pode ser baseada em várias considerações diferentes, como direcionamento de habilidades, nível de serviço, balanceamento de carga, alocação de porcentagem, estatísticas ou força de trabalho

Certos aspectos do roteamento podem ser configurados e salvos como Objetos Reutilizáveis. Existem vários tipos de objetos reutilizáveis, incluindo sub-rotinas, objetos de lista, dados de interação, etc. A reutilização desses blocos de construção dentro e entre aplicativos de roteamento melhora a eficiência, a qualidade e a simplicidade do roteamento.

Uma solução de roteamento bem projetada e implementada deve ser capaz de lidar com a maioria das necessidades de roteamento em andamento de maneira dinâmica e automatizada. No entanto, pode haver algumas situações em que a empresa precise ou queira fazer alterações frequentes ou contínuas. Esses elementos selecionados podem ser expostos aos usuários de negócios como Parâmetros Operacionais ou como Regras Genesys para facilitar uma maior agilidade nos negócios, mantendo a estabilidade do sistema:

- Parâmetros operacionais são variáveis ​​condicionais simples que dão aos usuários de negócios controle limitado (por exemplo, mensagens após o expediente, horário de funcionamento, status de emergência, etc.). Os usuários podem fazer alterações nessas configurações de parâmetros por meio da interface Genesys Administrator Extensions (GAX). (Como alternativa, isso também pode ser feito por meio de objetos de lista no Interaction Routing Designer (IRD).) O usuário de negócios não pode alterar a lógica subjacente (apenas os valores pré-especificados dos parâmetros expostos) e não requer nenhum treinamento técnico especializado.
- Regras Genesys são representações lógicas de roteamento subjacente que são escritas em linguagem simples (ou seja, metalinguagem, não código). Eles são úteis quando o usuário de negócios (normalmente um analista de negócios) deseja maior controle sobre as condições, lógica e ações associadas ao roteamento (por exemplo, criar tratamentos diferenciados de atendimento ao cliente com base em segmentação, campanhas de marketing etc.). Os usuários podem fazer atualizações nas regras de negócios, mas apenas para as partes do roteamento que foram expostas por meio da interface de usuário de negócios no Genesys Conversation Manager. Embora o usuário de negócios não esteja realmente visualizando ou alterando o código diretamente, ele ainda exige uma compreensão clara da lógica de negócios e do impacto potencial das alterações.

## Quais são alguns dos tipos mais comuns de roteamento?

<html xmlns:v="urn:schemas-microsoft-com:vml"
xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:x="urn:schemas-microsoft-com:office:excel"
xmlns="http://www.w3.org/TR/REC-html40">

<head>

<meta name=ProgId content=Excel.Sheet>
<meta name=Generator content="Microsoft Excel 15">
<link id=Main-File rel=Main-File
href="file:///C:/Users/FLAVILES/AppData/Local/Temp/msohtmlclip1/01/clip.htm">
<link rel=File-List
href="file:///C:/Users/FLAVILES/AppData/Local/Temp/msohtmlclip1/01/clip_filelist.xml">
<style>
<!--table
	{mso-displayed-decimal-separator:"\,";
	mso-displayed-thousand-separator:"\.";}
@page
	{margin:.79in .51in .79in .51in;
	mso-header-margin:.31in;
	mso-footer-margin:.31in;}
tr
	{mso-height-source:auto;}
col
	{mso-width-source:auto;}
br
	{mso-data-placement:same-cell;}
td
	{padding-top:1px;
	padding-right:1px;
	padding-left:1px;
	mso-ignore:padding;
	color:black;
	font-size:11.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:Calibri, sans-serif;
	mso-font-charset:0;
	mso-number-format:General;
	text-align:general;
	vertical-align:bottom;
	border:none;
	mso-background-source:auto;
	mso-pattern:auto;
	mso-protection:locked visible;
	white-space:nowrap;
	mso-rotate:0;}
.xl63
	{color:#444A52;
	font-weight:700;
	font-family:Inherit;
	mso-generic-font-family:auto;
	mso-font-charset:0;
	text-align:left;
	vertical-align:top;
	border:1.0pt solid #E4E9F0;
	background:#FDFDFD;
	mso-pattern:black none;
	white-space:normal;
	padding-left:9px;
	mso-char-indent-count:1;}
.xl64
	{color:#444A52;
	font-weight:700;
	font-family:Inherit;
	mso-generic-font-family:auto;
	mso-font-charset:0;
	text-align:left;
	vertical-align:top;
	border:1.0pt solid #E4E9F0;
	background:#F5F7F7;
	mso-pattern:black none;
	white-space:normal;
	padding-left:9px;
	mso-char-indent-count:1;}
.xl65
	{color:#444A52;
	font-family:Roboto;
	mso-generic-font-family:auto;
	mso-font-charset:0;
	text-align:left;
	vertical-align:top;
	border:1.0pt solid #E4E9F0;
	background:#F5F7F7;
	mso-pattern:black none;
	white-space:normal;
	padding-left:9px;
	mso-char-indent-count:1;}
.xl66
	{color:#444A52;
	font-family:Roboto;
	mso-generic-font-family:auto;
	mso-font-charset:0;
	text-align:left;
	vertical-align:top;
	border:1.0pt solid #E4E9F0;
	background:#FDFDFD;
	mso-pattern:black none;
	white-space:normal;
	padding-left:9px;
	mso-char-indent-count:1;}
-->
</style>
</head>

<body link="#0563C1" vlink="#954F72">



MODELO | DESCRIÇÃO
-- | --
Grupo de agentes/Agent Group | sRotear   interações para um grupo específico de agentes. Isso pode ser baseado no   tipo de trabalho (por exemplo, Tier1Agents), local ou local (por exemplo,   MiamiAgents), etc.
Auto atendimento/Auto Attendant | Roteamento   implementado para suportar menus simples (por exemplo, prompts de áudio e   seleções de toque), imitando a funcionalidade de um IVR básico.
Misturado/Blended | Roteamento   que permite que o mesmo agente ou recursos selecionados lidem com mais de um   tipo de interação (por exemplo, Inbound/Outbound, multimídia). A   combinação deve ser usada para fazer uso de recursos subutilizados e evitar   flutuações no nível de serviço (por exemplo, forçar os agentes a fazer logoff   de uma fila de voz devido a um influxo de interações de mídia   social). Considere quantas interações de cada tipo um agente pode   manipular por vez e defina as regras de capacidade de acordo. Além   disso, incremente e/ou limite os valores de prioridade com base nos tipos de   interação, para que as interações de voz nem sempre tenham precedência sobre   as que não são de voz ou vice-versa.
Caso de Negócios/Business Case | Roteamento   para fornecer tratamentos diferenciados de atendimento ao cliente para   processos de negócios específicos ou casos de uso (por exemplo, campanhas de   marketing, status da conta, pagamento devido, cobranças, regulamentação   etc.).
Retornos de chamada/Retenção virtual/Callbacks/Virtual Hold | Roteamento   responsável pela priorização e direcionamento quando uma chamada de retorno   para um cliente é necessária, solicitada ou agendada.
Roteamento em cascata /Cascading Routing| Roteamento   que usa várias camadas de decisão de roteamento priorizado, de modo que, se   as condições para as instruções de roteamento de prioridade mais alta não   forem atendidas, o roteamento transbordará automaticamente para o próximo   nível de instruções de roteamento. As condições também podem ser   verificadas em paralelo, para que não se perca tempo esperando para executar   a primeira camada de decisão antes de considerar a próxima.
Grupos de roteamento/caça de concierge /Concierge Routing/Hunt Groups | Encaminhamento   para um agente específico ou um pequeno grupo de indivíduos quando for   necessário atendimento especializado ou personalizado. Normalmente, a   interação é direcionada primeiro ao agente principal atribuído a uma conta de   cliente específica. No entanto, se esse agente não estiver disponível, o   roteamento procurará o próximo membro da equipe disponível em um pequeno   grupo de busca.
Canal cruzado /Cross-Channel| Roteamento   com base no que um cliente estava fazendo em outro canal (por exemplo, um   cliente está no site da empresa ou no aplicativo móvel e depois liga).
Roteamento padrão/Default Routing | Rotear   uma interação para o destino padrão que deve ser usado quando nenhuma das   condições para as camadas anteriores de decisão de roteamento for   atendida. Isso normalmente ocorre quando os volumes de tráfego aumentam   por algum motivo e os limites de tempo limite para as camadas anteriores   foram excedidos, de modo que a interação transborda para o destino final   padrão.
Roteamento dinâmico/Dynamic Routing | Roteamento   que se ajusta automaticamente com base em prioridades e condições   pré-especificadas. Os exemplos incluem: roteamento em cascata, expansão   de destino, limites de tempo limite, quedas de dados, feriados, emergências,   interrupções de serviço etc. ambientes de contact center para redirecionar   manualmente o tráfego.
Gerenciamento de carga de trabalho empresarial /Enterprise Workload Management| Roteamento   de itens de trabalho em toda a empresa. Os mesmos recursos de roteamento   da Genesys que podem ser usados ​​para direcionar as interações voltadas para   o cliente (chamadas, e-mails, bate-papo etc.) também podem ser aproveitados   para agendar, atribuir, distribuir e rastrear atividades de trabalho no   back-office.
Escalações/Escalations | Roteamento   de interações que requerem o suporte ou a intervenção de um agente mais   qualificado (por exemplo, "Nível 2") ou gerente. Isso pode ser   tratado como uma transferência, ou pode envolver uma teleconferência ou   suporte consultivo com o especialista.
Serviços eletrônicos/Multimídia/eServices/Multimedia/Interaction Type (a.k.a. Call Type) | Roteamento   de vários tipos de interações não-voz (por exemplo, e-mail, chat, texto,   social, vídeo, mídia aberta). Diferentes tipos de mídia podem exigir   habilidades exclusivas (por exemplo, +Escrita pode ser um tipo de habilidade   para e-mail, bate-papo e texto). Considere quantas interações de cada   tipo um agente pode lidar por vez e defina as regras de capacidade de acordo   (por exemplo, 1-4 chats por agente).
Tipo de interação (também conhecido como tipo de chamada) | Roteamento   baseado no tipo de cliente e/ou intenção do cliente. Isso geralmente é   determinado com base no número discado (DNIS), na seleção de menu do chamador   ou na atividade dentro do IVR, ou na análise de conteúdo em um e-mail ou   bate-papo.
Integração de resposta de voz interativa/Interactive Voice Response Integration | Rotear   uma chamada para o destino apropriado com base no que o chamador fez ou   selecionou em um IVR. Com base na integração com a Genesys Voice   Platform (GVP) ou um IVR de terceiros.
Roteamento do último agente/Last Agent Routing | Roteamento   para o último agente com o qual o cliente interagiu. Especialmente útil   para rotear para um único ponto de contato (como um responsável pelo caso) ou   para chamadas perdidas que retornam dentro de um período de tempo   especificado.
Saída/Outbound | Roteamento   de interações que são iniciadas pela organização e direcionadas para o   cliente (por exemplo, chamadas de saída, campanhas de marketing, cobranças,   e-mails de saída, mensagens de texto, contatos proativos etc.).
Agentes de estouro/compartilhamento/Overflow/Sharing Agents | Roteamento   para uma fila alternativa ou grupo de agentes, quando o destino principal não   estiver disponível ou estiver sendo utilizado em excesso. Empréstimos e   empréstimos de recursos podem depender do cumprimento de certas condições de   negócios predeterminadas, para que os picos no volume de uma equipe não   afetem indevidamente a disponibilidade ou os níveis de serviço de outra   equipe.
Alocação Percentual/Percentage Allocation | Distribuição   de interações entre filas com base em uma porcentagem do volume total (por   exemplo, 60% para o Site A e 40% para o Site B).
Fila de prioridade /Priority Queuing| Roteamento   que usa valores de prioridade para dar preferência a uma fila ou interação   sobre outra. As prioridades podem ser incrementadas ao longo do tempo,   portanto, se uma interação de classificação mais baixa estiver esperando por   mais tempo, ela será atendida antes de uma interação de classificação mais   alta que acabou de chegar. Isso garante que nenhuma interação espere   muito tempo pelo serviço.
Tratamentos de fila /Queue Treatments| Roteamento   que reproduz áudio (por exemplo, música, anúncios, mensagens) ou fornece   certas funcionalidades enquanto os chamadores estão esperando na fila ou em   espera.
Toque sem resposta/redirecionamento em caso de não resposta   (RONA) Ring No Answer/Redirect on No Answer (RONA)| Roteamento   para um destino alternativo se o destino original não responder (por exemplo,   o agente falhou ao efetuar logout). O agente será alvo da primeira vez,   mas depois disso uma ação pode ser especificada (por exemplo, sair) para que   o agente não seja alvo novamente posteriormente.
Segmentação/Segmentation | Roteamento   com base no tipo de cliente, no valor da oportunidade ou em outros dados de   segmentação de marketing.
Com base em habilidades /Skills-Based| Roteamento   para o agente disponível mais qualificado com base em uma combinação de   habilidades especificadas no roteamento. Isso às vezes é chamado de   "roteamento em nível de agente", pois o roteamento Genesys é capaz   de analisar o conjunto exclusivo de habilidades de um agente   individual. No entanto, na prática, o roteamento normalmente procura o   conjunto de habilidades desejado em uma "fila universal" para   otimizar a utilização em um grande conjunto de recursos.
Roteamento estatístico/Statistical Routing | Roteamento   baseado em várias pesquisas de banco de dados e condições operacionais, como   tempo de espera estimado (EWT), profundidade da fila, níveis de serviço   (SLAs), metas de desempenho, ocupação de agentes, utilização de habilidades,   sazonalidade, eventos especiais, processos de negócios etc.
Expansão de destino/Target Expansion | Roteamento   que expande seus destinos para aumentar o pool de agentes aptos a atender uma   interação, seja após um período de tempo ou acionado pelo Tempo de Espera   Estimado (EWT) superior a um limite definido. O nível de habilidade mais   alto é direcionado primeiro até que o limite de tempo seja atingido e, em   seguida, o roteamento se expande para incluir o próximo nível de habilidades,   em cascata até que todos os níveis de habilidade sejam incluídos na   segmentação. Isso garante que, se o conjunto de agentes mais adequado   não estiver disponível, após o tempo limite de expansão, o próximo conjunto   de agentes mais adequado será incluído no direcionamento.
Transferências/Transfers | Roteamento   para lidar com transferências. Necessidade de considerar o roteamento   para transferências direcionadas para dentro ou para fora do contact   center. A prioridade de roteamento pode variar dependendo se é uma   transferência interna (dentro do contact center) ou uma transferência externa   (de/para um grupo ou entidade externa).
trabalhadores/Workforce | Encaminhamento   que leva em consideração várias considerações da força de trabalho, como   horários, redução, absenteísmo, treinamento, desenvolvimento de habilidades,   área de trabalho/ferramentas, novas contratações/carreiras, afinidade do   agente para interações específicas, terceirizados, sindicatos, leis   trabalhistas etc.
Correio de voz/Voicemail | Encaminhamento   de chamadas de entrada para correio de voz (por exemplo, caixas de entrada de   correio de voz em grupo após o expediente). Ou roteamento de saída que   aborda o que fazer se um correio de voz for alcançado (ou seja, deixar uma   mensagem ou não).



</body>

</html>

## Quantas habilidades totais uma organização normalmente tem?
Depende do tamanho e dos requisitos da organização, mas geralmente vemos um intervalo entre 20 e 75 habilidades no total. Quando você começa a se aproximar de 100 ou mais habilidades, precisa questionar se está realmente aproveitando o poder combinatório das habilidades da Genesys (ou seja, onde os agentes podem ser multi-qualificados e o roteamento da Genesys pode procurar várias combinações de habilidades).O agente médio geralmente é altamente proficiente em 3-4 habilidades cada, mas pode ter proficiência menor em outras habilidades para fornecer backup. Agentes especialistas podem ser altamente proficientes em 10 ou mais habilidades.

## Quantos aplicativos de roteamento uma organização deve ter?
Como regra geral, uma grande solução de contact center (uma importante linha de negócios) não deve precisar de mais de 10 aplicativos de roteamento e sub-rotinas (sem contar objetos e sub-rotinas reutilizáveis ​​usados ​​em todos os aplicativos).

## O que são níveis de proficiência de habilidade e para que são usados?
A proficiência é uma maneira opcional de refletir o quão relativamente bom um agente é em uma habilidade específica (por exemplo, nível 5 de espanhol vs. 10). Seguindo o princípio de design "Simplicidade", é melhor manter três (ou menos) níveis de proficiência em habilidades &endash; por exemplo, Alto = 9, Médio = 6 e Baixo = 3. Isso permite que níveis de proficiência adicionais sejam adicionados se necessário no futuro.
A proficiência permite a Expansão de Destino &endash; por exemplo, primeiro direcione agentes com habilidade de proficiência em Vendas ≥ 9 por 15 segundos, depois direcione Vendas ≥ 6 por 15 segundos; em seguida, segmente Vendas > 0). Isso evita que os agentes tenham que fazer logoff de um grupo/fila de agentes e fazer logon em outro, o que é um problema comum com soluções baseadas em ACD legadas e pode ser evitado usando o roteamento Genesys.



## Referencias

https://docs.genesys.com/Documentation/Composer/8.1.4/Help/RoutingFAQs

