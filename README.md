# Ex04 Simple Calculator - React Project

## Date:24-11-2026

## Name : Danaseelan G

## Reg No : 212225040053

## AIM

To develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM

### STEP 1

Create a React App.

### STEP 2

Open a terminal and run:

  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3

Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4

Plan the UI: Display screen, number buttons (0-9), operators (+, -, \*, /), clear (C), and equal (=).

### STEP 5

Create a new file Calculator.css in src/ and add the styling.

### STEP 6

Open src/App.js and modify it.

### STEP 7

Start the development server.
npm start

### STEP 8

Open http://localhost:3000/ in the browser.

### STEP 9

Test the calculator by entering numbers and operations.

### STEP 10

Fix styling issues and refine content placement.

### STEP 11

Deploy the website.

### STEP 12

Upload to GitHub Pages for free hosting.

## PROGRAM

```
App.jsx
import { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearDisplay = () => {
    setInput("");
  };

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <h2>Simple Calculator</h2>

      <input
        type="text"
        value={input}
        readOnly
        className="display"
      />

      <div className="buttons">
        <button onClick={clearDisplay}>C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={calculate}>=</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("0")}>0</button>

        <button onClick={() => handleClick(".")}>.</button>
      </div>
    </div>
  );
}

export default App;

App.css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background: #f2f2f2;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  width: 320px;
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.3);
}

.calculator h2 {
  text-align: center;
  margin-bottom: 15px;
}

.display {
  width: 100%;
  height: 50px;
  font-size: 22px;
  text-align: right;
  padding-right: 10px;
  margin-bottom: 15px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 20px;
  cursor: pointer;
  border: none;
  background: #3498db;
  color: white;
  border-radius: 5px;
}

button:hover {
  background: #2980b9;
}

```

## OUTPUT

![alt text](<Screenshot 2026-11-24 152748.png>)
![alt text](<Screenshot 2026-11-24 152625.png>)
![alt text](<Screenshot 2026-11-24 152740.png>)

## RESULT

The program for developing a simple calculator in React.js is executed successfully.
