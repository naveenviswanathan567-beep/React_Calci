# Ex04 Simple Calculator - React Project
## Date:14-03-2026
## Name : NAVEEN V
## Reg No :212225240098

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
```

<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .calculator {
            background: #222;
            padding: 20px;
            border-radius: 15px;
            width: 280px;
        }

        #display {
            width: 100%;
            height: 60px;
            font-size: 28px;
            text-align: right;
            margin-bottom: 15px;
            border: none;
            border-radius: 8px;
            padding: 5px;
            box-sizing: border-box;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        button {
            height: 55px;
            font-size: 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
        }

        button:hover {
            background: #ccc;
        }

        .operator {
            background: #ff9500;
            color: white;
        }

        .equal {
            background: #28a745;
            color: white;
        }

        .clear {
            background: #dc3545;
            color: white;
        }
    </style>
</head>

<body>

    <div class="calculator">

        <input type="text" id="display" readonly>

        <div class="buttons">
            <button class="clear" onclick="clearDisplay()">C</button>
            <button onclick="deleteLast()">⌫</button>
            <button class="operator" onclick="addValue('%')">%</button>
            <button class="operator" onclick="addValue('/')">÷</button>

            <button onclick="addValue('7')">7</button>
            <button onclick="addValue('8')">8</button>
            <button onclick="addValue('9')">9</button>
            <button class="operator" onclick="addValue('*')">×</button>

            <button onclick="addValue('4')">4</button>
            <button onclick="addValue('5')">5</button>
            <button onclick="addValue('6')">6</button>
            <button class="operator" onclick="addValue('-')">−</button>

            <button onclick="addValue('1')">1</button>
            <button onclick="addValue('2')">2</button>
            <button onclick="addValue('3')">3</button>
            <button class="operator" onclick="addValue('+')">+</button>

            <button onclick="addValue('0')">0</button>
            <button onclick="addValue('.')">.</button>
            <button class="equal" onclick="calculate()">=</button>
        </div>

    </div>

    <script>
        function addValue(value) {
            document.getElementById("display").value += value;
        }

        function clearDisplay() {
            document.getElementById("display").value = "";
        }

        function deleteLast() {
            let display = document.getElementById("display");
            display.value = display.value.slice(0, -1);
        }

        function calculate() {
            let display = document.getElementById("display");

            try {
                display.value = eval(display.value);
            } catch {
                display.value = "Error";
            }
        }
    </script></body>
</html>
```





## OUTPUT
<img width="1196" height="812" alt="Screenshot 2026-08-25 141226" src="https://github.com/user-attachments/assets/779d28a9-bbf4-4609-a84c-c945b837542b" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
