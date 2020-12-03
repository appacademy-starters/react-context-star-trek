# Star Trek Project

In this project, you will make enhancements to an online trading card 
application. This application allows a user to select cards to build a deck for
game play or trading in the future.

The original developers set up the navigation (using `react-router-dom`) and
created the two primary screen layouts (using function components). Now, they 
need your help with capturing, storing and displaying the user's selection in 
their deck.

To begin

* Install the packages (`npm install`)
* Run the application and explore what's there (`npm start`)
** Notice that nothing happens when you click "buy" buttons on the home page
** See that the sample "friend" deck has cards, but the user's desk does not
** These are the gaps you will close!
* Commit this version before you make changes to a *GitHub* repo in your account
* Look through the code at the components, including UI and react-router setup

In particular, you should be looking for functionality gaps, such as the `const`
definitions at the start of several of the components. Write these down as 
you'll need the information later to provide those values through the context
you create.

## Phase 1 - Setup framework

To track the purchases, you'll be using *React Context*. Start by creating a new
function component called `AppContextProvider` and frame out the required pieces
(importing React, the function, and exporting the function).

As you may recall, one of the Object-Oriented Programming (OOP) concepts is
*encapsulation*, and a good principle to follow is to putting code that changes
for the same reason all together. So, that's the approach you're going to walk
through now. Specifically, this means putting the context and provider together
with the variables shared through the context (a.k.a. `value`), as well as the 
functions that update these variables.

### Define the *context* and its *provider*

The props of the function will include one variable named `children`. This 
variable is built into *React*. It holds a collection of JSX content passed to
the component between its opening and closing tags (which you'll do in the App 
in just a moment). In case you forgot, the easiest way to define your function 
with named props is using deconstruction of the props object into its individual
attributes. In other words, `const AppContextProvider = ({children}) => {`.

Above the function (and outside of it), declare a new constant (e.g. 
`AppContext`) which creates the context. Export this constant. (Later, you'll 
connect hooks to it in the UI components.)

Inside the function, return the provider for the context you created, and 
between the opening and closing JSX tags, place the children. For example:

```javascript
return (
  <AppContext.Provider>
    {children}
  </AppContext.Provider>
);
```

### Include one variable in the `value` as a starting point

Finally (for the moment), set the `value` prop on the component to an object.
In this object, you can start with just attribute, the `cards` array. The 
original developers left you *mock data* to use for this purpose, so you can 
`import` the appropriate constant from the class in `mockdata`.

In case you're stuck, here are a few hints...

```javascript
import { initialCards } from "./CardData";

// component function and other stuff

return (
  <AppContext.Provider value={{
    cards: initialCards
  }}>
    {children}
  </AppContext.Provider>
);
```

### Wrap the application in the *provider*

Open _App.js_. Import the new class you just made. Place it in the application 
such that all components that need to use the context are wrapped inside of it.
In other words, those components are children (or grandchildren, etc.) of the
context provider.

## Phase 2 - Connecting variable *state* to the *context provider*

Look back at the notes you took while you were reviewing the application. Which
variables did you find that were incomplete?

Hopefully, your list matches this one:

* cards (array)
* decks (also an array)
* inventory (object )
* buyCard (function)

Back in _AppContextProvider_, 

## Phase 3 - Buy cards

...

## Phase 4 - Display deck

...

## Bonus phase

...

