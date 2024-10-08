# Псевдоклассы

---

**Псевдокласс** - определяет особое состояние элемента.

- **:active** - стили применяются к элементам в момент взаимодействия
- **:checked** - применяется к элементам, состояние которых меняется с помощью атрибута `checked`
- **:focus** - при переключении клавишей `Tab` или выбор инпута
- **:hover** - состояние элемента, когда на него навели курсор

- **:focus-within** применяется к элементам, которые либо сами находятся в фокусе, либо имеют дочерние элементы в фокусе
- **:disabled** - позволяют находить элементы формы по состоянию их атрибута `disabled`
- **:empty** - используется для выбора пустых элементов. Пустыми считаются элементы без потомков и текста.
- **:child** - cелекторы элемента по его положению относительно родителя (первый, последний, n-й, единственный)

- **:link** - для оформления ссылок, которые пользователь ещё никогда не открывал
- **:visited** - добавляется ссылкам, по которым уже переходил пользователь
- **:any-link** - применяется ко всем элементам, которые могут иметь атрибут `href` (`<a>`, `<area>` и `<link>`).

- **:default** - применяется к элементам формы (`<input type="radio">, <input type="checkbox">, <option> и <button>`), у которых можно задать начальное состояние. Например, у `<input type="checkbox">` селектор применится к тому чекбоксу, у которого в разметке установлен атрибут `checked`, т. е. он по умолчанию выбран:

```
:default + span {
  color: #2E9AFF;
}
```

- **:is** - позволяет сгруппировать схожие селекторы, принимают вес наиболее специфичного селектора внутри скобок
- **:has** - позволяет выбрать элемент на основе дочернего или соседнего элемента, принимают вес наиболее специфичного селектора внутри скобок
- **:not()** - находит элемент, который не соответствует селектору, переданному в качестве аргумента, принимают вес наиболее специфичного селектора внутри скобок
- **:where()** - принимает один или несколько селекторов в качестве аргумента, работает также как `:is()`, не влияет не специфичность

```
h1 a, h2 a, h3 a, h4 a, h5 a, h6 a. Mожно переписать => :is(h1, h2, h3, h4, h5, h6) a
a:has(img) - применяем стили ко всем ссылкам, которые содержат изображения
dt:has(+ dd) - стили применятся только к такому <dt>, за которым сразу следует элемент <dd>
img:not([alt])
:where(header, main, footer) a  вместо header a, main a, footer a
```

---

- [Вопросы по CSS](./CSS.md)
