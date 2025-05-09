# MWAD-EXP_04-Simple-caluculator
## Date: 09.05.2025

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
sim.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="sim.css" />
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" disabled />
    <div class="buttons">
      <button class="btn" onclick="clearDisplay()">C</button>
      <button class="btn" onclick="deleteLast()">⌫</button>
      <button class="btn" onclick="appendOperator('/')">÷</button>
      <button class="btn" onclick="appendOperator('*')">×</button>

      <button class="btn" onclick="appendNumber('7')">7</button>
      <button class="btn" onclick="appendNumber('8')">8</button>
      <button class="btn" onclick="appendNumber('9')">9</button>
      <button class="btn" onclick="appendOperator('-')">−</button>

      <button class="btn" onclick="appendNumber('4')">4</button>
      <button class="btn" onclick="appendNumber('5')">5</button>
      <button class="btn" onclick="appendNumber('6')">6</button>
      <button class="btn" onclick="appendOperator('+')">+</button>

      <button class="btn" onclick="appendNumber('1')">1</button>
      <button class="btn" onclick="appendNumber('2')">2</button>
      <button class="btn" onclick="appendNumber('3')">3</button>
      <button class="btn equal" onclick="calculate()">=</button>

      <button class="btn zero" onclick="appendNumber('0')">0</button>
      <button class="btn" onclick="appendNumber('.')">.</button>
    </div>
  </div>

  <script src="sim.js"></script>
</body>
</html>
```
sim.css
```
body {
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(to right, #dbeafe, #000000);
    height: 100vh;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  
  .calculator {
    background: #fffdfd;
    padding: 20px;
    border-radius: 16px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    width: 320px;
  }
  
  #display {
    width: 100%;
    height: 60px;
    font-size: 28px;
    text-align: right;
    margin-bottom: 20px;
    padding: 8px;
    border: 1px solid #050606;
    border-radius: 10px;
  }
  
  .buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
  }
  
  .btn {
    padding: 20px;
    font-size: 20px;
    border: none;
    border-radius: 10px;
    background-color: #fdf5f5;
    cursor: pointer;
    transition: background-color 0.2s ease;
  }
  
  .btn:hover {
    background-color: #101215;
  }
  
  .equal {
    grid-row: span 2;
    background-color: #f6413b;
    color: rgb(0, 0, 0);
  }
  
  .equal:hover {
    background-color: #eb2525;
  }
  
  .zero {
    grid-column: span 2;
  }
  ```
sim.js
```
const display = document.getElementById('display');

function appendNumber(number) {
  display.value += number;
}

function appendOperator(operator) {
  const lastChar = display.value.slice(-1);
  if ('+-*/'.includes(lastChar)) return; // Prevent two operators in a row
  display.value += operator;
}

function clearDisplay() {
  display.value = '';
}

function deleteLast() {
  display.value = display.value.slice(0, -1);
}

function calculate() {
  try {
    display.value = eval(display.value);
  } catch {
    display.value = 'Error';
  }
}
```
## OUTPUT
![Screenshot 2025-05-06 210753](https://github.com/user-attachments/assets/a7a3a66d-fdb3-4ae6-b7ab-64644d6f02de)
![Screenshot 2025-05-06 210822](https://github.com/user-attachments/assets/3a92a307-08bd-4c50-9300-90db726fc5de)


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
