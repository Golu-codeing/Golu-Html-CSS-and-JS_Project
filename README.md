# Golu-Html-CSS-and-JS_Project
This is Advance Project end-to-end project

**#HTML Codeing**
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Animations</title>
    <link rel="stylesheet" href="nav.css">
</head>
<body>
    <div class="Welcome">Welcome to my Website</div>
  
    <div class="animated-box"><a href="file:///C:/Users/DELL/Documents/demo.html">Click me</a></div>

   
    <script src="nav.js"></script>
</body>
</html>


**#CSS Codeing**
body{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background: linear-gradient(to right, #ff416c, #bfff2b);
    font-family: Arial, sans-serif;
}

.Welcome{
    font-size: 2rem;
    color: rgb(172, 24, 209);
    animation: fadeIn 5s ease-in-out; 
    font-size: 50px;
    display: grid;
}

.animated-box {
    width: 150px;
    height: 150px;
    background-color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 20px;
    font-size: 18px;
    font-weight: bold;
    transition: all 0.3s ease-in-out;
}

.animated-box:hover {
    transform: scale(1.2) rotate(10deg);
    background-color: #f0db4f;
    box-shadow: 0px 5px 15px rgba(0,0,0,0.3);
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

**#Js Codeing**
document.getElementById("animate-btn").addEventListener("click", () => {
    gsap.to("animated-box", {
        duration: 1.5,
        x: 200,
        rotation: 360,
        backgroundColor: "#00ff99",
        scale: 1.5,
        ease: "elastic.out(1, 0.3)"
    });
});

