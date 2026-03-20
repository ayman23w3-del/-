<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عيد فطر مبارك 🎉</title>
<style>
  body {
    margin: 0;
    padding: 0;
    font-family: "Arial", sans-serif;
    background: linear-gradient(135deg, #2b2e4a, #904e95);
    color: #fff;
    text-align: center;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }
  #content {
    opacity: 0;
    transform: translateY(20px);
    transition: 1s ease;
  }
  h1 {
    font-size: 2.8rem;
  }
  p {
    font-size: 1.4rem;
    margin-top: 10px;
  }
</style>
</head>
<body>

<div id="content">
  <h1>🌙 عيد فطر مبارك يا زنوبتي ✨</h1>
  <p>كل عام وانتي بخير 🤍</p>
  <p>الغريب إنو العيد يجي كل سنة…</p>
  <p>بس مو كل مرة يكون إله نفس الشعور 😌</p>
  <p>يمكن لأنو بعض الناس يغيرون طعم الأيام بدون ما يقصدون.</p>
  <p>فـ بهاليوم الحلو…</p>
  <p>أتمنى الج كل شي يشبه قلبج 💫</p>
  <p>راحة، فرح، وضحكة تبقى أطول من العيد نفسه 🤍</p>
  <p>🎊✨</p>
</div>

<script>
// Fade in effect
window.onload = function() {
  setTimeout(() => {
    document.getElementById("content").style.opacity = "1";
    document.getElementById("content").style.transform = "translateY(0)";
  }, 300);
  
  // Confetti animation
  createConfetti();
};

function createConfetti() {
  const colors = ["#FFDD00","#FF5F00","#00D1FF","#FF0066","#9B59B6"];
  const duration = 3000;
  const end = Date.now() + duration;

  (function frame() {
    const confetti = document.createElement("div");
    confetti.style.position = "fixed";
    confetti.style.width = "10px";
    confetti.style.height = "10px";
    confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
    confetti.style.left = Math.random() * window.innerWidth + "px";
    confetti.style.top = "-10px";
    confetti.style.opacity = "0.8";
    document.body.appendChild(confetti);

    let posY = -10;
    const speed = Math.random() * 5 + 2;

    function fall() {
      if (Date.now() < end && posY < window.innerHeight) {
        posY += speed;
        confetti.style.top = posY + "px";
        requestAnimationFrame(fall);
      } else {
        confetti.remove();
      }
    }
    fall();

    if (Date.now() < end) {
      requestAnimationFrame(frame);
    }
  })();
}
</script>

</body>
</html>
