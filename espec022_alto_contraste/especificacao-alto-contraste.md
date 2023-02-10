---
title: "Alto Contraste"
Mantis: 
contrato_manutencao: INF 4504 
output:
  html_document:
    theme: united
    toc: yes
  word_document:
    toc: yes

---

# Visão geral da Demanda
<a href="#top">(inicio)</a>

Essa demanda visa incluir no Portal da Transparência o modo de  Alto Contraste para permiter ao usuário inverter as cores do primerio plano e plano de fundo, bem como aumentar ou reduzir a fonte do texto, o que ajuda a destacar melhor o texto.


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Alto Contraste é uma ferramenta que deixa o fundo da página totalmente escuro e as letras mais claras, podendo também ser relacionado à troca do tamanho das fontes. Este recurso, utilizado principalmente por pessoas que possuem médio ou alto déficit de visão, bem como usuários que apresentam algum grau de daltonismo, permite aumentar o contraste das cores do texto e das imagens na tela, facilitando sua identificação.

De acordo com o World Wide Web Consortium - W3C, um consórcio internacional no qual organizações filiadas trabalham juntas para desenvolver padrões para a web, as técnicas de acessibilidade na internet permite que cada pessoa possa “perceber, entender, navegar, interagir e contribuir para a web”.

Nesse contexto, a acessibilidade de sites e aplicativos envolvem todas as condições necessárias para melhorar o acesso à internet, de pessoas com deficiências visuais, auditivas, físicas, de fala, cognitivas, neurológicas, entre outras. Ainda segundo a cartilha de acessibilidade do W3C Brasil, acessibilidade na web significa que pessoas com deficiência devem ser incluídas no ambiente digital. Ela também beneficia outros indivíduos que, ainda que não apresentem algum distúrbio, podem ter sua experiência de navegação prejudicada, como idosos.

Assim, algumas combinações de cores podem ser fáceis de ler para algumas pessoas, difíceis ou quase impossíveis para outras. Isso geralmente se resume ao contraste de cores e a relação entre a luminância das cores do primeiro plano e do plano de fundo. 

Diante disso, para possibilitar a igualdade de oportunidades para que diferentes tipos de pessoas, independentemente de suas situações, possam ter autonomia para utilizar o Portal de Transparência do Estado de Minasd Gerais, é necessário considerar a implementação de algumas ferramentas de acessibilidade, como o alto contraste e o aumento ou redução da fonte da página.


# Especificação
<a href="#top">(inicio)</a>

## Página Inicial
<a href="#top">(inicio)</a>

Incluir em todas as páginas do Portal da Transparência, no canto superior esquerdo da página, a funcionalidade de Alto contraste, por meio do acionamento de botões.

### Localizações dos Botões

Página Atual

![image](https://user-images.githubusercontent.com/52920939/217844694-af7badea-cf8f-4375-81ae-d7b9895af279.png)

Nova Página

![image](https://user-images.githubusercontent.com/52920939/217846279-f7f2d9df-1d86-4436-b728-710f83abf682.png)



### Botão 1: Alto Contraste

Botão acima da página "Alto Contraste", que ao ser acionado aplica os recursos de aumento de contraste em todas as páginas do Portal.

![image](https://user-images.githubusercontent.com/52920939/217844860-7c56ff80-ddf4-4d49-985d-56da99e6ea28.png)

- Ao passar o mouse sobre o local, deve aparecer o tool tip com a informação "Aplicar Contraste"

- Quando acionado, o tool tip do botão deve ser alterado para "Retornar Contraste".

![image](https://user-images.githubusercontent.com/52920939/217845054-36b6c1af-72cb-4572-a47b-a545e57d4798.png)

- Observação: A funcionalidade de Alto Constraste ao ser acionada, será aplicada a todas as páginas do portal da transparência em que o usuário navegar, sem a necessidade de acionar novamente o botão na página seguinte.


### Botão 2 - Aumentar Fonte
<a href="#top">(inicio)</a>

Incluir em todas as páginas do Portal da Transparência a funcionalidade de Aumentar Fonte, por meio de um botão acima da página "A+", que ao ser acionado aumenta o tamanho da fonte da página em que o usuário está navegando.

![image](https://user-images.githubusercontent.com/52920939/217845748-df9b244b-60de-407b-b0da-73b6a991dec0.png)

- Ao passar o mouse sobre o local, deve aparecer o tool tip com a informação "Aumentar tamanho do texto"


### Botão 3 - Reduzir Fonte
<a href="#top">(inicio)</a>

Incluir em todas as páginas do Portal da Transparência a funcionalidade de Aumentar Fonte, por meio de um botão acima da página "A-", que ao ser acionado reduz o tamanho da fonte da página em que o usuário está navegando.

![image](https://user-images.githubusercontent.com/52920939/217845872-7a056fce-3cea-4e63-b2e5-7960ea1afbdd.png)

- Ao passar o mouse sobre o local, deve aparecer o tool tip com a informação "Reduzir tamanho do texto"


### Botão 4 - Tamanho Original da Fonte
<a href="#top">(inicio)</a>

Incluir em todas as páginas do Portal da Transparência a funcionalidade de Retornar ao Tamanho Original da Fonte, por meio de um botão acima da página "A=", que ao ser acionado retorna ao tamanho da fonte padrão da página em que o usuário está navegando.

![image](https://user-images.githubusercontent.com/52920939/217845968-c4e7e078-3811-471e-8884-fe0a6e6b44ce.png)


- Ao passar o mouse sobre o local, deve aparecer o tool tip com a informação "Retornar ao tamanho original do texto"



