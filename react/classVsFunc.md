# Какие основные различия между компонентами классов и функциональными компонентами в React?

---

1. **Синтаксис**:

   - **Классовые компоненты** создаются как классы и используют `extends React.Component`.
   - **Функциональные компоненты** — это простые функции, которые возвращают JSX.

2. **Состояние (state)**:

   - **Классовые компоненты** имеют встроенное состояние через this.state и используют метод setState() для его изменения.
   - **Функциональные компоненты** до появления хуков не имели состояния, но с хуками (например, useState) они могут работать с состоянием.

3. **Методы жизненного цикла**:

   - **Классовые компоненты** имеют методы жизненного цикла, такие как componentDidMount, componentDidUpdate, componentWillUnmount.
   - **Функциональные компоненты** управляют побочными эффектами с помощью хука useEffect, который может заменить все методы жизненного цикла.

4. **Пропсы**:
   - **В классовых компонентах** они передаются через атрибуты
   - **В функциональных компонентах** они передаются как аргументы функции

---

- [React](./react.md)
