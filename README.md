
# Discussion - Redux

Hide Assignment Information

Instructions

# Readings: Redux Basic

Below you will find some reading material and some additional resources that support today's topic and the upcoming lecture.

### Preparation Materials

-   [Fundamentals of Redux](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867 "https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867")
-   [Getting Started With Redux](https://redux.js.org/introduction/getting-started#basic-example "https://redux.js.org/introduction/getting-started#basic-example")
-   [Redux Terms and Concepts](https://redux.js.org/tutorials/essentials/part-1-overview-concepts#redux-terms-and-concepts "https://redux.js.org/tutorials/essentials/part-1-overview-concepts#redux-terms-and-concepts")


## What is Redux?
Redux is a predictable state container designed to help you write JavaScript apps that behave consistently across client, server, and native environments, and are easy to test.
*With Redux, the state of your application is kept in a store, and each component can access any state that it needs from this store.*

## When to use Redux?
Lately one of the biggest debates in the frontend world has been about Redux. Not long after its release, Redux became one of the hottest topics of discussion. Many favored it while others pointed out issues.

Redux allows you to manage your app’s state in a single place and keep changes in your app more predictable and traceable. It makes it easier to reason about changes occurring in your app. But all of these benefits come with tradeoffs and constraints. One might feel it adds up boilerplate code, making simple things a little overwhelming; but that depends upon the architecture decisions.

## Core Concepts
Imagine your app’s state is described as a plain object. For example, the state of a todo app might look like this:
```
{
  todos: [{
    text: 'Eat food',
    completed: true
  }, {
    text: 'Exercise',
    completed: false
  }],
  visibilityFilter: 'SHOW_COMPLETED'
}
```

This object is like a “model” except that there are no setters. This is so that different parts of the code can’t change the state arbitrarily, causing hard-to-reproduce bugs.

To change something in the state, you need to dispatch an action. An action is a plain JavaScript object (notice how we don’t introduce any magic?) that describes what happened. Here are a few example actions:
```
{ type: 'ADD_TODO', text: 'Go to swimming pool' }
{ type: 'TOGGLE_TODO', index: 1 }
{ type: 'SET_VISIBILITY_FILTER', filter: 'SHOW_ALL' }
```
