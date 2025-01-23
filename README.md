# React Learning Guide 📚🚀

Covering the fundamentals of React, and how to set up your first React project.

---

## 1. What is React? 🤔

**React** is a JavaScript library for building user interfaces, especially for a fast, dynamic, and responsive UI. 

<br>

---

## 2. Prerequisites 🖥️

Before you start a react project, you need to have **Node.js** and **npm** (Node Package Manager).

### Check if Node.js is installed:

Run this in your terminal:

```bash
node -v
npm -v
```

If you don't have Node.js and npm installed, go to the official website to install them: [Node.js](https://nodejs.org/en).

<br>

---

## 3. Create Your First React Project 🎨

### Run this command to create a new project:

This will bootstrap and set up everything for you, including a development server, build scripts, and a project structure.

```bash
npx create-react-app name --legacy-peer-deps
```

Replace ```name``` with your project name.

<br>

---

## 4. Navigating Your React Project 🔍

After creating your React project, navigate to your project directory:

```bash
cd name
```

Inside the ```name``` folder, you’ll find the following structure:

- ```src/```: Contains all of your application's source code, including React components (e.g., App.js).
- ```public/```: Contains static files, like index.html, where the React app is rendered.
- ```node_modules/```: Contains all the dependencies required to run the app.

<br>

---

## 5. Start the Development Server 🖥️

### Run this command to start the local server:

To run your React app and see it in the browser, start the development server with:

```bash
npm start
```
Your app will automatically open in the browser at ```http://localhost:3000```

<br>

---

## 6. Understanding React Components ⚙️

React apps are built using **components**.

### Key concepts:

- ```Components```: Reusable pieces of code that describe a part of the user interface. 
- ```JSX```: JavaScript XML is a syntax extension for JavaScript that looks like HTML. JSX is used to define the structure of your components.

### Example of a Functional Component:

In React, components are commonly written as functions (functional components) that return JSX. 

In your src/App.js file, you’ll see a default component that looks like this:

```jsx
import React from 'react';

function App() {
  return (
    <div className="App">
      <h1>Hello, React!</h1>
    </div>
  );
}

export default App;
```

You can implement other **custom-made components** by including them as **imports**, like so: 

```jsx
import React from 'react';
import Navbar from './Navbar'; // Import the Navbar component

function App() {
  return (
    <div className="App">
      <Navbar /> // Implements the component
      <h1>Hello, React!</h1>
    </div>
  );
}

export default App;
```

### **NOTE:** Anything you import into App.js will be implemented globally for the entire application.

<br>

---

## 8. Learning About Props and State 🔑
- ```Props```: Use props to pass data from one component to another.
- ```State```: Use state to store data that can change over time, like form inputs or API responses.

For example:

```jsx
import React, { useState } from 'react';

function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  const [name, setName] = useState("React Developer");

  return (
    <div className="App">
      <Greeting name={name} />
      <button onClick={() => setName("Minko82")}>Change Name</button>
    </div>
  );
}

export default App;
```

In this example:

- The **Greeting component** receives a ```prop``` name and displays it.
- The **App component** has ```state``` (name) that can be changed when you click the button.

<br>

---

## 9. Testing and Building 🛠️
Once you’ve written your components, you can:

- **Test** your components using ```npm test```.
- **Build** your app for production using ```npm run build```.

<br>

---

Yay we nade it to the end of my React speedrun lol ```\(^-^)/```✨

