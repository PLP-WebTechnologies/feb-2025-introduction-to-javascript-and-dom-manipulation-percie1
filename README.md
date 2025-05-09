# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨



HTML Document Structure

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dynamic DOM Manipulation</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>DOM Manipulation Example</h1>
  </header>

  <section>
    <p id="text">This text will be changed dynamically.</p>
    <button id="changeTextButton">Change Text</button>
    <button id="addElementButton">Add New Element</button>
    <button id="removeElementButton">Remove Element</button>
  </section>

  <footer>
    <p>Created for learning purposes.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>



 JavaScript File

 // Change the text content of the paragraph when the button is clicked
document.getElementById('changeTextButton').addEventListener('click', function() {
  document.getElementById('text').textContent = "The text has been changed dynamically!";
});

// Add a new element (a paragraph) to the page when the button is clicked
document.getElementById('addElementButton').addEventListener('click', function() {
  // Create a new paragraph element
  const newParagraph = document.createElement('p');
  newParagraph.textContent = "This is a new element added to the page.";
  
  // Append the new paragraph to the section
  document.querySelector('section').appendChild(newParagraph);
});

// Remove the last paragraph element from the section when the button is clicked
document.getElementById('removeElementButton').addEventListener('click', function() {
  const paragraphs = document.querySelectorAll('section p');
  if (paragraphs.length > 0) {
    paragraphs[paragraphs.length - 1].remove();  // Remove the last paragraph
  } else {
    alert("No elements to remove!");
  }
});


CSS

body {
  font-family: Arial, sans-serif;
  margin: 20px;
  background-color: #f4f4f4;
}

header {
  text-align: center;
  margin-bottom: 20px;
}

button {
  padding: 10px;
  margin: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

