# SpringBoot Framework
- Spring Versus Java EE
- O que é SpringBoot?
- Conceito de IoC/DI
- Beans \ AutoWired \ Scopes
- Spring Data JPA
- Etc...

## Spring Framework Fundamentos
- O que é Spring Framework
- Spring Versus Java EE
- Conceito de Inversão de Controle
- Injeção de Dependências
- Beans \ AutoWired \ Scopes

## Spring Framework?
É um framework open source desenvolvido para a plataforma Java baseado nos padrões de projeto, inversão de controle e injeção de dependências.</br>
Sua estrutura é composta por módulos afins de reduzir a complexidade no desenvolvimento de aplicações simples ou corporativa.

## Spring Módulos
<p align="center">
  <img height="350" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdVmXBnm1fS-t0pN7w-zAglYvKrx37zoEZ4HdeszACcU8Ig4PFs_mKlfU49SALDAtrWUE1bj8bZ6lnvDoc4SoM_VxH5Nerime9uuNlIc5S6picvT3ho6Jv8dEmFTv7zrOKFNVDMxg?key=Zq-Isk9ZAG_nIZ1YfHDMRfMs" alt="Spring Framework Runtime" />
</p>
O Spring é baseado no modulo core através dele a gente consegue inicializar um container Spring através do seu contexto e criando os Beans que são os objetos gerenciados pelo container 
Spring nós teremos uma baixa dependência um baixo acoplamento dentro das nossas aplicações e consequentemente conseguimos implementar um projeto baseado a interface para deixar nossas
implementações mais flexíveis e dinâmicas, também podemos em algumas situações ter interações com banco de dados via JDBC ou ORM utilizando alguns frameworks entre outras alternativas.</br>
Também como foco do Spring podemos ampliar a produtividade no desenvolvimento de aplicações web através do módulo de web, que tem na sua composição Servlets, Struts ou composição web conforme padrão Spring. </br>
Sem falta também de módulos para atuar com estruturas voltadas a testes unitários ou testes de n finalidades.
  
## Spring versus Java EE

## Inversão de Controle
Inversion of Control ou IoC, trata-se do redirecionamento do fluxo de execução de um código retirando parcialmente o controle sobre ele e delegando-o para um container.</br>
O principal propósito é minimizar o acoplamento do código.

## Sem - IoC
<p align="center">
  <img width="624" height="428" alt="image" src="https://github.com/user-attachments/assets/a4a8a06f-837e-4b42-9ed6-e3808bc04583" />
</p>

## Com IoC
<p align="center">
  <img width="645" height="473" alt="image" src="https://github.com/user-attachments/assets/ec9d539b-7e98-448b-9114-284e5a76f4f0" />
</p>

## Injeção de Dependências
Injeção de dependências é um padrão de desenvolvimento com a finalidade de manter baixo o nível de acoplamento entre módulos de um sistema.
<p align="center">
  <img width="510" height="446" alt="image" src="https://github.com/user-attachments/assets/587aa0ce-761f-4b83-96ac-c40753ea1408" />
</p>

## Beans 
Objeto que é instanciado (criado), montado e gerenciado por um container através do principio de inversão de controle.

# Scopes
<p align="center">
  <img width="733" height="430" alt="image" src="https://github.com/user-attachments/assets/88ca45b7-4ea5-4c9f-b7df-fb278b8a9529" />
</p>

## Singleton
O container Spring IoC define apenas uma instância do objeto para toda a aplicação.

## Prototype 
Será criado um novo objeto a cada solicitação ao container com finalidade de não inferir mudança de estrutura desses objetos.

## HTTP - Request
Um bean será criado para cada requisição http. Os Objetos existirão enquanto a requisição estiver em execução. No momento que a requisição for encerrada o bean é destruído.

## HTTP - Session
Uma bean será criada para a sessão de usuário.</br>
Precisamos acessar a mesma solicitação duas vezes para testar os escopos específicos da web. Costuma-se utilizar muito essa este escopo para acessar sessões de usuário, manter o status 
do usuário, carrinho de compras e etc...

## HTTP - Global
Ou Application Scope cria um bean para o ciclo de vida do contexto da aplicação. Objetos compartilhados por toda a aplicação.

## Autowired
Uma anotação(indicação) onde deverá ocorrer uma injeção automática de dependência.
- byName: É buscado um método set que corresponda ao nome do bean.
- byType: É considerado o tipo da classe para inclusão do bean.
- byConstrutor: Usamos o construtor para incluir a dependência.

