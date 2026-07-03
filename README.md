<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Quest ❤️</title>

<style>

body{
margin:0;
background:#111827;
font-family:Arial,Helvetica,sans-serif;
color:white;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
overflow:hidden;
}

.container{
width:90%;
max-width:700px;
background:#1f2937;
padding:30px;
border-radius:20px;
box-shadow:0 0 25px rgba(255,0,90,.4);
text-align:center;
}

h1{
color:#ff5c8a;
}

button{
padding:15px 30px;
margin-top:20px;
font-size:18px;
background:#ff5c8a;
border:none;
border-radius:10px;
color:white;
cursor:pointer;
transition:.3s;
}

button:hover{
transform:scale(1.05);
}

.choice{
display:block;
width:100%;
margin:10px auto;
}

#game{
font-size:22px;
line-height:1.6;
}

.progress{
height:12px;
background:#444;
border-radius:20px;
overflow:hidden;
margin-bottom:25px;
}

.bar{
height:100%;
width:0%;
background:#ff5c8a;
transition:.5s;
}

</style>

</head>

<body>

<div class="container">

<h1>🎮 LOVE QUEST ❤️</h1>

<div class="progress">
<div class="bar" id="bar"></div>
</div>

<div id="game">

Welcome Player...

<br><br>

Your mission is simple.

Unlock the heart of the cutest girlfriend. ❤️

<br><br>

<button onclick="next()">Start Game</button>

</div>

</div>

<script>

let level=0;

const game=document.getElementById("game");
const bar=document.getElementById("bar");

function progress(x){
bar.style.width=x+"%";
}

function next(answer){

if(level===0){

progress(20);

game.innerHTML=`
<h2>Level 1</h2>

Who is the prettiest girl?

<button class="choice" onclick="next('wrong')">Taylor Swift</button>

<button class="choice" onclick="next('correct')">Sasmita ❤️</button>

<button class="choice" onclick="next('wrong')">My Neighbour</button>
`;

level++;

}

else if(level===1){

if(answer==="correct"){

progress(45);

game.innerHTML=`
<h2>Level 2</h2>

Choose tonight's date.

<button class="choice" onclick="next('pizza')">🍕 Pizza Date</button>

<button class="choice" onclick="next('movie')">🎬 Movie Night</button>

<button class="choice" onclick="next('both')">Both 😌</button>
`;

level++;

}else{

alert("❌ Wrong Answer! Try Again 😂");

}

}

else if(level===2){

progress(70);

game.innerHTML=`
<h2>Level 3</h2>

What's my comfort food?

<button class="choice" onclick="next('wrong2')">Burger</button>

<button class="choice" onclick="next('right2')">Maggie 🍜</button>

<button class="choice" onclick="next('wrong2')">Salad</button>
`;

level++;

}

else if(level===3){

if(answer==="right2"){

progress(100);

game.innerHTML=`

<h1>🏆 YOU WON!</h1>

<h2>Achievement Unlocked</h2>

❤️ World's Best Boyfriend ❤️

<p>

You completed Love Quest.

Reward:

<br><br>

💌 Unlimited Hugs

<br>

💋 Unlimited Kisses

<br>

❤️ My Heart (Already Yours)

</p>

<button onclick="location.reload()">

Play Again

</button>

`;

}else{

alert("😂 Nope! You should know this!");

}

}

}

</script>

</body>
</html>
