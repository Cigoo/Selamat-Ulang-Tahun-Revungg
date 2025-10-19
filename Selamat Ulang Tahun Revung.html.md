<!DOCTYPE html>  
<html lang="id">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Happy Birthday Revunggg 🎂</title>  
<link rel="icon" href="https://cdn-icons-png.flaticon.com/512/869/869869.png" type="image/png">  
<style>  
  body {  
    margin: 0;  
    padding: 0;  
    overflow: hidden;  
    background: linear-gradient(135deg, #ffccff, #ccffff, #ffffcc);  
    background-size: 300% 300%;  
    animation: gradientShift 10s infinite alternate;  
    font-family: 'Comic Sans MS', cursive;  
    text-align: center;  
    color: #444;  
  }  
  
  @keyframes gradientShift {  
    0% { background-position: left; }  
    100% { background-position: right; }  
  }  
  
  h1 {  
    font-size: 2.3em;  
    margin-top: 80px;  
    color: #ff66b2;  
  }  
  
  p {  
    font-size: 1.1em;  
    margin: 20px;  
    line-height: 1.6em;  
  }  
  
  button {  
    background-color: #ff66b2;  
    color: white;  
    border: none;  
    padding: 15px 30px;  
    margin: 10px;  
    border-radius: 30px;  
    cursor: pointer;  
    font-size: 1em;  
  }  
  
  button:hover {  
    background-color: #ff3385;  
  }  
  
  footer {  
    margin-top: 40px;  
    font-style: italic;  
    font-size: 1.1em;  
    color: #ff66b2;  
  }  
  
  .balloon {  
    position: absolute;  
    bottom: -150px;  
    width: 50px;  
    height: 70px;  
    border-radius: 50%;  
    background-color: #ff7eb9;  
    animation: floatUp 8s linear infinite;  
  }  
  
  @keyframes floatUp {  
    0% { transform: translateY(0); opacity: 1; }  
    100% { transform: translateY(-110vh); opacity: 0; }  
  }  
</style>  
</head>  
<body>  
  
<h1>🎉 Selamat Ulang Tahun, Revunggg! 🎂</h1>  
<p>  
Aku harap di tahun ini kamu jadi pribadi yang lebih baik daripada tahun sebelumnya,    
dan hal yang belum tercapai di tahun lalu bisa tercapai di tahun ini.    
Kamu harus janji sama diri kamu sendiri untuk hidup lebih sehat dan lebih baik,    
nggak boleh sering sakit, kurangin kopi dan es krim 🍦☕, belajar makan sayur 🥦,    
jaga pola makan dan istirahat juga ya!    
<br><br>  
Semangat kuliahnya, semangat juga jalanin hari-harimu walau pasti ada aja yang bikin bete 😅    
Kamu harus capai cita-citamu, capai titik di mana kamu berjuang untuk sampai ke sana 💪    
Aku yakin kamu bisa kok — yakin 1000000000%!    
<br><br>  
Happy Birthday tuan putriii 👑✨    
Wish u all the best, God bless u, and love ur self yaa 💖    
Sekali lagi, Happy Brojoll Day Lepungggg 🎉🎂🎈  
</p>  
  
<button id="playMusic">🎵 Putar Musik</button>  
  
<footer>— dari Cigoo 💌</footer>  
  
<audio id="music" src="https://cdn.pixabay.com/download/audio/2021/09/01/audio_7b53a4972f.mp3?filename=happy-birthday-piano-version-7742.mp3"></audio>  
  
<script>  
  const playButton = document.getElementById('playMusic');  
  const music = document.getElementById('music');  
  
  playButton.addEventListener('click', () => {  
    music.play();  
    playButton.innerText = "🎶 Musik Sedang Diputar...";  
    playButton.disabled = true;  
  });  
  
  // Balon animasi  
  function createBalloon() {  
    const balloon = document.createElement('div');  
    balloon.classList.add('balloon');  
    const colors = ['#ff7eb9', '#7afcff', '#feff9c', '#fff740', '#f0a6ca'];  
    balloon.style.background = colors[Math.floor(Math.random() * colors.length)];  
    balloon.style.left = Math.random() * window.innerWidth + 'px';  
    balloon.style.animationDuration = (6 + Math.random() * 5) + 's';  
    document.body.appendChild(balloon);  
    setTimeout(() => balloon.remove(), 10000);  
  }  
  setInterval(createBalloon, 500);  
</script>  
  
</body>  
</html>  
