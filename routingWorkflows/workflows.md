# Introdução aos fluxos de trabalho de roteamento

Esta seção fornece uma visão geral de alto nível da criação de estratégias de roteamento baseadas em SCXML ("fluxos de trabalho") no ambiente de desenvolvimento integrado do Composer.

## O que é um fluxo de trabalho de roteamento(What is a Routing Workflow?)
**O que é Roteamento?**
Em termos mais simples, roteamento é o processo de enviar uma interação para um alvo, por exemplo, enviar uma chamada telefônica para um agente. Na prática, uma interação deve passar por vários tipos de processamento entre o momento em que chega ao contact center e a seleção e encaminhamento para o alvo apropriado. Cada ponto de processamento é uma oportunidade para que algum tipo de processamento ocorra ou para o Universal Routing Server (URS) tomar uma decisão com base na situação atual – com o objetivo de entregar a interação ao destino mais apropriado.


**O que é um fluxo de trabalho de roteamento?**
Um fluxo de trabalho de roteamento é um conjunto de decisões e instruções que informa ao Universal Routing Server como lidar e para onde direcionar as interações em diferentes circunstâncias.

Em qualquer ponto de processamento no fluxo de trabalho, apenas um dos vários resultados possíveis pode ser ideal. O Universal Routing Server usa as instruções de fluxo de trabalho para determinar qual resultado é ideal e envia a interação ao longo de uma rota especificada de acordo.

Existem várias maneiras de criar um fluxo de trabalho baseado em SCXML no Composer:

- Trabalhando com blocos para criar um fluxo de trabalho na perspectiva do Composer ou do Composer Design .
- Escrevendo código no Composer_Code_Editors (que pode incluir o uso de templates).
- Importando um fluxo de trabalho existente .

**Blocos de roteamento e portas**
Cada ponto de processamento é representado graficamente em um fluxo de trabalho por um bloco de roteamento , que possui:

- Uma porta de entrada
- Uma ou mais portas de exceção vermelhas
- Uma ou mais portas de saída verdes.

## Diagrama de arquitetura para fluxos de trabalho

1 - Para dar o "Big Picture" e mostrar os vários componentes Genesys usados ​​para fluxos de trabalho baseados em SCXML, abaixo está um diagrama de alto nível da arquitetura Universal Routing 8.x.As etapas de criação e processamento da estratégia baseada em SCXML acima são relacionadas aos números abaixo. O desenvolvedor especifica os objetos do Configuration Server como destinos de roteamento antes de criar o aplicativo de roteamento no Composer. Por exemplo, um destino de roteamento pode ser um agente (objeto Pessoa) ou Grupo de Agentes ou uma interação pode ser enviada para uma fila. O desenvolvedor também pode criar fluxos de trabalho que roteiam com base no valor de uma estatística do Stat Server ou uma estatística que você definiu no Composer's Statistics Builder .

2 - O desenvolvedor (ou outra pessoa) cria e testa o aplicativo de roteamento e o implanta manualmente em um servidor de aplicativos da web . Feito isso, o ciclo de vida de tempo de execução da lógica de roteamento pode começar com uma solicitação de roteamento.

3- O URS obtém uma mensagem EventRouteRequest do T-Server ou outro servidor de mídia , como um servidor de mídia eServices .  

4 - A solicitação vai para o Ponto de Roteamento. O URS obtém a URL do servidor de aplicação a ser contatado sobre a estratégia SCXML a ser fornecida, que é propriedade do Ponto de Roteamento. Depois que a URL é obtida, o ORS emite a solicitação HTTP GET (ou POST) para o servidor de aplicativos.

5 - O servidor de aplicativos executa a solicitação e retorna o documento SCXML de volta ao ORS.

6 - Ao obter a resposta, o ORS passa o documento SCXML recebido para o mecanismo SCXML. O mecanismo SCXML executa o aplicativo SCXML, invocando serviços ORS/URS conforme necessário.

7 - ORS ou URS emite uma mensagem RequestRouteCall para o servidor de mídia.

<img src="https://user-images.githubusercontent.com/52088444/151800103-73cf6dc5-bddc-46a6-b228-4ecb648d9677.png" width="90%"></img> 

**Entregando uma interação com o Agent Desktop**

Depois que o ORS/URS identifica um destino de roteamento, outros servidores são envolvidos no processo de entrega da interação ao desktop do agente.

- No caso de interações de voz, os servidores SIP/T-Servers estão envolvidos.
- No caso de arquiteturas baseadas em PBX (não servidores SIP), PBXs estão envolvidos (pelos comandos de T-Servers).

Resumindo
<html>
<body>
<!--StartFragment-->

Tipo de interação | Identificação do alvo | Entregue na área de trabalho
-- | -- | --
Multimídia | URS/ORS | Servidor de interação > Servidor de mídia
Voz sobre IP | URS/ORS | Servidor SIP (inclui controle de mídia)
Arquiteturas antigas/PBX | URS/ORS | T-Server > PABX

<!--EndFragment-->
</body>
</html>




## Referencias
https://docs.genesys.com/Documentation/Composer/8.1.4/Help/IntroductiontoRoutingWorkflows
https://docs.genesys.com/Documentation/Composer/8.1.4/Help/WhatisaRoutingWorkflow
https://docs.genesys.com/Documentation/Composer/8.1.4/Help/ArchitectureDiagramforWorkflows