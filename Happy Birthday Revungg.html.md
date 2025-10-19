<!doctype html>  
<html lang="id">  
<head>  
<meta charset="utf-8" />  
<meta name="viewport" content="width=device-width,initial-scale=1" />  
<title>Selamat Ulang Tahun — Revunggg 🎉</title>  
<style>  
  :root{  
    --bg1:#FFDEE9; --bg2:#B5FFFC; --accent:#FF8AB3;  
  }  
  html,body{height:100%;margin:0;font-family:"Poppins",system-ui;}  
  body{  
    background:linear-gradient(135deg,var(--bg1),var(--bg2));  
    overflow:hidden;  
    display:flex;  
    align-items:center;  
    justify-content:center;  
    padding:20px;  
    box-sizing:border-box;  
  }  
  .card{  
    position:relative;  
    width:100%;  
    max-width:900px;  
    background:rgba(255,255,255,0.9);  
    border-radius:18px;  
    box-shadow:0 10px 40px rgba(0,0,0,0.12);  
    padding:28px;  
  }  
  h1{margin:0;font-size:28px;color:#333;}  
  p.lead{margin:6px 0;color:#555;}  
  .message{margin-top:18px;padding:18px;border-radius:12px;background:rgba(255,255,255,0.7);font-size:15px;color:#222;line-height:1.6;}  
  .controls{margin-top:18px;display:flex;flex-wrap:wrap;gap:10px;}  
  .btn{  
    background:var(--accent);color:white;border:none;padding:10px 14px;border-radius:10px;  
    cursor:pointer;font-weight:600;box-shadow:0 6px 18px rgba(255,138,179,0.24);  
  }  
  .btn.secondary{background:transparent;color:var(--accent);border:2px solid var(--accent);}  
  .btn.whatsapp{  
    background:#25D366;color:#fff;  
  }  
  .balloon{position:absolute;bottom:-40px;width:60px;height:80px;border-radius:50% 50% 50% 50%/60% 60% 40% 40%;animation:floatUp linear infinite;}  
  .string{position:absolute;left:50%;bottom:-40px;width:2px;height:50px;background:rgba(0,0,0,0.12);transform:translateX(-50%);}  
  .balloon.b1{background:linear-gradient(180deg,#FFADAD,#FFD6A5);left:6%;animation-duration:10s}  
  .balloon.b2{background:linear-gradient(180deg,#FDFFB6,#CAFFBF);left:22%;animation-duration:12s}  
  .balloon.b3{background:linear-gradient(180deg,#9BF6FF,#A0C4FF);left:40%;animation-duration:11s}  
  .balloon.b4{background:linear-gradient(180deg,#BDB2FF,#FFC6FF);left:62%;animation-duration:13s}  
  .balloon.b5{background:linear-gradient(180deg,#CBAACB,#FFC6A8);left:78%;animation-duration:9s}  
  @keyframes floatUp{  
    0%{transform:translateY(0) rotate(-6deg);opacity:0}  
    10%{opacity:1}  
    50%{transform:translateY(-380px) rotate(4deg)}  
    100%{transform:translateY(-780px) rotate(-8deg);opacity:0}  
  }  
  footer{margin-top:14px;font-size:13px;color:#666;text-align:center;}  
</style>  
</head>  
<body>  
<div class="card">  
  <h1>Selamat Ulang Tahun, Revunggg 🎂</h1>  
  <p class="lead">Pesan dari sahabatmu 💕</p>  
  
  <div class="message">  
Selamat Ulang Tahun Revunggg, aku harap di tahun ini kamu jadi pribadi yg lebih baik dripada tahun sebelumnya, dan hal yg belum tercapai di tahun lalu bisa tercapai di tahun inii, kamu harus janji sama diri kamu sendiri utk hidup lebih sehat dan lebih baik, nda boleh sering sakit, kurangin kopi, eskrimm, belajar makan sayur, jaga pola makan , pola istirahat nya juga, semangat kuliahnya, semangat jugaa jalanin hari2nya walau pasti ada aja yg bikin bete, kamu harus capai cita2 kamu, capai titik dimana kamu berjuang utk sampai ke titik itu, aku yakin kamu bisa koo, yakin 1000000000% , okeiiiii, Happy Birthdayyyy tuan putrii, whist u all the best, god bless u, and love ur self yaa, sekali lagiii Happy Brojoll dayy Lepungggg ✨🎉🎉  
  </div>  
  
  <div class="controls">  
    <button class="btn" id="playBtn">Play Music ▶️</button>  
    <button class="btn secondary" id="stopBtn">Stop ⏹️</button>  
    <button class="btn whatsapp" id="shareBtn">Bagikan ke WhatsApp 💚</button>  
  </div>  
  
  <footer>🎈 Dibuat dengan cinta untuk Revunggg 🎈</footer>  
  
  <div class="balloon b1"><div class="string"></div></div>  
  <div class="balloon b2"><div class="string"></div></div>  
  <div class="balloon b3"><div class="string"></div></div>  
  <div class="balloon b4"><div class="string"></div></div>  
  <div class="balloon b5"><div class="string"></div></div>  
</div>  
  
<script>  
const AudioContext = window.AudioContext || window.webkitAudioContext;  
let ac, playing=false;  
let timeouts=[];  
const notes={"C4":261.63,"D4":293.66,"E4":329.63,"F4":349.23,"G4":392.00,"A4":440.00,"B4":493.88,"C5":523.25,"D5":587.33,"E5":659.25,"F5":698.46,"G5":783.99};  
const melody=[["G4",1],["G4",0.5],["A4",1.5],["G4",1],["C5",1],["B4",2],  
["G4",1],["G4",0.5],["A4",1.5],["G4",1],["D5",1],["C5",2],  
["G4",1],["G4",0.5],["G5",1.5],["E5",1],["C5",1],["B4",1],["A4",1.5],  
["F5",1],["F5",0.5],["E5",1.5],["C5",1],["D5",1],["C5",2]];  
function play(freq,dur){if(!ac)return;const o=ac.createOscillator(),g=ac.createGain();  
o.type="sine";o.frequency.value=freq;g.gain.setValueAtTime(0.001,ac.currentTime);  
g.gain.exponentialRampToValueAtTime(0.25,ac.currentTime+0.02);  
g.gain.exponentialRampToValueAtTime(0.001,ac.currentTime+dur-0.02);  
o.connect(g);g.connect(ac.destination);o.start();o.stop(ac.currentTime+dur);}  
function start(){if(playing)return;ac=new AudioContext();playing=true;let t=0;const beat=0.6;  
melody.forEach(([n,b])=>{const f=notes[n]||440;timeouts.push(setTimeout(()=>play(f,b*beat*0.9),t*1000));t+=b*beat;});  
timeouts.push(setTimeout(()=>{playing=false},t*1000));}  
function stop(){if(ac)ac.close();timeouts.forEach(clearTimeout);playing=false;}  
document.getElementById('playBtn').onclick=start;  
document.getElementById('stopBtn').onclick=stop;  
  
// share to WhatsApp  
document.getElementById('shareBtn').onclick=function(){  
  const text=`🎉 Selamat Ulang Tahun Revunggg! 🎂\n\nKlik link ini buat lihat ucapan spesial dari aku 👉 ${window.location.href}`;  
  const url=`https://wa.me/?text=${encodeURIComponent(text)}`;  
  window.open(url,'_blank');  
};  
</script>  
</body>  
</html>  
