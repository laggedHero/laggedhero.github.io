---
layout: post
title:  "Hack In PoA"
date:   2015-04-16 07:00:00
categories: hackathon
---

No final de semana dos dias 11/04 e 12/04 aconteceu o [Hack In PoA], da [globo.com], o qual eu tive o prazer de participar. Este post é basicamente um breve relato da minha experiência no evento.

O Hack In PoA foi realizado em um teatro da FIERGS, para o bem e para o mal. O lugar é excelente, e a estrutura estava show de bola. Só era meio longe de tudo...

### Sábado - 11/04 - 08:00 - Credenciamento

Bem, todo o evento tem o seu credenciamento, aqui não foi diferente. Todo caso, o credenciamento foi bem tranquilo e sem problemas. Foi entregue um kit contendo alguns brindes aos participantes:

 - Um caderninho para anotações
 - Uma caneta (ou, acredito, ia ser difícil usar o caderninho)
 - Uma camiseta (bem legal, por sinal)
 - Um Arduino Uno

Sim, podemos dizer que a coisa começou muito bem, com um brinde prá lá de interessante. Eu ainda não mexi no meu Arduino, e nem sei (ainda) como fazê-lo... mas vou ter que brincar um pouco. É o tipo de presente que o público de um hackathon pode realmente curtir. Veremos se os outros participantes terão ideias legais com o seu Arduino (e posso antecipar que houve um projeto no Hack In PoA utilizando o mesmo).

Após credenciamento foi pegar uma mesa. Escolhemos uma bem no meio (um pouco demais até para o meu gosto), com excelente vista para o palco. Ao nosso lado se sentou o time do [Ruim de Roda], formado por alguns colegas.

Por falar em times...

### Sábado - 11/04 - 09:00 - Abertura

A abertura contou com o pessoal da globo.com se apresentando (não todos, havia um monte deles lá), falando sobre o evento (incluindo as regras) e dando o início oficial. Neste momento, até às 13:00, o pessoal poderia escolher temas e montar os times.

Eu já tinha um time, mas teve um pessoal que procurou ali, na hora, um projeto para se juntar. No meio do vai e vem, o time recebeu um reforço e, então, estavamos prontos para começar.

Meu time foi o seguinte:

 - [Cléber Henriques]
 - [Henrique Güttler Morbin]
 - [Jean Carlo Emer]
 - Eu XD

Tinhamos um pool bem legal de talentos, mas nenhum designer. No final, isso não fez tanta falta, é verdade. O Jean fez bem as vezes de designer. :)

### Sábado - 11/04 - ~10:00 - WIP

Daqui para adiante foi só trabalho.

Começamos dicutindo melhor o conceito do app: o problema que atacava, como lidava com esse problema e etc. Nessa discussão inicial o app mudou. A mudança, inicialmente sútil, desencadeou mudanças mais profundas que se refletiram por todo o app. O resultado foi o Embarque.io como o conhecemos.

Nesse meio tempo tivemos o nosso almoço...

{% include widgets/image_figure.html url="https://scontent-mia.xx.fbcdn.net/hphotos-xta1/v/t1.0-9/11039146_887313431291072_3158592710260184645_n.jpg?oh=662cfe44818e610d9d37cc6111106907&oe=55DD5771" description="Grande almoço. Créditos: Guilherme Dias e Cristiano Sant'Anna" %}

### Estrutura e afins

Acho melhor falar disso em um 'capítulo' próprio.

A globo.com está de parabéns, até mais do que isso, pela estrutura e afins. Havia dedicação, empenho e qualidade em cada detalhe do evento.

Os cuidados com detalhes começavam no credenciamento. O crachá era feito de um plástico resistente, e não aqueles papeis duros que se amassam no primeiro descuido.

O time presente para acompanhar o evento (desenvolvedores, designers e etc) da globo.com demonstravam estar realmente contentes com o que estavam fazendo. Sempre bem-humorados, atenciosos e educados. Era visível o interesse e satisfação dos mesmos.

A estrutura estava 100%. Não faltaram tomadas, água, comida, Redbull ou milk-shake (OK, eu senti falta de umas pizzas). A rede, via Wi-Fi, funcionou que foi uma maravilha. E olha, Wi-Fi costuma dar trabalho.

Ou seja: a estrutura provida foi excelente. Fico no aguardo de um próximo, pois sei que posso ficar tranquilo quanto a isso.

### PRE-PA-RA

Bem, como todo hackathon, o grande evento foi o trabalho. Aqui o time distribuiu, e re-distribuiu, as tarefas e papéis de acordo com o necessário.

Isso é um ponto importante a se falar: nós rapidamente distribuimos as tarefas entre nós e começamos a trabalhar. Ao meu ver, esse foi um ponto muito importante para que fosse possível entregar os apps ao final do hackathon. Pudemos trabalhar em paralelo em diversas questões, sem causar bloqueios no processo.

Outro ponto importante: o uso de bibliotecas. Além de não re-inventar a roda, economizamos um bom tempo em tarefas que não eram o ponto central do app. E, indo além, não só bibliotecas, mas serviços: para que escrever um backend para o app, se poderíamos usar algo pronto? (Neste caso, o [parse.com])

Como curiosidade, olhem as dependencias declaradas no app Android.

```
dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    compile 'com.android.support:appcompat-v7:22.0.0'
    compile 'com.android.support:recyclerview-v7:22.0.0'
    compile 'com.android.support:cardview-v7:22.0.0'
    compile 'com.parse.bolts:bolts-android:1.+'
    compile 'com.google.android.gms:play-services-location:7.0.0'
    compile 'com.google.android.gms:play-services-analytics:7.0.0'
    compile 'com.afollestad:material-dialogs:0.7.1.3'
    compile 'com.squareup.okhttp:okhttp:2.3.0'
    compile 'com.squareup.picasso:picasso:2.5.2'
    compile 'com.squareup.retrofit:retrofit:1.9.0'
    compile 'com.jakewharton:butterknife:6.1.0'
    compile 'com.squareup:otto:1.3.6'
    compile 'com.getbase:floatingactionbutton:1.9.0'
    compile 'org.ocpsoft.prettytime:prettytime:3.2.7.Final'
}

```

Nem todas essas dependências foram usadas (o FAB foi removido e não foi preciso acessar uma API externa).

Entretanto, mesmo com dependências mil, o código precisou ser escrito. E aí, amigos... a noite foi longa. Muito longa.

### WIP WIP WIP .... sleep?

Dizem que uma imagem vale mais que mil palavras. Que tal essa?

{% include widgets/image_figure.html url="https://fbcdn-sphotos-f-a.akamaihd.net/hphotos-ak-xfp1/v/t1.0-9/10985373_887313944624354_9077641584791703829_n.jpg?oh=98f6d3c1c2a0d532786e55dbb35dfa91&oe=559DA781&__gda__=1436656392_e58eaeada0247135d6735e779654b4e4" description="Eu, o psicopata. Créditos: Guilherme Dias e Cristiano Sant'Anna" %}

Apesar da minha óbvia vocação para ser um psicopata, essa foto mostra um pouco do trabalho, que nunca deixou de ser divertido.

Essa é a parte, digamos, única de um hackathon: você tem pouco tempo para por as suas ideias em prática. Esse deadline curto (no nosso caso: 12/04 - 11:30) serve tanto como uma restrição, como inspiração. É impressionante o que um prazo curto faz com a nossa cabeça.

O foco acaba sendo totalmente em ter algo funcionando, e as perfumarias acabam ficando de lado (para serem feitas em um segundo momento, se possível). Esse é um mindset que perdemos no nosso dia-a-dia, e que faz falta. Quanta grana se joga fora fazendo ajustes e mais ajustes de algo que nem sabemos se será aceito?

Contanto com as definições de telas feitas pelo Henrique e pelo Jean, mais a mão no código Android pelo Jean, tudo o que fiz foi focar em ter feats funcionando. Algumas arestas ficaram um tanto vivas, mas podíamos ir vendo como a interação estava ficando, e ir ajustando a mesma ao longo do tempo (sem grandes investimentos de tempo, que tínhamos pouco).

Essa estratégia deu bem certo, também. Era fácil ver uma ideia, mudar um pouco, ajustar e etc. Após termos feito o 'grosso' do app, podemos revisitá-lo, fazendo os ajustes finos e outros.

Claro, nem tudo foram rosas. Imagem você, cansado, lá pelas 4:00 da manhã, tendo que fazer calculos para o desenho de uma view customizada. Admito que a coisa não estava dando muito certo. Ao chamar meu companheiro de códigos Android, resolvemos descartar o elemento como ele era, simplificando-o. Isso salvou a minha vida, tenho certeza.

Acabamos por dormir por turnos, ou quase isso, sem nenhum tipo de combinação formal. Por volta das 7:00 eu me deitei em um sofá e apaguei. Quando acordei, vi o Cléber dormindo ainda mais torto do que eu no sofá ao lado.

Eu sabia que estava tudo bem. XD

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="4" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://instagram.com/p/1X91duymJs/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_top">O #hackinpoa ta bem servido de devs!</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A photo posted by Moises Pio (@moisespio) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2015-04-12T12:13:46+00:00">Apr 12, 2015 at 5:13am PDT</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

Sim, pois dormir é preciso.

Pelas 09:00 do dia 12/04, com o fim do prazo chegando, resolvemos que era hora de acertar as últimas feats, adicionar um Google Analytics, e tocar a apresentação.

Sim, fechamos o app Android perto da finaleira, o app iOS em cima do laço... mas fechamos!!

E olhem a nossa apresentação (um oferecimento de Jean Carlo Emer):

<script async class="speakerdeck-embed" data-id="a31f710fa91b4bb498e985924caef0fb" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>


### Domingo - 12/04 - 12:00+ - Apresentações e premiações

A reta final do evento eram as apresentações. A premiação era só uma consequencia de tudo até então.

Com cara de pitch, para grupo tinha 5 minutos para apresentar o seu trabalho, mesmo aqueles que porventura não conseguiram terminar. Esses eram convidados a presentar o seu trabalho e um relato de como foi a experiência.

Foram 28 projetos. 10 web, 9 mobile e 9 de cidadania. Alguns projetos, ao meu ver, muito interessantes (e eu realmente gostaria de voltar a ouvir falar deles).

Dessa vez, não ganhamos. Pelo menos não os prêmios oficiais. Quem ganhou o que pode ser visto [aqui].

Mas eu acho que ganhamos muito mais. Eu me diverti pacas. Ri muito, me estressei o bom estresse e saí contente com o resultado (nem tanto, OK). Foi uma experiência excelente de um final de semana. E o resultado você pode ver no link abaixo.

<a href="https://play.google.com/store/apps/details?id=io.embarque.embarque" style="width: 130px; display: block; margin-left: auto; margin-right: auto;">
  <img alt="Get it on Google Play" src="https://developer.android.com/images/brand/pt-br_generic_rgb_wo_45.png" />
</a>

AH, muito importante: retweetem, favoritem e etc o tweet oficial deste post, que está logo abaixo. Ainda posso ganhar um brinde da globo.com. :D

PS.: As fotos eu tirei do [album oficial do Hack In PoA] do [TechTudo], tirando o Instagram, claro.

------
[Hack In PoA]:http://hackinpoa.globo.com/
[globo.com]: http://www.globo.com/
[Ruim de Roda]:http://ruimderoda.me/
[Cléber Henriques]:https://www.facebook.com/cleber.henriques
[Henrique Güttler Morbin]:https://www.facebook.com/hgmorbin
[Jean Carlo Emer]:https://www.facebook.com/jeancarloemer
[parse.com]:https://parse.com/
[album oficial do Hack In PoA]:https://www.facebook.com/media/set/?set=a.887313194624429.1073741920.159328784089544&type=3
[TechTudo]:http://www.techtudo.com.br/
[aqui]:http://www.techtudo.com.br/noticias/noticia/2015/04/hack-poa-vencedores-sao-anunciados-e-levam-iphone-6-e-moto-x.html
