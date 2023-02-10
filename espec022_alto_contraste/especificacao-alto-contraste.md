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

Essa demanda visa incluir no Portal da Transparência os modos de  Alto Contraste e Alteração no tamanho da fonte de texto, que permitirão que os usuários possam inverter as cores do primerio plano e plano de fundo, bem como aumentar ou reduzir a fonte do texto.


# Motivação / contexto da demanda
<a href="#top">(inicio)</a>

O Alto Contraste é uma ferramenta que deixa o fundo da página totalmente escuro e as letras mais claras, podendo também ser relacionado à troca do tamanho das fontes. Este recurso, utilizado principalmente por pessoas que possuem médio ou alto déficit de visão, permite aumentar o contraste das cores do texto e das imagens na tela, facilitando sua identificação.

Diante disso, para possibilitar a igualdade de oportunidades para que diferentes tipos de pessoas, independentemente de suas situações, possam ter autonomia para utilizar o Portal de Transparência do Estado de Minas Gerais, é necessário considerar a implementação de tais ferramentas de acessibilidade.


# Especificação
<a href="#top">(inicio)</a>

## Página Inicial
<a href="#top">(inicio)</a>

Incluir uma linha na parte superior do cabeçalho, na qual estarão contidos os botões referentes às fontes (aumentar,diminuir e manter o tamanho padrão) e alto contraste (conforme exemplificado no arquivo anexo - Nova Página).

### Localizações dos Botões

Página Atual

![image](https://user-images.githubusercontent.com/52920939/217844694-af7badea-cf8f-4375-81ae-d7b9895af279.png)

Nova Página

![image](https://user-images.githubusercontent.com/52920939/217846279-f7f2d9df-1d86-4436-b728-710f83abf682.png)



### Botão 1: Alto Contraste

Botão caracterizado geralmente por imagem (meia-lua, dentre outros) que identifique a alternância em "Alto Contraste" e que ao ser acionado aplica os recursos de aumento de contraste.

![image](https://user-images.githubusercontent.com/52920939/217844860-7c56ff80-ddf4-4d49-985d-56da99e6ea28.png)

- Ao passar o mouse sobre o local, deve aparecer o tool tip com a informação "Aplicar Contraste"

- Quando acionado, o tool tip do botão deve ser alterado para "Retornar Contraste".

![image](https://user-images.githubusercontent.com/52920939/217845054-36b6c1af-72cb-4572-a47b-a545e57d4798.png)

- Observação: A funcionalidade de "Alto Constraste" ao ser acionada, por estar presente no cabeçalho fixado, permanecerá ativa em qualquer navegação no Portal da Transparência, até que o usuário clique no botão de "Alto Contraste" novamente e desative-a.


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



