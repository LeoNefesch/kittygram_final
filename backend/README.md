### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram_backend.git
```

```
cd kittygram_backend
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

При активированном виртуальном окружении установить пакет gunicorn:

```
pip install gunicorn==20.1.0
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
gunicorn --bind 0.0.0.0:9000 kittygram_backend.wsgi
```
