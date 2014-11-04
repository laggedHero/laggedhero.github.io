---
layout: post
title:  "Blogging tools: O que estou usando"
date:   2014-10-30 14:32:00
categories: jekyll
---

Eu desisti de usar o [Octopress][octopress].

Eu tentei usar o mesmo para o meu blog... mas não deu muito certo. Não pelo projeto em si, que é muito bom (e bastante utilizado), mas acho que não me fechei com alguma coisa do workflow. (E você deveria experimentar o Octopress, sério)

Pensei em montar um blog estático utilizando o [AngularJS][angularjs] e arquivos JSON. Me parece uma coisa bem legal, e uma boa ideia, mas vai demorar para fazer algo assim. Estou com um pouco de pressa, aí preciso de algo pronto. (Mas talvez, só talvez, eu tente fazer algo assim no futuro)

Foi quando eu decidi dar uma olhada em [Jekyll][jekyll].

Bah, dei muita sorte.

Eu vou hospedar meu blog no [GitHub Pages][github-pages] (e por isso eu preciso de algo estático) e, como visto [aqui][gh-pages-jekyll], o Jekyll é suportado "nativamente".

O procedimento de configuração inicial descrito é bem simples (conforme visto [aqui][gh-pages-jekyll-install]).

 - Instalar o [Ruby][ruby] (caso você não o tenha)
 - Instalar o [Bundler][bundler] (caso você não o tenha, também)
 - Instalar o Jekyll, via o gem github-pages (na página do GitHub Pages citada acima tem um exemplo)

Pronto.

Ou quase.

A instalação é bem básica, não tendo nenhuma estrutura criada. Nos docs do GitHub Pages fala das configurações e etc, mas é pouca coisa. Se quisermos mesmo nos aprofundar em Jekyll, nada melhor do que a [documentação oficial][jekyll-official-docs].

Mas eu acho que posso adiantar algumas coisas. :)

Criando a estrutura básica:

IMPORTANTE: os comandos a seguir devem ser rodados na pasta onde o gem do gh-pages foi instalado! (Assim mantemos a paridade com o que está nos docs)

De acordo com a documentação no gh-pages, os comandos devem, preferencialmente, serem rodados pelo bundle. O que resulta em algo assim.

`bundle exec jekyll serve` -> comando para rodar o Jekyll e poder ter o preview do resultado no browser

Pois bem, pela documentação do Jekyll, existe como criar uma estrutura inicial para publicação de conteúdo, usando o `jekyll new`. No nosso caso, o que queremos é.

`bundle exec jekyll new tmp` -> comando para criar um novo projeto Jekyll na pasta tmp

Após rodar esse comando, podemos copiar todo o conteúdo da pasta tmp para a pasta do nosso futuro projeto (ou seja, para a pasta onde o comando foi rodado). Com isso, temos uma estrutura inicial pronta. Depois, podemos apagar a pasta tmp, que deve estar vazia.

Mas Tiago, pq não rodar `bundle exec jekyll new .` e já criar toda a estrutura na pasta certa? Pq quando fui fazer isso, deu um erro sobre a pasta não estar vazia. Talvez exista um comando para forçar a geração de qualquer forma, mas não procurei saber, admito. :/

Com isso, já temos um projeto pré-pronto (cujo o tema é o que estou usando atualmente - 30/10/2014).

Sobre o .gitignore: estou usando o seguinte.

```
.DS_Store
_site/
.sass-cache/
```

Assim o conteúdo gerado (site), nem o cache do sass serão versionados. Nem esses arquivos bizarros do Mac OS (.DS_Store).

Daí pra diante é com vocês. Eu ainda tenho muito o que aprender dessas ferramentas. ;)


[octopress]: http://octopress.org/
[angularjs]: https://angularjs.org/
[jekyll]: http://jekyllrb.com/
[github-pages]: https://pages.github.com/
[gh-pages-jekyll]: https://help.github.com/articles/using-jekyll-with-pages/
[gh-pages-jekyll-install]: https://help.github.com/articles/using-jekyll-with-pages/#installing-jekyll
[ruby]: https://www.ruby-lang.org/
[bundler]: http://bundler.io/
[jekyll-official-docs]: http://jekyllrb.com/docs/home/
