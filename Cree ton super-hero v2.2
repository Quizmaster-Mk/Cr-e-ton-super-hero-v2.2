<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Créateur de Super-Héros</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Bangers&display=swap');
  body {
    font-family: 'Bangers', cursive;
    background: radial-gradient(circle at center, #000 50%, #111);
    color: white;
    text-align: center;
    margin: 0; padding: 0;
    overflow-x: hidden;
  }
  h1, h2 { color: #ffeb3b; text-shadow: 3px 3px red; }
  .intro, .creator, .mission, .result, .ranking { animation: fadeIn 1.2s; }
  button {
    background: #ff4444;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 10px;
    font-size: 20px;
    cursor: pointer;
    transition: 0.3s;
    width: 85%;
    margin-top: 10px;
  }
  button:hover { background: #ff6666; transform: scale(1.05); }
  select, input {
    font-family: 'Bangers', cursive;
    width: 80%;
    margin: 8px 0;
    padding: 10px;
    font-size: 18px;
    text-align: center;
    border-radius: 8px;
    border: none;
  }
  .section { display: none; background: #111; padding: 25px; border-top: 3px solid yellow; }
  .hero-card, .ranking-card {
    margin-top: 20px;
    padding: 20px;
    border-radius: 10px;
    background: rgba(0,0,0,0.8);
    border: 3px solid #ffeb3b;
    box-shadow: 0 0 15px #ffeb3b;
    animation: fadeIn 1s;
  }
  .hero-emoji { font-size: 60px; }
  .choice {
    background: rgba(255,255,255,0.1);
    margin: 12px auto;
    padding: 10px;
    border-radius: 10px;
    max-width: 400px;
    cursor: pointer;
    transition: 0.3s;
  }
  .choice:hover { background: rgba(255,255,255,0.2); transform: scale(1.05); }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  canvas#bg {
    position: fixed;
    top: 0; left: 0;
    z-index: -1;
    width: 100%; height: 100%;
  }
</style>
</head>
<body>

<canvas id="bg"></canvas>

<!-- INTRO -->
<div class="section" id="intro" style="display:block;">
  <h1>💥 Deviens un Super-Héros 💥</h1>
  <p>Un événement cosmique déclenche ton pouvoir. Le monde a besoin d’un nouveau champion… ou d’un nouveau tyran.</p>
  <button onclick="startCreation()">Commencer</button>
</div>

<!-- CREATOR -->
<div class="section" id="creator">
  <input type="text" id="heroName" placeholder="Nom de ton héros...">
  <select id="heroPower">
    <option value="">-- Pouvoir principal --</option>
    <option>Contrôle du feu 🔥</option>
    <option>Super vitesse ⚡</option>
    <option>Télépathie 🧠</option>
    <option>Force surhumaine 💪</option>
    <option>Invisibilité 👻</option>
    <option>Technologie avancée 🤖</option>
    <option>Énergie cosmique 🌌</option>
  </select>
  <select id="heroOrigin">
    <option value="">-- Origine --</option>
    <option>New York 🇺🇸</option>
    <option>Wakanda 🌍</option>
    <option>Asgard 🌩️</option>
    <option>Gotham City 🌃</option>
    <option>Tokyo 🇯🇵</option>
    <option>Krypton 💫</option>
  </select>
  <select id="heroEmoji">
    <option value="">-- Avatar --</option>
    <option>🦸</option><option>🦹</option><option>🤖</option><option>🕷️</option>
    <option>🐆</option><option>⚡</option><option>🔥</option><option>💀</option>
  </select>
  <input type="text" id="heroMotto" placeholder="Devise héroïque...">
  <button onclick="generateHero()">✨ Révéler mon identité</button>
</div>

<!-- HERO CARD -->
<div class="section" id="heroCard">
  <div class="hero-card">
    <div class="hero-emoji" id="displayEmoji">🦸</div>
    <h2 id="displayName"></h2>
    <p id="displayPower"></p>
    <p id="displayOrigin"></p>
    <p id="displayMotto"></p>
  </div>
  <button onclick="startMission()">💥 Première mission</button>
</div>

<!-- MISSION -->
<div class="section" id="mission">
  <h2>🚨 Alerte !</h2>
  <p>Une explosion secoue ton quartier. Que fais-tu ?</p>
  <div class="choice" onclick="missionResult('sauver')">🦸 Sauver les civils</div>
  <div class="choice" onclick="missionResult('combattre')">💥 Affronter le criminel</div>
  <div class="choice" onclick="missionResult('analyser')">🧠 Analyser la situation</div>
</div>

<!-- RESULT -->
<div class="section" id="result">
  <h2 id="resultTitle"></h2>
  <p id="resultText"></p>
  <button onclick="showRanking()">Voir mes stats 🔥</button>
</div>

<!-- RANKING -->
<div class="section" id="ranking">
  <h2>🧬 Ton Profil de Héros</h2>
  <div class="ranking-card">
    <p><b>Niveau de puissance :</b> <span id="heroPowerLevel"></span></p>
    <p><b>Rareté :</b> <span id="heroRarity"></span></p>
    <p id="heroComment"></p>
  </div>
  <button onclick="restart()">🔁 Rejouer</button>
</div>

<script>
function startCreation() {
  show('creator');
  playSound();
}

function generateHero() {
  const name = val('heroName') || "Héros mystère";
  const power = val('heroPower') || "Pouvoir inconnu";
  const origin = val('heroOrigin') || "Origine secrète";
  const emoji = val('heroEmoji') || "🦸";
  const motto = val('heroMotto') || "La justice triomphe toujours !";

  set('displayEmoji', emoji);
  set('displayName', name);
  set('displayPower', "Pouvoir : " + power);
  set('displayOrigin', "Origine : " + origin);
  set('displayMotto', `"${motto}"`);

  show('heroCard');
  changeBackground(power);
}

function startMission() { show('mission'); }

function missionResult(choice) {
  show('result');
  const name = get('displayName').innerText;
  let title = "", text = "", score = 0;

  if (choice === "sauver") {
    title = "👏 Héros du peuple !";
    text = `${name} sauve des vies et gagne la confiance du monde.`;
    score = 80;
  } else if (choice === "combattre") {
    title = "⚡ Combat épique !";
    text = `${name} terrasse son ennemi dans un duel légendaire !`;
    score = 95;
  } else {
    title = "🧠 Stratège suprême !";
    text = `${name} découvre un complot mondial... et se prépare.`;
    score = 70;
  }

  set('resultTitle', title);
  set('resultText', text);

  // Stockage temporaire du score
  window.heroScore = score;
}

function showRanking() {
  show('ranking');
  const score = window.heroScore || 50;
  const power = val('heroPower');
  let level = Math.floor(score + Math.random() * 20);
  let rarity = "";
  let comment = "";

  if (level < 60) { rarity = "🟩 Commun"; comment = "Tu débutes ton aventure, mais le potentiel est là !"; }
  else if (level < 80) { rarity = "🟦 Rare"; comment = "Un héros reconnu dans sa ville."; }
  else if (level < 95) { rarity = "🟪 Épique"; comment = "Ton nom circule déjà dans les légendes..."; }
  else { rarity = "🟨 Légendaire"; comment = "Une aura mythique t'entoure, gardien des étoiles."; }

  set('heroPowerLevel', level + " / 100");
  set('heroRarity', rarity);
  set('heroComment', comment);
}

function restart() { location.reload(); }

// --- UTILITAIRES ---
function show(id) {
  ['intro','creator','heroCard','mission','result','ranking'].forEach(s => get(s).style.display='none');
  get(id).style.display='block';
  window.scrollTo(0,0);
}
function val(id){ return get(id).value.trim(); }
function set(id, txt){ get(id).innerText = txt; }
function get(id){ return document.getElementById(id); }

// --- ANIMATION DE FOND ---
const canvas = document.getElementById('bg');
const ctx = canvas.getContext('2d');
let particles = [];
resizeCanvas();
window.addEventListener('resize', resizeCanvas);

function resizeCanvas() { canvas.width = innerWidth; canvas.height = innerHeight; }
function createParticles(color) {
  particles = [];
  for (let i=0;i<60;i++) {
    particles.push({
      x:Math.random()*canvas.width,y:Math.random()*canvas.height,
      r:Math.random()*3+1,
      dx:(Math.random()-0.5)*1.5,dy:(Math.random()-0.5)*1.5,
      color
    });
  }
}
function animate() {
  ctx.clearRect(0,0,canvas.width,canvas.height);
  particles.forEach(p=>{
    ctx.beginPath();ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
    ctx.fillStyle=p.color;ctx.fill();
    p.x+=p.dx;p.y+=p.dy;
    if(p.x<0||p.x>canvas.width)p.dx*=-1;
    if(p.y<0||p.y>canvas.height)p.dy*=-1;
  });
  requestAnimationFrame(animate);
}
animate();

function changeBackground(power){
  let color='rgba(255,255,255,0.5)';
  if(power.includes('feu'))color='rgba(255,80,0,0.7)';
  else if(power.includes('vitesse'))color='rgba(255,255,0,0.7)';
  else if(power.includes('Technologie'))color='rgba(0,200,255,0.7)';
  else if(power.includes('Énergie'))color='rgba(150,0,255,0.7)';
  createParticles(color);
}

function playSound(){
  const a=new Audio('https://cdn.pixabay.com/download/audio/2022/03/15/audio_c17f61c367.mp3?filename=cinematic-whoosh-transition-1-14687.mp3');
  a.volume=0.3;a.play();
}
</script>

</body>
</html>
