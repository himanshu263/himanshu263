<h1 align="center">Hi 👋, I'm Himanshu</h1>
<h3 align="center">💻 Backend Developer | 🛠️ Full Stack Learner | 🧠 AI Enthusiast</h3>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Poppins&pause=1000&color=FFB300&center=true&vCenter=true&width=435&lines=Backend+Developer;Learning+React+Frontend;Building+Full-Stack+Projects;Open+Source+Contributor;AI%2C+PHP%2C+Django%2C+JS+Lover" alt="Typing animation" />
</p>

<p align="center">
  <img src="https://visitor-badge.laobi.icu/badge?page_id=himanshu263.himanshu263" alt="Profile Views" />
</p>

---

### 🚀 *“Keep building, keep growing — consistency beats perfection.”*

---

### 🚀 About Me
- 💻 **Backend Developer** with experience in **PHP**, **Python**, and now leveling up in **JavaScript**.
- 🌱 Currently learning **React.js** to become a Full Stack Developer.
- 👀 Passionate about **Backend APIs**, **Django**, and **AI Projects**.
- 🎯 Building side projects regularly and open to collaborations.

---

### 🐍 Snake Game – Just for Fun!

<div align="center">
  <canvas id="snakeCanvas" width="400" height="400" style="border:1px solid #000;"></canvas>
  <p>Use arrow keys to control the snake 🐍</p>
</div>

<script>
(function() {
  const canvas = document.getElementById("snakeCanvas");
  const ctx = canvas.getContext("2d");
  const grid = 20;
  let count = 0;
  let snake = { x: 160, y: 160, cells: [], maxCells: 4 };
  let apple = { x: 320, y: 320 };
  let dx = grid, dy = 0;

  function getRandom(min, max) {
    return Math.floor(Math.random() * (max - min) / grid) * grid + min;
  }

  document.addEventListener("keydown", e => {
    if (e.key === "ArrowLeft" && dx === 0) { dx = -grid; dy = 0; }
    if (e.key === "ArrowUp" && dy === 0) { dx = 0; dy = -grid; }
    if (e.key === "ArrowRight" && dx === 0) { dx = grid; dy = 0; }
    if (e.key === "ArrowDown" && dy === 0) { dx = 0; dy = grid; }
  });

  function loop() {
    requestAnimationFrame(loop);
    if (++count < 4) return;
    count = 0;
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    snake.x += dx; snake.y += dy;

    if (
      snake.x < 0 || snake.x >= canvas.width ||
      snake.y < 0 || snake.y >= canvas.height
    ) {
      snake.x = snake.y = 160;
      snake.cells = [];
      snake.maxCells = 4;
      dx = grid; dy = 0;
    }

    snake.cells.unshift({ x: snake.x, y: snake.y });
    if (snake.cells.length > snake.maxCells) snake.cells.pop();

    ctx.fillStyle = "red";
    ctx.fillRect(apple.x, apple.y, grid, grid);

    ctx.fillStyle = "green";
    snake.cells.forEach((cell, idx) => {
      ctx.fillRect(cell.x, cell.y, grid - 1, grid - 1);
      if (cell.x === apple.x && cell.y === apple.y) {
        snake.maxCells++;
        apple.x = getRandom(0, canvas.width);
        apple.y = getRandom(0, canvas.height);
      }
      for (let j = idx + 1; j < snake.cells.length; j++) {
        if (cell.x === snake.cells[j].x && cell.y === snake.cells[j].y) {
          snake.x = snake.y = 160;
          snake.cells = [];
          snake.maxCells = 4;
          dx = grid; dy = 0;
        }
      }
    });
  }

  requestAnimationFrame(loop);
})();
</script>

---

### 💼 Tech Stack
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node-dot-js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

---

### 📊 GitHub Stats

![Himanshu's GitHub Stats](https://github-readme-stats.vercel.app/api?username=himanshu263&show_icons=true&theme=radical)

---

### 📝 Projects Showcase
- 🎮 **[JS Calculator](https://github.com/himanshu263/js-calculator)**
- ✅ **[To-Do List App](https://github.com/himanshu263/js-to-do-list)**
- ❌ **[Tic Tac Toe Game](https://github.com/himanshu263/js-tic-tac-toe)**
- 🎁 **[Python Voice Assistant](https://github.com/himanshu263/python-jarvis)**
- 🌐 **[Blog Django](https://github.com/himanshu263/django-blog)**

---

### 🏆 GitHub Trophies
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=himanshu263&theme=radical&no-frame=true&no-bg=true&margin-w=4" alt="GitHub Trophies"/>
</p>

---

### 💬 Connect with Me
- 📧 **Email:** [write.himanshu263@gmail.com](mailto:write.himanshu263@gmail.com)
- 🐙 **GitHub:** [himanshu263](https://github.com/himanshu263)
- 📸 **Instagram (Personal):** [@snapperkush](https://instagram.com/snapperkush)
- 🤖 **Instagram (AI Projects):** [@snapperkush.ai](https://instagram.com/snapperkush.ai)
- 🐦 **Twitter/X:** [@yadav_263](https://x.com/himanshu_263)

---

*Built with ❤️ by Himanshu | Powered by Code & Curiosity*
