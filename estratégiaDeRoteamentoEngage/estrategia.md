# O que é um aplicativo de roteamento? Quais são os elementos básicos?
O roteamento fornece instruções sobre como lidar e para onde direcionar as interações em diferentes circunstâncias.  Conceitualmente, um aplicativo de roteamento é como uma série de instruções priorizadas que levam em consideração vários fatores para determinar o destino de roteamento ideal e o que fazer a seguir se essa ação não for possível dentro das restrições especificadas.

Os aplicativos de roteamento são compostos de vários elementos diferentes, descritos aqui em um nível conceitual:

Os dados podem vir de várias fontes e podem incluir dados de clientes, contextuais, operacionais ou analíticos. Dados anexados, que estão incluídos nas mensagens de chamada como pares de valores-chave (KVPs), são o que você sabe sobre uma interação específica. Os dados anexados podem ser adicionados e atualizados ao longo da vida da interação (por exemplo, à medida que uma chamada flui pelo IVR, roteamento, desktop do agente e relatórios).
Habilidades são o que você sabe sobre um agente. Para identificar o melhor recurso disponível para lidar com uma interação específica, o roteamento procura as combinações desejadas de habilidades no nível individual (por agente), no nível da equipe (por grupo de habilidades ou fila') ou em um pool virtual de recursos ( fila virtual').


## Quais são alguns dos tipos mais comuns de roteamento?

<html>
<body>
<!--StartFragment-->

MODELO | DESCRIÇÃO
-- | --
Grupo de agentes | sRotear interações para um grupo específico de agentes. Isso pode ser baseado no tipo de trabalho (por exemplo, Tier1Agents), local ou local (por exemplo, MiamiAgents), etc.
Auto atendimento | Roteamento implementado para suportar menus simples (por exemplo, prompts de áudio e seleções de toque), imitando a funcionalidade de um IVR básico.
Misturado | Roteamento que permite que o mesmo agente ou recursos selecionados lidem com mais de um tipo de interação (por exemplo, Inbound/Outbound, multimídia). A combinação deve ser usada para fazer uso de recursos subutilizados e evitar flutuações no nível de serviço (por exemplo, forçar os agentes a fazer logoff de uma fila de voz devido a um influxo de interações de mídia social). Considere quantas interações de cada tipo um agente pode manipular por vez e defina as regras de capacidade de acordo. Além disso, incremente e/ou limite os valores de prioridade com base nos tipos de interação, para que as interações de voz nem sempre tenham precedência sobre as que não são de voz ou vice-versa.
Caso de Negócios | Roteamento para fornecer tratamentos diferenciados de atendimento ao cliente para processos de negócios específicos ou casos de uso (por exemplo, campanhas de marketing, status da conta, pagamento devido, cobranças, regulamentação etc.).
Retornos de chamada/Retenção virtual | Roteamento responsável pela priorização e direcionamento quando uma chamada de retorno para um cliente é necessária, solicitada ou agendada.
Roteamento em cascata | Roteamento que usa várias camadas de decisão de roteamento priorizado, de modo que, se as condições para as instruções de roteamento de prioridade mais alta não forem atendidas, o roteamento transbordará automaticamente para o próximo nível de instruções de roteamento. As condições também podem ser verificadas em paralelo, para que não se perca tempo esperando para executar a primeira camada de decisão antes de considerar a próxima.
Grupos de roteamento/caça de concierge | Encaminhamento para um agente específico ou um pequeno grupo de indivíduos quando for necessário atendimento especializado ou personalizado. Normalmente, a interação é direcionada primeiro ao agente principal atribuído a uma conta de cliente específica. No entanto, se esse agente não estiver disponível, o roteamento procurará o próximo membro da equipe disponível em um pequeno grupo de busca.
Canal cruzado | Roteamento com base no que um cliente estava fazendo em outro canal (por exemplo, um cliente está no site da empresa ou no aplicativo móvel e depois liga).
Roteamento padrão | Rotear uma interação para o destino padrão que deve ser usado quando nenhuma das condições para as camadas anteriores de decisão de roteamento for atendida. Isso normalmente ocorre quando os volumes de tráfego aumentam por algum motivo e os limites de tempo limite para as camadas anteriores foram excedidos, de modo que a interação transborda para o destino final padrão.
Roteamento dinâmico | Roteamento que se ajusta automaticamente com base em prioridades e condições pré-especificadas. Os exemplos incluem: roteamento em cascata, expansão de destino, limites de tempo limite, quedas de dados, feriados, emergências, interrupções de serviço etc. ambientes de contact center para redirecionar manualmente o tráfego.
Gerenciamento de carga de trabalho empresarial | Roteamento de itens de trabalho em toda a empresa. Os mesmos recursos de roteamento da Genesys que podem ser usados ​​para direcionar as interações voltadas para o cliente (chamadas, e-mails, bate-papo etc.) também podem ser aproveitados para agendar, atribuir, distribuir e rastrear atividades de trabalho no back-office.
Escalações | Roteamento de interações que requerem o suporte ou a intervenção de um agente mais qualificado (por exemplo, "Nível 2") ou gerente. Isso pode ser tratado como uma transferência, ou pode envolver uma teleconferência ou suporte consultivo com o especialista.
Serviços eletrônicos/Multimídia | Roteamento de vários tipos de interações não-voz (por exemplo, e-mail, chat, texto, social, vídeo, mídia aberta). Diferentes tipos de mídia podem exigir habilidades exclusivas (por exemplo, +Escrita pode ser um tipo de habilidade para e-mail, bate-papo e texto). Considere quantas interações de cada tipo um agente pode lidar por vez e defina as regras de capacidade de acordo (por exemplo, 1-4 chats por agente).
Tipo de interação (também conhecido como tipo de chamada) | Roteamento baseado no tipo de cliente e/ou intenção do cliente. Isso geralmente é determinado com base no número discado (DNIS), na seleção de menu do chamador ou na atividade dentro do IVR, ou na análise de conteúdo em um e-mail ou bate-papo.
Integração de resposta de voz interativa | Rotear uma chamada para o destino apropriado com base no que o chamador fez ou selecionou em um IVR. Com base na integração com a Genesys Voice Platform (GVP) ou um IVR de terceiros.
Roteamento do último agente | Roteamento para o último agente com o qual o cliente interagiu. Especialmente útil para rotear para um único ponto de contato (como um responsável pelo caso) ou para chamadas perdidas que retornam dentro de um período de tempo especificado.
Saída | Roteamento de interações que são iniciadas pela organização e direcionadas para o cliente (por exemplo, chamadas de saída, campanhas de marketing, cobranças, e-mails de saída, mensagens de texto, contatos proativos etc.).
Agentes de estouro/compartilhamento | Roteamento para uma fila alternativa ou grupo de agentes, quando o destino principal não estiver disponível ou estiver sendo utilizado em excesso. Empréstimos e empréstimos de recursos podem depender do cumprimento de certas condições de negócios predeterminadas, para que os picos no volume de uma equipe não afetem indevidamente a disponibilidade ou os níveis de serviço de outra equipe.
Alocação Percentual | Distribuição de interações entre filas com base em uma porcentagem do volume total (por exemplo, 60% para o Site A e 40% para o Site B).
Fila de prioridade | Roteamento que usa valores de prioridade para dar preferência a uma fila ou interação sobre outra. As prioridades podem ser incrementadas ao longo do tempo, portanto, se uma interação de classificação mais baixa estiver esperando por mais tempo, ela será atendida antes de uma interação de classificação mais alta que acabou de chegar. Isso garante que nenhuma interação espere muito tempo pelo serviço.
Tratamentos de fila | Roteamento que reproduz áudio (por exemplo, música, anúncios, mensagens) ou fornece certas funcionalidades enquanto os chamadores estão esperando na fila ou em espera.
Toque sem resposta/redirecionamento em caso de não resposta (RONA) | Roteamento para um destino alternativo se o destino original não responder (por exemplo, o agente falhou ao efetuar logout). O agente será alvo da primeira vez, mas depois disso uma ação pode ser especificada (por exemplo, sair) para que o agente não seja alvo novamente posteriormente.
Segmentação | Roteamento com base no tipo de cliente, no valor da oportunidade ou em outros dados de segmentação de marketing.
Com base em habilidades | Roteamento para o agente disponível mais qualificado com base em uma combinação de habilidades especificadas no roteamento. Isso às vezes é chamado de "roteamento em nível de agente", pois o roteamento Genesys é capaz de analisar o conjunto exclusivo de habilidades de um agente individual. No entanto, na prática, o roteamento normalmente procura o conjunto de habilidades desejado em uma "fila universal" para otimizar a utilização em um grande conjunto de recursos.
Roteamento estatístico | Roteamento baseado em várias pesquisas de banco de dados e condições operacionais, como Tempo de Espera Estimado (EWT), profundidade da fila, níveis de serviço (SLAs), metas de desempenho, ocupação de agentes, utilização de habilidades, sazonalidade, eventos especiais, processos de negócios etc.
Expansão de destino | Roteamento que expande seus destinos para aumentar o pool de agentes aptos a atender uma interação, seja após um período de tempo ou acionado pelo Tempo de Espera Estimado (EWT) maior que um limite definido. O nível de habilidade mais alto é direcionado primeiro até que o limite de tempo seja atingido e, em seguida, o roteamento se expande para incluir o próximo nível de habilidades, em cascata até que todos os níveis de habilidade sejam incluídos na segmentação. Isso garante que, se o conjunto de agentes mais adequado não estiver disponível, após o tempo limite de expansão, o próximo conjunto de agentes mais adequado será incluído no direcionamento.
Transferências | Roteamento para lidar com transferências. Necessidade de considerar o roteamento para transferências direcionadas para dentro ou para fora do contact center. A prioridade de roteamento pode variar dependendo se é uma transferência interna (dentro do contact center) ou uma transferência externa (de/para um grupo ou entidade externa).
trabalhadores | Encaminhamento que leva em consideração várias considerações da força de trabalho, como horários, redução, absenteísmo, treinamento, desenvolvimento de habilidades, área de trabalho/ferramentas, novas contratações/carreiras, afinidade do agente para interações específicas, terceirizados, sindicatos, leis trabalhistas etc.
Correio de voz | Encaminhamento de chamadas de entrada para correio de voz (por exemplo, caixas de entrada de correio de voz em grupo após o expediente). Ou roteamento de saída que aborda o que fazer se um correio de voz for alcançado (ou seja, deixar uma mensagem ou não).

<!--EndFragment-->
</body>
</html>

## Genesys Routing Features

<img src="https://user-images.githubusercontent.com/52088444/151793188-aa551d27-559b-428c-a607-c4094d79adec.png" width="90%"></img> 



## Roteamento baseado em data e hora
<img src="https://user-images.githubusercontent.com/52088444/151793623-3b661bfe-3197-46ff-92e8-b57479565c58.png" width="90%"></img> 

## Roteamento baseado em Skills

<img src="https://user-images.githubusercontent.com/52088444/151793831-f220d9ef-9e69-4332-a83c-01d452129c07.png" width="90%"></img> 


## Threshold function


<img src="https://user-images.githubusercontent.com/52088444/151794602-bed14336-6812-4ead-9a0d-c204d3a2b1d6.png" width="90%"></img> 



<img src="https://user-images.githubusercontent.com/52088444/151794745-8314103a-bdd6-4e07-ac1f-bcaea2ba0a6e.png" width="90%"></img> 

**Obs: file lookup, config lookup, db lookup (pesquisa de arquivo, pesquisa de configuração,
pesquisa de banco de dados)

<img src="https://user-images.githubusercontent.com/52088444/151795268-ea2b72a9-7747-4cb7-8892-138bc69de69c.png" width="90%"></img> 

https://www.youtube.com/watch?v=R_7dr8GfZFo&t=16s