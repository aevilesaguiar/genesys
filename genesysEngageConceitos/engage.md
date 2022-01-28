# Composer

Composer fornece um ambiente de desenvolvimento integrado (IDE), que permite que usuários técnicos e não técnicos criem:

- Aplicativos de Roteamento




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

