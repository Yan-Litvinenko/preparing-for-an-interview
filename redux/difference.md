# Разница между Redux Toolkith и "классичкским" Redux

----

- Redux Toolkit используют библиотеку Immer, что позволяет писать "мутабельную" логику обновления состояния, которая становится корректным иммутабельным вариантом.

```javascript
// Redux Toolkith
decrement: (state) => {
    state.value -= 1
}
addTodo: (state, action) => {
  state.push(action.payload); // Immer сделает это иммутабельным
}

    // Классический Redux 
case 'ADD_TODO':
  return [...state, action.payload];

function counterReducer(state = { value: 0 }, action) {
  switch (action.type) {
    case 'DECREMENT':
      return { ...state, value: state.value - 1 };
    default:
      return state;
  }
}

```

- В классическом редаксе редьюсеры и типы action пишутся вручную

```javascript
// Classic Redux
const DECREMENT = 'DECREMENT';

const decrement = () => ({ type: DECREMENT });

function counterReducer(state = 0, action) {
  switch (action.type) {
    case DECREMENT:
      return state - 1;
    default:
      return state;
  }
}

// Redux Toolkith
import { createSlice } from '@reduxjs/toolkit';

const counterSlice = createSlice({
  name: 'counter',
  initialState: 0,
  reducers: {
    decrement: (state) => state - 1,
  },
});

export const { decrement } = counterSlice.actions;
export default counterSlice.reducer;
```
- В классическом Redux devTools и middleware (например, redux-logger) нужно подключать вручную.

- [Вопросы по Redux](redux.md)