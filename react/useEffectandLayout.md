# useEffect vs useLayoutEffect

---

## useEffect

Выполняется асинхронно после рендеринга компонента и отображения изменений на экране. Это означает, что изменения в DOM уже произошли, и эффект запускается позже, чтобы не блокировать отображение интерфейса. Используется для сетевых запросов, таймеров, подписок, логирования.

## useLayoutEffect

Выполняется синхронно сразу после того, как React закончил изменение DOM, но до того, как браузер отобразил эти изменения. Используется, когда нужно измерить DOM, прокрутка до определённого элемента, изменение стилей, которые могут повлиять на компоновку. Может замедлить рендеринг, так как выполняется синхронно и блокирует отображение, пока не завершит работу.

- [React](./react.md)
