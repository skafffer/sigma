# r  
  
<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
  
<title>Isaac | boy.rip</title>  
  
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">  
  
<script src="https://cdn.jsdelivr.net/npm/tsparticles@2/tsparticles.bundle.min.js"></script>  
  
<style>  
  
*{  
margin:0;  
padding:0;  
box-sizing:border-box;  
font-family:'Inter',sans-serif;  
}  
  
body{  
height:100vh;  
display:flex;  
align-items:center;  
justify-content:center;  
background:#050505;  
color:white;  
overflow:hidden;  
}  
  
/* particle background */  
  
#particles{  
position:fixed;  
width:100%;  
height:100%;  
z-index:0;  
}  
  
/* glass card */  
  
.card{  
  
position:relative;  
z-index:2;  
  
width:380px;  
  
padding:40px;  
  
border-radius:18px;  
  
background:rgba(20,20,20,0.45);  
  
backdrop-filter:blur(25px);  
  
border:1px solid rgba(160,90,255,0.25);  
  
box-shadow:  
0 0 40px rgba(140,60,255,.15),  
0 10px 40px rgba(0,0,0,.6);  
  
text-align:center;  
  
}  
  
/* name */  
  
.name{  
  
font-size:40px;  
font-weight:600;  
letter-spacing:1px;  
  
}  
  
.domain{  
  
opacity:.5;  
margin-top:4px;  
font-size:14px;  
  
}  
  
/* typing title */  
  
.title{  
  
margin-top:10px;  
font-size:16px;  
color:#b78cff;  
letter-spacing:1px;  
  
}  
  
.cursor{  
  
display:inline-block;  
width:2px;  
background:#b78cff;  
margin-left:4px;  
animation:blink 1s infinite;  
  
}  
  
@keyframes blink{  
0%,100%{opacity:1}  
50%{opacity:0}  
}  
  
/* buttons */  
  
.buttons{  
  
margin-top:36px;  
display:flex;  
flex-direction:column;  
gap:14px;  
  
}  
  
.btn{  
  
position:relative;  
  
padding:14px;  
  
border-radius:10px;  
  
background:rgba(30,30,30,0.55);  
  
border:1px solid rgba(150,90,255,0.2);  
  
color:white;  
  
font-size:15px;  
  
cursor:pointer;  
  
transition:.25s;  
  
overflow:hidden;  
  
}  
  
/* glow hover */  
  
.btn:hover{  
  
transform:translateY(-4px);  
  
border-color:#8b5cf6;  
  
box-shadow:0 10px 30px rgba(139,92,246,.4);  
  
}  
  
/* animated shine */  
  
.btn::before{  
  
content:"";  
  
position:absolute;  
  
top:0;  
left:-100%;  
  
width:100%;  
height:100%;  
  
background:linear-gradient(  
120deg,  
transparent,  
rgba(180,120,255,.35),  
transparent  
);  
  
transition:.6s;  
  
}  
  
.btn:hover::before{  
  
left:100%;  
  
}  
  
/* toast */  
  
.toast{  
  
position:fixed;  
  
bottom:40px;  
  
background:rgba(25,25,25,.8);  
  
border:1px solid #8b5cf6;  
  
padding:12px 18px;  
  
border-radius:8px;  
  
font-size:14px;  
  
opacity:0;  
  
transform:translateY(20px);  
  
transition:.3s;  
  
}  
  
.toast.show{  
  
opacity:1;  
transform:translateY(0);  
  
}  
  
</style>  
</head>  
<body>  
  
<div id="particles"></div>  
  
<div class="card">  
  
<div class="name">Isaac</div>  
  
<div class="domain">boy.rip</div>  
  
<div class="title">  
<span id="typing"></span><span class="cursor"></span>  
</div>  
  
<div class="buttons">  
  
<button class="btn" onclick="copy('telegram_user')">  
Telegram  
</button>  
  
<button class="btn" onclick="openLink('https://roblox.com/users/YOURID')">  
Roblox  
</button>  
  
<button class="btn" onclick="openLink('https://spotify.com/user/YOURNAME')">  
Spotify  
</button>  
  
<button class="btn" onclick="openLink('https://tiktok.com/@USERNAME')">  
TikTok  
</button>  
  
<button class="btn" onclick="copy('snap_user')">  
Snapchat  
</button>  
  
<button class="btn" onclick="copy('your@email.com')">  
Gmail  
</button>  
  
</div>  
  
</div>  
  
<div id="toast" class="toast"></div>  
  
<script>  
  
/* typing animation */  
  
const text = "Fullstack Developer"  
  
let i = 0  
  
function type(){  
  
if(i < text.length){  
  
document.getElementById("typing").innerHTML += text.charAt(i)  
  
i++  
  
setTimeout(type,80)  
  
}  
  
}  
  
type()  
  
/* copy function */  
  
function copy(text){  
  
navigator.clipboard.writeText(text)  
  
let toast=document.getElementById("toast")  
  
toast.innerText="Copied: "+text  
  
toast.classList.add("show")  
  
setTimeout(()=>{  
toast.classList.remove("show")  
},2000)  
  
}  
  
function openLink(url){  
window.open(url,"_blank")  
}  
  
/* particles */  
  
tsParticles.load("particles",{  
  
particles:{  
  
number:{value:70},  
  
color:{value:"#8b5cf6"},  
  
links:{  
enable:true,  
distance:140,  
color:"#8b5cf6",  
opacity:0.3  
},  
  
move:{  
enable:true,  
speed:1  
},  
  
opacity:{  
value:0.5  
},  
  
size:{  
value:2  
}  
  
},  
  
background:{  
color:"transparent"  
}  
  
})  
  
</script>  
  
</body>  
</html>  
