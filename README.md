# my-cal
my first cal
Sure! Here's a simple calculator using HTML, CSS, and JavaScript:

### HTML

```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <div class="buttons">
            <button onclick="appendNumber('1')">1</button>
            <button onclick="appendNumber('2')">2</button>
            <button onclick="appendNumber('3')">3</button>
            <button onclick="appendOperator('+')">+</button>
            <button onclick="appendNumber('4')">4</button>
            <button onclick="appendNumber('5')">5</button>
            <button onclick="appendNumber('6')">6</button>
            <button onclick="appendOperator('-')">-</button>
            <button onclick="appendNumber('7')">7</button>
            <button onclick="appendNumber('8')">8</button>
            <button onclick="appendNumber('9')">9</button>
            <button onclick="appendOperator('*')">*</button>
            <button onclick="appendNumber('0')">0</button>
            <button onclick="appendOperator('.')">.</button>
            <button onclick="calculate()">=</button>
            <button onclick="appendOperator('/')">/</button>
            <button onclick="clearDisplay()">C</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
/* styles.css */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

.calculator {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 200px;
}

#display {
    width: 100%;
    height: 40px;
    margin-bottom: 10px;
    text-align: right;
    padding: 10px;
    font-size: 1.2em;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}

button {
    font-size: 1.2em;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #f9f9f9;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
}

button:hover {
    background-color: #e0e0e0;
}
```

### JavaScript

```javascript
// script.js
let display = document.getElementById('display');
let currentInput = '';

function appendNumber(number) {
    currentInput += number;
    display.value = currentInput;
}

function appendOperator(operator) {
    currentInput += ' ' + operator + ' ';
    display.value = currentInput;
}

function calculate() {
    try {
        currentInput = eval(currentInput).toString();
        display.value = currentInput;
    } catch (e) {
        display.value = 'Error';
    }
}

function clearDisplay() {
    currentInput = '';
    display.value = '';
}
```

### Explanation

1. **HTML**: Defines the structure of the calculator with a display input and buttons for numbers and operators.
2. **CSS**: Styles the calculator, making it visually appealing with a centered layout, grid for buttons, and hover effects.
3. **JavaScript**: Handles the calculator logic, updating the display, appending numbers/operators, evaluating expressions, and clearing the display.

To test this, save the HTML, CSS, and JavaScript code in corresponding files (`index.html`, `styles.css`, `script.js`) and open the `index.html` file in a web browser.
