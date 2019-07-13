1.  Name 3 JavaScript Array/Object Methods that do not produce side-effects? Which method do we use to create a new object while extending the properties of another object?

Arrays -- .map, .filter, .concat. For instance, using concat instead of push because push mutates the original array and concat returns a new array and leaves the original array intact. Objects -- object.assign extends the properties of an object into a new object as it copies properties of source objects into a target object and then returns it. You can use object.assign by using an empty object as the target object to edit the objects. 

1.  Describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

The store is where the state of the whole application is stored in an object tree within a single store which makes it easy to create universal apps, debug an application, and provides a faster development cycle because it allows you to persist an app's state in development. With this, the only way to change the state is to provide an action (an object with a payload of information that sends data from the app to the store) that describes what's happening. This makes sure that the network callbacks won't write directly onto the state. Reducers are functions that take the previous state and an action, and specify how the state tree is transformed by the actions in the returned state. Reducers allow you to control the order in which they are called, pass data, and you can make reusable reducers. 

3.  What is the difference between Application state and Component state? When would be a good time to use one over the other?

The Application state is global and the Component state is local and isn't accessible from other components unless it's passed as props to sub components. It is a good time to use the Application state when the number of components increase and the passing of props become too cumbersome.

4.  What is middleware?

Middleware is software that lies between an operating system and the applications running on it, and provides services beyond those available from the operating system. It's like plumbing systems -- providing water and sanitation to rapidly-growing cities.

5.  Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

Redux-thunk is middleware that allows us to call action creators that return functions instead of an action object. The function receives the store's dispatch method and calls actions that are functions to return whatever they're supposed to return and then passes the action to the next middleware (next(action)).

1.  Which `react-redux` method links up our `components` with our `redux store`?

Provider store wraps the react application and makes the state available to container components and then connect creates the higher-order component for making container components based out of React components. 