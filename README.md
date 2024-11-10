# Ex-7: Interactive Image Gallery
## Date:10-11-2024

## AIM:
To design a book front cover page using HTML and CSS.

## DESIGN STEPS:

### Step 1: 
Create a Django Admin project.

### Step 2:
Create an app in the Django interface.

### Step 3:
Create a folder named 'static' in the app folder.

### Step 4:
Create a new HTML file in the static folder.

### Step 5:
Write the HTML code with relevant CSS properties.

### Step 6:
Choose the appropriate style and color scheme.

### Step 7:
Insert the images in their appropriate places.

### Step 8:
Publish the website in the LocalHost.

## PROGRAM:
index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Accessible Photo Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body onload="addTabIndex()">
    <center>
    <h1>My Accessible Photo Gallery</h1>
</center>
    <div id="image" class="image-container" tabindex="0">
        Hover over an image below to display here.
    </div>
    <div class="gallery">
        <figure tabindex="0">
            <img src="https://i.pinimg.com/564x/a4/8f/52/a48f52b5bddc53c8d6f9bb7e55fbfac9.jpg" alt="A beautiful sunrise" onmouseover="upDate(this)" onmouseout="undo()" onfocus="upDate(this)" onblur="undo()">
            <figcaption>Sunrise</figcaption>
        </figure>
        <figure tabindex="0">
            <img src="https://i.pinimg.com/564x/95/09/ab/9509ab59dd06f71c70744a71f7221e3b.jpg" alt="A serene beach" onmouseover="upDate(this)" onmouseout="undo()" onfocus="upDate(this)" onblur="undo()">
            <figcaption>Beach</figcaption>
        </figure>
        <figure tabindex="0">
            <img src="https://i.pinimg.com/736x/08/d9/fa/08d9fa64d718d65abd04ba79b66a43a6.jpg" alt="A snowy mountain" onmouseover="upDate(this)" onmouseout="undo()" onfocus="upDate(this)" onblur="undo()">
            <figcaption>Mountain</figcaption>
        </figure>
        <figure tabindex="0">
            <img src="https://i.pinimg.com/736x/7d/14/6b/7d146b82e8f443930a69663e87521d93.jpg" alt="A vibrant cityscape" onmouseover="upDate(this)" onmouseout="undo()" onfocus="upDate(this)" onblur="undo()">
            <figcaption>Cityscape</figcaption>
        </figure>
        <figure tabindex="0">
            <img src="https://i.pinimg.com/564x/a6/b2/9f/a6b29fd36ddd0f2342ac48fca88f8559.jpg" alt="A lush forest" onmouseover="upDate(this)" onmouseout="undo()" onfocus="upDate(this)" onblur="undo()">
            <figcaption>Forest</figcaption>
        </figure>
        <figure tabindex="0">
            <img src="https://i.pinimg.com/564x/1d/83/af/1d83af72cd5e58cf6711c68be768def5.jpg" alt="A tranquil lake" onmouseover="upDate(this)" onmouseout="undo()" onfocus="upDate(this)" onblur="undo()">
            <figcaption>Lake</figcaption>
        </figure>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
style.css

```
body {
    font-family: Arial, sans-serif;
}

.image-container {
    width: 400px;
    height: 400px;
    background-color: #f0f0f0;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px auto;
    border: 1px solid #ccc;
    text-align: center;
}

.gallery {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.gallery figure {
    margin: 10px;
}

.gallery img {
    width: 100px;
    height: 100px;
    cursor: pointer;
    border: 2px solid transparent;
}

.gallery figure:focus img {
    border: 2px solid #007BFF; /* Highlight border on focus */
}
```
script.js
```
function upDate(previewPic) {
    console.log("Mouse over:", previewPic.alt);
    document.getElementById("image").innerHTML = previewPic.alt;
    document.getElementById("image").style.backgroundImage = `url('${previewPic.src}')`;
}

function undo() {
    document.getElementById("image").innerHTML = "Hover over an image below to display here.";
    document.getElementById("image").style.backgroundImage = "url('')";
}

function addTabIndex() {
    const figures = document.querySelectorAll('.gallery figure');
    figures.forEach((figure, index) => {
        figure.setAttribute('tabindex', '0');
        console.log(`Tabindex added to figure ${index + 1}`);
    });
}
```

## OUTPUT:
![alt text](<Screenshot (195).png>)

![alt text](<Screenshot (196).png>)
## RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
