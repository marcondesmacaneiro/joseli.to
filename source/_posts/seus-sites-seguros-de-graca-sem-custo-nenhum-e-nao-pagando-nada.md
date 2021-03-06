---
title: Seus sites seguros de graça sem custo nenhum e não pagando nada
tags:
  - Código
  - ssl
date: 2016-01-19 20:13:30
---

#### ou A Grande Aventura de Como Obter Certificados SSL

A Internet está ai e — ao que tudo indica — veio pra ficar. Para vermos gifs de gatos em nossos dispositivos, mensagens são trocadas por uma pilha enorme de protocolos, que são basicamente os mesmos desde 1969.

<figure>![](https://cdn-images-1.medium.com/max/735/1*VvfPysmjfnoHZQ8OT8HB4A.png)</figure>

O _HTTPS_ é a versão mais atual do protocolo _HTTP_, com uma camada extra de segurança provida pelo protocolo _SSL/TLS_. Ou seja, é aquele cadeado verde que fica na barra de navegação.

Estar em um site com _SSL_ ativo é uma garantia de que os dados enviados estão sendo **criptografados** entre o cliente e website, evitando, por exemplo, que um terceiro obtenha aquelas informações fazendo um ataque “no meio do caminho” entre o usuário e o servidor.

Conseguir um _HTTPS_ há algum tempo atrás não era das tarefas mais fáceis, além de que era virtualmente impossível você conseguir sem pagar uma **boa quantia** para tal.

Para ter um cadeado verde pra chamar de seu, você precisa de um **Certificado SSL**. Tal qual domínios, que você pode comprar de _Registrars_, você também compra de companhias que tem autorização de emitir e vender tais certificados. Os certificados possuem uma chave única, atrelada a você, os dados do seu domínio, e a sua emissora.

O uso de _HTTPS_ é extremamente importante para **Progressive Apps** pois algumas das funcionalidades mais interessantes, como os **ServiceWorkers** e WebWorkers, requerem obrigatoriamente o uso de conexões seguras para funcionar. Descobriremos mais sobre essas funcionalidades futuramente.

Vamos aprender como ter nossos sites seguros usando serviços gratuitos. É bem provável que você já use algum deles, mas talvez não conheça todo o potencial.

### 0800:

#### [**GitHub Pages**](http://github.com)

**U**sado por 9 a cada 10 dentistas, o GitHub pode não ser o paraíso, mas é o herói que nós merecíamos. Páginas com o domínio **_*.github.io_** tem certificado SSL habilitado. Se você hospeda algo lá, experimente trocar de **_http://_** para **_https://_**, vai funcionar bonitinho.

#### [Surge.sh](http://surge.sh)

O Surge é algo tão maravilhoso que deve ter sido feito pelo Zack Snyder ou pelo Elon Musk. Não existe nada melhor para fazer aquele deploy instantâneo naquele projetinho estático que você acabou de fazer. Todos os domínios **_*.surge.sh_** também tem SSL ativo.

_O Surge é tão incrível que farei um post sobre ele em breve. Me cobrem._

#### [Firebase](http://firebase.com)

Banco de dados nunca mais foram os mesmos desde que o Firebase apareceu com essa mania maravilhosa de deixar tudo em tempo real. Os domínios **_*.firebaseapp.com_** tem HTTPS por padrão, se você quiser dar deploy no seu app por lá.

#### [Parse](http://parse.com)

O Parse continua a ser meu predileto na categoria everything-you-need-for-make-apps-in-a-box. Domínios **_*.parseapp.com_** também possuem SSL.

### Domínio próprio

Se você é dos meus e curte ter uma ~identidade própria, ou quer dar aquele tom opressor no rolê, você deve ter um domínio próprio, tanto no pessoal quanto no profissional.

Como já mencionado, a chave do SSL está ligada diretamente ao _domínio_, então os certificados acima não vão funcionar no seu domínio.

Porém não há razão para o choro, veja a solução a seguir:

> Se você não tem um domínio próprio e quer pagar bem barato em um, sugiro o [**Namecheap**](https://www.namecheap.com/?aff=94043). No momento de publicação desse post, domínios **.xyz** e domínios **.club** estavam a $1 e $0.88 (88 **centavos** de dólar) respectivamente.
> Muito barato maluco.

#### [CloudFlare](https://www.cloudflare.com/)

A CloudFlare é uma das maiores e mais renomadas _CDNs_ que podemos citar. Além disso, ela também oferece um serviço de DNS que adiciona uma proteção SSL ao seu domínio, gratuitamente.

Entretanto, existe um ponto importante a ressaltar: por ser uma _CDN_ o CloudFlare entra “no meio” da conexão entre o usuário e o host do seu domínio. O _SSL_ que a CloudFlare oferece criptografa apenas a primeira parte dessa conexão, entre o usuário e os servidores da CloudFlare. Apesar de ser bem melhor do que não ter _HTTPS_ nenhum, ele não oferece uma segurança 100% criptografada. Tenha isso em mente.

Com o DNS configurado no CloudFlare, você pode usar seu próprio Registrar e Hosting, tendo controle total sobre os servidores.

#### [StartSSL](https://www.startssl.com/)

O StartSSL é uma das companhias autorizadas a emitir certificados digitais como o _SSL/TLS_. No tier mais simples, ela oferece por um ano uma versão básica do certificado, totalmente gratuito. O certificado da SmartSLL oferece criptografia ponto a ponto completa, o que não é o caso do CloudFlare.

Após um ano, se quiser continuar com o certificado, terá que usar os meios tradicionais e pagar por ele.

#### [Let’s Encrypt](https://letsencrypt.org/)

Os certificados sempre foram algo caro pra se obter pois a licença de emissão é muito cara para as empresas. The Internet Serious Business. Como HTTPS é uma demanda crescente — e mais do que tudo necessária — empresas de internet se juntaram para prover um serviço de emissão pública de certificados.

Empresas como a Mozilla, Google, Facebook, Cisco se juntaram com a Linux Foundation e criaram o Let’s Encrypt para ser esse emissor.

Como praticamente tudo ligado a Linux, o processo não é nem tranquilo nem favorável: espere muito trabalho manual e configurações trabalhosas de fazer no seu servidor. Também tal qual o Linux, é 100% gratuito e o que lhe dá mais controle sobre o certificado.

Os certificados gerados duram de 30–90 dias e tem que ser renovados “manualmente” para continuarem funcionando. Sempre de graça. Se você não lembra a última vez que fez um **_cron-job_**, tá ai uma oportunidade.

### Use cinto de segurança

Ser web developer não é das tarefas mais fáceis hoje em dia, já que felizmente toda a internet está se derretendo com os 38 frameworks que são lançados por dia. Por outro lado, viver no futuro nos permite criar coisas incríveis. Não custa nada (literalmente) mantê-las seguras também.

No entanto, [lhe vendo um conselho por um tweet desse post](https://twitter.com/home?status=https%3A//medium.com/%40joselitojunior1/seus-sites-seguros-de-gra%25C3%25A7a-sem-custo-nenhum-e-n%25C3%25A3o-pagando-nada-49df4694bd85%20%40joselitojunior1): tudo dito acima só deve ser usado em testes ou em produtos com uma base de usuários pequena. Se você está planejando escalar, tire o escorpião do bolso e compre um certificado. Segurança é tão importante quanto ter a melhor estrutura de servidores do mundo, principalmente para o seu usuário.

**Até os próximos posts!**

![](https://medium.com/_/stat?event=post.clientViewed&amp;referrerSource=full_rss&amp;postId=49df4694bd85)