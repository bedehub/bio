<h1 align="center"> 
    <img src="https://readme-typing-svg.herokuapp.com/?font=Inter&size=48¢er=true&vCenter=true&width=500&height=70&color=4493F8&duration=4000&lines=Hai!+👋;+Saya+BedeHub!;" /> 
</h1> 
- 🌱 Saat ini saya sedang mempelajari **[ Desain Sistem ]( https://blog.bytebytego.com/p/free-system-design-pdf-158-pages )** 
- 💬 Tanyakan kepada saya tentang **Laravel, Node.js, React...atau apa pun [ di sini ]( https://github.com/{USERNAME}/{USERNAME}/issues )**

 <br> 

<div align="center"> 
  <a href="chijiokeokorji@gmail.com"> 
    <img src="https://img.shields.io/badge/Gmail-333333?style=for-the-badge&logo=gmail&logoColor=red" /> 
  </a> 
  <a href="https://linkedin.com/in/chijiokeokorji" target="_blank"> 
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=untuk-lencana&logo=linkedin&logoColor=putih" target="_blank" /> 
  </a> 
  <a href="https://medium.com/@chijiokeokorji" target="_blank"> 
    <img src="https://img.shields.io/badge/Medium-000000?style=untuk-lencana&logo=medium&logoColor=putih" target="_blank" /> 
  </a> 
  <a href="https://codepen.io/chijiokeokorji" target="_blank"> 
    <img src="https://img.shields.io/badge/CodePen-1e1f26?style=untuk-lencana&logo=codepen&logoColor=putih" target="_blank" /> 
  </a> 
</div>
<hr>
## 🛠️ Bahasa dan Alat

 <br> 

<p align="center"> 
  <img src="https://skillicons.dev/icons?i=java,spring,ts,nodejs,react,nextjs,mongodb,postgres,prisma" /> 
  <img src="https://skillicons.dev/icons?i=html,css,sass,tailwind,js,vue,redux,d3,git,postman,figma" /> 
</p> 

<hr>

## ⚡️ Statistik

 <br> 

<div align=center> 
  <img width=390 src="https://github-readme-stats.vercel.app/api?username=chijiokeokorji&theme=transparent&count_private=true&show_icons=true&rank_icon=github&locale=en" alt="Statistik GitHub ChijiokeOkorji" /> 
  <img width=390 src="https://github-readme-streak-stats.herokuapp.com/?user=chijiokeokorji&theme=transparent&count_private=true&border_radius=10&locale=en" alt="Statistik GitHub ChijiokeOkorji" /> 
  <img width=325 src="https://github-readme-stats.vercel.app/api/top-langs?username=chijiokeokorji&theme=transparent&layout=donut&hide=css&langs_count=8&border_radius=10&show_icons=true&locale=en" alt="Bahasa yang Paling Banyak Digunakan ChijiokeOkorji" /> 
</div> 

<hr>

Bahasa Indonesia: # GitHub Action untuk membuat grafik kontribusi dengan ular yang memakan kontribusi Anda.
 name: Generate Snake 

# Mengontrol kapan tindakan akan berjalan.
 on: 
  schedule: 
      # setiap 12 jam 
    - cron: "0 */12 * * *"

   # Perintah ini memungkinkan kita untuk menjalankan Action secara otomatis dari tab Actions. 
  workflow _dispatch: 
  
  # Juga jalankan pada setiap push di cabang utama 
  push: 
    branches: 
    - main 

# Urutan eksekusi dalam alur kerja ini: 
jobs: 
  # Alur kerja ini berisi satu pekerjaan yang disebut "build" 
  build: 
    # Jenis runner tempat pekerjaan akan berjalan 
    runs-on: ubuntu-latest 

    # Langkah-langkah mewakili urutan tugas yang akan dijalankan sebagai bagian dari 
    langkah-langkah pekerjaan: 
      - name: Klon repo 
        uses: actions/checkout@v3 
    
      - name: Hasilkan file ular di './dist/' 
        uses: Platane/snk@v3 
        id: snake-gif 
        with: 
          github_ user _name: ${{ github.repository_ owner }} 
          outputs: | 
            dist/github-contribution-grid-snake.svg 
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark 
            dist/github-contribution-grid-snake.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9 
        env: 
           GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }} 

      - name: Menampilkan status pembangunan 
        jalankan: git status 

      - name: Mendorong berkas baru ke cabang keluaran 
        menggunakan: crazy-max/ghaction-github-pages@v3.1.0 
        dengan: 
          target_branch: keluaran 
          build_dir: dist 
          commit_message: Memperbarui animasi ular 
        env: 
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
