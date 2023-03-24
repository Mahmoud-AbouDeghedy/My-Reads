# MyReads Project

## TL;DR

This is a bookshelf app that allows you to select and categorize books you have read, are currently reading, or want to read. The project was built using React and the BooksAPI provided by Udacity.

## Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installing](#installing)
- [Built With](#built-with)
- [Authors](#authors)

---

## Getting Started

To get started, clone the project repository to your local machine and install the necessary dependencies.

### Prerequisites

You will need to have Node.js and npm (Node Package Manager) installed on your machine to run this project.

### Installing

1. Clone the project repository:

git clone https://github.com/Mahmoud-AbouDeghedy/my-reads.git

2. Navigate to the project directory:

cd my-reads

3. Install the necessary dependencies:

npm install

4. Start the app:

npm start

The app will open in your default browser at [http://localhost:3000](http://localhost:3000).

## Built With

- [React](https://reactjs.org/) - JavaScript library for building user interfaces
- [BooksAPI](https://reactnd-books-api.udacity.com/) - Backend server provided by Udacity

---

## Authors

- Mahmoud Ehab AbouDeghedy - [GitHub Profile](https://github.com/Mahmoud-AbouDeghedy)

## What You're Getting

```bash
├── README.md - This file.
├── SEARCH_TERMS.md # The whitelisted short collection of available search terms for you to use with your app.
├── package.json # npm package manager file. It's unlikely that you'll need to modify this.
├── public
│   ├── favicon.ico # React Icon, You may change if you wish.
│   └── index.html # DO NOT MODIFY
└── src
    ├── App.css # Styles for your app. Feel free to customize this as you desire.
    ├── App.js # This is the root of your app. Contains static HTML right now.
    ├── App.test.js # Used for testing. Provided with Create React App. Testing is encouraged, but not required.
    ├── BooksAPI.js # A JavaScript API for the provided Udacity backend. Instructions for the methods are below.
    ├── icons # Helpful images for your app. Use at your discretion.
    │   ├── add.svg
    │   ├── arrow-back.svg
    │   └── arrow-drop-down.svg
    ├── index.css # Global styles. You probably won't need to change anything here.
    └── index.js # You should not need to modify this file. It is used for DOM rendering only.
```

## Backend Server

- [`getAll`](#getall)
- [`update`](#update)
- [`search`](#search)

### `getAll`

Method Signature:

```js
getAll();
```

- Returns a Promise which resolves to a JSON object containing a collection of book objects.
- This collection represents the books currently in the bookshelves in your app.

### `update`

Method Signature:

```js
update(book, shelf);
```

- book: `<Object>` containing at minimum an `id` attribute
- shelf: `<String>` contains one of ["wantToRead", "currentlyReading", "read"]
- Returns a Promise which resolves to a JSON object containing the response data of the POST request

### `search`

Method Signature:

```js
search(query);
```

- query: `<String>`
- Returns a Promise which resolves to a JSON object containing a collection of a maximum of 20 book objects.
- These books do not know which shelf they are on. They are raw results only. You'll need to make sure that books have the correct state while on the search page.

## Important

The backend API uses a fixed set of cached search results and is limited to a particular set of search terms, which can be found in [SEARCH_TERMS.md](SEARCH_TERMS.md). That list of terms are the _only_ terms that will work with the backend.

## Create React App

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app). You can find more information on how to perform common tasks [here](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md).
