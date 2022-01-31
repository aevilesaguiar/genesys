## O que é ccxml

Call Control eXtensible Markup Language (ccXML), como o nome sugere, é a linguagem de marcação padrão W3C, que fornece recursos avançados de controle de chamadas de telefonia para um aplicativo de fala interativo. Ele controla como as chamadas telefônicas são feitas, atendidas, transferidas, colocadas em conferência e muito mais. CCXML trabalha lado a lado com VoiceXML para fornecer uma solução 100% baseada em padrões e XML para qualquer aplicação de telefonia. No entanto, o ccXML também pode ser usado com outros sistemas de diálogo, como as plataformas tradicionais IVR (Interactive Voice Response) criadas antes do VoiceXML estar disponível.

Ao construir e implantar aplicativos interativos de reconhecimento de voz, os desenvolvedores sempre enfrentam o desafio de fornecer recursos avançados de controle de chamadas telefônicas. Em alguns casos, o ideal é fazer uma ponte entre duas chamadas para um aplicativo de conferência ou, talvez, fornecer roteamento básico de chamadas para que o chamador possa ser conectado a um agente de atendimento ao cliente apropriado, fazer chamadas de saída e assim por diante.

O VoiceXML, por definição, não foi feito para fornecer esses recursos sofisticados e avançados de controle de chamadas e telefonia por conta própria. VoiceXML como padrão foi projetado principalmente para ser uma linguagem de controle de diálogo. O ccXML fornece o mecanismo de controle de chamadas assíncrono baseado em eventos, muito necessário e sofisticado, e uma integração mais estreita com a plataforma de telefonia. Embora o VoiceXML suporte recursos básicos de controle de chamadas, eles são básicos demais para muitos aplicativos de telefonia.


## ccXML e VoiceXML:
ccXML e VoiceXML são complementares entre si, mas não são dependentes ou restritos entre si. O ccXML pode ser usado em conjunto com outros servidores de diálogo, ou mesmo sem um, se o aplicativo desejar apenas recursos de roteamento de chamadas. Embora apenas algumas chamadas telefônicas exijam uma "interação de voz automatizada", todas as chamadas telefônicas exigem o Controle de chamadas. Como resultado, o ccXML pode ser usado e suportado por tudo, desde PBXs até os comutadores telefônicos que executam a própria rede telefônica. Muitas dessas plataformas de telefonia não têm necessidade ou suporte para as coisas que o próprio VoiceXML pode fazer.

## Oportunidades do ccXML:
Há uma série de recursos que o VoiceXML não oferece atualmente, mas o ccXML oferece. Aqui estão alguns deles listados brevemente:
Tratamento e controle intrincados de várias chamadas - incluindo enfileiramento de chamadas e a capacidade de iniciar chamadas de saída a qualquer momento, independentemente da plataforma de diálogo (VoiceXML).
Manipulação de modelos de processamento de eventos mais ricos - Os sistemas de telecomunicações precisam fornecer sinalização contínua, eventos de status e transmissão de mensagens. VoiceXML em seu estado atual, não tem como integrar esses eventos "externos" assíncronos.
Conferência multipartidária + controle de áudio avançado.
A capacidade de vincular cada linha ativa à sua própria instância dedicada do interpretador VoiceXML permite o uso ideal de cada instância VoiceXML.
A capacidade de receber eventos e mensagens de sistemas fora da plataforma ccXML ou VoiceXML.

## Cenários de Aplicação:
- monitoramento de ligações
- call centers personalizados e assistente de telefone
- servidores de anúncios
- aplicativos encontre-me/siga-me
- roteamento inteligente
- conferência multipartidária
- chamada em espera e transferência supervisionada
- aplicativos de cartão telefônico, para citar alguns

