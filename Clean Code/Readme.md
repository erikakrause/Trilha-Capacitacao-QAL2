# Clean Code

## Conceito
Um código compreensivo possibilita a identificação de pontos que precisam ser melhorados.
Passamos mais tempo lendo código do que escrevendo, quanto mais fácil for ler o código menos esforço
fazendo para entendo-lo.
Nosso código deve ser passivo de alterações tanto para a adição de novas funcionalidades, quanto para
aumentar a legibilidade ou manutenibilidade.
Devemos testar nossos códigos, pois isso vai dar-nos segurança para podermnos alterá-los. E garantir que os
cenarios que previmos estão de acordo com o esperado.

## Objetivo 
O objetivo é tornar o desenvolvimento e a manutenção mais simples. Um código limpo evita gastos de manutenção e tornar o software apto para ser atualizado e receber melhorias quando necessário. 

Príncipios do Clean Code:

* Os nomes são importantes (variáveis, funcões, parametros, métodos e classes) - o nome precisa passar uma idéia central. Métodos e Funções usar nomes como verbos e Classes e Objetos como substantivos.
* Regra do Escotéiro, deixe seu código mais limpo do que estava antes de você fazer modificações nele.
* Realizar testes é boa forma de manter a integridade do sistema ao se realizar modificações no código e se torna mais seguro.
* Você é o autor do código, você deve contar uma história clara, simples, linear e curta.
* DRY(Don't Repeat Yourself), o principio diz que cada pedaço de conhecimento de um sistema deve ter uma representação única e totalmente livre de ambiguidades.

## Testes
Um código é considerado limpo uma vez que ele for validado através de testes, e estes também precisam ser limpos e devem utilizar a regra FIRST.
* FAST - Os testes unitários devem ser rápidos, caso contrário serão um enorme gargalo no desenvolvimento da sua aplicação. 
Uma das causas de lentidão nos testes é a dependência de coisas externas como bancos de dados, arquivos e aplicações externas. Eles levam muito tempo para entregar algum resultado. Para criar essas dependências você pode usar mock em seus testes.

* INDEPENDENT - Seus testes devem ser capazes de se validar sozinhos, sem depender do resultado ou estado de um teste anterior. Isso garante que cada teste seja executado individualmente e que o seu resultado só interfira no cenário esperado.

* REPEATABLE - Os testes devem ser capazes de ser executados repetidas vezes em qualquer ambiente sem variação dos seus resultados. 

* SELF-VALIDATING - Os testes unitários devem ser capazes de validar a si mesmos, interpretando os resultados para ver se é o esperado ou não sem uma intervenção manual.

* TIMELY - O principal objetivo ao escrever testes não é ter 100% de cobertura de código. O objetivo é ter testes em que possamos confiar. Mas o que realmente significa confiança? Significa que ao passar, seus testes garantem que o seu código realmente funciona e retorna os valores esperados.
