# Ex04 Simple Calculator - React Project
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

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
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

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
App.js
```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <div>
      <h2 style={{ textAlign: "center" }}>Simple React Calculator</h2>
      <Calculator />
    </div>
  );
}

export default App;
```
calc.jsx
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleEqual = () => {
    try {
      setInput(eval(input).toString()); 
    } catch (error) {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || "0"}</div>
      <div className="buttons">
  <button className="number" onClick={() => handleClick("7")}>7</button>
  <button className="number" onClick={() => handleClick("8")}>8</button>
  <button className="number" onClick={() => handleClick("9")}>9</button>
  <button className="operator" onClick={() => handleClick("/")}>/</button>

  <button className="number" onClick={() => handleClick("4")}>4</button>
  <button className="number" onClick={() => handleClick("5")}>5</button>
  <button className="number" onClick={() => handleClick("6")}>6</button>
  <button className="operator" onClick={() => handleClick("*")}>*</button>

  <button className="number" onClick={() => handleClick("1")}>1</button>
  <button className="number" onClick={() => handleClick("2")}>2</button>
  <button className="number" onClick={() => handleClick("3")}>3</button>
  <button className="operator" onClick={() => handleClick("-")}>-</button>

  <button className="number zero" onClick={() => handleClick("0")}>0</button>
  <button className="number" onClick={() => handleClick(".")}>.</button>
  <button className="operator" onClick={() => handleClick("+")}>+</button>
  
  <button className="equal" onClick={handleEqual}>=</button>
  <button className="clear" onClick={handleClear}>C</button>
</div>
   </div>
  );
}

export default Calculator;
```
calc.css
```
.calculator {
  width: 260px;
  margin: 40px auto;
  border: 2px solid #333;
  border-radius: 12px;
  padding: 15px;
  background: #f9f9f9;
  box-shadow: 0px 5px 15px rgba(0,0,0,0.2);
}

.display {
  height: 50px;
  background: #222;
  color: #fff;
  text-align: right;
  font-size: 1.5rem;
  padding: 10px;
  border-radius: 8px;
  margin-bottom: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 8px;
}

button {
  height: 50px;
  font-size: 1.2rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.2s;
}
button.equal {
  background-color: orange;
  grid-column: span 2; 
}

button.clear {
  background-color: red;
  grid-column: span 2; 
}


.number {
  background: #e0e0e0;
}
.number:hover {
  background: #cfcfcf;
}


.operator {
  background: #4a90e2;
  color: white;
}
.operator:hover {
  background: #357ab7;
}

.equal {
  background: #f39c12;
  color: white;
}
.equal:hover {
  background: #d68910;
}

.clear {
  background: #e74c3c;
  color: white;
}
.clear:hover {
  background: #c0392b;
}

.zero {
  grid-column: span 2;
}



```

## OUTPUT
<img width="482" height="298" alt="438298045-db575e1d-2132-45a4-8c79-3c5a6a2c6cda" src="https://github.com/user-attachments/assets/ea555142-b330-48fa-abc7-e3b4b0349f83" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
