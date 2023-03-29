# Superdom

This project demonstrates that vanilla javascript can generate dynamic html components with global state without the need for react and all its bloat

# How to try

Click here: https://supertestnet.github.io/superdom

# How it works

I create a component object that contains a function that returns an html element containing your component. The component object also contains:

- globally accessible key/value pairs
- a function called render() which re-renders whatever html element contains this component
- a function called setState() which can modify the state's key/value pairs and then call render() to rerender it
- any user-created methods that use render() or setState() or both

The result is an html component with rich global state and which, when updated using its built in setState() function (or any user-created methods that use that built-in function), automatically re-renders without affecting other html elements. Also, if you want it to affect other html elements (e.g. because they access and display this component's global state), you can -- when creating those other components -- easily add to the original function's render function so that, when the original component's state is modified using its setState() function (or whenever it's render() function is called), it also rerenders all other components that display a value from its state object.

Voila! The best part of react without the rest of react.
