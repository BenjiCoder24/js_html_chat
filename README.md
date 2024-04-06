# Introduction to JavaScript in HTML

This tutorial introduces how to use JavaScript within HTML to create interactive web pages.

## Embedding JavaScript in HTML

You can embed JavaScript directly into HTML using the `<script>` tag. The script can be placed in the `<head>` section, the `<body>` section, or both, depending on when you want the script to load.

```html
from IPython.display import HTML
HTML('''
<!DOCTYPE html>
<html>
<head>
    <title>Page Title</title>
    <script>
        function showMessage() {
            document.getElementById("demo").innerHTML = "Hello JavaScript!";
        }
    </script>
</head>
<body>

    <h1>My First Heading</h1>
    <p>My first paragraph.</p>
    <button onclick="showMessage()">Click me</button>
    <p id="demo"></p>

</body>
</html>
''')
```

### Explanation for JavaScript Input Example
In the JavaScript Input Example, an input field and a button are provided. When the user enters text into the input field and clicks the 'Submit' button, the JavaScript function `showInput()` is called. This function retrieves the value from the input field, using `document.getElementById('myInput').value`, and displays it in the paragraph with `id='inputResult'` by setting its `innerHTML` property.

## Explanation

In the above example, we have a simple HTML document with a JavaScript function defined within the `<script>` tag in the `<head>` section. This function, `showMessage`, changes the text of the paragraph with `id='demo'` when the button is clicked.

### Explanation for JavaScript Calculation Example
In this example, two input fields accept numerical values. Upon clicking the 'Calculate Sum' button, the `calculateSum()` JavaScript function is triggered. This function fetches the values from both input fields, calculates their sum, and displays the result in the paragraph with `id='sumResult'`. The sum is calculated by converting the input values to integers using `parseInt()` and then adding them.

This example demonstrates how to add basic interactivity to a web page using JavaScript. By clicking the button, the JavaScript function is called, and the paragraph text changes to 'Hello JavaScript!'.

## JavaScript Input Example

### Explanation for JavaScript Color Slider Example
This example features a color input (color slider) that allows users to select a color. When the 'Apply Color' button is clicked, the `changeColor()` function executes. It retrieves the selected color value from the color input and sets it as the background color of the document's body. This is done by modifying the `document.body.style.backgroundColor` property.

```html
from IPython.display import HTML
HTML('''
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Input Example</h2>

<input type="text" id="myInput" value="Type something...">
<button onclick="showInput()">Submit</button>

<p id="inputResult">Your input will appear here.</p>

<script>
function showInput() {
  var x = document.getElementById("myInput").value;
  document.getElementById("inputResult").innerHTML = "You wrote: " + x;
}
</script>

</body>
</html>
''')
```

## JavaScript Calculation Example

```html
from IPython.display import HTML
HTML('''
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Calculation Example</h2>

<p>Enter numbers to calculate their sum:</p>
<input type="number" id="num1" value="0">
<input type="number" id="num2" value="0">
<button onclick="calculateSum()">Calculate Sum</button>

<p id="sumResult">Result will appear here.</p>

<script>
function calculateSum() {
  var num1 = document.getElementById("num1").value;
  var num2 = document.getElementById("num2").value;
  var sum = parseInt(num1) + parseInt(num2);
  document.getElementById("sumResult").innerHTML = "Sum is: " + sum;
}
</script>

</body>
</html>
''')
```

# Basic Chat Message Input and Response Example

This example demonstrates a basic chat interface where the user can input a message. Upon submitting the message, a predefined response appears.

```html
from IPython.display import HTML
HTML('''
<!DOCTYPE html>
<html>
<body>

<h2>Basic Chat Interface</h2>

<input type="text" id="userMessage" placeholder="Type your message...">
<button onclick="sendMessage()">Send</button>

<div id="chat">
    <p><b>You:</b> <span id="userMsgDisplay"></span></p>
    <p><b>Bot:</b> <span id="botResponse">I'm here to help!</span></p>
</div>

<script>
function sendMessage() {
  var userMessage = document.getElementById("userMessage").value;
  document.getElementById("userMsgDisplay").innerHTML = userMessage;
  // For simplicity, bot response is static
  document.getElementById("botResponse").innerHTML = "Thanks for your message!";
}
</script>

</body>
</html>
''')
```

### Explanation for Basic Chat Message Input and Response
In the Basic Chat Interface example, an input field allows the user to type a message. When the 'Send' button is clicked, the `sendMessage()` JavaScript function is executed. This function captures the user's message from the input field and displays it under 'You:'. It then generates a predefined response under 'Bot:'. This simple interaction simulates a basic chat interface.
