<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nuestro pequeño universo 💜</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500;600&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    color: white;
    background: #080719;
    overflow-x: hidden;
}

/* FONDO GALÁCTICO */

.space {
    position: fixed;
    inset: 0;
    z-index: -2;
    background:
      radial-gradient(ellipse at 20% 30%, #542b85 0%, transparent 40%),
      radial-gradient(ellipse at 80% 70%, #38216c 0%, transparent 40%),
      linear-gradient(135deg, #080719, #17102e, #09081b);
}

.star {
    position: fixed;
    background: white;
    border-radius: 50%;
    animation: twinkle 2s infinite alternate;
    z-index: -1;
}

@keyframes twinkle {
    from { opacity: .2; transform: scale(.7); }
    to { opacity: 1; transform: scale(1.4); }
}

.shooting-star {
    position: fixed;
    width: 120px;
    height: 2px;
    background: linear-gradient(90deg, white, transparent);
    transform: rotate(-35deg);
    animation: shooting 4s linear infinite;
    opacity: 0;
    z-index: -1;
}

@keyframes shooting {
    0% { transform: translate(0,0) rotate(-35deg); opacity: 0; }
    10% { opacity: 1; }
    30% { transform: translate(-300px,300px) rotate(-35deg); opacity: 0; }
    100% { opacity: 0; }
}

/* SECCIONES */

section {
    min-height: 100vh;
    padding: 90px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.small {
    letter-spacing: 5px;
    color: #d8b8ff;
    font-size: 12px;
}

h1, h2 {
    font-weight: 400;
}

h1 {
    font-family: 'Great Vibes', cursive;
    font-size: clamp(65px, 12vw, 105px);
    color: #f5d8ff;
    margin: 20px 0;
    text-shadow: 0 0 25px #b46bff;
}

h2 {
    font-family: 'Great Vibes', cursive;
    font-size: 55px;
    color: #eac5ff;
    margin-bottom: 25px;
}

p {
    line-height: 1.9;
    color: #e8dff5;
    max-width: 650px;
}

button {
    padding: 14px 30px;
    border: 1px solid #d8b5ff;
    border-radius: 30px;
    background: #a36bd6;
    color: white;
    font-family: inherit;
    font-size: 14px;
    cursor: pointer;
    margin-top: 30px;
    transition: .3s;
}

button:hover {
    background: #c28aff;
    box-shadow: 0 0 25px #b46bff;
    transform: scale(1.06);
}

.moon {
    font-size: 75px;
    margin-bottom: 20px;
    filter: drop-shadow(0 0 25px #d7aaff);
    animation: moonFloat 4s ease-in-out infinite;
}

@keyframes moonFloat {
    50% { transform: translateY(-15px); }
}

/* CARTA */

.letter {
    display: none;
    background: rgba(255,255,255,.09);
    border: 1px solid rgba(220,180,255,.4);
    border-radius: 25px;
    padding: 35px;
    max-width: 650px;
    margin-top: 35px;
    backdrop-filter: blur(12px);
    animation: appear 1s ease;
}

.letter.show {
    display: block;
}

@keyframes appear {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

/* GALERÍA */

.gallery {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
    max-width: 850px;
    width: 100%;
    margin-top: 30px;
}

.photo {
    height: 260px;
    width: 100%;
    object-fit: cover;
    border-radius: 20px;
    border: 2px solid #bd91ef;
    box-shadow: 0 0 20px rgba(181,120,255,.2);
    transition: .4s;
}

.photo:hover {
    transform: scale(1.04);
    box-shadow: 0 0 30px #a36bd6;
}

/* MOTIVOS */

.reasons {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
    max-width: 750px;
    margin-top: 35px;
}

.reason {
    background: rgba(164,105,218,.15);
    border: 1px solid #9d72c7;
    border-radius: 20px;
    padding: 25px;
    transition: .3s;
}

.reason:hover {
    background: rgba(164,105,218,.35);
    transform: translateY(-7px);
}

.reason span {
    font-size: 35px;
    display: block;
    margin-bottom: 12px;
}

/* SORPRESA FINAL */

.final-heart {
    font-size: 80px;
    animation: heartbeat 1.5s infinite;
}

@keyframes heartbeat {
    50% { transform: scale(1.2); }
}

/* CORAZONES */

.floating {
    position: fixed;
    bottom: -40px;
    animation: float 8s linear forwards;
    pointer-events: none;
    z-index: 5;
}

@keyframes float {
    to {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
    }
}

/* RESPONSIVE */

@media(max-width:600px) {
    .gallery, .reasons {
        grid-template-columns: 1fr;
    }

    .photo {
        height: 300px;
    }

    section {
        padding: 70px 20px;
    }

    .letter {
        padding: 22px;
    }
}
</style>
</head>

<body>

<div class="space"></div>

<section id="inicio">
    <div class="moon">🌙</div>
    <p class="small">UNA SORPRESA BAJO LAS ESTRELLAS</p>

    <h1>Jesús...</h1>

    <p>
        Entre millones de estrellas, hay una persona
        que hace que mi universo sea mucho más bonito.
    </p>

    <button onclick="goTo('carta')">
        Descubre tu sorpresa ❤️
    </button>
</section>

<section id="carta">
    <p class="small">UN MENSAJE DESDE MI CORAZÓN</p>
    <h2>Una carta para ti</h2>

    <p>
        Hay cosas que no siempre se pueden explicar
        con palabras, pero hoy quiero intentarlo.
    </p>

    <button onclick="openLetter()">
        Abrir mi carta 💌
    </button>

    <div class="letter" id="loveLetter">
        <h2>Mi querido amor ❤️</h2>

        <p>
            Quiero recordarte lo especial que eres para mí.
            Desde que formas parte de mi vida, has llenado
            muchos de mis días de momentos bonitos,
            sonrisas y recuerdos que guardo con muchísimo cariño.
        </p>

        <br>

        <p>
            Me encanta compartir momentos contigo,
            descubrir nuevas experiencias y seguir creando
            recuerdos a tu lado.
        </p>

        <br>

        <p>
            Si pudiera pedir un deseo a las estrellas,
            sería que nunca nos falten motivos para sonreír,
            apoyarnos y seguir construyendo nuestra historia.
        </p>

        <br>

        <h2>Te amo muchísimo ❤️</h2>

        <p style="text-align:right">
            Con amor,<br>
            Tu mujer ❤️.
        </p>
    </div>
</section>

<section id="fotos">
    <p class="small">NUESTROS RECUERDOS FAVORITOS</p>
    <h2>Un universo de momentos 📸</h2>
    <p>
        Cada fotografía guarda un pedacito de nuestra historia.
        Y cada recuerdo tiene un lugar especial en mi corazón.
    </p>

    <div class="gallery">
        <img class="photo" src="WhatsApp Image 2026-11-16 at 11.09.47 PM (1).jpeg" alt="Nuestro recuerdo 1">
        <img class="photo" src="WhatsApp Image 2026-11-16 at 11.09.47 PM.jpeg" alt="Nuestro recuerdo 2">
        <img class="photo" src="WhatsApp Image 2026-11-16 at 11.09.48 PM (1).jpeg" alt="Nuestro recuerdo 3">
        <img class="photo" src="WhatsApp Image 2026-11-16 at 11.09.48 PM.jpeg" alt="Nuestro recuerdo 4">
    </div>
</section>

<section id="razones">
    <p class="small">PEQUEÑOS DETALLES, GRANDES SENTIMIENTOS</p>
    <h2>¿Por qué eres especial?</h2>

    <div class="reasons">
        <div class="reason">
            <span>❤️</span>
            <p>Por la felicidad que compartimos.</p>
        </div>

        <div class="reason">
            <span>✨</span>
            <p>Por cada recuerdo que construimos.</p>
        </div>

        <div class="reason">
            <span>🌙</span>
            <p>Por tu compañía en los días especiales.</p>
        </div>

        <div class="reason">
            <span>❤️</span>
            <p>Por ser alguien tan importante en mi vida.</p>
        </div>
    </div>
</section>

<section id="final">
    <div class="final-heart">❤️</div>

    <p class="small">Y AHORA, MI ÚLTIMA SORPRESA...</p>

    <h2>Jesús, una pregunta...</h2>

    <p>
        Si nuestra historia fuera una galaxia,
        ¿me acompañarías a descubrir cada una de sus estrellas?
    </p>

    <button onclick="finalSurprise()">
        ¡Claro que sí! ❤️
    </button>

    <div class="letter" id="finalMessage">
        <h2>¡Entonces sigamos creando recuerdos! 🌌</h2>

        <p>
            Porque mi lugar favorito no está en ningún planeta,
            sino en todos esos momentos bonitos que compartimos.
        </p>

        <br>

        <h1>Te amo, Jesús ❤️</h1>

        <p>Con mucho amor, Tu mujer ❤️.</p>
    </div>
</section>

<button id="musicButton"
style="position:fixed;bottom:15px;right:15px;z-index:10;margin:0">
    ♫ Música
</button>

<audio id="music" loop>
    <source src="Ladyfingers - Mariachi Nueva Luna.mp3" type="audio/mpeg">
</audio>

<script>

// CREAR ESTRELLAS
for (let i = 0; i < 120; i++) {
    const star = document.createElement("div");
    star.className = "star";

    star.style.left = Math.random() * 100 + "vw";
    star.style.top = Math.random() * 100 + "vh";
    star.style.width = (Math.random() * 3 + 1) + "px";
    star.style.height = star.style.width;
    star.style.animationDelay = Math.random() * 3 + "s";

    document.body.appendChild(star);
}

// ESTRELLAS FUGACES
setInterval(() => {
    const shooting = document.createElement("div");
    shooting.className = "shooting-star";

    shooting.style.top = Math.random() * 60 + "vh";
    shooting.style.left = Math.random() * 100 + "vw";

    document.body.appendChild(shooting);

    setTimeout(() => shooting.remove(), 4000);
}, 3500);

// NAVEGACIÓN
function goTo(id) {
    document.getElementById(id).scrollIntoView({
        behavior: "smooth"
    });
}

// ABRIR CARTA
function openLetter() {
    document.getElementById("loveLetter")
        .classList.add("show");
}

// CORAZONES FLOTANTES
function createHeart() {
    const heart = document.createElement("div");

    heart.className = "floating";
    heart.textContent = "💜";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (15 + Math.random() * 20) + "px";

    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 8000);
}

setInterval(createHeart, 900);

// SORPRESA FINAL
function finalSurprise() {
    document.getElementById("finalMessage")
        .classList.add("show");

    for (let i = 0; i < 30; i++) {
        setTimeout(createHeart, i * 100);
    }
}

// MÚSICA
const music = document.getElementById("music");
const musicButton = document.getElementById("musicButton");

musicButton.addEventListener("click", async () => {
    try {
        if (music.paused) {
            await music.play();
            musicButton.textContent = "♫ Pausar música";
        } else {
            music.pause();
            musicButton.textContent = "♫ Música";
        }
    } catch (error) {
        alert("Coloca tu archivo musica.mp3 en la carpeta de la página.");
    }
});

</script>

</body>
</html>
