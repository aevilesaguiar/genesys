# Conceitos Iniciais


*DAC*: Esse “Distribuidor Automático de Chamadas” permite definir como as chamadas serão distribuídas para os colaboradores, em tempo real. Assim, seleciona um usuário livre para direcional as ligações por ordem de chegada.

 *VDN* do inglês Vector Directory Number, é um ramal virtual (não-físico) utilizado para o roteamento das chamadas. Toda chamada proveniente do PABX está associada a um VDN que, por sua vez, está sempre associado a um vetor. O VDN funciona como referência na vetorização

**O que é REST?**
 Um estilo arquitetônico que define um conjunto de recomendações para o design de aplicações que usam o protocolo HTTP para transmissão de dados.  
As diretrizes dessa API permite que os desenvolvedores implementem os detalhes necessários de acordo com suas próprias necessidades. Os serviços da Web criados seguindo o estilo de arquitetura REST são chamados RESTful Webservices.


**O que é SOAP?**
SOAP é um sistema de protocolo de comunicação padrão que permite que processos usando diferentes sistemas operacionais, como Linux e Windows, se comuniquem via HTTP e XML. As APIs baseadas em SOAP foram projetadas para criar, recuperar, atualizar e excluir registros como contas, senhas, leads e objetos personalizados.
As APIs SOAP aproveitam as vantagens de criar protocolos baseados na Web, como HTTP e XML, que já estão operando em todos os sistemas operacionais. É por isso que seus desenvolvedores podem manipular facilmente os serviços da Web e obter respostas sem se importar com o idioma e as plataformas.

## REST x SOAP
O REST opera por meio de uma interface consistente para acessar os recursos nomeados. É mais usado quando se publica uma API pública pela Internet. 
Já o SOAP, por outro lado, expõe componentes da lógica do aplicativo como serviços, e não como dados. Além disso, opera por meio de diferentes interfaces. 
Simplificando, o REST acessa os dados enquanto o SOAP executa operações por meio de um conjunto mais padronizado de mensagens. Ainda assim, na maioria dos casos, tanto REST como o SOAP podem ser usados para obter o mesmo resultado (e ambos são infinitamente escaláveis), com algumas diferenças na forma como são configurados.

*Os tópicos abaixo vão ajudar a entender o embate REST x SOAP:*
•	A API REST não possui um padrão oficial, pois é um estilo de arquitetura. A API SOAP, por outro lado, possui um padrão oficial porque é um protocolo;
•	REST usa vários padrões como HTTP, JSON, URL e XML, enquanto SOAP é baseada em HTTP e XML;
•	Como REST implementa vários padrões, são necessários menos recursos e largura de banda em comparação com o SOAP que usa XML para a sua criação, resultando em um arquivo de tamanho grande;
•	As maneiras pelas quais as duas APIs expõem as lógicas de negócios também são diferentes. REST aproveita a exposição da URL como @path (“/ WeatherService”), enquanto o uso da API SOAP de interfaces de serviços como @WebService;
•	REST usa a linguagem de descrição de aplicações da Web e SOAP usa a linguagem de descrição de serviços da Web para descrever as funcionalidades oferecidas pelos serviços da web;
•	REST é compatível com JavaScript e também pode ser implementado facilmente. Já SOAP também é conveniente com JavaScript, mas não suporta uma implementação maior. 

