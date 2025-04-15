# Book API (Spring Boot + Hibernate + PostgreSQL)

Проект представляет собой RESTful API для управления библиотекой книг. Используется Spring Boot для создания серверной части, Hibernate для работы с базой данных и PostgreSQL для хранения данных.

## 🚀 Установка и настройка

### 1. Требования
- Java 17 или выше
- Maven (или Gradle)
- PostgreSQL (или другая СУБД, настроенная в `application.properties`)

### 2. Клонирование репозитория
Клонируйте проект в свой локальный репозиторий:

```bash
git clone https://github.com/EmilDias123/book-api.git
```
3. Настройка базы данных
Установите и запустите PostgreSQL, если ещё не установлен.

Создайте новую базу данных
sql
```bash
CREATE TABLE book (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255),
  author VARCHAR(255),
  year INT,
  isbn VARCHAR(255)
);
```
4. Конфигурация application.properties
Откройте файл src/main/resources/application.properties и настройте параметры подключения к вашей базе данных PostgreSQL.

```bash
spring.datasource.url=jdbc:postgresql://localhost:5432/book_api
spring.datasource.username=your_username
spring.datasource.password=your_password
```


5. Запуск проекта
Запустите приложение с помощью Maven: BookapiAplication.java


🛠 API Endpoints
1. Получить все книги
```bash
GET /api/books
```
2. Получить книгу по ID
```bash
GET /api/books/{id}
```
3. Создать новую книгу
```bash
POST /api/books
```
4. Обновить информацию о книге
```bash
PUT /api/books/{id}
```
5. Удалить книгу
```bash
DELETE /api/books/{id}
```
🧑‍💻 Технологии

Java 24 — основной язык программирования

Spring Boot — фреймворк для построения приложений

Spring Data JPA — для работы с базой данных

PostgreSQL — СУБД для хранения данных

MapStruct — для преобразования между сущностями и DTO

📝 Дополнительная информация
Модели данных: сущности книг, с полями id, title, author, isbn, year.

DTO: объекты, которые используются для передачи данных через API.
## Автор
Создатель: Юрий Черединов
GitHub: EmilDias123

📄 Лицензия
Проект с открытым исходным кодом (MIT License).

Репозиторий: github.com/EmilDias123/bookapi
