<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Plataforma Educativa PWA</title>
<link rel="manifest" href="manifest.json">
<link rel="stylesheet" href="css/style.css">
</head>
<body>

<header>
<h1>📚 Escola Offline</h1>
</header>

<nav>
<button onclick="show('home')">Início</button>
<button onclick="show('biblioteca')">Biblioteca</button>
<button onclick="show('aulas')">Aulas</button>
<button onclick="show('quiz')">Exercícios</button>
<button onclick="show('relatorios')">Relatórios</button>
</nav>

<main>
<section id="home">
<h2>Login do Aluno</h2>
<input id="user" placeholder="Nome do aluno">
<button onclick="login()">Entrar</button>
<p id="userDisplay"></p>
</section>

<section id="biblioteca" class="hidden">
<h2>Biblioteca</h2>
<iframe src="assets/exemplo.pdf"></iframe>
<video controls>
<source src="assets/video.mp4" type="video/mp4">
</video>
</section>

<section id="aulas" class="hidden">
<h2>Aulas</h2>
<div id="listaAulas"></div>
</section>

<section id="quiz" class="hidden">
<h2>Exercícios</h2>
<div id="quizBox"></div>
</section>

<section id="relatorios" class="hidden">
<h2>Relatórios</h2>
<p id="relatorio"></p>
</section>
</main>

<script src="js/app.js"></script>
</body>
</html>


<!-- ===================== css/style.css ===================== -->
body { font-family: Arial; margin:0; background:#eef; }
header { background:#2c3e50; color:white; text-align:center; padding:1rem; }
nav { display:flex; flex-wrap:wrap; }
nav button { flex:1; padding:1rem; border:none; background:#34495e; color:white; }
.hidden { display:none; }
main { padding:1rem; }
button { margin:5px; padding:10px; }


<!-- ===================== js/app.js ===================== -->
function show(id){
 document.querySelectorAll('section').forEach(s=>s.classList.add('hidden'));
 document.getElementById(id).classList.remove('hidden');
}

// LOGIN
function login(){
 let user = document.getElementById('user').value;
 localStorage.setItem('user', user);
 document.getElementById('userDisplay').innerText = 'Aluno: '+user;
}

// AULAS
const aulas=[
 {disc:'Matemática', conteudo:'Soma básica'},
 {disc:'Português', conteudo:'Leitura'}
];

function carregarAulas(){
 let div=document.getElementById('listaAulas');
 aulas.forEach(a=>{
  let el=document.createElement('div');
  el.innerHTML=`<b>${a.disc}</b>: ${a.conteudo}`;
  div.appendChild(el);
 });
}
carregarAulas();

// QUIZ
const quiz=[
 {q:'2+2?', a:['3','4'], c:1},
 {q:'Capital da Guiné-Bissau?', a:['Bissau','Dakar'], c:0}
];
let i=0,score=0;
function loadQuiz(){
 let box=document.getElementById('quizBox');
 if(i>=quiz.length){
  localStorage.setItem('score',score);
  box.innerHTML=`Resultado: ${score}`;
  gerarRelatorio();
  return;
 }
 let q=quiz[i];
 box.innerHTML=`<p>${q.q}</p>`;
 q.a.forEach((opt,idx)=>{
  let b=document.createElement('button');
  b.innerText=opt;
  b.onclick=()=>{ if(idx==q.c) score++; i++; loadQuiz(); };
  box.appendChild(b);
 });
}
loadQuiz();

// RELATÓRIO
function gerarRelatorio(){
 let user=localStorage.getItem('user');
 let score=localStorage.getItem('score');
 document.getElementById('relatorio').innerText=
 `Aluno: ${user} | Pontuação: ${score}`;
}

// SERVICE WORKER
if('serviceWorker' in navigator){
 navigator.serviceWorker.register('sw.js');
}


<!-- ===================== manifest.json ===================== -->
{
 "name": "Escola Offline",
 "short_name": "Escola",
 "start_url": "index.html",
 "display": "standalone",
 "background_color": "#ffffff",
 "theme_color": "#2c3e50",
 "icons": []
}


<!-- ===================== sw.js ===================== -->
const CACHE='pwa-escola-v1';
const FILES=[
 '/',
 'index.html',
 'css/style.css',
 'js/app.js'
];
self.addEventListener('install',e=>{
 e.waitUntil(caches.open(CACHE).then(c=>c.addAll(FILES)));
});
self.addEventListener('fetch',e=>{
 e.respondWith(caches.match(e.request).then(r=>r||fetch(e.request)));
});
