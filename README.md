# week-5-assignment-web-development
📂 Project Folder Structure
📂 JavaScript-DOM-Project
   📄 index.html
   📄 script.js
   📄 styles.css (optional)

 index.html
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <h1 id="main-title">Welcome to JavaScript DOM Manipulation</h1>
    <p id="info-text">Click the button to change this text.</p>

    <button onclick="changeText()">Change Text</button>
    <button onclick="changeColor()">Change Color</button>
    <button onclick="addItem()">Add Item</button>
    <button onclick="removeItem()">Remove Item</button>

    <ul id="item-list">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <script src="script.js"></script>
</body>
</html>


script.js
// Function to change the text content of a paragraph
function changeText() {
    document.getElementById("info-text").innerText = "The text has been changed!";
}

// Function to change the color of the heading
function changeColor() {
    document.getElementById("main-title").style.color = "blue";
}

// Function to add a new item to the list
function addItem() {
    let ul = document.getElementById("item-list");
    let li = document.createElement("li");
    li.innerText = "New Item";
    ul.appendChild(li);
}

// Function to remove the last item from the list
function removeItem() {
    let ul = document.getElementById("item-list");
    if (ul.children.length > 0) {
        ul.removeChild(ul.lastElementChild);
    } else {
        alert("No more items to remove!");
    }
}
 styles.css

 body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 20px;
}

button {
    margin: 5px;
    padding: 10px;
    cursor: pointer;
}
