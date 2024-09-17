# Что происходит, когда пользователь вводит адрес и нажимает enter?

---

1. Браузер проверяет нет ли в хеше `DNS` (Domain Name System), если нет, то отправляет запрос `DNS` на сервер. `DNS` переводит в `IP` адрес
2. Установка `HTTP/HTTPS` соединения
3. Браузер отправляет `GET` запрос на сервер `HTML` файла. Сервер начинает ответ с заголовков и содержимым `HTML` файла

---

- [Что такое полифил и зачем он нужен?](./polifil.md)
- [Принципы разработки. KISS, DRY, YAGNI](./principles.md)
- [Разница между LocalStorage, SessionStorage и файлами cookie](./storageDifference.md)
- [Что такое HTTP?](./http.md)
- [Назовите основные методы HTTP?](./httpMethods.md)
- [Вопросы по JavaScript](../javaScript.md)
- [Главное меню](../../README.md)