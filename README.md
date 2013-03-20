# Szablon Bloga dla generatora Jekyll

> „Computer class” can’t be about teaching to use today’s software;<br>
> it must be about teaching kids to make tomorrow’s software.
>
> *Douglas Rushkoff*

Za pomocą programu [jekyll](https://github.com/mojombo/jekyll) z plików
z gałęzi *dinky-theme* można wygenerować bloga.

W katalogu *_posts* jest przykładowy wpis *2013-02-28-jekyll-howto.md*,
a przykładowa konfiguracja – *_config.yml*.


## User Pages na serwerze Github

Aby utworzyć swojego bloga na serwerze Github,
wykonujemy kolejno:

- rejestrujemy się na serverze *github.com*
  (wybieramy *Free Plan*) i logujemy się na swoim koncie
- tworzymy nowe repozytorium o nazwie *TWÓJ_LOGIN.github.com*
  i klonujemy puste repozytorium na swój komputer
  do katalogu o takiej samej nazwie jak nazwa repozytorium
- wchodzimy na stronę [wb://blog](http://wbzyl.github.com/)
  skąd pobieramy archiwum ZIP lub TAR.
- rozpakowujemy archiwum do katalogu ze sklonowanym repozytorium

Na przykład, dla archiwum TAR, zapisujemy plik z archiwum
w katalogu */tmp* i rozpakowujemy je do do katalogu *TWÓJ_LOGIN.github.com*:

```sh
tar --strip-components=1 -C TWÓJ_LOGIN.github.com/ -zxvf /tmp/wbzyl-jekyll-template-ce4680a.tar.gz
cd TWÓJ_LOGIN.github.com
```

W pliku *Rakefile* jest zapisane zadanie zadanie do
wdrożenia bloga na serwerze Github:

desc "Deploy blog to GitHub User Pages"
task :deploy_to_user_pages do
  sh "git push github master"
end
```

Po kilku minutach wdrożony blog będzie dostępny tutaj:

```sh
http://TWÓJ_LOGIN.github.com/
```

## Project Pages na serwerze Github

…czyli blog przypisany do konkretnego repozytorium.

Aby dodać bloga do istniejącego repozytorium o nazwie, na przykład,
*xxl* wykonujemy kolejno:

```sh
git clone https://github.com/TWÓJ_LOGIN/xxl.git
cd xxl
git checkout --orphan gh-pages
git rm -rf .
tar --strip-components=1 -zxvf /tmp/wbzyl-jekyll-template-ce4680a.tar.gz
git add .
git commit -m "add dinky-template themed pages"
git push origin gh-pages
```
Po chwili blog powinien być dostepny z tego adresu:

    http://TWÓJ_LOGIN.github.com/xxl/

Dodajemy zadanie ułatwiające wdrażania bloga:

```ruby
desc "Deploy to gh-pages TWÓJ_LOGIN/REPO"
task :deploy_to_repo do
  sh "git push origin gh-pages"
end
```


# Piszemy pierwszy post

Posty umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.md

Przykładowo:

    2013-02-29-jekyll-howto.md

Po napisaniu posta generujemy statyczną wersję bloga wykonując
z katalogu z blogiem polecenie:

Testujemy i sprawdzamy post lokalnie:

```sh
jekyll --auto --server --port 4000
```

i blog będzie dostępny stąd:

    http://localhost:4000


## Różne rzeczy…

* wdrażanie bloga na Githubie, [Creating Project Pages manually](https://help.github.com/articles/creating-project-pages-manually)
* korzystanie z rozszerzeń
  - [Template Data](https://github.com/mojombo/jekyll/wiki/template-data);
  - howto? [README](http://github.com/rfelix/jekyll_ext) gemu *jekyll_ext*


## 2013.03.21 – już nieaktualne

Dla *repository pages*, dopisujemy w *_config.yml*:

```yaml
baseurl: /nazwa_repozytorium
```

Testujemy strony *user/organization/repository*:

```sh
jekyll --server PORT --auto # testowanie, localhost:PORT
```

Jeśli wszystko jest OK, to wdrażamy bloga na Githubie:

```sh
rake deploy
```
