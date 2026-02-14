# Will-you-be-my-valantine
A Valentine's Day confession page
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Layal ❤️</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        font-family: Arial, sans-serif;
        overflow: hidden;
        text-align: center;
    }

    .container {
        position: relative;
    }

    h1 {
        font-size: 2.5rem;
        color: #fff;
        margin-bottom: 40px;
    }

    button {
        padding: 15px 30px;
        font-size: 1.2rem;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        transition: 0.3s;
        margin: 10px;
        position: absolute;
    }

    #yesBtn {
        background-color: #ff4d6d;
        color: white;
        left: 50%;
        transform: translateX(-120%);
    }

    #noBtn {
        background-color: #555;
        color: white;
        left: 50%;
        transform: translateX(20%);
    }

    .message {
        font-size: 2rem;
        color: white;
        margin-top: 80px;
        display: none;
    }
</style>
</head>
<body>

<div class="container">
    <h1>Layal, will you be my Valentine? ❤️</h1>
    <button id="yesBtn">Yes 💖</button>
    <button id="noBtn">No 💔</button>
    <div class="message" id="loveMessage">
        Yaaay! I love you so much Layal ❤️🥰
    </div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const message = document.getElementById("loveMessage");

    function moveButton() {
        const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
        const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
        noBtn.style.transform = "none";
    }

    noBtn.addEventListener("mouseover", moveButton);
    noBtn.addEventListener("touchstart", moveButton);

    yesBtn.addEventListener("click", () => {
        message.style.display = "block";
        yesBtn.style.display = "none";
        noBtn.style.display = "none";
    });
</script>

</body>
</html>
