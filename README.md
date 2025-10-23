<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Thiệp Mời Đám Cưới</title>
<style>
    body {
        margin: 0;
        font-family: "Dancing Script", cursive;
        background: linear-gradient(to bottom right, #ffe6e6, #fff0f5);
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        overflow: hidden;
    }

    .envelope {
        width: 300px;
        height: 200px;
        background: #fff;
        position: relative;
        border: 2px solid #ffb6c1;
        border-radius: 10px;
        cursor: pointer;
        transition: all 0.6s ease;
        box-shadow: 0 5px 20px rgba(255, 182, 193, 0.5);
    }

    .envelope.open {
        transform: rotateX(180deg);
    }

    .invitation {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        padding: 20px;
        background: white;
        border-radius: 10px;
        backface-visibility: hidden;
        text-align: center;
    }

    .invitation h2 {
        color: #e91e63;
        font-size: 28px;
        margin-bottom: 10px;
    }

    .invitation p {
        color: #555;
        font-size: 18px;
        margin: 5px 0;
    }

    .invitation .names {
        font-size: 26px;
        color: #d81b60;
        margin: 15px 0;
    }

    .invitation .heart {
        font-size: 24px;
        color: red;
        animation: pulse 1s infinite alternate;
    }

    @keyframes pulse {
        from { transform: scale(1); }
        to { transform: scale(1.3); }
    }

    .music-btn {
        position: absolute;
        bottom: 20px;
        right: 20px;
        background: #ffb6c1;
        border: none;
        border-radius: 50%;
        width: 50px;
        height: 50px;
        cursor: pointer;
        box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        font-size: 22px;
        color: white;
    }

</style>
</head>
<body>

<div class="envelope" id="envelope">
    <div class="invitation">
        <h2>Thiệp Mời Đám Cưới</h2>
        <p>Kính mời bạn đến chung vui cùng chúng tôi</p>
        <div class="names">💖 Khánh & Người Thương 💖</div>
        <p>Vào lúc <b>10:00 sáng</b> ngày <b>25/12/2025</b></p>
        <p>Tại: Nhà hàng Hoa Hồng, TP. Đà Nẵng</p>
        <p class="heart">💞</p>
    </div>
</div>

<audio id="bg-music" src="https://cdn.pixabay.com/audio/2022/10/09/audio_960b4b6f4f.mp3" loop></audio>

<button class="music-btn" id="musicBtn">🎵</button>

<script>
    const envelope = document.getElementById("envelope");
    const music = document.getElementById("bg-music");
    const musicBtn = document.getElementById("musicBtn");

    envelope.addEventListener("click", () => {
        envelope.classList.toggle("open");
    });

    musicBtn.addEventListener("click", () => {
        if (music.paused) {
            music.play();
            musicBtn.textContent = "⏸️";
        } else {
            music.pause();
            musicBtn.textContent = "🎵";
        }
    });
</script>

</body>
</html>
