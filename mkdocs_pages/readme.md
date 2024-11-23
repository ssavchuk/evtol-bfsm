## Настройка окружения

Скачать и установить [python версии 3.12.7](https://www.python.org/ftp/python/3.12.7/python-3.12.7-amd64.exe) (т.к. данная версия используется в action для деплоя на github.com)

> **Note**
> Не забыть установить галочку "Add Python to environment variables"

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

Установить зависимости и запустить локальный web сервер.
```
cd mkdocs_pages
python -m pip install -r requirements.txt
python -m mkdocs serve
```

## Деплой:

Не обязательно, т.е. на github.com через actions настроен автодеплой

```
cd mkdocs_pages
mkdocs gh-deploy
```

## Материалы:

[Создание статических сайтов из Markdown без HTML (pandoc, mkdocs, hugo и jekyll)](https://habr.com/ru/articles/826474/)

[MarkedText — маркдаун здорового человека](https://habr.com/ru/articles/536448/)

[Пошаговая инструкция как использовать MkDocs для создания сайта с документацией продукта](https://habr.com/ru/companies/rostelecom/articles/570098/)

[Docs as Code для художественной литературы. Делаем творческий сайт ребенка с помощью MkDocs](https://habr.com/ru/articles/720584/)

https://www.mkdocs.org/user-guide/configuration/