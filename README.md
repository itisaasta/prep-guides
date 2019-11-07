# prep-guides

## React

### Prerequisites
From the Terminal, install the react app creator.
```
sudo npm install -g create-react-app
```

### Create the React App
From the Terminal, go to the folder where you want to create the React app.
```
create-react-app APPNAME
```

### Install Dependencies
From the Terminal, go to the folder where the React app was created. The first three commands are for React dependencies and bootstrap templates. Axios is for making RESTful service calls to an API. React Color is for color pickers. Font Awesome is for icons.
```
yarn add react-route-dom
yarn add react-bootstrap bootstrap
npm install -D babel-loader @babel/core @babel/preset-env
npm install axios -- save
npm install react-color --save
npm install @fortawesome/fontawesome-svg-core --save
npm install @fortawesome/free-solid-svg-icons --save
npm install @fortawesome/react-fontawesome --save
```

### Open the App in VSCode
From the Terminal, this command will launch VSCode for the app.
```
code .
```

### Run the App
From the Terminal, this command will launch the app in a browser window and live update.
```
yarn start
```

### Example App
An example app for create, read, update, delete (CRUD) is available here: https://github.com/didinj/react-hooks-example/tree/master/src

### Tree for App
An app can be framed using the following structure:
* src
  * api - API definitions
  * components - Reusable pieces, like a Search Bar
  * context - Data objects like Auth, Products, etc.
  * hooks - API calls
  * images - Image assets
  * screens - Display of components
  * App.js
  * index.js
  * serviceWorker.js
  * App.css
  * index.css
* package.json - All dependencies for the product
* README.md - The how to guide for the product and how it was built
* .gitignore - Things not to load to the GitHub repo

### Key React Concepts
A few concepts to grasp to make working with React easier:
* Code: The code you write is JSX, stored in JavaScript files. The return statement is what gets displayed on the screen. It behaves very much like HTML with custom properties. The properties can be anything: examples include onChange, onSubmit, and placeholder.
* properties/props: Properties pass from parent to child. Passing props enables composing screens of reusable components.
* Context: Enables data storage and reuse across screens. Key data objects will be stored here. The context provider needs to be setup in index.js. The context consumer can be called from any asset that needs it. ``` const { state } = useContext(AuthContext); ```
* Variables: Screen rerender is triggered when variables are changed through setters. This means no direct variable manipulation for items rendered on screen. So if there is a variable productName, you'll also need setProductName. If you want to show/hide something, you'll need a variable productVisibility, with a setProductVisibility setter. These can be created for you using useState.
* useState: Stores variable state for a page. Creates the variable and a setter. You can pass in the default value. ``` const [product, setProduct] = useState(''); ```
* React Bootstrap & React Router: Any links need to reference the React Router component Link in order to work properly. Failing to do so will reload the app, resetting all state. ``` <Nav.Link as={Link} to='/list'>List</Nav.Link> ```
* The JSX returned to render components can only be one element. If many elements need to be returned, wrap them in ```<></>``` or ```<div></div>```.
* Common asset flow:
  * Import Dependencies
  * Call Contexts Needed
  * Call Hooks Needed
  * Setup State
  * Reusable Functions
  * Return JSX to be Displayed

### Dependency Reference
For reference while building, these are guides related to dependencies:
* React Bootstrap Components: https://react-bootstrap.github.io/components/alerts
* Font Awesome Guide: https://github.com/FortAwesome/react-fontawesome
* Font Awesome Icon Library: https://fontawesome.com/icons?d=gallery
* Color Picker Guide: https://casesandberg.github.io/react-color/
* Axios Guide: https://github.com/axios/axios

### Build the App for AWS
From the terminal, this command will build the app for production.
```
npm run build
```
