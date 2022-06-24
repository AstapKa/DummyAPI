# DummyAPI
описание тестирование проекта DummyApi
## Оглавление
1. Описание проекта
    1. [POST](#POST)
        1. GET /post (Get List)
        2. POST /post/create (Create Post)
2. Майнд-карта
3. Тест-кейсы
4. Баг-репорты
5. Коллекции POSTMAN

## Описание проекта
https://dummyapi.io/ Данный сайт представляет собой сервис для тестирования API 
Для выполнения запросов необходим App-id, который генерируется автоматически после регистрации на сайте.
В качестве тестирования был взят объект **POST**
### POST
___

#### GET /post (Get List)
Возвращает список публикаций, отсортированных по дате создания
- доступны query params для вывода определенной страницы

**Response body**: 
```js
{
 data: Array(Model)
 total: number(total items in DB)
 page: number(current page)
 limit: number(number of items on page)
}
```
**Post Preview**:
```js
{
 id: string(autogenerated)
 text: string(length: 6-50, preview only)
 image: string(url)
 likes: number(init value: 0)
 tags: array(string)
 publishDate: string(autogenerated)
 owner: object(User Preview)
}
```
___
#### POST /post/create (Create Post)
Создает новую публикацию от конкретного пользователя и возвращает информацию о публикации

**Request body**: 
Ключи owner и text должны быть обязательно заполнены
```js
{
 text: string(length: 6-50, preview only)
 image: string(url)
 likes: number(init value: 0)
 tags: array(string)
 owner: string(User id)
}
```
**Response body**: 
```js
{
 id: string(autogenerated)
 text: string(length: 6-1000)
 image: string(url)
 likes: number(init value: 0)
 link: string(url, length: 6-200)
 tags: array(string)
 publishDate: string(autogenerated)
 owner: object(User Preview)
}
```

## Майнд-карта
Данные майнд-карты представляет собой набор тестов для тестирования объекта **POST**. Подробная проверка расписана для **GET List** и **Create POST**
![Майнд-карта](https://drive.google.com/drive/folders/195EKk7y_6-1I25pvd-bN47urN4_KA5u8 "Майнд-карта")

Также Майнд-карту можно [скачать](https://github.com/AstapKa/DummyAPI/blob/main/DummyApi.xmind)

## Тест-кейсы

Также были офррмлены тест-кейсы в соответствии с Майнд-картой.
Тест-кейсы можно посомтреть [тут]()

## Баг-репорты

## Коллекции POSTMAN
https://github.com/AstapKa/DummyAPI/blob/main/Postman_collection_changes.json Эта коллекция проверяет...
https://github.com/AstapKa/DummyAPI/blob/main/DummyApi_DZ3_4_postman_collection.json Эта коллекция проверяет...
https://github.com/AstapKa/DummyAPI/blob/main/Postman_environment.json Эта коллекция проверяет...





