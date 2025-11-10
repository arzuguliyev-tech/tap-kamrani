<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Three Cup Monte</title>
<style>
body { 
    background: #111; 
    color: #fff; 
    font-family: sans-serif; 
    display: flex; 
    flex-direction: column; 
    align-items: center; 
    justify-content: center; 
    min-height: 100vh; 
    margin: 0; 
}
h1 { text-align: center; }
.game { 
    display: flex; 
    gap: 20px; 
    perspective: 1000px; 
    flex-wrap: wrap;
    justify-content: center;
}
.box { 
    width: 120px; 
    height: 150px; 
    background: #444; 
    border: 3px solid #888; 
    border-radius: 10px; 
    display: flex; 
    align-items: flex-end; 
    justify-content: center; 
    cursor: pointer; 
    position: relative; 
    transition: transform 0.5s ease, border 0.3s, background 0.3s; 
    box-shadow: 0 8px 15px rgba(0,0,0,0.5); 
}
.box:hover { transform: translateY(-10px); }
.ball { 
    width: 150px; 
    height: 150px; 
    display: none; 
    position: absolute; 
    bottom: -25px; 
    border-radius: 50%; 
    object-fit: cover; 
    transition: transform 0.3s ease; 
}
.highlight { border-color: yellow; }
.wrong { 
    border-color: red; 
    animation: shake 0.3s;
}
@keyframes shake {
    0% { transform: translateX(0); }
    25% { transform: translateX(-5px); }
    50% { transform: translateX(5px); }
    75% { transform: translateX(-5px); }
    100% { transform: translateX(0); }
}
#message { margin-top: 20px; font-size: 18px; text-align:center; }
#score { margin-top: 10px; font-size: 20px; }
#restartBtn { 
    margin-top: 15px; 
    padding: 10px 20px; 
    font-size: 16px; 
    border: none; 
    border-radius: 5px; 
    cursor: pointer; 
    background-color: #28a745; 
    color: white; 
}
@media (max-width: 500px) {
    .box { width: 80px; height: 100px; }
    .ball { width: 100px; height: 100px; bottom: -20px; }
}
</style>
</head>
<body>

<h1>Tap Kamranı, Qazan pulu</h1>
<div class="game" id="game">
    <div class="box" data-index="0"><img class="ball" src="kamran1.jpg"></div>
    <div class="box" data-index="1"><img class="ball" src="kamran1.jpg"></div>
    <div class="box" data-index="2"><img class="ball" src="kamran1.jpg"></div>
</div>
<div id="message">Oyuna başla — bir qutu seç.</div>
<div id="score">Xal: 0</div>
<button id="restartBtn">Yenidən Başlat</button>

<script>
let correctBox;
let boxes = document.querySelectorAll('.box');
let gameLocked = true;
let score = 0;
const message = document.getElementById('message');
const scoreEl = document.getElementById('score');
const restartBtn = document.getElementById('restartBtn');

// Səs faylları
const startSound = new Audio('start.mp3'); // start səsi
const correctSound = new Audio('qeseng.mp3'); // düzgün qutu səsi
const wrongSounds = [ new Audio('gozlerin.mp3'), new Audio('suur.mp3') ]; // səhv qutu səsi

function delay(ms) { return new Promise(res => setTimeout(res, ms)); }

async function startGame() {
    correctBox = Math.floor(Math.random() * 3);
    boxes.forEach(b => {
        b.querySelector('.ball').style.display = 'none';
        b.classList.remove('highlight', 'wrong');
    });
    gameLocked = true;
    let ball = boxes[correctBox].querySelector('.ball');
    ball.style.display = 'block';
    message.textContent = 'Topu yadda saxla!';
    await delay(1000);
    ball.style.display = 'none';
    message.textContent = 'Qutular qarışdırılır...';
    await shuffleBoxes();
    gameLocked = false;
    message.textContent = 'İndi bir qutu seç!';
}

// Qutuları qarışdır
async function shuffleBoxes() {
    let times = 12;
    for (let i = 0; i < times; i++) {
        let a = Math.floor(Math.random() * 3);
        let b = Math.floor(Math.random() * 3);
        while(a===b) b=Math.floor(Math.random()*3);
        boxes[a].style.transform='translateX(50px) rotateY(180deg)';
        boxes[b].style.transform='translateX(-50px) rotateY(180deg)';
        await delay(250);
        swapNodes(boxes[a], boxes[b]);
        boxes = document.querySelectorAll('.box');
        boxes.forEach(b => b.style.transform='translateX(0) rotateY(0deg)');
        await delay(250);
    }
}

function swapNodes(node1,node2){
    const parent = node1.parentNode;
    const temp = document.createElement('div');
    parent.insertBefore(temp,node1);
    parent.replaceChild(node1,node2);
    parent.replaceChild(node2,temp);
}

boxes.forEach(box => {
    box.addEventListener('click', async () => {
        if(gameLocked) return;
        let index = Array.from(boxes).indexOf(box);
        gameLocked = true;

        if(index===correctBox){
            box.querySelector('.ball').style.display='block';
            box.classList.add('highlight');
            message.textContent='Kamran bunu bəyəndi.';
            correctSound.currentTime=0;
            correctSound.play().catch(()=>{});
            score += 10;
            scoreEl.textContent = `Xal: ${score}`;
        } else {
            message.textContent='Kamran əsəbləşdi!';
            boxes[correctBox].querySelector('.ball').style.display='block';
            boxes[correctBox].classList.add('highlight');
            box.classList.add('wrong');
            const sound = wrongSounds[Math.floor(Math.random()*wrongSounds.length)];
            sound.currentTime=0;
            sound.play().catch(()=>{});
        }
    });
});

// Yenidən başlat
restartBtn.addEventListener('click', () => {
    startGame();
});

// Start səsi kliklə çalınması (autoplay problemi üçün)
document.body.addEventListener('click', () => {
    startSound.play().catch(()=>{});
}, { once: true });

window.addEventListener('load', startGame);
</script>

</body>
</html>
