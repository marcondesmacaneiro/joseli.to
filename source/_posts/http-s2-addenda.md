---
title: 'HTTP S2, addenda'
tags:
  - Código
  - ssl
date: 2016-02-05 16:37:17
---

#### A segunda parte de um texto que não sabia que teria uma segunda parte.

<figure>![](https://cdn-images-1.medium.com/max/1024/1*Yf5gwJMuq7DOze2y-MFANA.png)</figure>

Aconteceu muita coisa desde o dia 19, quando publiquei [**_“Seus sites seguros de graça sem custo nenhum e não pagando nada”_**](https://medium.com/@joselitojunior1/seus-sites-seguros-de-gra%C3%A7a-sem-custo-nenhum-e-n%C3%A3o-pagando-nada-49df4694bd85) nesta rede social Medium. Apesar de relevante pra situação atual da web, não esperava que acontecessem tantas coisas relacionadas, em tão poucos dias.

Com isso em mente, me sinto mais que na obrigação de informar o mais relevante que rolou. Vem, jovem:

<figure>![](https://cdn-images-1.medium.com/max/69/1*D7wNBluOwrIvS3A83BhldA.png)</figure>

#### [**O Chrome fará sites _HTTP-only_ passar vergonha**](http://motherboard.vice.com/read/google-will-soon-shame-all-websites-that-are-unencrypted-chrome-https)

Não se sabe com exatidão quando, mas eventualmente, o Google Chrome irá tratar sites sem HTTPS com um comportamento parecido de quando o site é inseguro ou possui um certificado falso: a ícone de cadeado na barra de navegação irá possuir um “X” vermelho. A diferença básica é que você conseguirá acessar o conteúdo normalmente, sem nenhum aviso que “sua conexão é insegura”.

A ideia do time do Chrome é justamente deixar claro que o simples fato de você não estar utilizando uma conexão HTTPS, por conseguinte não encriptada, já é inseguro o bastante.

Se você quiser testar no seu Chrome, vá em

<pre>chrome://flags</pre>

e procure por “mark non-secure as”, e selecione “mark non-secure origins as non-secure”. Reinicie o Chrome e veja o futuro.

<figure>![](https://cdn-images-1.medium.com/max/624/1*PB_wfnGtyoWW0Q0bmzC7Xw.png)</figure>

#### [**O Firefox também não vai deixar sites sem HTTPS impunes**](https://hacks.mozilla.org/2016/01/login-forms-over-https-please/)

A partir do Firefox Developer Edition 46 (que já é a versão atual, no momento da publicação), sites que **possuem formulário com campo de senha e não possuem HTTPS serão indicados como inseguros**. A estratégia é bem menos violenta que a do Chrome, mas também deixa claro quando está tendo cheiro vacilo no ar.

Uma coisa bem interessante é que não basta você estar enviando os dados via HTTPs (pra um servidor num domínio diferente, por exemplo), você também tem que estar **servindo** via HTTPS, e isso impede vários tipos de ataques locais.

<figure>![](https://cdn-images-1.medium.com/max/24/1*On7OB7g1_RYp9GbHyksV-g.png)</figure>

#### **Let’s Encrypt comemora com o peito em festa e coração a gargalhar ter emitido mais de 500 mil certificados**

Título de notícia do EGO, mas é bem verdade:

<figure>![](https://cdn-images-1.medium.com/max/24/1*HWtIibcQyvvwnJdhA0fi5A.png)</figure>

#### [**O maldito Facebook fechou o Parse**](http://blog.parse.com/announcements/moving-on/)

O Facebook provou mais uma vez que não é digno de confiança e fechou o [(m)BaaS](https://en.wikipedia.org/wiki/Mobile_backend_as_a_service) mais completo que existia. [Existe um excelente texto refletindo o porquê](https://medium.com/@s2o/they-never-wanted-to-host-your-app-the-real-reasons-why-parse-shut-down-6ec3d7d5c53c). Mas no nosso contexto, destaco isso pois sugeri o Parse como um bom local para você hospedar seu site, e ainda vinha com HTTPs.

Tenho umas novidades pra me redimir.

### Ainda mais opções para ter um HTTPS pra chamar de seu

Só seu e de mais ninguém.

#### [**Pancake.io**](https://pancake.io/)

A Pancake.io é uma plataforma extremamente amigável, com um deploy tão fácil que dá pra fazer pelo Dropbox (literalmente). Mas se você é uma pessoa de bem e usa controle de versão, você pode usar Git também.

Os domínios _*.pancakeapps.com_ tem HTTPS habilitados por padrão.

#### [**Google App Engine**](https://appengine.google.com)

Confesso que não mencionar o App Engine no post original foi realmente um ponto fora da curva. Mas é pra isso que adendos servem, correto?

Domínios _*.appspot.com_ já tem certificado HTTPS. Você também pode fazer upload de um certificado SSL próprio, se for usar seu próprio domínio no App Engine.

### Ferramentas bônus

Em barras de ouro, pois estas valem mais do que dinheiro.

#### [**Get HTTPS for Free**](https://gethttpsforfree.com/)

A cada dia que passa temos mais certezas que a internet veio pra ficar. Um cidadão automatizou o suficiente de todo o processo manual do Let’s Encrypt em um formulário simples.

#### [**badssl.com**](https://badssl.com/)

Esse site é uma mão na roda para você que quer ver como os navegadores se comportam em diferentes situações. Se seu próprio HTTPS der algum problema, você tem uma base para comparar e descobrir o que está acontecendo.

### **Stairway to heaven**

Parte do trabalho de desenvolvedores web é fazer a própria web evoluir. Não deixa de ser curioso como um assunto tão marginal gerou tanto conteúdo em tão pouco tempo.

Comentar sobre [a importância de HTTPS não é de hoje](http://mashable.com/2011/05/31/https-web-security/). Porém ainda a muito a ser discutido e debatido sobre o assunto, e pelo que os indícios mostram, ele irá se tornar cada vez mais relevante.

**Proponha uma discussão sobre HTTPS na sua comunidade**, ele se encaixa em vários contextos. Me dê um [ping no Twitter](http://twitter.com/joselitojunior1) se eu puder ajudar em algo. Há um longo caminho a ser percorrido.