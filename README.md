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
