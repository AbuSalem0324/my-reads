# MyReads Project

This is the final assessment project for Udacity's React Fundamentals course. A static example of the CSS and HTML markup was provided and was used to write React code that was needed to complete the project. Progressively, added interactivity to the app by refactoring the static code.

![My reads App](https://github.com/nidhigaday/My-Reads/blob/master/public/Completed-app.gif)


## Getting Started

* Download this repo
* Install all project dependencies with `npm install`
* Start the development server with `npm start`

## Folders details
```bash
├── CONTRIBUTING.md
├── README.md - This file.
├── SEARCH_TERMS.md # The whitelisted short collection of available search terms.
├── package.json # npm package manager file.
├── public # icons and images
└── src
    ├── App.css # Styles for the app.
    ├── App.js # Root of the app.
    ├── App.test.js # Used for testing.
    ├── BooksAPI.js # A JavaScript API for the provided Udacity backend.
    ├── Bookshelves.js # JS file for the component to render each shelf items.
    ├── ListBooks.js # JS file for the component to render all components on the page.
    ├── SearchBooks.js # JS file for the component to render Seacrh books page.
    ├── icons # Helpful images for the app.
    ├── index.css # Global styles.
    └── index.js # Used for DOM rendering.
```
## Highlights:

* Created a new JS file for each component; following DOT (Do One Thing).
* Component state is passed down from parent to child component. SetState() is used to modify the state of the component.

## Backend Server

The provided file [`BooksAPI.js`](src/BooksAPI.js) contains following methods to perform necessary operations on the backend:

* [`getAll`](#getall) To get all the books from the API
* [`update`](#update) Update shelf information of the book
* [`search`](#search) Search book in the database

## Completed Tasks:

* GetAll books from API
  ```
  ├── Leveraged (#getall) in the component lifecycle - componentDidMount()
  └── Used SetState() to render books in the UI
  ```
* Able to move books between the shelves
  ```
  ├── Leveraged (#update) in the component to update shelf value of the book in the backend 
  ├── Re-rendered UI with updated state by using setState
  └── Component state is passed from Parent to Child component using Props
  ```
* Keep UI and URL in sync
  ```
  └── Leveraged <BrowserRouter /> from react-router-dom to render the UI based on its URL instead of the state 
  ```
* Able to Search and add books
  ```
  └── Leveraged top-bottom approach by passing updated state of the Parent to Child component
  ```
* Book shelf or state should reflect on both Search and Main page
  ```
  └── Used ES6 concat function to sustain state of the existing books under Search page
  ```
* Added a Error 404: Page not found for invalid URL
  ```
  └── Used Switch from react-router-dom to switch between the URLs and render No page found error if does not match with any valid URLs
  ```
  
## Resources & Dependencies

* [react-router-dom](https://www.npmjs.com/package/react-router-dom)
