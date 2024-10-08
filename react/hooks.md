# Какие существуют хуки в React?

---

1. **useState()** - предназначен для управления состоянием компонента. Данная функция возвращает пару геттер/сеттер - значение начального состояния и функцию для обновления этого значения. Функцию имеет следующую сигнатуру: `const [value, setValue] = useState(defaultValue)`

2. **useEffect()** - предназначен для запуска побочных эффектов (например, выполнение сетевого запроса или добавление обработчика событий) после монтирования и отрисовки компонента. Данная функция принимает колбек и массив зависимостей.

- массив не указан: эффект запускается при каждом рендеринге
- указан пустой массив: эффект запускается только один раз
- указан массив с элементами: эффект запускается при изменении любого элемента`

3. **useLayoutEffect()** - похож на хук useEffect(), за исключением того, что он запускает эффект перед отрисовкой компонента. Данный хук предназначен для запуска эффектов, влияющих на внешний вид DOM, незаметно для пользователя. Эта функция имеет такую же сигнатуру, что и useEffect().

4. **useContext()** - предназначен для прямой передачи пропов компонентам, находящимся на любом уровне вложенности. Он позволяет избежать так называемого "бурения пропов" `(prop drilling)`, т.е. необходимости последовательной передачи пропов на каждом уровне вложенности.

5. **useReducer()** - как и хук useState(), предназначен для управления состоянием. Он используется при наличии сложной логики управления состоянием или когда следующее состояние зависит от предыдущего. useReducer() принимает редуктор (reducer), обновляющий состояние на основе типа (type) и, опционально, полезной нагрузки (payload) переданной операции (action).

6. **useCallback()** - возвращает мемоизированную версию переданной функции обратного вызова. Данный хук принимает колбек и массив зависимостей. колбек повторно вычисляется только при изменении значений одной из зависимостей.

7. **useMemo()** - является альтернативой хука `useCallback()`, но принимает любые значения, а не только функции.

8. **useRef()** - возвращает объект, свойство `current` которого содержит ссылку на узел DOM. Данный хук также может использоваться для сохранения любого мутирующего значения.

---

- [React](./react.md)
