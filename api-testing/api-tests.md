# API Testing (Postman)

## POST /users

### Валидный запрос
Request:
{
  "name": "Test QA",
  "email": "testqa@gmail.com"
}

Response:
- Status: 201 Created
- Пользователь создан

---

### Невалидный email

Request:
{
  "name": "TestBug1",
  "email": "test1@gmailcom"
}

Ожидаемый результат:
- Ошибка валидации

Фактический результат:
- Пользователь создается

Баг: API принимает невалидный email

---

### Невалидные данные

Request:
{
  "name": 12345,
  "email": "not-an-email"
}

Фактический результат:
- Status: 201 Created

Баг: API принимает некорректные типы данных
