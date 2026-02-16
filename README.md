<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>GALIAN 2026</title>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #000;
}

/* ================= NAVIGATION ================= */
nav {
    position: relative;
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 36px;
    font-weight: bold;
    letter-spacing: 4px;
    color: white;
    overflow: hidden;
}

/* Blurred + Dark CORE Background */
nav::before {
    content: "";
    position: absolute;
    inset: 0;
    background: url("1771214576903.jpg") no-repeat center center;
    background-size: cover;
    filter: blur(6px) brightness(40%);
    z-index: -1;
}

/* ================= CONTAINER ================= */
.container {
    width: 100%;
    margin: 0;
    padding: 0;
}

/* ================= GALLERY SECTION ================= */
.gallery {
    min-height: 100vh;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
    align-items: center;
    background: url("1771214562396.jpg") no-repeat center center;
    background-size: cover;
    padding: 60px 20px;
    position: relative;
}

/* Dark Overlay */
.gallery::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(to bottom, rgba(0,0,0,0.8), rgba(0,0,0,0.7));
    z-index: 0;
}

.image-box {
    width: 300px;
    text-align: center;
    cursor: pointer;
    position: relative;
    z-index: 1;
    color: white;
}

.image-box img {
    width: 100%;
    border-radius: 10px;
    transition: transform 0.3s;
}

.image-box img:hover {
    transform: scale(1.05);
}

.caption {
    display: none;
    margin-top: 10px;
    font-size: 14px;
    font-style: italic;
    background: rgba(255,255,255,0.95);
    color: #333;
    padding: 12px;
    border-radius: 8px;
    line-height: 1.6;
}

/* ================= PARAGRAPH ================= */
p {
    text-align: justify;
    font-size: 18px;
    line-height: 1.7;
    padding: 40px 10%;
    background: #111;
    color: white;
    margin: 0;
}

/* ================= FOOTER ================= */
footer {
    text-align: center;
    padding: 20px;
    background-color: #000;
    color: white;
}
</style>
</head>

<body>

<nav>
    GALIAN 2026
</nav>

<div class="container">

    <div class="gallery">

        <div class="image-box" onclick="toggleCaption('cap1')">
            <img src="IMG_20260215_112547_876.jpg" alt="Dance Performance">
            <div class="caption" id="cap1">
                This performance captures the energy and passion of students as they move 
                in perfect synchronization on stage. Their confident gestures and expressive 
                movements reflect months of dedication and teamwork. The applause and excitement 
                from the audience made this one of the most unforgettable highlights of GALIAN 2026.
            </div>
        </div>

        <div class="image-box" onclick="toggleCaption('cap2')">
            <img src="1771125539772.jpg" alt="School Performance">
            <div class="caption" id="cap2">
                This stage presentation showcases unity, discipline, and artistic creativity. 
                The vibrant lighting and enthusiastic crowd created a powerful atmosphere 
                that truly represented collaboration and celebration during GALIAN 2026.
            </div>
        </div>

        <div class="image-box" onclick="toggleCaption('cap3')">
            <img src="1771125667469.jpg" alt="MoBot Invention">
            <div class="caption" id="cap3">
                The Mobile Robot (MoBot) invention highlights the brilliance and innovation 
                of students in technology. This project demonstrates programming skills, 
                logical thinking, and technical expertise — proving that GALIAN 2026 celebrates 
                both creativity and academic excellence.
            </div>
        </div>

    </div>

    <p>
        GALIAN 2026 is a remarkable celebration of talent, innovation, and youthful ambition. 
        It brings together artistic expression and technological brilliance in one inspiring event. 
        From breathtaking performances to impressive inventions, students demonstrate excellence, 
        teamwork, and determination. The event reflects strong community spirit and commitment 
        to growth and creativity.
    </p>

</div>

<footer>
    Credits: Core Gateway College Inc. © 2026
</footer>

<script>
function toggleCaption(id) {
    var captions = document.querySelectorAll(".caption");

    captions.forEach(function(cap) {
        if (cap.id !== id) {
            cap.style.display = "none";
        }
    });

    var selected = document.getElementById(id);

    if (selected.style.display === "block") {
        selected.style.display = "none";
    } else {
        selected.style.display = "block";
    }
}
</script>

</body>
</html>
