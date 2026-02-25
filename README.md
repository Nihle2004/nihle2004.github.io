# Nihle2004.github.io
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nihle Coşkun | AI Engineer</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Inter',sans-serif;
    background: linear-gradient(-45deg,#fce4ec,#f3e5f5,#e3f2fd,#f8bbd0);
    background-size:400% 400%;
    animation: gradientBG 15s ease infinite;
    color:#333;
    overflow-x:hidden;
}

/* Animated Background */
@keyframes gradientBG{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

/* Floating Light */
.light{
    position:fixed;
    width:300px;
    height:300px;
    background:radial-gradient(circle,#ffffff55,#ffffff00);
    border-radius:50%;
    animation:float 8s infinite alternate ease-in-out;
    z-index:-1;
}

.light1{top:-100px;left:-100px;}
.light2{bottom:-100px;right:-100px;animation-duration:12s;}

@keyframes float{
    from{transform:translateY(0px);}
    to{transform:translateY(60px);}
}

/* Navbar */
nav{
    position:fixed;
    width:100%;
    padding:20px 8%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    backdrop-filter:blur(15px);
    background:rgba(255,255,255,0.3);
    z-index:1000;
}

nav a{
    text-decoration:none;
    margin-left:25px;
    font-weight:500;
    color:#6a1b9a;
}

/* Hero */
header{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:20px;
}

header h1{
    font-size:3.2rem;
    font-weight:700;
    background:linear-gradient(45deg,#c2185b,#6a1b9a);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

header p{
    margin-top:20px;
    max-width:600px;
    font-size:1.1rem;
}

.btn{
    margin-top:35px;
    padding:14px 30px;
    border-radius:30px;
    background:linear-gradient(45deg,#f48fb1,#ce93d8);
    color:white;
    text-decoration:none;
    transition:.3s;
    box-shadow:0 10px 25px rgba(0,0,0,0.1);
}

.btn:hover{
    transform:translateY(-5px);
    box-shadow:0 15px 35px rgba(0,0,0,0.2);
}

/* Sections */
section{
    padding:100px 8%;
}

.section-title{
    font-size:2rem;
    margin-bottom:40px;
    color:#6a1b9a;
}

/* Glass Cards */
.card{
    background:rgba(255,255,255,0.4);
    backdrop-filter:blur(20px);
    padding:25px;
    margin-bottom:25px;
    border-radius:20px;
    box-shadow:0 15px 35px rgba(0,0,0,0.1);
    transform:translateY(50px);
    opacity:0;
    transition:all .8s ease;
}

.card:hover{
    transform:translateY(-8px) scale(1.02);
}

/* Footer */
footer{
    text-align:center;
    padding:30px;
    background:rgba(255,255,255,0.4);
    backdrop-filter:blur(10px);
}

/* Responsive */
@media(max-width:768px){
    header h1{font-size:2.2rem;}
}
</style>
</head>

<body>

<div class="light light1"></div>
<div class="light light2"></div>

<nav>
    <strong>Nihle Coşkun</strong>
    <div>
        <a href="#egitim">Eğitim</a>
        <a href="#deneyim">Deneyim</a>
        <a href="#iletisim">İletişim</a>
    </div>
</nav>

<header>
    <h1>Nihle Coşkun 🤖</h1>
    <p>
        Yapay zeka ve makine öğrenmesi alanında kendini geliştiren,
        teorik bilgisini gerçek projelere dönüştürmeyi hedefleyen
        bir Yapay Zeka Mühendisliği öğrencisi.
    </p>
    <a href="#iletisim" class="btn">Benimle İletişime Geç</a>
</header>

<section id="egitim">
    <div class="section-title">🎓 Eğitim</div>
    <div class="card">Ostim Teknik Üniversitesi – Yapay Zeka Mühendisliği (2023 - Devam)</div>
    <div class="card">Biltek Koleji (2021 - 2023)</div>
    <div class="card">Öncü Koleji (2019 - 2021)</div>
</section>

<section id="deneyim">
    <div class="section-title">💼 Deneyim</div>
    <div class="card">Mavinci Bilişim A.Ş. – Staj (2025)</div>
    <div class="card">Lotus AI A.Ş. – Staj (2025)</div>
</section>

<section id="iletisim">
    <div class="section-title">📫 İletişim</div>
    <div class="card">
        📧 nihlecoskun@gmail.com <br><br>
        📱 +90 553 928 42 55 <br><br>
        📍 Ankara, Türkiye
    </div>
</section>

<footer>
    © 2026 Nihle Coşkun | AI Engineer in Progress ✨
</footer>

<script>
const cards = document.querySelectorAll('.card');

const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
        if(entry.isIntersecting){
            entry.target.style.opacity = 1;
            entry.target.style.transform = "translateY(0)";
        }
    });
},{ threshold:0.2 });

cards.forEach(card=>{
    observer.observe(card);
});
</script>

</body>
</html>
