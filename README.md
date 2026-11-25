<div align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0EA5E9,50:312E81,100:0F172A&height=220&section=header&text=Christian%20Fachini&fontSize=60&fontColor=ffffff&fontAlignY=38" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=1100&color=67E8F9&center=true&vCenter=true&width=800&lines=Jovem+Aprendiz+na+WEG+%F0%9F%8F%AD;Estudante+de+Desenvolvimento+de+Sistemas+%F0%9F%92%BB;Aprendendo%2C+criando+e+evoluindo+um+projeto+por+vez+%F0%9F%9A%80" alt="Texto animado de apresentação" />
</div>

<br>

<div align="center">
  <img src="https://img.shields.io/badge/WEG-Jovem%20Aprendiz-00579D?style=for-the-badge" alt="WEG" />
  <img src="https://img.shields.io/badge/Foco-Desenvolvimento%20de%20Sistemas-312E81?style=for-the-badge" alt="Foco" />
</div>



## 🛠️ Stack

<div align="center">

**Linguagens e tecnologias**

<img src="https://skillicons.dev/icons?i=html,css,js,java,tailwind,mysql&perline=8" alt="HTML, CSS, JavaScript, Java, Tailwind, MySQL," />

<br><br>

**Ferramentas**

<img src="https://skillicons.dev/icons?i=git,github,vscode,eclipse&perline=8" alt="Git, GitHub, VS Code, Eclipse" />

</div>

---

## 🎯 Meu universo de desenvolvimento

<div align="center">
  <table>
    <tr>
      <td align="center" width="33%">
        <h3>🌐 Front-end</h3>
        <p>Interfaces, interatividade e experiências web.</p>
        <img src="https://skillicons.dev/icons?i=html,css,js,tailwind,vscode" />
      </td>
      <td align="center" width="33%">
        <h3>⚙️ Back-end</h3>
        <p>APIs, regras de negócio e desenvolvimento de sistemas.</p>
        <img src="https://skillicons.dev/icons?i=java,spring,mysql,idea" />
      </td>
    </tr>
  </table>
</div>

---

## 📊 GitHub Analytics

<div align="center">

  <img height="170" src="https://github-readme-stats.vercel.app/api?username=ChristianFachini&show_icons=true&theme=tokyonight&hide_border=true" />

  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ChristianFachini&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />

  <br><br>

  <img width="60%" src="https://streak-stats.demolab.com?user=ChristianFachini&theme=tokyonight&hide_border=true" />

</div>

---

## 📈 Minha atividade no GitHub

<div align="center">
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=ChristianFachini&theme=tokyo-night&hide_border=true&area=true" />
</div>

---

## 🐍 Minhas contribuições em movimento

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ChristianFachini/ChristianFachini/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/ChristianFachini/ChristianFachini/output/github-contribution-grid-snake.svg" />
    <img alt="Animação da cobrinha percorrendo minhas contribuições" src="https://raw.githubusercontent.com/ChristianFachini/ChristianFachini/output/github-contribution-grid-snake.svg" />
  </picture>
</div>


---

<div align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" alt="Frase do dia" />
</div>

<div align="center">
  <h3>✨ Obrigado por visitar meu perfil!</h3>
  <p>Um código de cada vez. Um projeto de cada vez. Sempre evoluindo. 🚀</p>
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0EA5E9,50:312E81,100:0F172A&height=110&section=footer" alt="" />
</div>





name: Generate Contribution Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: Generate Snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ChristianFachini
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Publish Snake
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
