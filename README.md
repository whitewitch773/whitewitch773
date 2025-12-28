<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Для дорогой Настены ❤️</title>

<style>
body {
    margin:0;
    background: radial-gradient(circle at top, #120022, #000);
    color: #fff;
    font-family: 'Segoe UI', sans-serif;
    overflow:hidden;
    text-align:center;
}

h1 {
    font-size: 60px;
    margin-top: 80px;
    text-shadow: 0 0 20px #ff00ff;
}

.photo{
    width:260px;
    border-radius:20px;
    margin-top:25px;
    box-shadow:0 0 30px #ff00ff;
    animation: glow 3s infinite alternate;
}
@keyframes glow{
    from{box-shadow:0 0 20px #ff00ff;}
    to{box-shadow:0 0 55px #ff66ff;}
}

p {
    font-size: 24px;
    width: 80%;
    margin: 35px auto;
    line-height: 1.6;
}

button {
    padding: 15px 40px;
    font-size: 22px;
    border:none;
    border-radius: 40px;
    background: linear-gradient(45deg,#ff0080,#ff8c00);
    color:#fff;
    cursor:pointer;
    box-shadow:0 0 30px #ff0080;
}

button:hover {transform: scale(1.1);}

#magic {
    display:none;
    font-size: 32px;
    margin-top: 50px;
    color:#ffb3ff;
    text-shadow:0 0 25px #ff00ff;
}

/* снежок */
.snow {
    position: fixed;
    top:-10px;
    color:white;
    animation: fall linear infinite;
    pointer-events:none;
}
@keyframes fall {
    to {transform: translateY(110vh);}
}
</style>
</head>
<body>

<h1>🎄 Настена 🎄</h1>

<img src="love.jpg" class="photo">

<p>
Этот сайт — не просто страница.  
Это маленький портал, где живёт вся моя любовь к тебе.  
Пусть Новый год принесёт тебе тепло, улыбки и мечты, которые обязательно сбудутся <3
</p>

<button onclick="showMagic()">Нажми сюда ✨</button>

<div id="magic">
Ты — самое светлое чудо моего мира.  
С Новым годом, моя родная ❤️
</div>

<!-- МУЗЫКА -->
<audio id="bgm" src="music.mp3" loop></audio>

<script>
function showMagic(){
 document.getElementById("magic").style.display="block";
}

document.addEventListener("click",()=>{
  document.getElementById("bgm").play();
},{once:true});

for(let i=0;i<80;i++){
 let s=document.createElement("div");
 s.innerHTML="❄️";
 s.className="snow";
 s.style.left=Math.random()*100+"vw";
 s.style.animationDuration=3+Math.random()*5+"s";
 s.style.fontSize=12+Math.random()*30+"px";
 document.body.appendChild(s);
}
</script>

</body>
</html>
