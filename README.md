const noBtn = document.getElementById("no");

noBtn.addEventListener("mouseover", () => {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

document.getElementById("yes").addEventListener("click", () => {
    document.getElementById("card").innerHTML = `
        <h1>Yay! 💖🥰</h1>
        <p>You just made this day special ✨</p>
        <p>Happy Valentine’s Day, Isha ❤️</p>
    `;
    hearts();
});

function hearts() {
    setInterval(() => {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 6000);
    }, 300);
}
</script>

</body>
</html>
