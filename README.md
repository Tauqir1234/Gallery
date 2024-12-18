# Ex.08 Design of Interactive Image Gallery
# Date:18/11/2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            background-color: #f4f4f4;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 10px;
            padding: 20px;
            width: 100%;
            max-width: 1200px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.2s ease-in-out;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .lightbox.active {
            display: flex;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 30px;
            color: white;
            text-decoration: none;
            background: transparent;
            border: none;
            cursor: pointer;
        }

        .close:hover {
            color: #f00;
        }
    </style>
</head>
<body>
    <h1>Interactive Image Gallery</h1>
    <div class="gallery">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 083149.png" alt="Image 1" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 083149.png">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 083611.png" alt="Image 2" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 083611.png">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 082633.png" alt="Image 3" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 082633.png">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 082509.png" alt="Image 4" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 082509.png">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-12 124713.png" alt="Image 5" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-12 124713.png">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-13 131701.png" alt="Image 6" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-13 131701.png">
        <img src="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 083027.png" alt="Image 7" data-full="c:\Users\admin\Pictures\Screenshots\Screenshot 2024-12-17 083027.png">
    </div>

    <div id="lightbox" class="lightbox">
        <img id="lightbox-img" src="" alt="Expanded Image">
        <button class="close" id="lightbox-close">&times;</button>
    </div>

    <script>
        const galleryImages = document.querySelectorAll('.gallery img');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = document.getElementById('lightbox-img');
        const lightboxClose = document.getElementById('lightbox-close');

        galleryImages.forEach(image => {
            image.addEventListener('click', () => {
                lightboxImg.src = image.getAttribute('data-full');
                lightbox.classList.add('active');
            });
        });

        lightboxClose.addEventListener('click', () => {
            lightbox.classList.remove('active');
        });

        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) {
                lightbox.classList.remove('active');
            }
        });
    </script>
</body>
</html>
```
# OUTPUT:

![Screenshot 2024-12-18 103530](https://github.com/user-attachments/assets/7c808c47-5962-4581-896c-2bf19d610c06)
![Screenshot 2024-12-18 103909](https://github.com/user-attachments/assets/1d7c2160-fd20-4f39-ac64-7672c0d6a279)
![Screenshot 2024-12-18 103923](https://github.com/user-attachments/assets/763b6899-a423-4b8b-8129-fc7e745d030d)


# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
