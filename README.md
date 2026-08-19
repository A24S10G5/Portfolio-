<div align="center">
<img src="https://demolab.com" alt="Typing SVG" />
<br>

### 💻 UI/UX & Web Designer | Crafting clean, modern digital experiences

[![Profile Views](https://komarev.com)](https://github.com)
[![Hits](https://seeyoufarm.com)](https://github.com)

[![Email](https://shields.io)](mailto:adhamsameh241005@gmail.com)
[![WhatsApp](https://shields.io)](https://wa.me)
[![My Projects](https://shields.io)](https://github.com?tab=repositories)

</div>

<hr>

### 🎨 About Me

- 🖥️ &nbsp; I design **websites & mobile applications** with a core focus on user experience, modern layout, and high responsiveness.
- 🚀 &nbsp; I bridges the gap between creative visual layouts and clean frontend structure to deliver functional digital products.
- 🤖 &nbsp; I utilize advanced **AI systems** as productivity accelerators to optimize my workflow, generate ideas, and solve design roadblocks.
- ⚡ &nbsp; **Fun Fact:** I believe a great user interface is like a joke—if you have to explain it, it’s probably not that good!

<hr>

### 🧰 Tools & Technologies

#### 🌐 Web & UI/UX Design
![Figma](https://shields.io)
![Adobe XD](https://shields.io)
![Photoshop](https://shields.io)
![WordPress](https://shields.io)

#### 🛠️ Frontend Development & Tools
![HTML5](https://shields.io)
![CSS3](https://shields.io)
![JavaScript](https://shields.io)
![Bootstrap](https://shields.io)
![Git](https://shields.io)

#### 🧠 AI Co-Pilots
![Claude](https://shields.io)
![ChatGPT](https://shields.io)
![Gemini](https://shields.io)

<hr>

### ⚙️ Code Cycle
<div align="center">
<strong>It's Broken... ➜ It Works! ➜ Wait, Why?!</strong>
<br><br>
<img src="https://githubusercontent.com" width="55" alt="Broken"/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://githubusercontent.com" width="55" alt="Works"/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://githubusercontent.com" width="55" alt="Confused"/>
</div>
name: Generate Snake
on:
  schedule: [{ cron: "0 0 * * *" }]
  workflow_dispatch:
jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
