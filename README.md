<div align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=500&size=28&pause=1000&color=00E5FF&center=true&vCenter=true&width=850&lines=Building+Sovereign+Industrial+Intelligence;Focusing+on+Object-Centric+Process+Mining;Advocating+for+Open+Source+%26+Independence" alt="Typing Animation" />
  </a>
</div>

---

### 🖖 Hi, I'm Frederic.

I’m a developer and open-source advocate dedicated to bringing true digital sovereignty to the industrial and medical sectors. I build tools that empower users and industries, freeing them from walled gardens and SaaS dependencies.

### 🛰️ What I'm currently exploring

Right now, I'm operating at the intersection of complex process data and semantic reasoning. I'm building "Logic Cells"—autonomous, offline-capable knowledge systems designed for SMEs. 

Most of my day-to-day revolves around **Object-Centric Process Mining (OCPM)** and ML:

* ⚗️ **Data Alchemy:** Extracting structured, meaningful data out of messy, real-world industrial machine logs and medical records.
* 👁️‍🗨️ **Semantic Reasoning:** Moving beyond flat event logs. I use OCPM and semantic databases to map complex, multi-object relationships in manufacturing.
* 🏰 **Autonomy by Design:** Ensuring that the systems we build can run completely independent of centralized cloud infrastructure. 

---

### 🐍 
name: Generate Snake Animation

on:
  # Führt die Action alle 12 Stunden aus
  schedule:
    - cron: "0 */12 * * *"
  # Erlaubt es dir, die Action jederzeit manuell zu starten
  workflow_dispatch:
  # Führt die Action aus, wenn du etwas pusht
  push:
    branches:
    - main
    - master

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    
    steps:
      # Generiert die SVG-Bilder (Hell und Dunkel)
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          # Holt automatisch deinen GitHub-Nutzernamen
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
      # Speichert (pusht) die generierten Bilder in den "output"-Branch
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

---

### 🏗️ Working with: 

<div align="left">
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Semantic_DB_(TypeDB)-4479A1?style=for-the-badge&logo=database&logoColor=white" alt="TypeDB" />
  <img src="https://img.shields.io/badge/OCPM-FF6F00?style=for-the-badge&logo=code-igniter&logoColor=white" alt="OCPM" />
</div>

---

### ☕ Beyond the Code

When I'm not working or studying, you can find me tinkering with my **Homelab**, exploring self-hosted and local-first architectures.

### 📡 Let's Connect

I'm always looking to connect with like-minded people who champion independent software. Whether you want to collaborate, swap ideas about OCPM and Rust, or just chat about the future of tech—reach out!

**Email:** frederic.lange@arcen-research.com
