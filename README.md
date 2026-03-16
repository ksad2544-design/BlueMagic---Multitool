50 star for the full src
<!DOCTYPE html>
<html>
<head>
<title>Game Diamond</title>
<style>
body{font-family:Arial;text-align:center;background:#111;color:#fff}
button{padding:10px;margin:10px}
</style>
</head>

<body>

<h1>Game Diamond</h1>

<div id="login">
<input type="text" id="username" placeholder="Masukkan Username">
<button onclick="login()">Login</button>
</div>

<div id="game" style="display:none">
<h2>Halo <span id="user"></span></h2>
<p>Diamond: <span id="diamond">0</span></p>

<button onclick="mainGame()">Main Game (+10 Diamond)</button>
<button onclick="topup()">Top Up 100 Diamond</button>
</div>

<script>

let diamond = 0;

function login(){
let username = document.getElementById("username").value;

if(username==""){
alert("Masukkan username");
return;
}

document.getElementById("login").style.display="none";
document.getElementById("game").style.display="block";
document.getElementById("user").innerText=username;
}

function mainGame(){
diamond += 10;
updateDiamond();
}

function topup(){
diamond += 100;
updateDiamond();
}

function updateDiamond(){
document.getElementById("diamond").innerText=diamond;
}

</script>

</body>
</html>
