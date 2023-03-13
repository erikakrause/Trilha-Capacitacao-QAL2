# Arquitetura de Software de Mensageria

Arquitetura orientada a eventos é um tipo de arquitetura que reage a eventos de um serviço disparando mensagens para outros serviços interessados no evento. 
É um tipo de arquitetura utilizada nas aplicações que contém microsserviços, pois a mensagem é uma conexão dos serviços em seus respectivos processos. 

Uma aplicação orientada a eventos é uma aplicação que esta organizada para reagir a eventos que por definição é algo que acontece em um determinado tempo. A arquitetura orientada a eventos tem uma grande aderenecia a estrutura de microserviços, mas nada impede que um desenvolvedor faça em uma estrutura monolitica, afinal eventos podem ser disparados dentro de um mesmo ambiente ou para ambientes diferentes.
A diferença é que se pode usar aplicações de mensageria para conectar os serviços ou processos de fila internos do software. 

Alguns módulos ao executar uma determinada tarefa vão disparar eventos os chamados produtores, estes eventos serão enviados para uma cama de transportes. A camada de transporte é responsábel por receber todos os eventos  mandalos para a camada de manipulação.
A camada de manipulação é responsável por organizar os eventos e colocá-los nas filas adequadas para enviá-los para os respectivos consumidores.

A EDA podem utilizar estruturas robustas de mensageria para trabalhar o fluxos de eventos e mensagens ou podem usar estruturas internas das ferramentas para fazer esse processo. Tudo dependerá do tamanho tamanho e escopo do projeto. 

Publisher/Subcriber

Utilizando o método Pub/Sub os eventos são enviados ao por exemplo ao *Apache Kafka* que por sua vez tem o trabalho de endereçá-los aos respectivos consumidores dos eventos.

Temos também o *Event Sourcing* este é um padrão orientado a eventos, todos os eventos são registrados e alguns estado passado podem ser recriado a qualquer momento e essa base de registros torna a única fonte de confiaça dos estados da aplicação. Um exemplo é o GIT onde o estado atual é criado a partir de todos os commits já feitos  e podemos dar um rollback nos commmits e retornar a um estado anterior da aplicação.
A utilização desse padrão traz alguns benefícios como audotiria (podem ver o que aconteceu exatamente em cada atualização), criação de um histórico de status e a possibilidade de explorar alternativas diferentes e voltando a um certo ponto do histórico e indo por caminhos diferentes. 

Conforme se utiliza este evento e o projeto crescendo e será notado a importancia de desacoplar do fluxo principal da aplicaçãoe e é mais fácil de dar manutenção.

Pontos positivos:
* sistema independente
* as mensagens ficam armazenadas no *buffer* e serão consumidas quando os recursos estiverem disponíveis 
* os serviços escalam de uma forma mais fácil como um alto volume de processamento das requisições 
* as plataformas de mensageria tem alta disponibilidade e é tolerante a falhas 
* produtores e consumidores de eventos podem ser implementados em diversas linguagens e tecnologias diferentes 

  Pontos fracos:
  * implementar a arquitetura traz uma complexidade operacional grande e requer conhecimento avançado em plataformas de mensageria
  * lidar com falhas parciais podem ser desafiador

  A EDA está cada vez mais ganhando mais popularidade pois ela prove uma maneira efetiva de conectar microsserviços e pode ajudar a criar sistemas que não ficaram obsoletos com facilidade. Quando acomplado com modernas ferramentas de streaming de dados como o próprio Apache Kafka ele se tornará mais versátil, resiliente e confiável. 



