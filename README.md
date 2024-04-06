{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "01ad7b65",
   "metadata": {},
   "source": [
    "# Introduction to JavaScript in HTML"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1ab606a1",
   "metadata": {},
   "source": [
    "This tutorial introduces how to use JavaScript within HTML to create interactive web pages."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "c3437e14",
   "metadata": {},
   "source": [
    "## Embedding JavaScript in HTML"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f5850598",
   "metadata": {},
   "source": [
    "You can embed JavaScript directly into HTML using the `<script>` tag. The script can be placed in the `<head>` section, the `<body>` section, or both, depending on when you want the script to load."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "395d9df0",
   "metadata": {},
   "outputs": [],
   "source": [
    "from IPython.display import HTML\n",
    "HTML('''\n",
    "<!DOCTYPE html>\n",
    "<html>\n",
    "<head>\n",
    "    <title>Page Title</title>\n",
    "    <script>\n",
    "        function showMessage() {\n",
    "            document.getElementById(\"demo\").innerHTML = \"Hello JavaScript!\";\n",
    "        }\n",
    "    </script>\n",
    "</head>\n",
    "<body>\n",
    "\n",
    "    <h1>My First Heading</h1>\n",
    "    <p>My first paragraph.</p>\n",
    "    <button onclick=\"showMessage()\">Click me</button>\n",
    "    <p id=\"demo\"></p>\n",
    "\n",
    "</body>\n",
    "</html>\n",
    "''')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "54ad70c0",
   "metadata": {},
   "source": [
    "### Explanation for JavaScript Input Example\n",
    "In the JavaScript Input Example, an input field and a button are provided. When the user enters text into the input field and clicks the 'Submit' button, the JavaScript function `showInput()` is called. This function retrieves the value from the input field, using `document.getElementById('myInput').value`, and displays it in the paragraph with `id='inputResult'` by setting its `innerHTML` property."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b0b455c2",
   "metadata": {},
   "source": [
    "## Explanation"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "da8c3234",
   "metadata": {},
   "source": [
    "In the above example, we have a simple HTML document with a JavaScript function defined within the `<script>` tag in the `<head>` section. This function, `showMessage`, changes the text of the paragraph with `id='demo'` when the button is clicked."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b06dc41f",
   "metadata": {},
   "source": [
    "### Explanation for JavaScript Calculation Example\n",
    "In this example, two input fields accept numerical values. Upon clicking the 'Calculate Sum' button, the `calculateSum()` JavaScript function is triggered. This function fetches the values from both input fields, calculates their sum, and displays the result in the paragraph with `id='sumResult'`. The sum is calculated by converting the input values to integers using `parseInt()` and then adding them."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "33d83ed7",
   "metadata": {},
   "source": [
    "This example demonstrates how to add basic interactivity to a web page using JavaScript. By clicking the button, the JavaScript function is called, and the paragraph text changes to 'Hello JavaScript!'."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2c3a4cdb",
   "metadata": {},
   "source": [
    "## JavaScript Input Example"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9c133567",
   "metadata": {},
   "source": [
    "### Explanation for JavaScript Color Slider Example\n",
    "This example features a color input (color slider) that allows users to select a color. When the 'Apply Color' button is clicked, the `changeColor()` function executes. It retrieves the selected color value from the color input and sets it as the background color of the document's body. This is done by modifying the `document.body.style.backgroundColor` property."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "588da66f",
   "metadata": {},
   "outputs": [],
   "source": [
    "from IPython.display import HTML\n",
    "HTML('''\n",
    "<!DOCTYPE html>\n",
    "<html>\n",
    "<body>\n",
    "\n",
    "<h2>JavaScript Input Example</h2>\n",
    "\n",
    "<input type=\"text\" id=\"myInput\" value=\"Type something...\">\n",
    "<button onclick=\"showInput()\">Submit</button>\n",
    "\n",
    "<p id=\"inputResult\">Your input will appear here.</p>\n",
    "\n",
    "<script>\n",
    "function showInput() {\n",
    "  var x = document.getElementById(\"myInput\").value;\n",
    "  document.getElementById(\"inputResult\").innerHTML = \"You wrote: \" + x;\n",
    "}\n",
    "</script>\n",
    "\n",
    "</body>\n",
    "</html>\n",
    "''')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "d59a148d",
   "metadata": {},
   "source": [
    "## JavaScript Calculation Example"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "79031853",
   "metadata": {},
   "outputs": [],
   "source": [
    "from IPython.display import HTML\n",
    "HTML('''\n",
    "<!DOCTYPE html>\n",
    "<html>\n",
    "<body>\n",
    "\n",
    "<h2>JavaScript Calculation Example</h2>\n",
    "\n",
    "<p>Enter numbers to calculate their sum:</p>\n",
    "<input type=\"number\" id=\"num1\" value=\"0\">\n",
    "<input type=\"number\" id=\"num2\" value=\"0\">\n",
    "<button onclick=\"calculateSum()\">Calculate Sum</button>\n",
    "\n",
    "<p id=\"sumResult\">Result will appear here.</p>\n",
    "\n",
    "<script>\n",
    "function calculateSum() {\n",
    "  var num1 = document.getElementById(\"num1\").value;\n",
    "  var num2 = document.getElementById(\"num2\").value;\n",
    "  var sum = parseInt(num1) + parseInt(num2);\n",
    "  document.getElementById(\"sumResult\").innerHTML = \"Sum is: \" + sum;\n",
    "}\n",
    "</script>\n",
    "\n",
    "</body>\n",
    "</html>\n",
    "''')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "d3b9e12f",
   "metadata": {},
   "source": [
    "# Basic Chat Message Input and Response Example"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "d362c2cf",
   "metadata": {},
   "source": [
    "This example demonstrates a basic chat interface where the user can input a message. Upon submitting the message, a predefined response appears."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "373d4044",
   "metadata": {},
   "outputs": [],
   "source": [
    "from IPython.display import HTML\n",
    "HTML('''\n",
    "<!DOCTYPE html>\n",
    "<html>\n",
    "<body>\n",
    "\n",
    "<h2>Basic Chat Interface</h2>\n",
    "\n",
    "<input type=\"text\" id=\"userMessage\" placeholder=\"Type your message...\">\n",
    "<button onclick=\"sendMessage()\">Send</button>\n",
    "\n",
    "<div id=\"chat\">\n",
    "    <p><b>You:</b> <span id=\"userMsgDisplay\"></span></p>\n",
    "    <p><b>Bot:</b> <span id=\"botResponse\">I'm here to help!</span></p>\n",
    "</div>\n",
    "\n",
    "<script>\n",
    "function sendMessage() {\n",
    "  var userMessage = document.getElementById(\"userMessage\").value;\n",
    "  document.getElementById(\"userMsgDisplay\").innerHTML = userMessage;\n",
    "  // For simplicity, bot response is static\n",
    "  document.getElementById(\"botResponse\").innerHTML = \"Thanks for your message!\";\n",
    "}\n",
    "</script>\n",
    "\n",
    "</body>\n",
    "</html>\n",
    "''')"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "ef53b422",
   "metadata": {},
   "source": [
    "### Explanation for Basic Chat Message Input and Response\n",
    "In the Basic Chat Interface example, an input field allows the user to type a message. When the 'Send' button is clicked, the `sendMessage()` JavaScript function is executed. This function captures the user's message from the input field and displays it under 'You:'. It then generates a predefined response under 'Bot:'. This simple interaction simulates a basic chat interface."
   ]
  }
 ],
 "metadata": {},
 "nbformat": 4,
 "nbformat_minor": 5
}
