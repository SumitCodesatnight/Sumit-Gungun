<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gungun ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ffe6f0, #ffd6eb);
  overflow: hidden;
  height: 100vh;
}

/* Floating hearts */
.heart {
  position: absolute;
  color: rgba(255, 0, 102, 0.3);
  font-size: 20px;
  animation: float 8s linear infinite;
}
@keyframes float {
  from { transform: translateY(100vh); }
  to { transform: translateY(-10vh); }
}

.container {
  text-align: center;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  padding: 20px;
}

h1 {
  color: #ff2e7a;
  font-size: 2.2rem;
}

p {
  font-size: 1.1rem;
  color: #444;
}

.buttons {
  margin-top: 30px;
  position: relative;
}

button {
  border: none;
  padding: 15px 28px;
  font-size: 1rem;
  border-radius: 30px;
  cursor: pointer;
  transition: 0.3s;
}

#yesBtn {
  background: linear-gradient(45deg, #ff2e7a, #ff6fa5);
  color: white;
  box-shadow: 0 6px 15px rgba(255, 46, 122, 0.4);
}

#noBtn {
  background: white;
  color: #555;
  position: absolute;
  left: 60%;
  top: 0;
  box-shadow: 0 6px 15px rgba(0,0,0,0.1);
}

.popup {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.6);
  display: none;
  align-items: center;
  justify-content: center;
}

.popup-content {
  background: white;
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  animation: pop 0.4s ease;
}

@keyframes pop {
  from { transform: scale(0.7); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}
</style>
</head>

<body>

<!-- Floating hearts -->
<script>
for(let i=0;i<25;i++){
  const heart=document.createElement("div");
  heart.className="heart";
  heart.innerHTML="❤️";
  heart.style.left=Math.random()*100+"vw";
  heart.style.fontSize=(12+Math.random()*20)+"px";
  heart.style.animationDuration=(5+Math.random()*5)+"s";
  document.body.appendChild(heart);
}
</script>

<div class="container">
  <h1>Gungun 💖</h1>
  <p>Will you be my Valentine? 🥺</p>

  <div class="buttons">
    <button id="yesBtn">Yes 💕</button>
    <button id="noBtn">No</button>
  </div>

  <p id="message" style="margin-top:20px;color:#ff2e7a;font-weight:500;"></p>
</div>

<div class="popup" id="popup">
  <div class="popup-content">
    <h2>Yayyy Gungun 😍</h2>
    <p>
      You just made my world brighter 💖  
      I promise lots of smiles, hugs,  
      and endless love ❤️  
    </p>
    <p>Happy Valentine’s Day my love 🌸</p>
  </div>
</div>

<script>
const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");
const message = document.getElementById("message");
const popup = document.getElementById("popup");

const texts = [
  "Really?? 🥺",
  "Gunnu please 😘",
  "Think again 💞",
  "I’ll be sad 💔",
  "Pretty please 🥹",
  "You can’t say no 😝",
  "Just press yes 😍"
];

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("click", moveButton);

function moveButton(){
  const x = Math.random()*70;
  const y = Math.random()*50;
  noBtn.style.left = x+"%";
  noBtn.style.top = y+"%";
  message.textContent = texts[Math.floor(Math.random()*texts.length)];
}

yesBtn.addEventListener("click", ()=>{
  popup.style.display="flex";
});
</script>

</body>
</html>
