<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Happy Valentine Sayang 💖</title>

<style>
body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ff9ecf, #ff4f81);
    font-family: 'Poppins', sans-serif;
    text-align: center;
    overflow-x: hidden;
    color: white;
}

.container {
    margin-top: 60px;
}

h1 {
    font-size: 38px;
}

.foto-box {
    margin-top: 30px;
}

.foto-box img {
    width: 250px;
    height: 250px;
    object-fit: cover;
    border-radius: 20px;
    border: 5px solid white;
    box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    transition: 0.4s;
}

.foto-box img:hover {
    transform: scale(1.05);
}

button {
    background: white;
    color: #ff4f81;
    border: none;
    padding: 15px 35px;
    font-size: 20px;
    border-radius: 50px;
    cursor: pointer;
    margin-top: 25px;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.1);
    background: #ffe6f2;
}

.surat {
    display: none;
    margin-top: 40px;
    font-size: 20px;
    width: 80%;
    margin-left: auto;
    margin-right: auto;
}

.heart {
    position: fixed;
    color: white;
    animation: fall 5s linear infinite;
}

@keyframes fall {
    0% { top: -10%; opacity: 1; }
    100% { top: 110%; opacity: 0; }
}
</style>
</head>

<body>

<div class="container">
    <h1>Happy Valentine Sayangku 💖</h1>

    <!-- TEMPAT FOTO -->
    <div class="foto-box">
        <img src="foto.jpg" alt="Foto Pacarku 💕">
    </div>

    <p>Aku punya sesuatu buat kamu...</p>
    <button onclick="bukaSurat()">💗 Buka Cinta Aku 💗</button>

    <div class="surat" id="surat">
        <p>
        Untuk kamu yang paling aku sayang 💞<br><br>
        Setiap lihat foto kamu, aku selalu senyum sendiri 😍<br>
        Kamu itu hadiah terindah dalam hidup aku 💕<br><br>
        Semoga cinta kita selalu hangat seperti hari ini ❤️<br><br>
        I Love You So Much 💖
        </p>
    </div>
</div>

<script>
function bukaSurat() {
    document.getElementById("surat").style.display = "block";
    buatHati();
}

function buatHati() {
    setInterval(function() {
        let heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = Math.random() * 30 + 20 + "px";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 5000);
    }, 300);
}
</script>

</body>
</html>
