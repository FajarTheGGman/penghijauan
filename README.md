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


```yml
# This is a basic workflow to help you get started with Actions

name: Penghijauan

# Controls when the workflow will run
on:
  push:
    branches: master
  workflow_dispatch:
  schedule:
    - cron: '* 1 * * *'

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
      - name: Banner
        run: echo Mulai Penghijauan...

      # Runs a set of commands using the runners shell
      - name: update readme 
        run: date >> README.md
      - name: push git
        run: |
          git add .
          git config user.name 'yourusername'
          git config user.email 'yourmail@example.com'
          git commit -m "Penghijauan"
          git push 
      - name: update
        run: sed -i '$ d' README.md
      - name: second push
        run: |
          git add .
          git config user.name 'yourusername'
          git config user.email 'yourmail@example.com'
          git commit -m "Penghijauan"
          git push 
```
