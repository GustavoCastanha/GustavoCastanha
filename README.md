<h1 align="left">Gustavo Castanha</h1>

###

<p align="left">
Sou estudante de tecnologia na <b>Universidade Federal da Fronteira Sul (UFFS)</b> e desenvolvedor em formação, com foco em programação em <b>C e Python</b>.
Atualmente estudo e pratico conceitos de <b>inteligência artificial</b> e <b>visão computacional</b>, buscando aplicar o aprendizado em projetos simples e funcionais.
<br><br>
Tenho interesse em:
<br><br>
• Programação em Python e C  
<br>
• Fundamentos de IA e processamento de imagens  
<br>
• Organização de código e versionamento com Git/GitHub  
<br>
• Aprendizado contínuo e desenvolvimento prático  
<br><br>
Este GitHub reúne meus estudos, exercícios e projetos em andamento, acompanhando minha evolução na área de tecnologia.
</p>

###

<h2 align="left">I code with</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="python logo"/>
  <img width="12"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="c logo"/>
  <img width="12"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"/>
  <img width="12"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"/>
  <img width="12"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css logo"/>
</div>

###

<picture>
  <source media="(prefers-color-scheme: dark)"
    srcset="https://raw.githubusercontent.com/GustavoCastanha/GustavoCastanha/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)"
    srcset="https://raw.githubusercontent.com/GustavoCastanha/GustavoCastanha/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph"
    src="https://raw.githubusercontent.com/GustavoCastanha/GustavoCastanha/output/pacman-contribution-graph.svg">
</picture>

###

<div align="left">
  <a href="https://www.linkedin.com/in/gustavo-castanha-7a7337327/" target="_blank">
    <img
      src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg"
      width="52"
      height="40"
      alt="linkedin logo"
    />
  </a>
</div>

###

# Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: GustavoCastanha
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

<p align="left">Hello World!!</p>
