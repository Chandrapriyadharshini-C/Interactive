# Ex.08 Design of Interactive Image Gallery
## Date: 07/05/2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
gallery.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body bgcolor="lightpink">
    <header>
        <h1 align="center">GALLERY</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gallery 1.jpeg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 3.jpg"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 6.webp" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 2.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 4.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 5.jpg" >
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>
```
style.css
```
img{
    width : 160px;
    height: 210px;
    object-fit: cover;
    display: flex;
    border-radius: 10px;
}
.gallery{
    display: flex;
    justify-content: center;
    gap: 40px;
    margin-top: 20px;
}
.modal{
    margin-top: 50px;
    margin-left: 45%;
}
```
style.js
```
function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
```
## OUTPUT:
![Screenshot 2025-05-07 111113](https://github.com/user-attachments/assets/d2011359-93f0-435c-97af-dcd96a4f2ca8)
![Screenshot 2025-05-07 111128](https://github.com/user-attachments/assets/3daf7d72-b2ba-45e1-a22e-2a5d7d901225)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
