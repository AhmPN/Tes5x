<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Kelas X-7 - SMAN 1 Pangkalan Lada</title>
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
      --shadow-soft: spx 4px 12px rgba(0, 0, 0, 0.06);
      --radius: 16px;
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Plus Jakarta Sans', sans-serif;
    }
    body {
      background-color: #f1f5f9;
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      width: 100%;
      overflow-x: hidden;
    }
    /* Header */
    header {
      position: relative;
      width: 100%;
      min-height: 200px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: var(--white);
      padding: 20px 16px;
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
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.88) 0%, rgba(30, 58, 138, 0.78) 100%);
      z-index: 2;
    }
    header .header-content {
      position: relative;
      z-index: 3;
      width: 100%;
      max-width: 450px;
    }
    header h1 {
      font-size: 1.25rem;
      font-weight: 700;
      margin-bottom: 4px;
      text-shadow: 0 2px 4px rgba(0,0,0,0.3);
    }
    header h2 {
      font-size: 0.85rem;
      font-weight: 500;
      color: #93c5fd;
      margin-bottom: 8px;
    }
    #waktu {
      display: inline-block;
      background: rgba(255, 255, 255, 0.15);
      padding: 3px 10px;
      border-radius: 50px;
      font-size: 0.7rem;
      backdrop-filter: blur(4px);
    }
    /* Navigasi Menu Grid 3 Kolom yang Pas dan Rapi di HP */
    .nav-container {
      width: 94%;
      max-width: 450px;
      margin: -15px auto 12px auto;
      position: relative;
      z-index: 10;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 8px;
    }
    .menu-btn {
      background: var(--white);
      color: var(--text-main);
      border: 1px solid #e2e8f0;
      padding: 10px 6px;
      border-radius: 12px;
      font-weight: 600;
      font-size: 0.75rem;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 4px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
      text-decoration: none;
      text-align: center;
      transition: 0.2s;
    }
    .menu-btn i {
      color: var(--primary-color);
      font-size: 1rem;
    }
    .menu-btn:active, .menu-btn:hover {
      background-color: var(--primary-color);
      color: var(--white);
      border-color: var(--primary-color);
    }
    .menu-btn:active i, .menu-btn:hover i {
      color: var(--white);
    }
    /* Area Konten Utama */
    main {
      flex: 1;
      width: 94%;
      max-width: 450px;
      margin: 0 auto 20px auto;
    }
    .card-content {
      background: var(--white);
      padding: 16px 14px;
      border-radius: var(--radius);
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
      border: 1px solid #e2e8f0;
      width: 100%;
    }
    .card-content h2 {
      color: var(--primary-color);
      font-size: 1.1rem;
      margin-bottom: 10px;
      padding-bottom: 6px;
      border-bottom: 2px solid #f1f5f9;
    }
    p {
      font-size: 0.85rem;
      color: var(--text-muted);
      line-height: 1.45;
    }
    /* Tabel Responsif */
    .table-responsive {
      width: 100%;
      overflow-x: auto;
      -webkit-overflow-scrolling: touch;
      margin-top: 8px;
      border-radius: 8px;
      border: 1px solid #e2e8f0;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.78rem;
      white-space: nowrap;
    }
    th, td {
      padding: 8px 10px;
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
    td {
      border-bottom: 1px solid #e2e8f0;
      color: var(--text-main);
    }
    /* Galeri Grid (2 Kolom) */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 8px;
      margin-top: 8px;
    }
    .gallery-item {
      background: #f8fafc;
      border: 1px solid #e2e8f0;
      border-radius: 10px;
      overflow: hidden;
    }
    .gallery-item img {
      width: 100%;
      height: 100px;
      object-fit: cover;
      display: block;
    }
    .gallery-item p {
      padding: 5px;
      font-size: 0.72rem;
      color: var(--text-main);
      text-align: center;
      font-weight: 500;
    }
    /* Footer */
    footer {
      background-color: #0f172a;
      color: #94a3b8;
      text-align: center;
      padding: 16px 12px;
      margin-top: auto;
      font-size: 0.75rem;
      border-top: 1px solid #1e293b;
    }
    footer .social-links {
      margin-top: 6px;
      display: flex;
      justify-content: center;
      gap: 14px;
    }
    footer a {
      color: var(--white);
      text-decoration: none;
      font-weight: 500;
      display: flex;
      align-items: center;
      gap: 4px;
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <img src="x75.jpg" alt="Background Sekolah" class="header-bg">
    <div class="header-overlay"></div>
    <div class="header-content">
      <h1>SMAN 1 Pangkalan Lada</h1>
      <h2>Informasi Kelas X-7</h2>
      <div id="waktu">Memuat waktu...</div>
    </div>
  </header>
  <!-- Navigasi Menu Grid 3x3 yang Rapi di HP -->
  <div class="nav-container">
    <button class="menu-btn" onclick="showContent('beranda')"><i class="fa-solid fa-house"></i> Beranda</button>
    <button class="menu-btn" onclick="showContent('struktur')"><i class="fa-solid fa-sitemap"></i> Struktur</button>
    <button class="menu-btn" onclick="showContent('anggota')"><i class="fa-solid fa-users"></i> Anggota</button>
    <button class="menu-btn" onclick="showContent('pelajaran')"><i class="fa-solid fa-calendar-days"></i> Jadwal</button>
    <button class="menu-btn" onclick="showContent('piket')"><i class="fa-solid fa-broom"></i> Piket</button>
    <button class="menu-btn" onclick="showContent('pr')"><i class="fa-solid fa-book"></i> Tugas</button>
    <button class="menu-btn" onclick="showContent('galeri')"><i class="fa-solid fa-images"></i> Galeri</button>
    <a href="https://aku-sehat.vercel.app/" target="_blank" class="menu-btn"><i class="fa-solid fa-list-check"></i> Jurnal</a>
    <button class="menu-btn" onclick="showContent('pesan')"><i class="fa-solid fa-envelope"></i> Pesan</button>
  </div>
  <!-- Konten Utama -->
  <main>
    <div id="content" class="card-content">
      <h2>Selamat Datang di Website Kelas X-7!</h2>
      <p>Website resmi kelas X-7 untuk mempermudah koordinasi, melihat jadwal, serta berbagai informasi penting lainnya secara cepat dan rapi.</p>
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
  <!-- Script -->
  <script>
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
    const contentData = {
      beranda: `
        <h2>Selamat Datang di Website Kelas X-7!</h2>
        <p>Website resmi kelas X-7 untuk mempermudah koordinasi akademik, melihat jadwal, serta berbagai informasi penting lainnya secara cepat, rapi, dan terpadu.</p>
      `,
      struktur: `
        <h2>Struktur Organisasi Kelas X-7</h2>
        <div class="table-responsive">
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
        <h2>Daftar Anggota Siswa Kelas X-7</h2>
        <div class="table-responsive">
          <table>
            <tr>
              <th style="width: 35px; text-align: center;">No</th>
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
        <div class="table-responsive">
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
        <div class="table-responsive">
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
        <div style="background: #f8fafc; border-left: 3px solid var(--primary-color); padding: 10px; border-radius: 6px;">
          <h4 style="color: var(--primary-color); margin-bottom: 2px; font-size: 0.85rem;">Pengumuman Tugas</h4>
          <p style="font-size: 0.78rem;">Silakan cek secara berkala atau tanyakan langsung melalui kotak pesan jika ada tugas yang belum dimengerti.</p>
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
        <div style="max-width: 100%; margin: 0 auto; background: #efeae2; border-radius: 10px; box-shadow: 0 4px 12px rgba(0,0,0,0.08); overflow: hidden;">
          <div style="background: #005e54; color: white; padding: 8px 12px; display: flex; align-items: center; gap: 8px;">
            <div style="width: 30px; height: 30px; background: #128c7e; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; font-size: 13px;">
              <i class="fa-solid fa-user"></i>
            </div>
            <div>
              <h4 style="margin: 0; font-size: 13px; font-weight: 600;">Admin Kelas X-7 (WA)</h4>
              <span style="font-size: 9px; opacity: 0.8;">online</span>
            </div>
          </div>
          <div style="padding: 10px; display: flex; flex-direction: column; gap: 8px;">
            <div style="background: #ffffff; padding: 8px; border-radius: 0 8px 8px 8px; box-shadow: 0 1px 0.5px rgba(0,0,0,0.1);">
              <label style="font-size: 10px; color: #005e54; font-weight: bold; display: block; margin-bottom: 2px;">Nama Kamu:</label>
              <input type="text" id="wa-nama" placeholder="Ketik nama di sini..." style="width: 100%; border: none; outline: none; font-size: 12px; background: transparent;">
            </div>
            <div style="background: #ffffff; padding: 8px; border-radius: 0 8px 8px 8px; box-shadow: 0 1px 0.5px rgba(0,0,0,0.1);">
              <label style="font-size: 10px; color: #005e54; font-weight: bold; display: block; margin-bottom: 2px;">Tulis Pesan / Tugas:</label>
              <textarea id="wa-pesan" placeholder="Ketik pesan atau tanyakan tugas..." rows="2" style="width: 100%; border: none; outline: none; font-size: 12px; background: transparent; resize: none;"></textarea>
            </div>
            <div style="display: flex; align-items: center; gap: 6px; background: #f0f2f5; padding: 4px 8px; border-radius: 18px;">
              <div style="flex-grow: 1; font-size: 10px; color: #667781;">Kirim ke WhatsApp</div>
              <button type="button" onclick="kirimKeWhatsApp()" style="background: #00a884; color: white; border: none; width: 30px; height: 30px; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; font-size: 12px;">
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
    function kirimKeWhatsApp() {
      const nama = document.getElementById('wa-nama').value.trim();
      const pesan = document.getElementById('wa-pesan').value.trim();
      if (!nama || !pesan) {
        alert('Mohon isi Nama dan Pesan terlebih dahulu!');
        return;
      }
      const nomorWa = '6285824522033';
      const teksFormat = `Halo Admin Kelas X-7,%0A%0A*Nama Pengirim:* ${encodeURIComponent(nama)}%0A*Pesan:* ${encodeURIComponent(pesan)}`;
      window.open(`https://wa.me/${nomorWa}?text=${teksFormat}`, '_blank');
    }
  </script>
</body>
</html>
