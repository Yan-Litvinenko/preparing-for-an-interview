# Типы данных в js

---

1. **null**
   - может иметь только 1 примитивное значение - `null`
   - `null` задаётся переменной явно и означает, что она является объектом, но структура этого объекта ещё не определена
   ```
    typeof null        // object
    null === null      // true
    null == null       // true
    null == undefined  // true
   ```
2. **undefined**

   - `undefined` является свойством глобального объекта, то есть, это переменная в глобальной области видимости. Начальным значением `undefined` является примитивное значение `undefined`.
   - `undefined` присваивается переменной, когда она была объявлена, но не было определено её начальное значение, это происходит автоматически в отличии от `null`, где мы задаём отсутсвие значения явно

   ```
   typeof undefined        // undefined
   undefined === undefined // true
   undefined == undefined  // true
   undefined == null       // true
   ```

3. **string**
4. **number**
   - **infinity** - числовое значение, которое представляет собой положительное бесконечное числовое значение
   - **NaN** – числовое значение, являющееся значением, которое представляет собой "не-число". Не равно ничему, даже самому себе. isNaN - вернёт `true` для всех NaN. Number.isNan - только для NaN
5. **boolean**
6. **symbol** - примитивное значение, представляющее уникальный ключ свойства объекта, не являющийся строковым
7. **bigInt** - примитивное значение, соответствующее целочисленному значению больше `253 - 1`
8. **object** - коллекция, представляет собой набор свойств. Он имеет единственный прототип, который может иметь
   значение null
   - **function** - элемент типа `Object`, являющийся экземпляром стандартного встроенного конструктора `Function`

---

- [Вопросы по JavaScript](../javaScript.md)
