# Szablon dla bloga

TODO

## Instalacja szablonu

1. Forkujemy repo klikając w ikonkę **fork**.
1. Klonujemy sforkowane repo na swój komputer.

Cała procedura może wyglądać tak:
<pre>git clone git@github.com:⟨twój login na <b>githubie</b>⟩/jekyll-template.git my_blog
cd my_blog
</pre>


## Piszemy pierwszy artykuł?

Wpisy do bloga umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.md

na przykład:

    2013-02-29-jekyll-howto.md

Po napisaniu posta generujemy statyczną wersję bloga wykonując
z katalogu z blogiem, czyli z katalogu **blog/** polecenie:

    jekyll --server PORT # testowanie, localhost:PORT


## Wdrażamy bloga na Githubie

Jeśli wszystko jest OK, to wdrażamy bloga na Github:

    rake deploy          # uaktualnić DESTINATION

Po wykonaniu polecenia blog jest dostępny tutaj:

<pre>http://⟨twój login na <b>githubie</b>⟩.github.com/
</pre>


## Korzystamy z rozszerzeń

Jak? Opisane jest to [README](http://github.com/rfelix/jekyll_ext)
*jekyll_ext*.
