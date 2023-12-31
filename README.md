## api для создания и просмотра одноразовых секретов


### Технологии:
- python 3.7
- fastapi 0.103.1
- Mongo DB
- pymongo
- Docker
- Docker-compose
- pydantic
- pytest
- pycrypto

### Инструкция для развертывания проекта с использованием Docker:

Клонирование проекта:
```
git clone https://github.com/qwerty124808/secrets_manager
```
Запуск:

Запустить команду, указанную ниже из корня проекта 
```
sudo docker-compose up -d
```

Пример использования:

1. Заходим в postman
3. Создаем секрет
4. Отправляем POST запрос на эндпоинт - чтобы получить ссылку на наш секрет:
```
http://127.0.0.1:8000/generate
```

Тело запроса должно быть в формате Json и выглядеть примерно так:
```
{
    "secret": "Ваш секрет",
    "password": "Ваш пароль"
}
```
Далее переходим по ссылке которую мы получили 

Отправляем POST запрос для получения содержания секрета на эндпоинт:
```
http://localhost/secret/<id-секрета>
```
Body в запросе должно быть в формате Json и выглядеть вот так:
```
{
    "password": "Ваш пароль"
}
```
Посмотреть все реализованные эндпоинты можно по адресу:
```
http://127.0.0.1:8000/docs
```

Автор проекта Дмитрий Алтарев