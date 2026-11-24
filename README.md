<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RYGYL - Driving Theory</title>
<style>
*{box-sizing:border-box}
body{
 margin:0;font-family:Arial,sans-serif;
 background:linear-gradient(145deg,#101d3b,#253c70);
 color:#fff;min-height:100vh
}
header{
 text-align:center;padding:25px 15px 20px;
 background:linear-gradient(120deg,#087fbd,#5945bd);
 border-radius:0 0 28px 28px
}
.logo{font-size:38px;font-weight:900;letter-spacing:3px}
header p{margin:7px;color:#e4f5ff}
main{max-width:600px;margin:auto;padding:18px}
.welcome{
 background:linear-gradient(120deg,#ff9e43,#ff557b);
 padding:20px;border-radius:20px;margin-bottom:18px
}
.welcome h2{margin:0 0 8px}
.welcome p{margin:0;line-height:1.5}
.stats{display:flex;gap:10px;margin:15px 0}
.stat{
 flex:1;text-align:center;background:#263b63;
 padding:13px 5px;border-radius:15px
}
.stat strong{display:block;font-size:23px;color:#ffe17b}
.stat small{color:#d4e3ff}
nav{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin:18px 0}
nav button{
 border:0;border-radius:12px;padding:13px 5px;
 color:white;background:#344b78;font-weight:bold;font-size:14px
}
nav button.active{background:#19b88a;color:#062d2a}
.card{
 background:#fff;color:#17233d;
 padding:20px;border-radius:20px;margin-bottom:15px;
 box-shadow:0 8px 25px #0003
}
h2{color:#087fbd;margin-top:0}
h3{margin-bottom:8px}
.muted{color:#65738b;line-height:1.5}
.question{font-size:19px;line-height:1.5;font-weight:bold}
.turkish{
 background:#fff4d9;color:#79500b;
 padding:12px;border-radius:12px;line-height:1.5
}
.option{
 width:100%;text-align:left;margin:7px 0;padding:14px;
 border:2px solid #dce5f1;border-radius:13px;
 background:#f5f8ff;color:#17233d;font-size:15px;
 line-height:1.5
}
.option small{display:block;color:#65738b;margin-top:3px}
.option.correct{background:#d7f8e8;border-color:#18ae72}
.option.wrong{background:#ffe0e4;border-color:#e34d65}
.option:disabled{opacity:1}
.btn{
 display:block;width:100%;border:0;border-radius:13px;
 padding:15px;background:#13b98b;color:white;
 font-weight:bold;font-size:16px;margin-top:12px
}
.progressbar{height:10px;background:#e5eaf2;border-radius:20px;overflow:hidden}
.progressfill{height:100%;background:#18bb8c;width:0%}
.light{
 display:flex;align-items:center;gap:15px;
 padding:13px;background:#f1f5fb;border-radius:14px;margin:10px 0
}
.lamp{
 width:43px;height:100px;border-radius:25px;
 background:#222b3c;display:flex;flex-direction:column;
 align-items:center;justify-content:space-around;padding:5px
}
.bulb{width:23px;height:23px;border-radius:50%;background:#555}
.red{background:#ff394e;box-shadow:0 0 12px #ff394e}
.amber{background:#ffb52e;box-shadow:0 0 12px #ffb52e}
.green{background:#22cb79;box-shadow:0 0 12px #22cb79}
.memory{
 background:#eee7ff;color:#5532a0;padding:13px;
 border-radius:13px;line-height:1.6;margin-top:12px
}
.video{
 display:block;text-decoration:none;color:#fff;
 background:linear-gradient(120deg,#e84c67,#9b45bd);
 padding:16px;border-radius:15px;margin:12px 0
}
.video span{font-size:27px;float:left;margin-right:12px}
.video strong{display:block;margin-bottom:5px}
.video small{color:#ffe8ef}
#feedback{line-height:1.6;margin-top:14px}
footer{text-align:center;padding:25px;color:#b9c8e6}
.hidden{display:none}
</style>
</head>
<body>

<header>
 <div class="logo">🚘 RYGYL</div>
 <p>Relax, You'll Get Your Licence</p>
 <p>🇬🇧 UK Driving Theory Test</p>
</header>

<main>
 <section class="welcome">
  <h2>Ready to become a driver? 🌟</h2>
  <p>Learn a little every day. Practise, remember and pass!</p>
 </section>

 <div class="stats">
  <div class="stat"><strong id="score">0</strong><small>⭐ Points</small></div>
  <div class="stat"><strong id="done">0</strong><small>📝 Answers</small></div>
  <div class="stat"><strong id="percent">0%</strong><small>🎯 Success</small></div>
 </div>

 <nav>
  <button class="active" onclick="showTab('learn',this)">📚 Learn</button>
  <button onclick="showTab('practice',this)">✏️ Practice</button>
  <button onclick="showTab('videos',this)">🎬 Videos</button>
 </nav>

 <section id="learn">
  <div class="card">
   <h2>🚦 Traffic Lights</h2>
   <p class="muted">Learn the three important traffic light colours.</p>

   <div class="light">
    <div class="lamp">
     <div class="bulb red"></div>
     <div class="bulb"></div>
     <div class="bulb"></div>
    </div>
    <div>
     <h3 style="color:#e52e48">RED = STOP</h3>
     <p>Red means you must stop.</p>
     <p class="muted">Kırmızı = Durmalısın.</p>
    </div>
   </div>

   <div class="light">
    <div class="lamp">
     <div class="bulb"></div>
     <div class="bulb amber"></div>
     <div class="bulb"></div>
    </div>
    <div>
     <h3 style="color:#d88a00">AMBER = STOP IF SAFE</h3>
     <p>Stop if you can do so safely. Do not speed up.</p>
     <p class="muted">Sarı = Güvenliyse dur. Hızlanma.</p>
    </div>
   </div>

   <div class="light">
    <div class="lamp">
     <div class="bulb"></div>
     <div class="bulb"></div>
     <div class="bulb green"></div>
    </div>
    <div>
     <h3 style="color:#12965e">GREEN = GO IF CLEAR</h3>
     <p>Go only if the road is clear.</p>
     <p class="muted">Yeşil = Yol açıksa ilerle.</p>
    </div>
   </div>

   <div class="memory">
    🧠 <strong>Memory Trick – Hafıza Kodu</strong><br>
    🔴 RED → STOP → DUR<br>
    🟡 AMBER → STOP IF SAFE → GÜVENLİYSE DUR<br>
    🟢 GREEN → GO IF CLEAR → YOL AÇIKSA İLERLE
   </div>
  </div>

  <div class="card">
   <h2>💡 Remember!</h2>
   <p><strong>Mirror = Ayna</strong></p>
   <p><strong>Seat belt = Emniyet kemeri</strong></p>
   <p><strong>Blind spot = Kör nokta</strong></p>
   <p><strong>Pedestrian = Yaya</strong></p>
  </div>
 </section>

 <section id="practice" class="hidden">
  <div class="card">
   <p class="muted" id="progress">Question 1</p>
   <div class="progressbar"><div class="progressfill" id="bar"></div></div>
   <h2>🎯 Practice Test</h2>
   <p class="question" id="question"></p>
   <p class="turkish" id="translation"></p>
   <div id="answers"></div>
   <div id="feedback"></div>
   <button class="btn hidden" id="next" onclick="nextQuestion()">Next Question →</button>
  </div>
 </section>

 <section id="videos" class="hidden">
  <div class="card">
   <h2>🎬 Video Learning</h2>
   <p class="muted">Watch driving lessons and learn visually. Video searches open on YouTube.</p>

   <a class="video" target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query=UK+driving+traffic+lights+lesson">
    <span>🚦</span><strong>Traffic Lights</strong>
    <small>Trafik ışıkları eğitimi</small>
   </a>

   <a class="video" target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query=UK+roundabout+driving+lesson">
    <span>🔄</span><strong>Roundabouts</strong>
    <small>Dönel kavşak eğitimi</small>
   </a>

   <a class="video" target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query=UK+hazard+perception+practice">
    <span>👀</span><strong>Hazard Perception</strong>
    <small>Tehlike algılama eğitimi</small>
   </a>

   <a class="video" target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query=UK+road+signs+theory+test">
    <span>🛑</span><strong>Road Signs</strong>
    <small>Trafik işaretleri eğitimi</small>
   </a>

   <a class="video" target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query=UK+motorway+driving+lesson">
    <span>🛣️</span><strong>Motorways</strong>
    <small>Otoyol eğitimi</small>
   </a>
  </div>
 </section>
</main>

<footer>
 RYGYL © 2026<br>
 Learn ❤️ Practise ⭐ Pass 🏆
</footer>

<script>
const questions=[
{
q:"What should you do when approaching a red traffic light?",
tr:"Kırmızı trafik ışığına yaklaşırken ne yapmalısınız?",
a:["Stop","Speed up","Sound your horn","Turn left"],
t:["Durmalısınız","Hızlanmalısınız","Korna çalmalısınız","Sola dönmelisiniz"],
correct:0,
ex:"A red traffic light means you must stop.",
extr:"Kırmızı ışıkta durmak zorundasınız.",
memory:"RED = STOP. Kırmızı gördüğünde dur!"
},
{
q:"When should you wear a seat belt?",
tr:"Ne zaman emniyet kemeri takmalısınız?",
a:["Only on motorways","Only at night","Whenever required in a vehicle","Only on long journeys"],
t:["Sadece otoyollarda","Sadece geceleri","Yasaların gerektirdiği durumlarda","Sadece uzun yolculuklarda"],
correct:2,
ex:"Seat belts must be worn when required by law.",
extr:"Yasa gereği emniyet kemeri takılmalıdır.",
memory:"SEAT BELT = EMNİYET KEMERİ. Her yolculukta kemerini hatırla!"
},
{
q:"What should you do before changing lanes?",
tr:"Şerit değiştirmeden önce ne yapmalısınız?",
a:["Check mirrors and blind spots","Accelerate immediately","Only look ahead","Sound your horn"],
t:["Aynaları ve kör noktaları kontrol etmelisiniz","Hemen hızlanmalısınız","Sadece ileri bakmalısınız","Korna çalmalısınız"],
correct:0,
ex:"Check your mirrors and blind spots before moving.",
extr:"Hareket etmeden önce aynaları ve kör noktaları kontrol edin.",
memory:"MIRRORS → SIGNAL → MANOEUVRE. Ayna → Sinyal → Hareket."
},
{
q:"What should you do when the traffic light changes to amber?",
tr:"Trafik ışığı sarıya döndüğünde ne yapmalısınız?",
a:["Always speed up","Stop if you can do so safely","Reverse","Sound your horn"],
t:["Her zaman hızlanmalısınız","Güvenli şekilde durabiliyorsanız durmalısınız","Geri gitmelisiniz","Korna çalmalısınız"],
correct:1,
ex:"Amber means stop, unless you have already crossed the stop line or stopping might cause an accident.",
extr:"Sarı ışıkta, durma çizgisini geçmiş değilseniz ve güvenli durabiliyorsanız durmalısınız.",
memory:"AMBER = STOP IF SAFE. Sarı ışıkta hızlanma!"
}
];

let current=0,score=0,answered=0,finished=false;

function showTab(name,button){
 document.querySelectorAll("main section").forEach(s=>s.classList.add("hidden"));
 document.getElementById(name).classList.remove("hidden");
 document.querySelectorAll("nav button").forEach(b=>b.classList.remove("active"));
 button.classList.add("active");
}

function updateStats(){
 document.getElementById("score").textContent=score*10;
 document.getElementById("done").textContent=answered;
 document.getElementById("percent").textContent=
 answered?Math.round(score/answered*100)+"%":"0%";
}

function showQuestion(){
 if(finished)return;
 const q=questions[current];
 document.getElementById("progress").textContent=
 "Question "+(current+1)+" / "+questions.length;
 document.getElementById("bar").style.width=
 (current/questions.length*100)+"%";
 document.getElementById("question").textContent=q.q;
 document.getElementById("translation").textContent=q.tr;
 document.getElementById("feedback").innerHTML="";
 document.getElementById("next").classList.add("hidden");
 const area=document.getElementById("answers");
 area.innerHTML="";
 q.a.forEach((answer,i)=>{
  const btn=document.createElement("button");
  btn.className="option";
  const strong=document.createElement("strong");
  strong.textContent=answer;
  const small=document.createElement("small");
  small.textContent=q.t[i];
  btn.append(strong,small);
  btn.onclick=()=>checkAnswer(i,btn);
  area.appendChild(btn);
 });
}

function checkAnswer(i,btn){
 if(finished)return;
 const q=questions[current];
 const buttons=document.querySelectorAll(".option");
 buttons.forEach((b,index)=>{
  b.disabled=true;
  if(index===q.correct)b.classList.add("correct");
 });
 answered++;
 if(i===q.correct){
  score++;
  document.getElementById("feedback").innerHTML=
   "🎉 <strong style='color:#11945d'>Correct! Well done!</strong><br>"+
   "Doğru cevap! Harika!<br>"+q.ex+"<br>"+q.extr;
 }else{
  btn.classList.add("wrong");
  document.getElementById("feedback").innerHTML=
   "💡 <strong style='color:#d43d58'>Not quite! Try to remember.</strong><br>"+
   "Doğru cevap: <strong>"+q.a[q.correct]+"</strong><br>"+
   q.ex+"<br>"+q.extr;
 }
 document.getElementById("feedback").innerHTML+=
  "<div class='memory'>🧠 <strong>Memory Trick</strong><br>"+q.memory+"</div>";
 updateStats();
 document.getElementById("next").classList.remove("hidden");
}

function nextQuestion(){
 current++;
 if(current<questions.length){
  showQuestion();
 }else{
  finished=true;
  document.getElementById("bar").style.width="100%";
  document.querySelector("#practice .card").innerHTML=
   "<h2>🏆 Test Completed!</h2>"+
   "<p>Deneme tamamlandı!</p>"+
   "<h1 style='font-size:45px;color:#13a978'>"+score+" / "+questions.length+"</h1>"+
   "<p>Correct answers / Doğru cevaplar</p>"+
   "<p>Başarı oranı: "+Math.round(score/questions.length*100)+"%</p>"+
   "<button class='btn' onclick='restart()'>🔄 Try Again / Tekrar Dene</button>";
 }
}

function restart(){
 current=0;score=0;answered=0;finished=false;
 updateStats();
 document.querySelector("#practice .card").innerHTML=
 '<p class="muted" id="progress"></p>'+
 '<div class="progressbar"><div class="progressfill" id="bar"></div></div>'+
 '<h2>🎯 Practice Test</h2>'+
 '<p class="question" id="question"></p>'+
 '<p class="turkish" id="translation"></p>'+
 '<div id="answers"></div><div id="feedback"></div>'+
 '<button class="btn hidden" id="next" onclick="nextQuestion()">Next Question →</button>';
 showQuestion();
}

showQuestion();
updateStats();
</script>
</body>
</html>
