## Настройка окружения

```
python -m venv .venv
```

windows:
```
.venv\Scripts\activate
```

*nix:
```
source .venv\Scripts\activate
```

```
cd mkdocs_pages
python -m install -r requirements.txt
python -m pip install -r requirements.txt
python -m mkdocs serve
```

## Деплой:

```
cd mkdocs_pages
mkdocs gh-deploy
```


## Материалы:

[Создание статических сайтов из Markdown без HTML (pandoc, mkdocs, hugo и jekyll)](https://habr.com/ru/articles/826474/)

[MarkedText — маркдаун здорового человека](https://habr.com/ru/articles/536448/)

[Пошаговая инструкция как использовать MkDocs для создания сайта с документацией продукта](https://habr.com/ru/companies/rostelecom/articles/570098/)
