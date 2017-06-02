% Desenvolvimento guiado por testes
% Eduardo de Santana Medeiros Alexandre
% 2017
---
institute: Faculdade Internacional da Paraíba
# Warsaw #theme: Ilmenau #theme: Darmstadt #theme: Antibes #theme: Darmstadt Ilmenau
theme: PaloAlto
lang: pt-BR
graphics: true
slide-level: 2
titlepage-note: Título menor aqui.
header-includes:
  - "\\usepackage{amsfonts}"
#  - "\\logo{logo.png}"
  - "\\logo{\\includegraphics[height=0.7cm]{logo.png}}"
---



# Desenvolvimento

## Papéis

### Revisão de alguns papéis envolvidos no desenvolvimento

- Cliente
- *Stakeholder*
- *Product Owner*
- Usuário
- Desenvolvedor
- QA (*Quality assurance*)
- Testador

## Estórias do Usuário

### Como estórias de usuários são escritas

#### Cartão da estória

\begin{center}
\includegraphics[width=0.9\textwidth]{user-story-value.jpg}
\end{center}

### Critérios de aceitação no verso do cartão


\begin{center}
\includegraphics[width=0.9\textwidth]{user-story.png}
\end{center}

### Estórias posteriormente irão para implementação

\begin{center}
\includegraphics[width=0.9\textwidth]{board.jpg}
\end{center}


## Testando as implementações

### Precisamos testar nossos códigos?

\begin{center}
\includegraphics[width=0.4\textwidth]{code.png}
\end{center}


- Funciona corretamente na primeira execução? \pause
- Que garantia temos que nossa implementação irá funcionar corretamente? \pause

    * **Funcionou quando executei no meu computador...**

### Teste Manual vs Teste automatizados


\begin{center}
\includegraphics[width=0.4\textwidth]{teste-manual.jpg}

\includegraphics[width=0.4\textwidth]{teste-automatico.png}
\end{center}

### Quais os benefícios de testes automatizados para o desenvolvedor?

- Testes de regressão

    * *Garantia* que o software está funcionando *conforme especificado* \pause
    * Minhas alterações estão impactando as demais funcionalidades? \pause

- Proporciona confiança para **refatorar** código \pause

- Fonte de aprendizado para novos desenvolvedores

## TDD (1996)


### O que é TDD?

- **TDD** (Test-Driven-Development): desenvolvimento guiado por testes. \pause

#### Os benefícios do TDD são aqueles dos testes automatizados?

- Sim \pause mas aqueles benefícios são apenas consequências da produção de testes.


### Como funciona TDD? {.allowframebreaks}

- Desenvolvedor escreve testes, desenvolve o **mínimo** para fazer os testes passarem e em seguida **refatora** o código para melhorar a implementação. (*Test-Driven Development by Example* - Kent Beck)
- Também conhecido como UTDD (*Unit Test-Driven Development*)

\begin{center}
\includegraphics[width=0.9\textwidth]{tdd.png}
\end{center}

### Demais benefícios do TDD

- Influencia no Design do código
- Produz códigos testáveis
- Agiliza a verificação das funcionalidades implementadas
- Desenvolvedores aceitam mudanças com mais facilidade
- *Produtividade* \pause

#### Dificuldade

- Requer conhecimentos e habilidades específicas para implementar os testes.

### Estou implementando corretamente a coisa certa?


\begin{center}
\includegraphics[width=0.9\textwidth]{tdd_atdd.png}
\end{center}



## ATDD (2003)

### Problemática

- O que eu estou implementando será aceito pelo cliente?
- Quando eu sei que terminei o desenvolvimento de uma estória?

### Acceptance Test-Driven Development (ATDD)


#### Proposta de solução do ATDD:

- Implementar testes automatizados contemplando os critérios de aceitação do cliente.
- Desenvolvimento termina quando todos os testes de aceitação estão passando.


## ATDP (2004)

### Problemática

- Eu entendi o que o cliente realmente deseja? \pause

#### Estratégia

- Os testes serão implementados juntos com o cliente, durante reuniões de planejamento ou antes delas.

### Acceptance Test-Driven Planning (ATDP)

\begin{center}
\includegraphics[width=0.6\textwidth]{atddfig6.jpg}
\end{center}

- Aplica ATDD integralmente \pause

#### Problema

Os clientes não compreendem os testes codificados

### Testes escritos juntamente com o cliente

\begin{center}
\includegraphics[width=0.9\textwidth]{ATDDdiagram.jpg}
\end{center}


##  BDD (2006)

### Princípios do Behavior Driven Development (BDD)

> “Behaviour-Driven Development is about implementing an application by **describing its behavior from the perspective of its stakeholders**.” – David Chelimsky, The RSpec Book.

### Características do BDD

<!-- > "Em apenas um repositório, você mantém os testes de aceite automatizados de uma forma simples de ler para o cliente, desenvolvedores, QAs e demais membros da equipe e ao mesmo tempo esses testes são automatizados antes do desenvolvimento, formando um conjunto de testes de aceite que guiam o desenvolvimento das estórias e em seguida são usados como testes de regressão."
-->

- Os testes produzidos podem ser lidos por todos: **clientes, desenvolvedores e QAs**.
- Os testes são automatizados durante o desenvolvimento.
- Testes serão utilizados como testes de regressão.



<!--
Exemplo de ATDD:

https://gist.github.com/camiloribeiro/1833149/
-->

### Princípios do BDD

1. O suficiente é suficiente
2. Entregar valor para os *stakeholders*
3. Tudo é comportamento

### Como BDD é diferente do TDD?

- Enquanto o TDD foca mais no design do código, o BDD foca no negócio.

## Complementos

### Dicas

- Utilize *Issue Tracks*
- Escreva um teste que represente o bug
- Faça o teste passar e refatore
- Busque cobertura de código (*code coverage*) 100%
- TDD desenvolve-se com a prática


### O que precisamos para escrever testes {.allowframebreaks}

#### Essencial

- Tipos de testes: **Unitários, Funcionais, de Integração, de Interface e de Regressão**
- MVC
- Sistema de controle de versão (git)
- Framework de teste (opções e invocação)

#### Recomendado

- Técnicas/Padrões de teste: *mock*, *factory*
- Servidor de integração contínua

### Ferramentas para java

- http://junit.org
- http://testng.org
- http://site.mockito.org ou http://www.jmock.org
- http://concordion.org
- https://cucumber.io/docs/reference/jvm
- https://en.wikipedia.org/wiki/Java_Code_Coverage_Tools

### Algumas referências {.allowframebreaks}

AMBLER, Scott. **Introduction to Test Driven Development (TDD)**. 2013. Disponível em: <http://agiledata.org/essays/tdd.html>.

RIBEIRO, Camilo. **Entendendo BDD com Cucumber – Parte I**. 2012. Disponível em: <http://www.bugbang.com.br/entendendo-bdd-com-cucumber-parte-i/>.

KOPS, Micha. **BDD Testing with Cucumber, Java and JUnit**. 2014. Disponível em: <http://www.hascode.com/2014/12/bdd-testing-with-cucumber-java-and-junit/>.

ROSE, Seb. **An Introduction to Behavior-Driven Development (BDD) with Cucumber for Java**. 2015. <https://www.youtube.com/watch?v=MCaXumfckmQ>.


# Prática

## BDD+TDD+JAVA

### Propostas para prática

\begin{center}
\includegraphics[width=0.5\textwidth]{user-story-value.jpg}
\end{center}


- Quem propõe uma estória?
- **Vamos começar sem TDD para perceber a diferença!**

### Funcionamento de uma Vending Machine

\begin{center}
\includegraphics[width=0.95\textwidth]{maquina.jpg}
\end{center}

### Obrigado!

#### Contato

E-mail: eduardo.ufpb@gmail.com

http://edusantana.github.io - slides e códigos serão disponibilizados aqui.


