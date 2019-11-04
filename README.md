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
From the Terminal, go to the folder where the React app was created. The first three commands are for React dependencies and bootstrap templates. Axios is for making RESTful service calls to an API. MDBReact is for the bootstrap icon library (font awesome). React Color is for color pickers. 
```
yarn add react-route-dom
yarn add react-bootstrap bootstrap
npm install -D babel-loader @babel/core @babel/preset-env
npm install axios -- save
npm install mdbreact --save
npm install react-color --save
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

### Build the App for AWS
From the terminal, this command will build the app for production.
```
npm run build
```
