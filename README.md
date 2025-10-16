# Ex.08 Design of Interactive Image Gallery
## Date:16-10-2025

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
```

{%load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Interactive Photo Gallery</title>
  <style>
    .gallery img {
      width: 200px;
      margin: 10px;
      cursor: pointer;
      transition: transform 0.3s;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }
    .gallery img:hover {
      transform: scale(1.1);
    }
    #lightbox {
      position: fixed;
      top:0; left:0; right:0; bottom:0;
      background: rgba(0,0,0,0.8);
      display:none;
      justify-content:center;
      align-items:center;
      z-index: 999;
    }
    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 15px white;
    }
  </style>
</head>
<body>

<h1>Interactive Photo Gallery</h1>
<div class="gallery">
  {% for img in images %}
    <img src="{% static 'gallery/images/'|add:img %}" alt="Photo" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<div id="lightbox" onclick="closeLightbox()">
  <img id="lightbox-img" src="" alt="Large view">
</div>

<script>
  function openLightbox(src) {
    document.getElementById('lightbox-img').src = src;
    document.getElementById('lightbox').style.display = 'flex';
  }
  function closeLightbox() {
    document.getElementById('lightbox').style.display = 'none';
  }
</script>

</body>
</html>

```

## OUTPUT:
<img width="1425" height="697" alt="Screenshot 2025-10-16 112954" src="https://github.com/user-attachments/assets/c6406aef-0af1-409c-981a-ea18c45c4d19" />

<img width="735" height="895" alt="Screenshot 2025-10-16 113040" src="https://github.com/user-attachments/assets/d2670630-33a4-452f-a855-9fa124c895c0" />

<img width="1634" height="844" alt="Screenshot 2025-10-16 113108" src="https://github.com/user-attachments/assets/041af24b-3872-40c2-929b-199bbfd53456" />



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
