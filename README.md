<!--título-->
<div id="user-content-toc">
  <ul align="center">
    <summary><h1 style="display: inline-block">Welcome to my profile</h1></summary>
</div>

<!-- Presentation -->
<p>
  Hi 👋, I'm Teodoro! I have a degree in Information Technology Management and I live in Brazil..

  - 🌱 I'm currently studying Linux, devops and azure database. <img align="center" alt="html5" src="https://img.shields.io/badge/Edx-193A3E?style=for-the-badge&logo=edx&logoColor=white" />

  - :octocat: I'm looking for my first job opportunity. I want to pursue a career in devops and become a professional in the area..
</p>

<!-- Dropdown -->
<details>
  <summary>👨‍💻 More about me</summary>

  - 💬 I study Systems Analysis and have been working with the technical side of IT for over 4 years, especially hardware and systems. Oh, and I've already given computer classes to a cool bunch of people, more than 30 students! 💻✨

Now I'm embarking on the Cloud School, where I'm discovering the secrets and tricks of the AWS cloud. All this because my dream is to be a DevOps ninja! 🚀🌐 


  - ⚡ I like to travel, in my free time I play sports like playing football and skateboarding’. I am a musician not only in church but I am part of a musical association called LiraCarlosGomes and I play some instruments such as guitar, alto sax, clarinet, flute, harmonica. I like reading, whether it's a good book, as well as watching movies, series and anime.. \o/
</details>

<!-- Links -->

<!-- GithubStats -->


<!-- GIF -->
<p align="left">
  <img align="center" src="https://github.com/VariableBee/VariableBee/assets/77739311/4e9f41af-6b57-49a7-b15a-74322e96b4d7" alt="Imagem">
</p>

## 🔥 Skills
<!-- Skills: Programming Languages -->
  <div style="flex-basis: 48%;">
    <h3>Programming Languages</h3>
    <img align="center" alt="Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
    <img align="center" alt="HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
    <img align="center" alt="CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
    <img align="center" alt="Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
    <img align="center" alt="C" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg">
  </div>
  
  <!-- Skills: Tools & Frameworks -->
  <div style="flex-basis: 48%;">
    <h3>Tools & Frameworks</h3>
    <img align="center" alt="VScode" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg">
    <img align="center" alt="AWS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg">
    <img align="center" alt="Jupyter" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg">
    <img align="center" alt="Chris-AWS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg">
    <img align="center" alt="Bash" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg">
  </div>
  
  <!-- Skills: Libraries -->
  <div style="flex-basis: 48%;">
    <h3>Libraries</h3>
    <img align="center" alt="Numpy" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg">
    <img align="center" alt="Pandas" src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/>
    <img align="center" alt="Seaborn" src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/>
    <img align="center" alt="Scikit-learn" src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/>

       # GitHub Action for generating a contribution graph with a snake eating your contributions.

name: Generate Snake

# Controls when the action will run. This action runs every 6 hours.

on:
  schedule:
      # every 6 hours
    - cron: "0 */6 * * *"

# This command allows us to run the Action automatically from the Actions tab.
  workflow_dispatch:

# The sequence of runs in this workflow:
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Generates the snake  
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Teodoro-RuyLuques
          # these next 2 lines generate the files on a branch called "output". This keeps the main branch from cluttering up.
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

     # show the status of the build. Makes it easier for debugging (if there's any issues).
      - run: git status

      # Push the changes
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
  </div>

  

