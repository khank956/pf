<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Thiệp Mời Đám Cưới</title>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&display=swap');

    body {
        margin: 0;
        padding: 0;
        font-family: 'Quicksand', sans-serif;
        background: linear-gradient(to bottom, #ffe6e6, #fff0f5);
        overflow-x: hidden;
    }

    .invitation {
        width: 100%;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        padding: 20px;
        box-sizing: border-box;
        animation: slideDown 2s ease-in-out;
    }

    @keyframes slideDown {
        0% {
            transform: translateY(-100%);
            opacity: 0;
        }
        100% {
            transform: translateY(0);
            opacity: 1;
        }
    }

    .invitation img {
        width: 300px;
        height: 300px;
        object-fit: cover;
        border-radius: 10px;
        margin-top: 30px;
        box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        border: 5px solid #fff;
    }

    h1 {
        font-family: 'Great Vibes', cursive;
        color: #d81b60;
        font-size: 50px;
        margin-top: 40px;
        text-align: center;
    }

    h2 {
        color: #e91e63;
        font-size: 26px;
        margin: 10px 0;
    }

    p {
        color: #444;
        font-size: 18px;
        text-align: center;
        margin: 5px 0;
    }

    .heart {
        font-size: 30px;
        color: red;
        animation: pulse 1s infinite alternate;
        margin: 10px 0;
    }

    @keyframes pulse {
        from { transform: scale(1); }
        to { transform: scale(1.4); }
    }

    .date-place {
        background: #ffe4ec;
        padding: 15px 25px;
        border-radius: 10px;
        margin-top: 15px;
        box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }

    .footer {
        margin-top: 40px;
        font-size: 16px;
        color: #555;
    }

    .flowers {
        position: fixed;
        top: -50px;
        width: 100%;
        height: 100%;
        overflow: hidden;
        z-index: -1;
    }

    .flower {
        position: absolute;
        top: -10%;
        width: 30px;
        height: 30px;
        background: url('https://cdn-icons-png.flaticon.com/512/2909/2909879.png');
        background-size: cover;
        opacity: 0.8;
        animation: fall linear infinite;
    }

    @keyframes fall {
        0% { transform: translateY(0) rotate(0deg); opacity: 1; }
        100% { transform: translateY(120vh) rotate(360deg); opacity: 0; }
    }

</style>
</head>
<body>

<div class="flowers"></div>

<div class="invitation">
    <h1>Thiệp Mời Đám Cưới</h1>

    <!-- 📸 KHU VỰC THÊM ẢNH -->
    <img src="your-image.jpg" alt="Ảnh Cặp Đôi"> 
    <!-- 👉 Thay "your-image.jpg" bằng link ảnh thật hoặc đường dẫn ảnh -->

    <div class="heart">💞</div>

    <h2>Khánh & Người Thương</h2>

    <p>Trân trọng kính mời bạn đến chung vui cùng chúng tôi trong ngày trọng đại.</p>

    <div class="date-place">
        <p><b>⏰ Thời gian:</b> 10:00 sáng, ngày 25/12/2025</p>
        <p><b>📍 Địa điểm:</b> Nhà hàng Hoa Hồng, TP. Đà Nẵng</p>
    </div>

    <p class="footer">Sự hiện diện của bạn là niềm vinh hạnh cho chúng tôi 💖</p>
</div>

<audio id="bg-music" src="https://cdn.pixabay.com/audio/2022/10/09/audio_960b4b6f4f.mp3" autoplay loop></audio>

<script>
    // 🌸 Tạo hiệu ứng hoa rơi
    const flowersContainer = document.querySelector('.flowers');
    for (let i = 0; i < 15; i++) {
        const flower = document.createElement('div');
        flower.classList.add('flower');
        flower.style.left = Math.random() * 100 + 'vw';
        flower.style.animationDuration = 4 + Math.random() * 6 + 's';
        flower.style.animationDelay = Math.random() * 3 + 's';
        flower.style.width = flower.style.height = 20 + Math.random() * 20 + 'px';
        flowersContainer.appendChild(flower);
    }
</script>

</body>
</html>
