# useSelector

[useSelector()](https://react-redux.js.org/api/hooks#useselector)

- useStelector was released as a part of react-redux v7.1.0
- Its sole purpose is to extract data from the Redux store using a selector function.

`import { useSelector } from ‘react-redux’

function Profile () {
const user = useSelector ((state)) => state.user)
...
}`

- The function you pass to useSelector will be passed the state from the store.
- From there you can grab any value from the state by returning it.
- The only caveat around useSelector has to do with selecting multiple values from the store. For example, say we wanted to grab users, autherd and notifications.

`const { user, authed, notifications } = useSelector((state) => ({ user: state.user, authed: state.authed, notifications: state.notifications }))`

- Though this will work, it won’t be as performant as it could be.
- The reason for this is because under the hood, useSelector uses strict reference equality to decide when to re-render the component. By returning an object from useSelector, the strict reference equality.
- `(oldReturnValue === new ReturnValue`
- will never be true meaning the component will always re-render. There are a few ways to get around this - my favorite being breaking out each piece of state into its own selector.

`const user = useSelector((state) => state.use) const author = useSelector((state) => state.authed) const notifications = useSelector((state) => state.notifications)`

- The reason this works is because react-redux will batch each of the selectors together causing only a single re-render.

- You may call useSelector() multiple times within a single function component.

- Each call to useSelector() creates an individual subscription to the Redux store.

- Because of the React update batching behavior use in React Redux v7

- A dispatched action that causes multiple useSelector()s in the same component to return new values should only result in a single re-render, - React Redux Docs useSelector