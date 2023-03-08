# CI (Continuos Integration)/CD (Continuos Delivery) Pipeple

O principal objetivo de se utilizar a *Pipeline* é automatizar o processo de entrega de software colocando em produção de forma rápida e continua sem perde a qualidade do projeto.

A Pipeline é uma sequencia de etapas que precisam ser executadas para colocar a aplicação em produção, como fazer o *build*, executar testes automatizados e a implantação em ambientes de testes e produção.
O objetivo principal da entrega continua é permitir um fluxo constante de atualizações disponinilizadas em produção por uma espécie de linha de produção de software automatizado, o Pipeline de entrega continua que fazem as coisas acontecerem. Tudo isso está ligado ao metodologia ágil para gerar entregas constantes e entregar que gere valor para o cliente. 

A utilização da *Pipeline* traz vantagens e benéficas por si só, pois agiliza e evita os erros humanos e com um número menor de erros permite uma entrega rápida.
Os *bugs* são identificados mais rápidamente e os desenvolvedores consegue atuar em novas *features* sem se preocupar em colocar o código em produção. Logs de atualizações, testes e *deploys* são acessíveis para verificação a qualquer momento.

Não existe um modo fixo da *Pipeline*, ele pode ser construido de acordo com as caracteristicas, necessidades do projeto e das equipes de desenvolvimento. O Pipleine é multidisciplinar ele envolve equipes e profissionais bem distindos na criação e utulização.

Uma boa *Pipeline* deve ser, boa, rápida e precisa.

## Ciclo Básico de Vida da Pipeline

* O código é comitado para o gerenciamento de controle de versão
* Build - será feito o merge para unificar o código já existente com a atualização
* Teste Unitários/Automatizados onde é executado vários testes para garantir o funcionamento da aplicação
* Deploy - realizado no ambiente de testes para
* Teste em ambiente QA
* Deploy em produção
* Avaliar e Validar

Neste ciclo a qualquer momento pode ser obter um feedback para a equipe de desenvolvimento, e isto é feito sempre que um erro foi encontrado de forma automática através do disparo de e-mail ou mensagem.
A *Pipeline* também deverá prever o que acontecerá em caso de erro, como por exemplo fazer um *rollback*.

Existem algumas ferramentas para criar uma *Pipeline*, como por exemplo o Jenkins que é opensource e oferece puglins para dar suporte na criação, implantação e automatização
Tem também o Azure Pipelines e AWS CodePipeline voltados para os serviços da Amazon.
GitHub, Gitlab e o Bitbucket também oferecem ferramentas para automatizar.

Antes de uma empresa de desenvolvimento adotar um CI/CD Pipeline deve analisar o processo atual para poder decidir qual o método melhor que se aplica as suas necessidades.

