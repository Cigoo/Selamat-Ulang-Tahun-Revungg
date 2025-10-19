<!DOCTYPE html>  
<html lang="id">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Selamat Ulang Tahun Revung 🎂</title>  
<link rel="icon" href="https://cdn-icons-png.flaticon.com/512/869/869869.png" type="image/png">  
<style>  
  body {  
    margin:0;  
    padding:0;  
    overflow:hidden;  
    background: linear-gradient(135deg, #ffccff, #ccffff);  
    background-size:300% 300%;  
    animation: gradientShift 10s infinite alternate;  
    font-family: 'Poppins', sans-serif;  
    text-align:center;  
    color:#333;  
  }  
  @keyframes gradientShift {  
    0% { background-position: left; }  
    100% { background-position: right; }  
  }  
  h1 {  
    margin-top:80px;  
    font-size:2.4em;  
    color:#ff66b2;  
  }  
  p {  
    font-size:1.15em;  
    margin:20px 40px;  
    line-height:1.6em;  
  }  
  button {  
    background-color:#66ccff;  
    color:white;  
    border:none;  
    padding:14px 28px;  
    border-radius:30px;  
    cursor:pointer;  
    font-size:1em;  
    margin-top:20px;  
    transition: background 0.3s;  
  }  
  button:hover {  
    background-color:#3399ff;  
  }  
  footer {  
    margin-top:40px;  
    font-size:1.1em;  
    color:#ff66b2;  
    font-style:italic;  
  }  
  .balloon {  
    position:absolute;  
    bottom:-150px;  
    width:50px;  
    height:70px;  
    border-radius:50%;  
    animation: floatUp linear infinite;  
  }  
  @keyframes floatUp {  
    0%   { transform: translateY(0); opacity:1; }  
    100% { transform: translateY(-110vh); opacity:0; }  
  }  
</style>  
</head>  
<body>  
  
<h1>🎉 Selamat Ulang Tahun, Revung! 🎂</h1>  
<p>  
Selamat Ulang Tahun Revunggg, aku harap di tahun ini kamu jadi pribadi yg lebih baik daripada tahun sebelumnya,    
dan hal yg belum tercapai di tahun lalu bisa tercapai di tahun ini.    
Kamu harus janji sama diri kamu sendiri utk hidup lebih sehat dan lebih baik,    
nda boleh sering sakit, kurangin kopi, eskrimm, belajar makan sayur, jaga pola makan, pola istirahatnya juga,    
semangat kuliahnya, semangat juga jalanin hari-harinya walau pasti ada aja yang bikin bete.    
Kamu harus capai cita2 kamu, capai titik dimana kamu berjuang utk sampai ke titik itu,    
aku yakin kamu bisa koo, yakin 1000000000%!    
<br><br>  
Okeiiiii, Happy Birthdayyyy tuan putrii, wish u all the best, god bless u, and love ur self yaa,    
sekali lagiii Happy Brojoll dayy Lepungggg ✨🎉🎉  
</p>  
  
<button id="playMusic">🎵 Putar Musik</button>  
  
<footer>— dari Cigoo 💌</footer>  
  
<audio id="music" preload="auto">  
  <source src="https://cdn.pixabay.com/download/audio/2021/09/01/audio_7b53a4972f.mp3?filename=happy-birthday-piano-version-7742.mp3" type="audio/mpeg">  
</audio>  
  
<script>  
  const btn = document.getElementById('playMusic');  
  const music = document.getElementById('music');  
  let playing = false;  
  btn.addEventListener('click', () => {  
    if (!playing) {  
      music.play().then(() => {  
        btn.textContent = "⏸️ Musik Sedang Diputar";  
        btn.style.backgroundColor = '#ff66b2';  
        playing = true;  
      }).catch(err => {  
        alert("Klik tombol lagi agar musik bisa diputar di perangkat kamu 😊");  
      });  
    } else {  
      music.pause();  
      btn.textContent = "🎵 Putar Musik";  
      btn.style.backgroundColor = '#66ccff';  
      playing = false;  
    }  
  });  
  
  function spawnBalloon() {  
    const b = document.createElement('div');  
    b.classList.add('balloon');  
    const colors = ['#ff7eb9','#7afcff','#feff9c','#fff740','#a0c4ff'];  
    b.style.background = colors[Math.floor(Math.random()*colors.length)];  
    b.style.left = Math.random() * window.innerWidth + 'px';  
    b.style.animationDuration = (6 + Math.random()*5) + 's';  
    document.body.appendChild(b);  
    setTimeout(() => b.remove(), 10000);  
  }  
  setInterval(spawnBalloon, 500);  
</script>  
  
</body>  
</html>  
