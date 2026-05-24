<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Response London</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI',sans-serif;
}

body{
    overflow-x:hidden;
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(-45deg,
    #ff0000,#ff7300,#ffee00,#00ff88,
    #00e1ff,#0051ff,#8a2be2,#ff00ff);
    background-size:400% 400%;
    animation:bg 12s ease infinite;
}

@keyframes bg{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

.container{
    width:90%;
    max-width:1000px;
    text-align:center;
    padding:40px;
    border-radius:30px;
    background:rgba(255,255,255,0.08);
    backdrop-filter:blur(20px);
    box-shadow:
    0 0 30px rgba(255,255,255,.3),
    0 0 80px rgba(0,255,255,.2);
}

.logo{
    font-size:90px;
    animation:spin 8s linear infinite;
    text-shadow:
    0 0 20px white,
    0 0 40px cyan,
    0 0 80px magenta;
}

@keyframes spin{
    from{transform:rotateY(0deg);}
    to{transform:rotateY(360deg);}
}

h1{
    color:white;
    font-size:65px;
    margin-top:10px;
    text-transform:uppercase;
    letter-spacing:5px;
    animation:rainbow 5s linear infinite;
    text-shadow:
    0 0 10px white,
    0 0 30px cyan,
    0 0 60px magenta;
}

@keyframes rainbow{
    from{filter:hue-rotate(0deg);}
    to{filter:hue-rotate(360deg);}
}

.description{
    color:white;
    margin-top:15px;
    font-size:20px;
}

.buttons{
    margin-top:35px;
}

.btn{
    display:inline-block;
    margin:10px;
    padding:18px 35px;
    text-decoration:none;
    color:white;
    font-weight:bold;
    border-radius:50px;
    transition:0.3s;
    font-size:18px;
}

.roblox{
    background:linear-gradient(90deg,#00e1ff,#0066ff);
}

.discord{
    background:linear-gradient(90deg,#5865F2,#9c27b0);
}

.btn:hover{
    transform:scale(1.1);
    box-shadow:
    0 0 20px white,
    0 0 40px cyan;
}

.staff-title{
    color:white;
    margin-top:40px;
    font-size:35px;
}

.staff{
    margin-top:20px;
}

.member{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:18px;
    margin:12px 0;
    border-radius:15px;
    background:rgba(255,255,255,.12);
    color:white;
    font-size:20px;
    transition:0.3s;
}

.member:hover{
    transform:translateX(10px);
    box-shadow:0 0 20px rgba(255,255,255,.4);
}

.particles{
    position:fixed;
    inset:0;
    pointer-events:none;
}

.circle{
    position:absolute;
    border-radius:50%;
    background:rgba(255,255,255,.15);
    animation:float linear infinite;
}

@keyframes float{
    from{
        transform:translateY(110vh) scale(0);
    }
    to{
        transform:translateY(-120vh) scale(1);
    }
}
</style>
</head>
<body>

<div class="particles" id="particles"></div>

<div class="container">

    <div class="logo">🎮</div>

    <h1>Response London</h1>

    <p class="description">
        Welcome to the official Response London community.
        Join the game, meet the staff team and become part
        of the adventure.
    </p>

    <div class="buttons">

        <a class="btn roblox"
        href="https://www.roblox.com/games/71350675430720/Response-London"
        target="_blank">
        🎮 Play Roblox
        </a>

        <a class="btn discord"
        href="https://discord.gg/UFhpVPVK"
        target="_blank">
        💬 Join Discord
        </a>

    </div>

    <h2 class="staff-title">👑 Staff Team</h2>

    <div class="staff">

        <div class="member">
            <span>Nadz</span>
            <span>Lead Developer</span>
        </div>

        <div class="member">
            <span>Raz</span>
            <span>Community Support</span>
        </div>

        <div class="member">
            <span>PETE</span>
            <span>Community Manager</span>
        </div>

        <div class="member">
            <span>Alex</span>
            <span>Founder</span>
        </div>

    </div>

</div>

<script>
const particles=document.getElementById("particles");

for(let i=0;i<60;i++){

    const c=document.createElement("div");

    c.classList.add("circle");

    let size=Math.random()*80+20;

    c.style.width=size+"px";
    c.style.height=size+"px";

    c.style.left=Math.random()*100+"vw";

    c.style.animationDuration=
    (Math.random()*12+5)+"s";

    particles.appendChild(c);
}
</script>

</body>
</html>
