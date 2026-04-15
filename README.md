!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tanay Mourya | Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
scroll-behavior:smooth;
}

body{
background:#0f172a;
color:white;
}

/* NAVBAR */

nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 8%;
background:rgba(0,0,0,0.5);
position:fixed;
width:100%;
top:0;
backdrop-filter:blur(10px);
z-index:1000;
}

nav h2{
color:#38bdf8;
}

nav a{
color:white;
margin:0 15px;
text-decoration:none;
transition:0.3s;
}

nav a:hover{
color:#38bdf8;
}

/* HERO */

.hero{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
background:linear-gradient(135deg,#0f172a,#1e293b);
}

.hero h1{
font-size:60px;
}

.hero span{
color:#38bdf8;
}

.typing{
margin-top:10px;
font-size:22px;
color:#94a3b8;
}

.btn{
margin-top:25px;
padding:12px 30px;
border:none;
border-radius:30px;
background:#38bdf8;
cursor:pointer;
font-weight:bold;
transition:0.3s;
}

.btn:hover{
transform:scale(1.1);
}

/* SECTION */

section{
padding:100px 8%;
}

.title{
text-align:center;
font-size:40px;
margin-bottom:50px;
color:#38bdf8;
}

/* ABOUT */

.about-container{
display:flex;
align-items:center;
gap:40px;
flex-wrap:wrap;
}

.about img{
width:250px;
border-radius:20px;
}

.about-text{
flex:1;
color:#cbd5f5;
line-height:1.8;
}

/* SKILLS */

.skill{
margin-bottom:20px;
}

.bar{
height:8px;
background:#334155;
border-radius:10px;
margin-top:5px;
}

.progress{
height:8px;
background:#38bdf8;
border-radius:10px;
}

/* PROJECTS */

.projects{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:25px;
}

.card{
background:#1e293b;
padding:20px;
border-radius:15px;
transition:0.3s;
}

.card:hover{
transform:translateY(-10px);
}

.card button{
margin-top:10px;
padding:8px 15px;
border:none;
background:#38bdf8;
cursor:pointer;
}

/* SERVICES */

.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.service{
background:#1e293b;
padding:20px;
border-radius:15px;
text-align:center;
}

/* CONTACT */

form{
max-width:500px;
margin:auto;
display:flex;
flex-direction:column;
gap:15px;
}

input,textarea{
padding:10px;
border:none;
border-radius:5px;
}

/* FOOTER */

footer{
text-align:center;
padding:20px;
background:#020617;
}

</style>

</head>

<body>

<!-- NAVBAR -->

<nav>
<h2>Tanay</h2>
<div>
<a href="#about">About</a>
<a href="#skills">Skills</a>
<a href="#projects">Projects</a>
<a href="#services">Services</a>
<a href="#contact">Contact</a>
</div>
</nav>

<!-- HERO -->

<div class="hero">
<h1>Hi, I'm <span>Tanay Mourya</span></h1>
<div class="typing" id="typing"></div>
<button class="btn" onclick="scrollToSection('projects')">Explore Work</button>
</div>

<!-- ABOUT -->

<section id="about">
<h2 class="title">About Me</h2>

<div class="about-container">

<img src="https://via.placeholder.com/250" alt="profile">

<div class="about-text">
I am a B.Tech 3rd year student passionate about web development and content creation.
I create modern websites and engaging content. My goal is to become a professional developer.
</div>

</div>

</section>

<!-- SKILLS -->

<section id="skills">
<h2 class="title">Skills</h2>

<div class="skill">HTML<div class="bar"><div class="progress" style="width:90%"></div></div></div>
<div class="skill">CSS<div class="bar"><div class="progress" style="width:85%"></div></div></div>
<div class="skill">JavaScript<div class="bar"><div class="progress" style="width:75%"></div></div></div>

</section>

<!-- PROJECTS -->

<section id="projects">
<h2 class="title">Projects</h2>

<div class="projects">

<div class="card">
<h3>Portfolio Website</h3>
<p>Modern portfolio with animations.</p>
<button>View</button>
</div>

<div class="card">
<h3>Steganography</h3>
<p>Hidden data inside images.</p>
<button>View</button>
</div>

<div class="card">
<h3>Web App</h3>
<p>Interactive JavaScript app.</p>
<button>View</button>
</div>

</div>

</section>

<!-- SERVICES -->

<section id="services">
<h2 class="title">Services</h2>

<div class="services">

<div class="service">Web Development</div>
<div class="service">UI Design</div>
<div class="service">Content Creation</div>

</div>

</section>

<!-- CONTACT -->

<section id="contact">
<h2 class="title">Contact</h2>

<form>
<input type="text" placeholder="Your Name">
<input type="email" placeholder="Your Email">
<textarea rows="4" placeholder="Message"></textarea>
<button class="btn">Send</button>
</form>

</section>

<footer>
<p>© 2026 Tanay Mourya | All Rights Reserved</p>
</footer>

<!-- JS -->

<script>

const text = ["Web Developer", "Content Creator", "Freelancer"];
let i=0,j=0,current="",isDeleting=false;

function type(){
current=text[i];
if(!isDeleting){
document.getElementById("typing").innerHTML=current.substring(0,j++);
if(j>current.length){isDeleting=true;setTimeout(type,1000);return;}
}else{
document.getElementById("typing").innerHTML=current.substring(0,j--);
if(j==0){isDeleting=false;i=(i+1)%text.length;}
}
setTimeout(type,isDeleting?50:100);
}

type();

function scrollToSection(id){
document.getElementById(id).scrollIntoView();
}

</script>

</body>
</html>
