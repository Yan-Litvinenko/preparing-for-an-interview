# Прототипны объектов

----

**Прототипы** - это механизм, с помощью которого объекты могут наследовать свойства и методы от других объектов. Каждый объект имеет внутреннее свойство `[[Prototype]]`, которое ссылается на другой объект или null.

**prototype** - это свойство функции конструктора, которое хранит в себе интерфейс предка. Prototype есть у всех функций/классов
**proto** - свойство объекта (функции это те же объекты), которое содержит ссылку на `prototype`.

```javascript
function User(name) {
    this.name = name
}

const yan = new User("Yan")

User.prototype.say = function () {
    console.log(`Hello, my name is ${this.name}`)
}

yan.say() // Hello, my name is Yan
```

- [Вопросы по JavaScript](../javaScript.md)
