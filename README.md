# Redux React Module Project: Movie CRUD

This module explored the redux philosophy, creation of the redux store and using connect to link state and action to arbitrary components.

## Objectives
- Understand the use and setup of Redux
- Use Redux to connect existing state and actions to components
- Use the combineReducer method to combine states.
- Build reducers, actions and redux connections from scratch

## Introduction
In this project, you take a fairly complex application used to search a movie database and connect it to two different reducers through redux. You will both connect existing state definitions and build entire reducer / redux pairings from scratch.

![Movie DB Example](project-goals.gif)

***Make sure to complete your tasks one at a time and complete test each task before proceeding forward.***

## Instructions
### Task 1: Project Set Up
* [ ] Create a forked copy of this project.
* [ ] Clone your OWN version of the repository in your terminal
* [ ] cd into the project base directory `cd web-module-project-redux`
* [ ] Download project dependencies by running `npm install``
* [ ] Start up the app using `npm start`

### Task 2: Project Requirements
#### Setup Redux
> *The DOM and movie reducer has been provided for you, but it's up to to connect it to redux...*

* [ ] In index.js, make use of the createStore method and Provider component to link your App to redux.

#### Connecting the Movie reducer
> *Within the reducers folder is the file movieReducers.js. We have state already setup up here with some initial data. Let's connect that state to our component.*

* [ ] In movieReducer.js, make sure that we are setting our state by default to initialState. Otherwise

* [ ] The MovieList component prints all of our movies to the screen. Use the connect method here to push the movies state value into props. Replace our static movie variable with that prop.

* [ ] The Movie component needs to access our list of movies to function. Connect movies to props here as well.

* [ ] Finally, MovieHeader uses appTitle to display some title text. Connect this component to appTitle and test appTitle is correctly displayed in your app.


#### Connecting the Delete and Add Movie actions
> *Looks like you got a good handle on connecting stateToProps! Now let's connect some actions.*

* [ ] Notice that the deleteMovie reducer case and action creator are already available.

* [ ] Connect deleteMovie to the Movie component through the connect method.

* [ ] Create and connect the necessary event handlers to call deleteMovie on the current movie's id AND redirect the user using push('/movies').

* [ ] Add in an ADD_MOVIE case to the movieReducer.
* [ ] Code that case to add a new movie passed in through payload to our list of movies.
* [ ] Create an action creator for addMovie.
* [ ] Connect addMovie to the appropriate component.
* [ ] Create and connect the necessary event handlers to call addMovie, passing in the appropriate values.

#### Build out the favorites reducer
> *Alright! Now that the movie reducer is complete, you have the chance to build a reducer from scratch to handle favorite movie functionality.*

* [ ] Create a reducer file for handling business logic for favorites. Include state the following state values:
  -  favorites: an array of movie objects
  -  displayFavorites: a boolean that holds if favorite elements should be displayed in app

* [ ] Import you new reducer file into the ./reducers/index.js file.
* [ ] Use the combineReducers method to connect both movies and favorite movies to redux.
* [ ] Notice that your movie functions no longer work. Why? Make changes necessary to get the component connected to the movie reducer working again.
* [ ] Connect the favorites state to the FavoriteMovieList component and test.
* [ ] Connect the displayFavorites state to the Movie and MovieHeader component.

#### Build out the favorites actions
1. Add in reducer cases, action creators and event handler code for the following actions:
  - toggleFavorites : Switches the displayFavorites state value between true and false.
  - addFavorites: Adds in a new movie object into the favorites list.
  - removeFavorite: Removes a movie Object from the favorites list with an id passed in.

### Stretch goals
- It makes sense to not allow the user to favorite an item if favorites is not displayed. Add in means for the favorite button to ONLY display if displayFavorite is true.
- Right now, you can favorite the same movie multiple times. Change the addFavorite action to only add in a new favorite if it doesn't already exist.
- Add in the ability to remove a movie from the favorites list if that movie is removed from our main movie list.
- Style to your heart's content ❤️