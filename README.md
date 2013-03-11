# Szablon Bloga dla generatora Jekyll

> „Computer class” can’t be about teaching to use today’s software;<br>
> it must be about teaching o make tomorrow’s software.
>
> *Douglas Rushkoff*


## TODO: Instalacja szablonu

1. Klikamy i pobieramy archiwum zip.
1. Rozpakowujemy do pustego katalogu:

Na przykład:
```sh
unzip ...
```

Cała procedura może wyglądać tak:
<pre>git clone git@github.com:⟨twój login na <b>githubie</b>⟩/jekyll-template.git my_blog
cd my_blog
</pre>

## Piszemy pierwszy post

Posty umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.md

Przykładowo:

    2013-02-29-jekyll-howto.md

Po napisaniu posta generujemy statyczną wersję bloga wykonując
z katalogu z blogiem, czyli z katalogu **my_blog/** polecenie:

If Repository pages, add to *_config.yml*:

```yaml
baseurl: /repository_name
```

User/Organization/Repository pages:

    jekyll --server PORT --auto # testowanie, localhost:PORT


## TODO: Wdrażamy bloga na Githubie

* [Creating Project Pages manually](https://help.github.com/articles/creating-project-pages-manually)
* [Sample Rakefile](https://github.com/gitready/gitready/blob/en/Rakefile)
* *_config.yml* – *baseurl*

Jeśli wszystko jest OK, to wdrażamy bloga na Github:

    rake deploy          # uaktualnić DESTINATION

Po wykonaniu polecenia blog jest dostępny tutaj:

<pre>http://⟨twój login na <b>githubie</b>⟩.github.com/
</pre>


## TODO: Korzystamy z rozszerzeń

* [Template Data](https://github.com/mojombo/jekyll/wiki/template-data)

Jak? Opisane jest to [README](http://github.com/rfelix/jekyll_ext)
*jekyll_ext*.


## Ściągawka z Gita

Pushing local branch named *dinky-theme* to remote (github repo):

```sh
git push origin dinky-theme
git checkout dinky-theme -- README.md
git diff master:README.md dinky-theme:README.md
```
