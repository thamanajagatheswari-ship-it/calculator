# Ex.No:06 JavaScript Calculator
## Date:25/11/2026
## AIM

To design and develop a simple calculator using HTML, CSS, and JavaScript to perform basic arithmetic operations such as addition, subtraction, multiplication, and division.

## ALGORITHM

1. Create an HTML page to design the calculator interface.
2. Create a display field to show the numbers and calculation results.
3. Create buttons for digits from 0 to 9 and arithmetic operators.
4. Use CSS to arrange and style the calculator buttons and display.
5. Write JavaScript functions to handle button clicks.
6. Store the entered numbers and operators in the calculator display.
7. Use JavaScript to evaluate the arithmetic expression.
8. Display the calculated result on the calculator screen.
9. Provide a clear button to reset the calculator.
10. Test the calculator with different arithmetic operations.

## PROGRAM
```
<!DOCTYPE html>
<html>
<head>
<title>Calculator</title>
<style>
body{ display:flex; justify-content:center; align-items:center; height:100vh; background:#1e1e2e; font-family:Arial; margin:0; }
.calc{ background:#2a2a3d; padding:20px; border-radius:20px; width:300px; }
#display{ width:100%; height:60px; font-size:28px; text-align:right; border:none; outline:none; border-radius:10px; padding:10px; box-sizing:border-box; background:#fff; margin-bottom:15px; }
.btns{ display:grid; grid-template-columns:repeat(4,1fr); gap:10px; }
button{ height:55px; font-size:20px; border:none; border-radius:10px; cursor:pointer; background:#3a3a55; color:white; }
.op{ background:#ff9500 !important; }
.eq{ background:#34c759 !important; }
.clear{ background:#ff3b30 !important; }
</style>
</head>
<body>
<div class="calc">
<input id="display" readonly placeholder="0">
<div class="btns">
<button class="clear" onclick="clearAll()">C</button>
<button onclick="delOne()">DEL</button>
<button class="op" onclick="add('/')">÷</button>
<button class="op" onclick="add('*')">×</button>
<button onclick="add('7')">7</button>
<button onclick="add('8')">8</button>
<button onclick="add('9')">9</button>
<button class="op" onclick="add('-')">-</button>
<button onclick="add('4')">4</button>
<button onclick="add('5')">5</button>
<button onclick="add('6')">6</button>
<button class="op" onclick="add('+')">+</button>
<button onclick="add('1')">1</button>
<button onclick="add('2')">2</button>
<button onclick="add('3')">3</button>
<button class="eq" onclick="calculate()">=</button>
<button onclick="add('0')" style="grid-column:span 2">0</button>
<button onclick="add('.')">.</button>
</div>
</div>
<script>
let display = document.getElementById("display");
function add(v){ display.value += v; }
function clearAll(){ display.value = ""; }
function delOne(){ display.value = display.value.slice(0,-1); }
function calculate(){
  try{
    let result = eval(display.value);
    if(!isFinite(result)) display.value = "Cannot divide by zero";
    else display.value = result;
  }catch(e){ display.value = "Invalid"; }
}
</script>
</body>
</html>
```


## OUTPUT

<img width="1188" height="488" alt="Screenshot 2026-11-25 131646" src="https://github.com/user-attachments/assets/b4f9d9c8-6f98-4cf7-abfa-047e17efca68" />


## RESULT

Thus, a JavaScript-based calculator was successfully designed and developed to perform basic arithmetic operations using HTML, CSS, and JavaScript.

