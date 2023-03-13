# O que é Page Object?

*Page Object* é um padrão de design que ajuda a aprimorar a manutenção de testes e reduzir a duplicação de código, também pode ser utilizado para descrever e documentar o fluxo de uma aplicação. Para entender na prática como aplicar *PageObject* criaremos um teste automatizado responsável por fazer o login em uma aplicação.

```
describe('Login', function(){
  it('Sign in', function(){
    cy.visit('www.site.com.br')
    cy.get('input[type="email"]').type('endereco@email.com')
    cy.get('input[type="password"]').type('senha')
    cy.get('btn').contains('Entrar').click()
   })
})
```

A ideia do PageObject é separar os elementos em arquivos diferentes baseados nas páginas em que eles aparecem, assim, escrevemos todos os elementos e métodos específicos daquela página em seu arquivo que é uma classe JavaScript e usamos diretamente nos scripts de teste.

Seguindo esse princípio, criamos uma classe que vai representar o login do nosso teste:

```
class login {
  email(){
    return cy.get('input[type="email"]')
   }
  senha(){
   return cy.get('input[type="password"]')
    }
   entrar(){
    return cy.get('btn').contains('Entrar')
    }
 }

export default login
```

Cada um dos métodos dessa classe representa uma ação de teste. Com a classe criada podemos chamar os métodos da classe login dentro do arquivo de teste login:
```
import Login from '../login.js'

describe('Login', function(){
 const login = new Login()
  it('Sign in', function(){
    cy.visit('www.site.com.br')
    login.email().type('endereco@email.com')
    login.senha().type('senha')
    login.entrar().click()
  })
})
```
Como podemos ver no código acima, a página de login corresponde a um PageObject e esse PageObject pode ser chamado nos Scripts de teste para realizar o login na aplicação. O benefício que ganhamos é que, se a interface mudar, os testes em si não precisam mudar, apenas o código dentro do objeto da página precisa mudar.