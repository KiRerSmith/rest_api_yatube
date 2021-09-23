### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/KiRerSmith/api_final_yatube
```

```
cd yatube_api
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```
Для *nix
```
source venv/bin/activate
```
Для Windows
```
source venv/scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

Пример запроса к API:
```
GET http://127.0.0.1:8000/api/v1/posts/
```
Ответ:
```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2019-08-24T14:15:22Z",
      "image": "string",
      "group": 0
    }
  ]
}
```
