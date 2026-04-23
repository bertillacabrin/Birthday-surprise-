<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Womb Escape 🎉</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(135deg, #2ecc71, #27ae60);
        font-family: Arial, sans-serif;
        overflow: hidden;
    }

    .box {
        width: 150px;
        height: 150px;
        background: #145a32;
        position: relative;
        cursor: pointer;
        border-radius: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        font-weight: bold;
    }

    .lid {
        position: absolute;
        width: 150px;
        height: 40px;
        background: #1e8449;
        top: -40px;
        border-radius: 10px 10px 0 0;
        transition: 0.5s;
    }

    .open .lid {
        transform: rotateX(120deg);
        transform-origin: bottom;
    }

    .baby {
        display: none;
        text-align: center;
    }

    .baby img {
        width: 120px;
    }

    .baby p {
        color: white;
        font-size: 18px;
        margin-top: 10px;
        font-weight: bold;
    }

    .confetti {
        position: absolute;
        width: 10px;
        height: 10px;
        background: yellow;
        animation: fall 3s linear infinite;
    }

    @keyframes fall {
        from { transform: translateY(-100px); }
        to { transform: translateY(100vh); }
    }
</style>
</head>
<body>

<div class="box" onclick="openGift()">
    <div class="lid"></div>
    Click Me 🎁
</div>

<div class="baby" id="baby">
    <img src="https://cdn-icons-png.flaticon.com/512/194/194938.png" alt="baby">
    <p>Happy Womb Escape 🎉</p>
</div>

content://media/external/downloads/1000029405

<script>
function openGift() {
    document.querySelector(".box").classList.add("open");
    document.querySelector(".box").style.display = "none";
    document.getElementById("baby").style.display = "block";

    // Play music
    document.getElementById("music").play();

    // Create confetti
    for (let i = 0; i < 50; i++) {
        let confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = Math.random() * window.innerWidth + "px";
        confetti.style.animationDuration = (Math.random() * 3 + 2) + "s";
        confetti.style.background = `hsl(${Math.random()*360}, 100%, 50%)`;
        document.body.appendChild(confetti);
    }
}
</script>

</body>
</html>
