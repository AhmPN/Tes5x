<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Kelas X 7 - SMAN 1 Pangkalan Lada</title>
  <!-- Google Fonts & Font Awesome -->
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    :root {
      --primary-color: #1e3a8a;
      --accent-color: #3b82f6;
      --text-main: #1e293b;
      --text-muted: #64748b;
      --white: #ffffff;
      --shadow-soft: 0 10px 30px -5px rgba(0, 0, 0, 0.08);
      --radius: 20px;
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Plus Jakarta Sans', sans-serif;
    }
    body {
      background-color: #f8fafc;
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      overflow-x: hidden;
    }
    /* Header dengan Foto Latar Belakang */
    header {
      position: relative;
      width: 100%;
      min-height: 280px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: var(--white);
      padding: 30px 16px;
      overflow: hidden;
    }
    .header-bg {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: 1;
    }
    .header-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.85) 0%, rgba(30, 58, 138, 0.75) 100%);
      z-index: 2;
    }
    header .header-content {
      position: relative;
      z-index: 3;
      width: 100%;
      max-width: 800px;
      padding: 0 10px;
    }
    header h1 {
      font-size: 1.6rem;
      font-weight: 700;
      letter-spacing: 0.5px;
      margin-bottom: 6px;
      text-shadow: 0 2px 4px rgba(0,0,0,0.3);
    }
    header h2 {
      font-size: 1rem;
      font-weight: 500;
      color: #93c5fd;
      margin-bottom: 15px;
    }
    #waktu {
      display: inline-block;
      background: rgba(255, 255, 255, 0.15);
      padding: 6px 14px;
      border-radius: 50px;
      font-size: 0.8rem;
      backdrop-filter: blur(8px);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }
    /* Navigasi Mengambang (Floating Menu) Responsif HP & PC */
    .nav-container {
      max-width: 950px;
      width: 92%;
      margin: -25px auto 15px auto;
      position: relative;
      z-index: 10;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(110px, 1fr));
      gap: 8px;
    }
    .menu-btn {
      background: var(--white);
      color: var(--text-main);
      border: 1px solid #e2e8f0;
      padding: 12px 10px;
      border-radius: 12px;
      font-weight: 600;
      font-size: 0.82rem;
      cursor: pointer;
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
      text-align: center;
      text-decoration: none;
    }
    .menu-btn i {
      color: var(--primary-color);
      font-size: 0.9rem;
      transition: transform 0.3s;
    }
    .menu-btn:hover {
      background-color: var(--primary-color);
      color: var(--white);
      border-color: var(--primary-color);
      transform: translateY(-2px);
    }
    .menu-btn:hover i {
      color: var(--white);
      transform: scale(1.1);
    }
    /* Area Konten Utama */
    main {
      flex: 1;
      max-width: 950px;
      width: 92%;
      margin: 10px auto 30px auto;
    }
    .card-content {
      background: var(--white);
      padding: 20px 16px;
      border-radius: var(--radius);
      box-shadow: var(--shadow-soft);
      animation: fadeIn 0.4s ease-in-out;
      border: 1px solid #f1f5f9;
      overflow-x: auto;
    }
    @media (min-width: 768px) {
      .card-content {
        padding: 40px;
      }
      header {
        min-height: 320px;
      }
      header h1 {
        font-size: 2rem;
      }
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .card-content h2 {
      color: var(--primary-color);
      font-size: 1.3rem;
      margin-bottom: 15px;
      padding-bottom: 10px;
      border-bottom: 2px solid #f1f5f9;
    }
    /* Styling Tabel Responsif agar tidak terpotong di HP */
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
      font-size: 0.85rem;
    }
    th, td {
      padding: 10px 12px;
      text-align: left;
    }
    th {
      background-color: var(--primary-color);
      color: var(--white);
      font-weight: 600;
    }
    tr:nth-child(even) {
      background-color: #f8fafc;
    }
    tr:hover {
      background-color: #f1f5f9;
    }
    td {
      border-bottom: 1px solid #e2e8f0;
      color: var(--text-main);
    }
    /* Galeri Grid Style (Responsif 2 kolom di HP, fleksibel di PC) */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 12px;
      margin-top: 15px;
    }
    .gallery-item {
      background: #f8fafc;
      border: 1px solid #e2e8f0;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 6px rgba(0,0,0,0.02);
    }
    .gallery-item img {
      width: 100%;
      height: 130px;
      object-fit: cover;
      display: block;
    }
    .gallery-item p {
      padding: 8px;
      font-size: 0.8rem;
      color: var(--text-main);
      text-align: center;
      font-weight: 500;
    }
    /* Footer */
    footer {
      background-color: #0f172a;
      color: #94a3b8;
      text-align: center;
      padding: 25px 16px;
      margin-top: auto;
      font-size: 0.85rem;
      border-top: 1px solid #1e293b;
    }
    footer .social-links {
      margin-top: 12px;
      display: flex;
      justify-content: center;
      gap: 20px;
    }
    footer a {
      color: var(--white);
      text-decoration: none;
      font-weight: 500;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: color 0.2s;
    }
    footer a:hover {
      color: #93c5fd;
    }
  </style>
</head>
<body>
  <!-- Header dengan Foto Latar Belakang -->
  <header>
    <img src="fotox75.jpg" alt="Background Sekolah" class="header-bg">
    <div class="header-overlay"></div>    
    <div class="header-content">
      <h1>SMAN 1 Pangkalan Lada</h1>
      <h2>Informasi Kelas X-7</h2>
      <div id="waktu">Memuat waktu...</div>
    </div>
  </header>
  <!-- Navigasi Mengambang (Floating Menu) Responsif -->
  <div class="nav-container">
    <button class="menu-btn" onclick="showContent('beranda')"><i class="fa-solid fa-house"></i> Beranda</button>
    <button class="menu-btn" onclick="showContent('struktur')"><i class="fa-solid fa-sitemap"></i> Struktur</button>
    <button class="menu-btn" onclick="showContent('anggota')"><i class="fa-solid fa-users"></i> Anggota</button>
    <button class="menu-btn" onclick="showContent('pelajaran')"><i class="fa-solid fa-calendar-days"></i> Jadwal</button>
    <button class="menu-btn" onclick="showContent('piket')"><i class="fa-solid fa-broom"></i> Piket</button>
    <button class="menu-btn" onclick="showContent('pr')"><i class="fa-solid fa-book"></i> Tugas PR</button>
    <button class="menu-btn" onclick="showContent('galeri')"><i class="fa-solid fa-images"></i> Galeri</button>
    <a href="https://aku-sehat.vercel.app/" target="_blank" class="menu-btn"><i class="fa-solid fa-list-check"></i> Jurnal</a>
    <button class="menu-btn" onclick="showContent('pesan')"><i class="fa-solid fa-envelope"></i> Pesan</button>
  </div>
  <!-- Konten Utama -->
  <main>
    <div id="content" class="card-content">
      <h2>Selamat Datang di Website Kelas X-7!</h2>
      <p style="color: var(--text-muted); line-height: 1.6; margin-top: 10px; font-size: 0.95rem;">Website resmi kelas X-7 untuk mempermudah koordinasi, melihat jadwal, serta berbagai informasi penting lainnya secara cepat, rapi, dan terpadu.</p>
    </div>
  </main>
  <!-- Footer -->
  <footer>
    <p>Hak Cipta &copy; 2026 Kelas X-7 | SMAN 1 Pangkalan Lada</p>
    <div class="social-links">
      <a href="https://www.instagram.com" target="_blank"><i class="fab fa-instagram"></i> Instagram</a>
      <a href="https://www.tiktok.com" target="_blank"><i class="fab fa-tiktok"></i> TikTok</a>
    </div>
  </footer>
  <!-- Script JavaScript -->
  <script>
    // Jam Realtime
    function updateWaktu() {
      const hariNama = ["Minggu","Senin","Selasa","Rabu","Kamis","Jumat","Sabtu"];
      const bulanNama = ["Januari","Februari","Maret","April","Mei","Juni","Juli","Agustus","September","Oktober","November","Desember"];
      let sekarang = new Date();
      let hari = hariNama[sekarang.getDay()];
      let tanggal = sekarang.getDate();
      let bulan = bulanNama[sekarang.getMonth()];
      let tahun = sekarang.getFullYear();
      let jam = String(sekarang.getHours()).padStart(2, '0');
      let menit = String(sekarang.getMinutes()).padStart(2, '0');
      let detik = String(sekarang.getSeconds()).padStart(2, '0');      
      const elemenWaktu = document.getElementById("waktu");
      if(elemenWaktu) {
        elemenWaktu.innerHTML = `${hari}, ${tanggal} ${bulan} ${tahun} &bull; ${jam}:${menit}:${detik}`;
      }
    }
    setInterval(updateWaktu, 1000);
    updateWaktu();
    // Data Konten Lengkap
    const contentData = {
      beranda: `
        <h2>Selamat Datang di Website Kelas X-7!</h2>
        <p style="color: var(--text-muted); line-height: 1.6; margin-top: 10px; font-size: 0.95rem;">Website resmi kelas X-7 untuk mempermudah koordinasi akademik, melihat jadwal, serta berbagai informasi penting lainnya secara cepat, rapi, dan terpadu.</p>
      `,
      struktur: `
        <h2>Struktur Organisasi Kelas X-7</h2>
        <div style="overflow-x: auto;">
          <table>
            <tr><th>Jabatan</th><th>Nama Lengkap</th></tr>
            <tr><td>Wali Kelas</td><td>Arif Dedy Purwanto, S.Pd.</td></tr>
            <tr><td>Ketua Kelas</td><td>Roland Putra Lana</td></tr>
            <tr><td>Wakil Ketua</td><td>Ahmad Putra Nurrohim</td></tr>
            <tr><td>Sekretaris 1</td><td>Jordan Sophy Rosenelly</td></tr>
            <tr><td>Sekretaris 2</td><td>Amelia Nur Damayanti</td></tr>
            <tr><td>Bendahara 1</td><td>Nayra Yasyifa Ramadhania</td></tr>
            <tr><td>Bendahara 2</td><td>Amanda Yurin Elaeis Oleifera</td></tr>
            <tr><td>Keamanan</td><td>Yoga & Hafid</td></tr>
            <tr><td>Kesehatan</td><td>Nabila & Jafna</td></tr>
            <tr><td>Kebersihan</td><td>Kenya & Rianty</td></tr>
            <tr><td>Keimanan</td><td>Lisfa & Ifan</td></tr>
          </table>
        </div>
      `,
      anggota: `
        <h2>Daftar Anggota Siswa Kelas X-7 (35 Siswa)</h2>
        <div style="overflow-x: auto;">
          <table>
            <tr>
              <th style="width: 50px; text-align: center;">No</th>
              <th>Nama Lengkap Siswa</th>
            </tr>
            <tr><td style="text-align: center;">1</td><td>ACHMAD NOOR HAFIID</td></tr>
            <tr><td style="text-align: center;">2</td><td>AHMAD PUTRA NURROHIM</td></tr>
            <tr><td style="text-align: center;">3</td><td>AMANDA YURIN ELAEIS OLEIFERA</td></tr>
            <tr><td style="text-align: center;">4</td><td>AMELIA NUR DAMAYANTI</td></tr>
            <tr><td style="text-align: center;">5</td><td>ANITA SULFANIA</td></tr>
            <tr><td style="text-align: center;">6</td><td>ARDI EXSA PUTRA PRATAMA</td></tr>
            <tr><td style="text-align: center;">7</td><td>AULIA NOVA VELISYA</td></tr>
            <tr><td style="text-align: center;">8</td><td>DAFA RISKI NUGROHO PRATAMA</td></tr>
            <tr><td style="text-align: center;">9</td><td>DIAH ANNISA FITRI</td></tr>
            <tr><td style="text-align: center;">10</td><td>DIFRI BAGUS WIBOWO</td></tr>
            <tr><td style="text-align: center;">11</td><td>ISTNAIN ROMDHONI</td></tr>
            <tr><td style="text-align: center;">12</td><td>JAFNA PUTRA PRATAMA</td></tr>
            <tr><td style="text-align: center;">13</td><td>JORDAN SOPHY ROSENELLY</td></tr>
            <tr><td style="text-align: center;">14</td><td>KENYA LAXVICA SASTRI</td></tr>
            <tr><td style="text-align: center;">15</td><td>LISFA DWI PRASETIANI</td></tr>
            <tr><td style="text-align: center;">16</td><td>MEYLA ALIFFIA</td></tr>
            <tr><td style="text-align: center;">17</td><td>MOCHAMMAD DARREN AL-FARIZI</td></tr>
            <tr><td style="text-align: center;">18</td><td>MUHAMAD AZHAR SUHARTOYO</td></tr>
            <tr><td style="text-align: center;">19</td><td>MUHAMAD IFAN NUGROHO</td></tr>
            <tr><td style="text-align: center;">20</td><td>MUHAMMAD ARJUNA MUARIF SALAM</td></tr>
            <tr><td style="text-align: center;">21</td><td>MUHAMMAD DEVANATA ROHAN</td></tr>
            <tr><td style="text-align: center;">22</td><td>MUHAMMAD JOE'S AKBAR</td></tr>
            <tr><td style="text-align: center;">23</td><td>MUHAMMAD RISHAD TABATALA ARSODIQ</td></tr>
            <tr><td style="text-align: center;">24</td><td>NABILA AULIA QORIK</td></tr>
            <tr><td style="text-align: center;">25</td><td>NAYRA YASYIFA RAMADHANIA</td></tr>
            <tr><td style="text-align: center;">26</td><td>NIKEN RARA ISTIQOMAN</td></tr>
            <tr><td style="text-align: center;">27</td><td>NUR AZIZAH LAILATUL JANNAH</td></tr>
            <tr><td style="text-align: center;">28</td><td>PUTRI NUR AINIYYAH ZAHRAA</td></tr>
            <tr><td style="text-align: center;">29</td><td>RIANTY ISRA KUSUMA AYU</td></tr>
            <tr><td style="text-align: center;">30</td><td>ROLAND PUTRA LANA</td></tr>
            <tr><td style="text-align: center;">31</td><td>ROSA DWI OVILIA</td></tr>
            <tr><td style="text-align: center;">32</td><td>SELA OKTAVIANA</td></tr>
            <tr><td style="text-align: center;">33</td><td>TRI YOGA SAPUTRA</td></tr>
            <tr><td style="text-align: center;">34</td><td>VELLYNA ERKYLIA SEPTIRA PUTRI</td></tr>
            <tr><td style="text-align: center;">35</td><td>ZAHRA DWI YUDHA</td></tr>
          </table>
        </div>
      `,
      pelajaran: `
        <h2>Jadwal Pelajaran Kelas X-7</h2>
        <div style="overflow-x: auto;">
          <table>
            <tr><th>Hari</th><th>Mata Pelajaran</th></tr>
            <tr><td>Senin</td><td>MTK Wajib, Geografi, B.Indonesia, B.inggris</td></tr>
            <tr><td>Selasa</td><td>Ekonomi, Sejarah, Seni Budaya, Informatika, P.Pancasila</td></tr>
            <tr><td>Rabu</td><td>B.Indonesia, Pend.Agama, PJOK, PBJBL, Sosiologi</td></tr>
            <tr><td>Kamis</td><td>PBJBL, Fisika, P.Pancasila</td></tr>
            <tr><td>Jumat</td><td>BK, Biologi, Kimia</td></tr>
          </table>
        </div>
      `,
      piket: `
        <h2>Jadwal Piket Harian</h2>
        <div style="overflow-x: auto;">
          <table>
            <tr><th>Hari</th><th>Nama Petugas Piket</th></tr>
            <tr><td>Senin</td><td>Amanda, Sophy, Nayra, Rosa, Putra, Nain, Arjuna, Yoga</td></tr>
            <tr><td>Selasa</td><td>Amelia, Kenya, Niken, Sela, Hafid, Jafna, Defa</td></tr>
            <tr><td>Rabu</td><td>Anita, Lisfa, Azizah, Vellyna, Aldi, Darren, Jojo</td></tr>
            <tr><td>Kamis</td><td>Aulia, Mayla, Putri Nur, Zahra Dwi, Dafa, Azhar, Rishad</td></tr>
            <tr><td>Jumat</td><td>Diah, Nabila, Rianty, Difri, Ifan, Roland</td></tr>
          </table>
        </div>
      `,
      pr: `
        <h2>Informasi Tugas & PR Terbaru</h2>
        <div style="background: #f8fafc; border-left: 4px solid var(--primary-color); padding: 15px; border-radius: 8px; margin-bottom: 20px;">
          <h4 style="color: var(--primary-color); margin-bottom: 5px; font-size: 0.95rem;">Pengumuman Tugas</h4>
          <p style="color: var(--text-muted); font-size: 0.9rem;">Silakan cek secara berkala atau tanyakan langsung melalui kotak pesan jika ada tugas yang belum dimengerti.</p>
        </div>
      `,
      galeri: `
        <h2>Galeri Foto & Kenangan MPLS</h2>
        <div class="gallery-grid">
          <div class="gallery-item">
            <img src="x71.jpg" alt="Foto MPLS 1">
            <p>📸 MPLS 1</p>
          </div>
          <div class="gallery-item">
            <img src="x72.jpg" alt="Foto MPLS 2">
            <p>📸 MPLS 2</p>
          </div>
          <div class="gallery-item">
            <img src="x73.jpg" alt="Foto MPLS 3">
            <p>📸 MPLS 3</p>
          </div>
          <div class="gallery-item">
            <img src="x74.jpg" alt="Foto MPLS 4">
            <p>📸 MPLS 4</p>
          </div>
        </div>
      `,
      pesan: `
        <div style="max-width: 450px; margin: 0 auto; background: #efeae2; border-radius: 12px; box-shadow: 0 8px 24px rgba(0,0,0,0.15); overflow: hidden; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; position: relative;">
          <!-- Header WhatsApp -->
          <div style="background: #005e54; color: white; padding: 12px 16px; display: flex; align-items: center; gap: 12px;">
            <div style="position: relative;">
              <div style="width: 38px; height: 38px; background: #128c7e; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 18px; color: white;">
                <i class="fa-solid fa-user"></i>
              </div>
              <span style="position: absolute; bottom: 0; right: 0; width: 9px; height: 9px; background: #25d366; border: 2px solid #005e54; border-radius: 50%;"></span>
            </div>
            <div>
              <h4 style="margin: 0; font-size: 15px; font-weight: 600;">Admin Kelas X-7 (WA)</h4>
              <span style="font-size: 11px; opacity: 0.8;">online</span>
            </div>
          </div>
          <!-- Form Kirim WhatsApp -->
          <div style="padding: 14px; display: flex; flex-direction: column; gap: 10px;">         
            <!-- Bubble Chat: Input Nama -->
            <div style="background: #ffffff; padding: 10px 14px; border-radius: 0 12px 12px 12px; max-width: 90%; box-shadow: 0 1px 0.5px rgba(0,0,0,0.13); align-self: flex-start;">
              <label style="font-size: 11px; color: #005e54; font-weight: bold; display: block; margin-bottom: 2px;">Nama Kamu:</label>
              <input type="text" id="wa-nama" required placeholder="Ketik nama di sini..." 
                     style="width: 100%; border: none; outline: none; font-size: 14px; background: transparent; color: #333; box-sizing: border-box;">
            </div>
            <!-- Bubble Chat: Input Pesan -->
            <div style="background: #ffffff; padding: 10px 14px; border-radius: 0 12px 12px 12px; max-width: 90%; box-shadow: 0 1px 0.5px rgba(0,0,0,0.13); align-self: flex-start; position: relative; width: 100%;">
              <label style="font-size: 11px; color: #005e54; font-weight: bold; display: block; margin-bottom: 2px;">Tulis Pesan / Tugas:</label>
              <textarea id="wa-pesan" required placeholder="Pesan pengaduan, atau tanyakan tugas PR..." rows="3"
                        style="width: 100%; border: none; outline: none; font-size: 14px; background: transparent; color: #333; resize: none; box-sizing: border-box;"></textarea>
            </div>
            <!-- Panel Tombol Kirim ala WhatsApp Input Bar -->
            <div style="display: flex; align-items: center; gap: 8px; margin-top: 4px; background: #f0f2f5; padding: 6px 10px; border-radius: 24px; position: relative;">
              <div style="flex-grow: 1; font-size: 12px; color: #667781; overflow: hidden; white-space: nowrap; textile: ellipsis;">Kirim ke WhatsApp</div>          
              <button type="button" onclick="kirimKeWhatsApp()"
                      style="background: #00a884; color: white; border: none; width: 38px; height: 38px; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; font-size: 15px; box-shadow: 0 1px 3px rgba(0,0,0,0.2);">
                <i class="fa-solid fa-paper-plane"></i>
              </button>
            </div>
          </div>
        </div>
      `
    };
    function showContent(menu) {
      const container = document.getElementById("content");
      container.innerHTML = contentData[menu] || "<p>Halaman tidak ditemukan.</p>";
    }
    // Fungsi untuk mengarahkan data ke WhatsApp
    function kirimKeWhatsApp() {
      const nama = document.getElementById('wa-nama').value.trim();
      const pesan = document.getElementById('wa-pesan').value.trim();
      if (!nama || !pesan) {
        alert('Mohon isi Nama dan Pesan terlebih dahulu!');
        return;
      }
      // Nomor WhatsApp tujuan
      const nomorWa = '6285824522033';
      // Format teks pesan
      const teksFormat = `Halo Admin Kelas X-7,%0A%0A*Nama Pengirim:* ${encodeURIComponent(nama)}%0A*Pesan:* ${encodeURIComponent(pesan)}`;
      // Membuka URL WhatsApp
      const urlWa = `https://wa.me/${nomorWa}?text=${teksFormat}`;
      window.open(urlWa, '_blank');
    }
  </script>
</body>
</html>
