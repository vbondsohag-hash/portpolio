<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Sohag Molla — Web Architect</title>
<meta name="description" content="Sohag Molla, Web Architect. I design and build fast, scalable web apps and AI-powered products.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700;12..96,800&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0b1a2e; --bg2:#10233d; --ink:#e8eef7; --muted:#9db0c9; --line:rgba(157,176,201,.22);
  --accent:#4cc9f0; --accent-ink:#06121f; --card:#0f2440;
  --head:"Bricolage Grotesque","Segoe UI",Arial,sans-serif; --body:"IBM Plex Sans","Segoe UI",Arial,sans-serif;
}
:root[data-theme="light"]{
  --bg:#f3f6fb; --bg2:#e8eef8; --ink:#0d1b2e; --muted:#4a5d78; --line:rgba(13,27,46,.18);
  --accent:#0b5fd6; --accent-ink:#fff; --card:#ffffff;
}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth;scroll-padding-top:80px}
body{font-family:var(--body);background:var(--bg);color:var(--ink);line-height:1.65;font-size:17px;transition:background .3s,color .3s}
h1,h2,h3{font-family:var(--head);line-height:1.1;letter-spacing:-.02em}
a{color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:3px}
.wrap{max-width:1080px;margin:0 auto;padding:0 24px}
section{padding:96px 0}
h2{font-size:clamp(2rem,4vw,2.9rem);margin-bottom:12px}
.lead{color:var(--muted);max-width:60ch;margin-bottom:40px}

/* Nav */
header{position:sticky;top:0;z-index:10;background:color-mix(in srgb,var(--bg) 88%,transparent);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
nav{display:flex;align-items:center;justify-content:space-between;height:64px}
.logo{font-family:var(--head);font-weight:800;text-decoration:none;font-size:1.15rem}
nav ul{display:flex;gap:26px;list-style:none;padding:0}
nav ul a{text-decoration:none;color:var(--muted);font-size:.95rem}
nav ul a:hover{color:var(--ink)}
.tools{display:flex;gap:10px;align-items:center}
.icon-btn{background:none;border:1px solid var(--line);color:var(--ink);border-radius:8px;width:40px;height:40px;cursor:pointer;font-size:1.05rem}
.icon-btn:hover{border-color:var(--accent)}
#menu{display:none}

/* Hero */
.hero{position:relative;overflow:hidden;padding:110px 0 100px;
  background-image:linear-gradient(var(--line) 1px,transparent 1px),linear-gradient(90deg,var(--line) 1px,transparent 1px);
  background-size:40px 40px;background-position:-1px -1px}
.hero::after{content:"";position:absolute;inset:0;background:radial-gradient(ellipse at 30% 40%,transparent 30%,var(--bg) 85%);pointer-events:none}
.hero .wrap{position:relative;z-index:1}
.hero p.hi{color:var(--accent);font-weight:500;margin-bottom:14px}
.hero h1{font-size:clamp(3rem,9vw,6.4rem);font-weight:800}
.hero h1 span{display:block;color:var(--muted);font-weight:500;font-size:.5em;margin-top:.25em}
.hero .intro{max-width:56ch;margin:26px 0 34px;font-size:1.15rem;color:var(--muted)}
.btns{display:flex;gap:14px;flex-wrap:wrap}
.btn{display:inline-block;padding:13px 26px;border-radius:8px;font-weight:500;text-decoration:none;border:1px solid var(--accent);transition:transform .15s}
.btn.primary{background:var(--accent);color:var(--accent-ink)}
.btn.ghost{color:var(--ink)}
.btn:hover{transform:translateY(-2px)}
.load{animation:rise .8s ease both}
.load:nth-child(2){animation-delay:.12s}.load:nth-child(3){animation-delay:.24s}.load:nth-child(4){animation-delay:.36s}
@keyframes rise{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:none}}

/* About */
.about{display:grid;grid-template-columns:1.4fr 1fr;gap:56px}
.about p+p{margin-top:16px}
.facts{border:1px solid var(--line);border-radius:12px;padding:26px;background:var(--card);align-self:start}
.facts h3{font-size:1.1rem;margin-bottom:14px}
.facts li{list-style:none;padding:10px 0;border-top:1px solid var(--line);color:var(--muted);font-size:.95rem}
.facts li:first-of-type{border-top:0}
.facts b{color:var(--ink);font-weight:500}

/* Skills */
.skills{background:var(--bg2)}
.groups{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:22px}
.group h3{font-size:1.05rem;margin-bottom:14px}
.tags{display:flex;flex-wrap:wrap;gap:8px}
.tags span{border:1px solid var(--line);background:var(--card);padding:6px 14px;border-radius:99px;font-size:.9rem}

/* Projects */
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:28px}
.card{background:var(--card);border:1px solid var(--line);border-radius:14px;overflow:hidden;display:flex;flex-direction:column;transition:transform .2s,border-color .2s}
.card:hover{transform:translateY(-4px);border-color:var(--accent)}
.shot{aspect-ratio:16/9;background:linear-gradient(135deg,var(--bg2),var(--bg));border-bottom:1px solid var(--line);display:flex;align-items:center;justify-content:center;padding:22px}
.mock{width:100%;height:100%;border:1px solid var(--line);border-radius:8px;background:var(--card);padding:10px;display:grid;gap:8px;grid-template-columns:1fr 2fr}
.mock i{display:block;border-radius:5px;background:var(--line)}
.mock i.a{background:var(--accent);opacity:.85}
.mock i.wide{grid-column:span 2}
.card .body{padding:26px;display:flex;flex-direction:column;gap:12px;flex:1}
.card h3{font-size:1.45rem}
.card p{color:var(--muted);font-size:.98rem}
.card .tags span{font-size:.8rem;padding:3px 11px}
.links{display:flex;gap:18px;margin-top:auto;padding-top:8px;font-weight:500}
.links a{color:var(--accent)}

/* Services */
.services{background:var(--bg2)}
.svc{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:22px}
.svc div{border-left:3px solid var(--accent);padding:4px 0 4px 18px}
.svc h3{font-size:1.2rem;margin-bottom:6px}
.svc p{color:var(--muted);font-size:.96rem}

/* Contact */
.contact{display:grid;grid-template-columns:1fr 1.2fr;gap:56px}
.contact ul{list-style:none;padding:0;display:grid;gap:12px;margin-top:22px}
.contact ul a{color:var(--accent);text-decoration:none;font-weight:500}
form{display:grid;gap:16px}
label{display:grid;gap:6px;font-size:.92rem;color:var(--muted)}
input,textarea{font:inherit;color:var(--ink);background:var(--card);border:1px solid var(--line);border-radius:8px;padding:12px 14px;width:100%}
input:focus,textarea:focus{outline:2px solid var(--accent);border-color:var(--accent)}
textarea{min-height:140px;resize:vertical}
button.btn{cursor:pointer;font:inherit;font-weight:500;justify-self:start}
#status{color:var(--accent);min-height:1.5em;font-size:.95rem}

footer{border-top:1px solid var(--line);padding:32px 0;color:var(--muted);font-size:.92rem}
footer .wrap{display:flex;justify-content:space-between;flex-wrap:wrap;gap:14px}
footer nav{height:auto;gap:20px}footer a{text-decoration:none}footer a:hover{color:var(--ink)}

@media(max-width:760px){
  nav ul{display:none;position:absolute;top:64px;left:0;right:0;flex-direction:column;gap:0;background:var(--bg);border-bottom:1px solid var(--line);padding:8px 24px}
  nav ul.open{display:flex}
  nav ul li a{display:block;padding:12px 0}
  #menu{display:inline-block}
  .about,.contact{grid-template-columns:1fr;gap:36px}
  section{padding:72px 0}
  .grid{grid-template-columns:1fr}
}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important;scroll-behavior:auto!important}}
</style>
</head>
<body>

<header>
  <div class="wrap">
    <nav aria-label="Main">
      <a class="logo" href="#top">Sohag Molla</a>
      <ul id="links">
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <div class="tools">
        <button class="icon-btn" id="theme" aria-label="Switch to light theme">☀</button>
        <button class="icon-btn" id="menu" aria-label="Open menu" aria-expanded="false">☰</button>
      </div>
    </nav>
  </div>
</header>

<main id="top">
<section class="hero">
  <div class="wrap">
    <p class="hi load">Hi, I'm</p>
    <h1 class="load">Sohag Molla<span>Web Architect</span></h1>
    <p class="intro load">I plan and build web products from the ground up: clean front ends, solid back ends, and AI features that people actually use.</p>
    <div class="btns load">
      <a class="btn primary" href="#projects">View projects</a>
      <a class="btn ghost" href="#contact">Contact me</a>
    </div>
  </div>
</section>

<section id="about">
  <div class="wrap about">
    <div>
      <h2>About me</h2>
      <p>I'm a web architect from Bangladesh. I start with the structure of a product (data, pages, APIs, performance) and then build it with the tool that fits, whether that's plain HTML, CSS and JavaScript, React, Next.js or Vue.</p>
      <p>I also work as an AI/ML engineer and context engineer. I connect language models to real product data, write the prompts and context they need, and test that the results hold up.</p>
      <p>Outside of work I read about system design, experiment with machine learning models, and tinker with side projects.</p>
    </div>
    <aside class="facts">
      <h3>Quick facts</h3>
      <ul>
        <li><b>Based in:</b> Bangladesh</li>
        <li><b>Focus:</b> Web apps, AI features</li>
        <li><b>Works with:</b> Startups and small teams</li>
        <li><b>Availability:</b> Open to freelance work</li>
      </ul>
    </aside>
  </div>
</section>

<section id="skills" class="skills">
  <div class="wrap">
    <h2>Skills</h2>
    <p class="lead">The tools I use most, grouped by what they do.</p>
    <div class="groups">
      <div class="group"><h3>Front end</h3><div class="tags"><span>HTML</span><span>CSS</span><span>JavaScript</span><span>React</span><span>Next.js</span><span>Vue</span></div></div>
      <div class="group"><h3>Back end and languages</h3><div class="tags"><span>Node.js</span><span>Python</span><span>C++</span><span>REST APIs</span></div></div>
      <div class="group"><h3>AI and machine learning</h3><div class="tags"><span>ML engineering</span><span>Context engineering</span><span>Prompt design</span><span>LLM apps</span></div></div>
      <div class="group"><h3>Workflow</h3><div class="tags"><span>Git</span><span>GitHub</span><span>Responsive design</span><span>Performance</span></div></div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <h2>Projects</h2>
    <p class="lead">Two projects I'm proud of. Replace the text, screenshots and links with your own.</p>
    <div class="grid">
      <article class="card">
        <div class="shot" role="img" aria-label="Dashboard layout preview"><div class="mock"><i class="a"></i><i></i><i></i><i class="wide"></i></div></div>
        <div class="body">
          <h3>Insight Dashboard</h3>
          <p>A analytics dashboard that turns raw sales data into charts and weekly summaries. It includes role-based login, CSV upload, and an AI assistant that answers questions about the data.</p>
          <div class="tags"><span>Next.js</span><span>React</span><span>Node.js</span><span>Python</span></div>
          <div class="links"><a href="#" target="_blank" rel="noopener">Live demo</a><a href="https://github.com/" target="_blank" rel="noopener">Source code</a></div>
        </div>
      </article>
      <article class="card">
        <div class="shot" role="img" aria-label="Chat interface preview"><div class="mock"><i></i><i class="a"></i><i class="wide"></i><i class="wide"></i></div></div>
        <div class="body">
          <h3>DocuChat AI</h3>
          <p>A chat app that answers questions from uploaded PDF files. I designed the context pipeline that splits documents, finds the right passages, and gives the model only what it needs.</p>
          <div class="tags"><span>Vue</span><span>Python</span><span>LLM</span><span>Vector search</span></div>
          <div class="links"><a href="#" target="_blank" rel="noopener">Live demo</a><a href="https://github.com/" target="_blank" rel="noopener">Source code</a></div>
        </div>
      </article>
    </div>
  </div>
</section>

<section id="services" class="services">
  <div class="wrap">
    <h2>Services</h2>
    <p class="lead">How I can help your team or business.</p>
    <div class="svc">
      <div><h3>Website and web app development</h3><p>Fast, responsive sites built with plain HTML/CSS/JS, React, Next.js or Vue.</p></div>
      <div><h3>Architecture and code review</h3><p>A clear plan for structure, data flow and performance before you build.</p></div>
      <div><h3>AI feature integration</h3><p>Chatbots, search and document tools powered by language models.</p></div>
      <div><h3>Context engineering</h3><p>Prompts, retrieval and evaluation so your AI gives reliable answers.</p></div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap contact">
    <div>
      <h2>Contact me</h2>
      <p class="lead">Tell me about your project and I'll reply by email.</p>
      <ul>
        <li><a href="mailto:you@example.com">you@example.com</a></li>
        <li><a href="https://github.com/your-username" target="_blank" rel="noopener">GitHub</a></li>
        <li><a href="https://www.linkedin.com/in/your-username" target="_blank" rel="noopener">LinkedIn</a></li>
      </ul>
    </div>
    <form id="form">
      <label>Name<input name="name" required autocomplete="name"></label>
      <label>Email<input name="email" type="email" required autocomplete="email"></label>
      <label>Message<textarea name="message" required></textarea></label>
      <button class="btn primary" type="submit">Send message</button>
      <p id="status" role="status"></p>
    </form>
  </div>
</section>
</main>

<footer>
  <div class="wrap">
    <span>© <span id="year"></span> Sohag Molla. All rights reserved.</span>
    <nav aria-label="Footer"><a href="#about">About</a><a href="#projects">Projects</a><a href="#contact">Contact</a><a href="https://github.com/your-username" target="_blank" rel="noopener">GitHub</a><a href="https://www.linkedin.com/in/your-username" target="_blank" rel="noopener">LinkedIn</a></nav>
  </div>
</footer>

<script>
const root=document.documentElement, themeBtn=document.getElementById('theme');
function setTheme(t){
  root.dataset.theme=t;
  themeBtn.textContent=t==='dark'?'☀':'☾';
  themeBtn.setAttribute('aria-label',t==='dark'?'Switch to light theme':'Switch to dark theme');
  try{localStorage.setItem('theme',t)}catch(e){}
}
let saved=null;try{saved=localStorage.getItem('theme')}catch(e){}
setTheme(saved||(matchMedia('(prefers-color-scheme: light)').matches?'light':'dark'));
themeBtn.onclick=()=>setTheme(root.dataset.theme==='dark'?'light':'dark');

const menu=document.getElementById('menu'), links=document.getElementById('links');
menu.onclick=()=>{const o=links.classList.toggle('open');menu.setAttribute('aria-expanded',o);};
links.querySelectorAll('a').forEach(a=>a.onclick=()=>{links.classList.remove('open');menu.setAttribute('aria-expanded',false);});

document.getElementById('year').textContent=new Date().getFullYear();

// Contact form: opens the visitor's email app. Replace the address below.
document.getElementById('form').addEventListener('submit',e=>{
  e.preventDefault();
  const f=new FormData(e.target);
  const body=encodeURIComponent(`${f.get('message')}\n\nFrom: ${f.get('name')} (${f.get('email')})`);
  location.href=`mailto:you@example.com?subject=${encodeURIComponent('Portfolio message from '+f.get('name'))}&body=${body}`;
  document.getElementById('status').textContent='Opening your email app to send the message.';
});
</script>
</body>
</html>
