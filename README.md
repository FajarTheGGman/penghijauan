# Penghijauan
<p>Penghijauan aktivitas github dengan auto commit</p>

![](https://img.shields.io/badge/github-actions-blue)
![](https://img.shields.io/badge/ci-cd-red) 
![](https://img.shields.io/badge/git-commit-lime)
![](https://img.shields.io/badge/author-FajarTheGGman-white)



<div align="center">
  <img src="https://i.ibb.co/ygMh8GG/2913483.png" width="190" />
</div>


<b>File Konfigurasi</b>

![](https://img.shields.io/badge/active_every-5:05_AM-lime)

```yml
# This is a basic workflow to help you get started with Actions

name: CI

# Controls when the workflow will run
on:
  # Triggers the workflow on push or pull request events but only for the main branch
  push:
    branches: [ main ]
  workflow_dispatch:
  schedule:
    - cron: '0 */6 * * *'

  pull_request:
    branches: [ main ]

  # Allows you to run this workflow manually from the Actions tab

# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v2

      # Runs a single command using the runners shell
      - name: first commit
        run: date >> dump.md

      # Runs a set of commands using the runners shell
      - name: second commit
        run: |
          git add .
          git config user.name 'FajarTheGGman'
          git config user.email 'newstrooper731@gmail.com'
          git push 
