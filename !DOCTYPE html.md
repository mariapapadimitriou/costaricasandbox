<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <title>Costa Rica Travel Journal</title>  
  <style>  
    body {  
      margin: 0;  
      font-family: 'Georgia', serif;  
      background: #f5efe6;  
      color: #2b2b2b;  
    }  
  
    header {  
      text-align: center;  
      padding: 2rem 1rem;  
      background: linear-gradient(to right, #ff9966, #ff5e62);  
      color: white;  
      font-size: 2rem;  
      letter-spacing: 2px;  
    }  
  
    .container {  
      max-width: 1000px;  
      margin: auto;  
      padding: 1rem;  
    }  
  
    .location {  
      margin-bottom: 3rem;  
      background: white;  
      border-radius: 16px;  
      box-shadow: 0 8px 20px rgba(0,0,0,0.08);  
      padding: 1rem;  
    }  
  
    .location h2 {  
      margin-top: 0;  
      font-size: 1.5rem;  
    }  
  
    .carousel {  
      display: flex;  
      overflow-x: auto;  
      gap: 10px;  
      padding-bottom: 10px;  
    }  
  
    .carousel img {  
      height: 250px;  
      border-radius: 12px;  
      flex-shrink: 0;  
      object-fit: cover;  
    }  
  
    footer {  
      text-align: center;  
      padding: 2rem;  
      font-size: 0.9rem;  
      opacity: 0.7;  
    }  
  </style>  
</head>  
<body>  
  
<header>  
  Costa Rica Travel Journal ✈️🌴  
</header>  
  
<div class="container" id="gallery"></div>  
  
<footer>  
  Tru Travels Costa Rica 🇨🇷  
</footer>  
  
<script>  
  const locations = [  
    "santa-teresa",  
    "la-fortuna",  
    "monteverde"  
  ];  
  
  const gallery = document.getElementById("gallery");  
  
  locations.forEach(location => {  
    const section = document.createElement("div");  
    section.className = "location";  
  
    const title = document.createElement("h2");  
    title.innerText = location.replace("-", " ").toUpperCase();  
  
    const carousel = document.createElement("div");  
    carousel.className = "carousel";  
  
    // Automatically try loading images 1–20  
    for (let i = 1; i <= 20; i++) {  
      const img = document.createElement("img");  
      img.src = `images/${location}/${i}.jpg`;  
  
      img.onerror = () => img.remove();  
  
      carousel.appendChild(img);  
    }  
  
    section.appendChild(title);  
    section.appendChild(carousel);  
    gallery.appendChild(section);  
  });  
</script>  
  
</body>  
</html>  
