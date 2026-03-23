# SQL Queries (QA Practice)

## 📌 Базовые запросы

### Получить всех пользователей
SELECT * FROM users;

### Получить только имя пользователей
SELECT name FROM users;

---

## 📌 Поиск по условию (WHERE)

### Найти пользователя по id
SELECT * FROM users WHERE id = 2;

### Найти пользователя по имени
SELECT * FROM users WHERE name = 'Anna';

### Найти пользователя по email
SELECT * FROM users WHERE email = 'test@gmail.com';

---

## 📌 LIKE (поиск по шаблону)

### Имена на букву A
SELECT * FROM users WHERE name LIKE 'A%';

### Email содержит gmail
SELECT * FROM users WHERE email LIKE '%gmail%';

---

## 📌 Комбинации условий

### Найти по имени и id
SELECT * FROM users WHERE name = 'Anna' AND id = 2;

### Найти по имени или email
SELECT * FROM users WHERE name = 'Ivan' OR email = 'test@gmail.com';

---

## 📌 Проверка данных после API

### Проверка, что пользователь создан
SELECT * FROM users WHERE email = 'testreal@gmail.com';

### Проверка на дубликаты
SELECT * FROM users WHERE email = 'anna@gmail.com';

### Подсчёт количества пользователей с email
SELECT COUNT(*) FROM users WHERE email = 'anna@gmail.com';

---

## 📌 Негативные проверки

### Проверка некорректных данных
SELECT * FROM users WHERE name = '   ';

### Проверка странных символов
SELECT * FROM users WHERE name LIKE '%$%';

---

## 📌 Важные проверки QA

### Проверка, что email не NULL
SELECT * FROM users WHERE email IS NULL;

### Проверка, что id не NULL
SELECT * FROM users WHERE id IS NULL;
