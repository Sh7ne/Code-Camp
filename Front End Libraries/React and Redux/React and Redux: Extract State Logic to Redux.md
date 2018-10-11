```js

// define ADD, addMessage(), messageReducer(), and store here:

const ADD = 'ADD';

const addMessage = message => {
  return { 
    type: ADD,
    message: message
    };
  };

const messageReducer = (prevstate,action) =>{
  return [...prevstate, action.message];
}

let store = {
  state: [],
  getState: () => store.state,
  dispatch: (action) => {
    if (action.type == ADD){
      store.state = messageReducer(store.state, action) 
    }
  }
}

```
