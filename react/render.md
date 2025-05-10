# React render

----

**Render в React** — это процесс, React запрашивает [JSX](./jsx.md) у компонента, проанализировав JSX React преобразует его в вызов функции React.createElement() который вернет [Virtual-DOM](./virtual-dom.md). Далее инииализация **реконциляции(diffing)** - сравнение актуального Virtual DOM с предыдущим и **commit** - вставка в реальный DOM объект компонента

`render -> reconciliation (diffing) -> commit`

- [React](./react.md)
