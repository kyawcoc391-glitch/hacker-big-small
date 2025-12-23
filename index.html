<!DOCTYPE html>
<html lang="my" data-theme="green">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HACKER BIG / SMALL</title>

<style>
:root{
  --bg:#000;
  --neon:#00ff99;
  --red:#ff3355;
  --glass:rgba(0,255,153,.12);
}

[data-theme="red"]{
  --neon:#ff3355;
  --red:#00ff99;
  --glass:rgba(255,51,85,.12);
}

*{box-sizing:border-box}

body{
  margin:0;
  height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  background:#000;
  color:var(--neon);
  font-family:Consolas,monospace;
  overflow:hidden;
}

/* MATRIX */
canvas{
  position:fixed;
  inset:0;
  z-index:-2;
}

/* CARD */
.box{
  width:320px;
  padding:30px 25px;
  text-align:center;
  background:rgba(0,0,0,.65);
  border-radius:18px;
}

#online,#period{font-size:13px;margin-bottom:6px}
#timer1m{font-size:34px;margin:12px 0}
#randomWord{font-size:42px;font-weight:bold}

.big{color:var(--neon)}
.small{color:var(--red)}

/* LINEAR */
.linear-wrap{
  width:100%;
  height:16px;
  background:rgba(255,255,255,.15);
  border-radius:10px;
  overflow:hidden;
  margin-top:15px;
  opacity:0;
  transition:.3s;
}

.linear{
  height:100%;
  width:100%;
  background:linear-gradient(90deg,var(--neon),var(--red));
  transition:width 1s linear;
  position:relative;
}

#linearTimer{
  position:absolute;
  inset:0;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:11px;
  font-weight:bold;
  color:#000;
  mix-blend-mode:screen;
}
</style>
</head>

<body>

<canvas id="matrix"></canvas>

<div class="box">
  <div id="online">🟢 Online Users: 0</div>
  <div id="period">Period: ----</div>
  <div id="timer1m">00:30</div>
  <div id="randomWord">WAIT</div>

  <div class="linear-wrap" id="linearWrap">
    <div class="linear" id="linearBar">
      <span id="linearTimer">5</span>
    </div>
  </div>
</div>

<script>
/* MATRIX */
const canvas=document.getElementById("matrix");
const ctx=canvas.getContext("2d");
function resize(){canvas.width=innerWidth;canvas.height=innerHeight}
resize();addEventListener("resize",resize);

const letters="01アイウエオ0123456789";
const fontSize=16;
let drops=Array(Math.floor(canvas.width/fontSize)).fill(1);

setInterval(()=>{
  ctx.fillStyle="rgba(0,0,0,0.05)";
  ctx.fillRect(0,0,canvas.width,canvas.height);
  ctx.fillStyle=getComputedStyle(document.documentElement).getPropertyValue("--neon");
  ctx.font=fontSize+"px monospace";
  drops.forEach((y,i)=>{
    ctx.fillText(letters[Math.random()*letters.length|0],i*fontSize,y*fontSize);
    if(y*fontSize>canvas.height&&Math.random()>0.98)drops[i]=0;
    drops[i]++;
  });
},33);

/* ONLINE */
const onlineEl=document.getElementById("online");
let online=Math.floor(Math.random()*300)+120;
setInterval(()=>{
  if(navigator.onLine){
    online+=Math.floor(Math.random()*7-3);
    onlineEl.textContent=`🟢 Online Users: ${online}`;
  }
},2000);

/* GAME + TIMER + LINEAR */
const timerEl=document.getElementById("timer1m");
const randomWordEl=document.getElementById("randomWord");
const periodEl=document.getElementById("period");
const linearWrap=document.getElementById("linearWrap");
const linearBar=document.getElementById("linearBar");
const linearTimer=document.getElementById("linearTimer");

const words=["သေး","အကြီး"];
let lastRound=-1;

setInterval(()=>{
  const now=new Date();
  const sec=now.getUTCSeconds();
  const remain=30-(sec%30);
  timerEl.textContent=`00:${String(remain).padStart(2,"0")}`;

  if(remain<=5 && remain>0){
    linearWrap.style.opacity=1;
    linearBar.style.width=(remain/5*100)+"%";
    linearTimer.textContent=remain;
  }
  else if(remain===0){
    linearBar.style.width="0%";
    linearTimer.textContent="0";
    setTimeout(()=>{
      linearWrap.style.opacity=0;
      linearBar.style.width="100%";
    },300);
  }
  else{
    linearWrap.style.opacity=0;
    linearBar.style.width="100%";
  }

  const round=Math.floor(sec/30);
  if(round!==lastRound){
    lastRound=round;
    const r=words[Math.random()*2|0];
    randomWordEl.textContent=r;
    randomWordEl.className=r==="အကြီး"?"big":"small";
    document.documentElement.setAttribute(
      "data-theme", r==="အကြီး"?"green":"red"
    );
  }

  const d=`${now.getUTCFullYear()}${String(now.getUTCMonth()+1).padStart(2,"0")}${String(now.getUTCDate()).padStart(2,"0")}`;
  const idx=now.getUTCHours()*120+now.getUTCMinutes()*2+Math.floor(sec/30);
  periodEl.textContent=`Period: ${d}1000${10001+idx}`;
},1000);
</script>

</body>
</html>
