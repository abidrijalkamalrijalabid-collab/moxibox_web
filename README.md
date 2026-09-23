<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Moxibox - Syarat dan Ketentuan Layanan</title>
    <!-- Gabungan CSS dalam satu file -->
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #161823;
            line-height: 1.6;
        }

        /* Navbar Styling */
        header {
            background-color: #ffffff;
            border-bottom: 1px solid #fe2c5520;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: bold;
            color: #fe2c55;
            font-size: 1.3rem;
            cursor: pointer;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        .nav-links a {
            text-decoration: none;
            color: #161823;
            font-size: 0.95rem;
            transition: color 0.3s;
            cursor: pointer;
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: #fe2c55;
            font-weight: 600;
        }

        /* Sub-header Date */
        .date-banner {
            text-align: center;
            padding: 15px;
            background-color: #ffffff;
            border-bottom: 1px solid #eee;
            font-size: 0.85rem;
            color: #666;
        }

        .date-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #f1f1f2;
            padding: 6px 16px;
            border-radius: 20px;
            border: 1px solid #e3e3e4;
        }

        /* Main Container */
        .main-container {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 280px 1fr;
            gap: 40px;
        }

        /* Sidebar Daftar Isi */
        .sidebar {
            background: transparent;
            position: sticky;
            top: 90px;
            height: fit-content;
        }

        .sidebar h3 {
            font-size: 0.85rem;
            text-transform: uppercase;
            color: #8a8b91;
            letter-spacing: 0.5px;
            margin-bottom: 15px;
        }

        .sidebar ul {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .sidebar ul li a {
            text-decoration: none;
            color: #565865;
            font-size: 0.9rem;
            display: block;
            transition: color 0.2s, font-weight 0.2s;
            cursor: pointer;
        }

        .sidebar ul li a:hover,
        .sidebar ul li a.active {
            color: #fe2c55;
            font-weight: 600;
        }

        /* Content Area */
        .content {
            background: transparent;
        }

        .alert-box {
            background-color: #fe2c550d;
            border: 1px solid #fe2c5530;
            color: #161823;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 30px;
            font-size: 0.95rem;
        }

        .section-title {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 20px;
        }

        .section-number {
            background-color: #fe2c55;
            color: white;
            width: 32px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 6px;
            font-weight: 600;
            font-size: 0.95rem;
        }

        .section-title h2 {
            font-size: 1.3rem;
            color: #161823;
        }

        .content p {
            margin-bottom: 16px;
            color: #565865;
            font-size: 0.95rem;
            line-height: 1.7;
        }

        .content strong {
            color: #161823;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        /* Contact Action Button Styling */
        .contact-card {
            background: #ffffff;
            border: 1px solid #e3e3e4;
            padding: 20px;
            border-radius: 8px;
            margin-top: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .btn-call {
            background-color: #fe2c55;
            color: white;
            padding: 10px 20px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: background-color 0.3s;
        }

        .btn-call:hover {
            background-color: #e02449;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .main-container {
                grid-template-columns: 1fr;
            }
            .sidebar {
                display: none;
            }
            .nav-links {
                display: none;
            }
            .contact-card {
                flex-direction: column;
                gap: 15px;
                align-items: flex-start;
            }
        }
    </style>
</head>
<body>

    <!-- Header / Navbar -->
    <header>
        <div class="navbar">
            <div class="logo-area" onclick="switchTab(event, 'ketentuan-layanan')">
                <span>🎵 Moxibox</span>
            </div>
            <ul class="nav-links">
                <li><a onclick="switchTab(event, 'page-beranda')">Beranda</a></li>
                <li><a onclick="switchTab(event, 'page-tentang')" class="active">Tentang</a></li>
                <li><a onclick="switchTab(event, 'page-newsroom')">Newsroom</a></li>
                <li><a onclick="switchTab(event, 'page-karier')">Karier</a></li>
                <li><a onclick="switchTab(event, 'page-bantuan')">Pusat Bantuan</a></li>
                <li><a onclick="switchTab(event, 'page-keamanan')">Keamanan</a></li>
                <li><a onclick="switchTab(event, 'page-kontak')">Kontak</a></li>
            </ul>
        </div>
    </header>

    <!-- Date Banner -->
    <div class="date-banner">
        <div class="date-badge">
            <span>🕒</span> Terakhir diperbarui: 18 September 2026
        </div>
    </div>

    <!-- Main Layout -->
    <main class="main-container">

        <!-- Sidebar Daftar Isi -->
        <aside class="sidebar">
            <h3>Daftar Isi</h3>
            <ul>
                <li><a onclick="switchTab(event, 'ketentuan-layanan')">1. Ketentuan Layanan</a></li>
                <li><a onclick="switchTab(event, 'pemberi-layanan')">2. Pemberi Layanan</a></li>
                <li><a onclick="switchTab(event, 'kelayakan-usia')">3. Kelayakan Usia & Akun</a></li>
                <li><a onclick="switchTab(event, 'akses-layanan')">4. Akses & Penggunaan Layanan</a></li>
                <li><a onclick="switchTab(event, 'konten-pengguna')">5. Konten Pengguna & Hak Cipta</a></li>
                <li><a onclick="switchTab(event, 'aturan-komunitas')">6. Panduan & Aturan Komunitas</a></li>
                <li><a onclick="switchTab(event, 'pembelian-virtual')">7. Koin & Item Virtual</a></li>
                <li><a onclick="switchTab(event, 'penangguhan')">8. Penangguhan & Penghentian Akun</a></li>
                <li><a onclick="switchTab(event, 'tanggung-jawab')">9. Batasan Tanggung Jawab</a></li>
                <li><a onclick="switchTab(event, 'ganti-rugi')">10. Ganti Rugi</a></li>
                <li><a onclick="switchTab(event, 'hukum-yang-berlaku')">11. Hukum yang Berlaku</a></li>
                <li><a onclick="switchTab(event, 'perubahan')">12. Perubahan Ketentuan</a></li>
            </ul>
        </aside>

        <!-- Content Area -->
        <section class="content">
            <div class="alert-box">
                Selamat datang di Moxibox! Gunakan navigasi di atas dan samping untuk menjelajahi informasi dan ketentuan layanan kami.
            </div>

            <!-- Konten Menu Navbar: Beranda -->
            <div id="page-beranda" class="tab-content">
                <div class="section-title">
                    <div class="section-number">🏠</div>
                    <h2>Beranda Moxibox</h2>
                </div>
                <p>Selamat datang di halaman utama portal informasi resmi Moxibox. Platform kami dirancang untuk menginspirasi kreativitas dan membawa kegembiraan melalui video pendek yang kreatif, autentik, dan menghibur.</p>
                <p>Jelajahi berbagai tren global, temukan kreator favorit Anda, dan mulailah membagikan momen berharga Anda ke seluruh dunia.</p>
            </div>

            <!-- Konten Menu Navbar: Tentang -->
            <div id="page-tentang" class="tab-content active">
                <div class="section-title">
                    <div class="section-number">ℹ️</div>
                    <h2>Tentang Kami</h2>
                </div>
                <p>Moxibox adalah destinasi terdepan untuk video seluler berdurasi pendek. Misi kami adalah menginspirasi kreativitas dan membawa kegembiraan.</p>
                <p>Kami memiliki kantor utama di <strong>PT SOFHTWHARE TECHNOLOGY CAPITAL</strong> yang berlokasi di Sidomulyo, Sumbergedong, Trenggalek, Jawa Timur.</p>
            </div>

            <!-- Konten Menu Navbar: Newsroom -->
            <div id="page-newsroom" class="tab-content">
                <div class="section-title">
                    <div class="section-number">📰</div>
                    <h2>Newsroom Moxibox</h2>
                </div>
                <p>Temukan berita terbaru, pengumuman resmi, pembaruan fitur produk, serta berbagai cerita inspiratif langsung dari pusat berita global Moxibox.</p>
            </div>

            <!-- Konten Menu Navbar: Karier -->
            <div id="page-karier" class="tab-content">
                <div class="section-title">
                    <div class="section-number">💼</div>
                    <h2>Karier di Moxibox</h2>
                </div>
                <p>Jadilah bagian dari tim yang dinamis dan inovatif. Kami selalu mencari talenta-talenta berbakat di bidang teknik, produk, desain, keselamatan, dan pemasaran untuk membangun masa depan hiburan digital bersama.</p>
            </div>

            <!-- Konten Menu Navbar: Pusat Bantuan -->
            <div id="page-bantuan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">❓</div>
                    <h2>Pusat Bantuan</h2>
                </div>
                <p>Butuh bantuan seputar pengaturan akun, pemulihan kata sandi, panduan kreator, atau pelaporan masalah teknis? Tim dukungan kami siap membantu Anda menemukan solusi dengan cepat.</p>
            </div>

            <!-- Konten Menu Navbar: Keamanan -->
            <div id="page-keamanan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">🛡️</div>
                    <h2>Pusat Keamanan</h2>
                </div>
                <p>Keamanan komunitas adalah prioritas utama kami. Pelajari berbagai alat kontrol orang tua, panduan privasi digital, serta komitmen kami dalam menjaga lingkungan platform yang aman dan positif.</p>
            </div>

            <!-- Konten Menu Navbar: Kontak -->
            <div id="page-kontak" class="tab-content">
                <div class="section-title">
                    <div class="section-number">📞</div>
                    <h2>Hubungi Kami</h2>
                </div>
                <p>Untuk pertanyaan bisnis, kerja sama media, urusan hukum, atau dukungan regulasi, Anda dapat menghubungi kantor operasional kami atau mengirimkan pesan langsung melalui formulir di bawah ini:</p>

                <!-- Informasi Kontak -->
                <div class="contact-card">
                    <div>
                        <strong>Layanan Pelanggan & Dukungan Resmi</strong>
                        <p style="margin: 5px 0 0 0; color: #fe2c55; font-weight: bold; font-size: 1.1rem;">+62 21 5088 0000</p>
                        <p style="margin: 5px 0 0 0; font-size: 0.85rem;">Senin - Jumat (09.00 - 17.00 WIB)</p>
                    </div>
                    <!-- Tombol mailto ke CS Muxibox -->
                    <a href="mailto:csmuxibox@gmail.com?subject=Pertanyaan%20Dukungan%20Moxibox" class="btn-call">✉️ Kirim Email ke CS</a>
                </div>

                <!-- Formulir Pesan Langsung -->
                <div style="margin-top: 30px; background: #ffffff; border: 1px solid #e3e3e4; padding: 25px; border-radius: 8px;">
                    <h3 style="margin-bottom: 15px; font-size: 1.1rem; color: #161823;">Kirim Pesan Langsung ke CS</h3>
                    <form onsubmit="kirimPesanGmail(event)">
                        <div style="margin-bottom: 15px;">
                            <label style="display: block; margin-bottom: 5px; font-size: 0.9rem; font-weight: 600;">Email Anda:</label>
                            <input type="email" id="user-email" required placeholder="nama@email.com" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 6px; font-size: 0.95rem;">
                        </div>
                        <div style="margin-bottom: 15px;">
                            <label style="display: block; margin-bottom: 5px; font-size: 0.9rem; font-weight: 600;">Pesan:</label>
                            <textarea id="user-message" required rows="4" placeholder="Tuliskan kendala atau pertanyaan Anda di sini..." style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 6px; font-size: 0.95rem;"></textarea>
                        </div>
                        <button type="submit" style="background-color: #fe2c55; color: white; border: none; padding: 10px 20px; border-radius: 6px; font-weight: 600; cursor: pointer; font-size: 0.9rem;">Kirim Pesan</button>
                    </form>
                </div>
            </div>

            <!-- Tab 1: Ketentuan Layanan -->
            <div id="ketentuan-layanan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">1</div>
                    <h2>Ketentuan Layanan</h2>
                </div>
                <p>Ketentuan Layanan ini merupakan perjanjian mengikat secara hukum antara Anda ("Pengguna" atau "Anda") dengan pihak Moxibox mengenai akses dan penggunaan Anda terhadap aplikasi seluler, situs web, serta produk digital lainnya yang kami sediakan.</p>
                <p>Dengan membuat akun, mengunduh, atau menggunakan aplikasi Moxibox dalam bentuk apa pun, Anda menyatakan bahwa Anda telah membaca, memahami, dan setuju untuk terikat oleh seluruh syarat dan ketentuan yang tercantum dalam dokumen ini.</p>
                <p>Jika Anda tidak menyetujui sebagian atau seluruh ketentuan ini, Anda tidak diperkenankan untuk mengakses atau menggunakan layanan Moxibox.</p>
            </div>

            <!-- Tab 2: Pemberi Layanan -->
            <div id="pemberi-layanan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">2</div>
                    <h2>Pemberi Layanan</h2>
                </div>
                <p>Bergantung pada lokasi tempat tinggal Anda saat mengakses platform Moxibox, entitas hukum yang menyediakan layanan kepada Anda adalah:</p>
                <p><strong>PT SOFHTWHARE TECHNOLOGY CAPITAL / MOXIBOX PTE. LTD.</strong><br>
                Sidomulyo, Sumbergedong, Trenggalek, Jawa Timur.<br>
                Email Dukungan Hukum: legal@moxibox.com</p>
                <p>Entitas ini memiliki kendali penuh atas pengoperasian platform, pemrosesan data, serta penyediaan fitur-fitur hiburan digital di wilayah operasional terkait.</p>
            </div>

            <!-- Tab 3: Kelayakan Usia & Akun -->
            <div id="kelayakan-usia" class="tab-content">
                <div class="section-title">
                    <div class="section-number">3</div>
                    <h2>Kelayakan Usia & Akun</h2>
                </div>
                <p>Anda harus berusia minimal 13 tahun (atau batasan usia minimum yang lebih tinggi di yurisdiksi Anda) untuk membuat akun dan menggunakan layanan Moxibox.</p>
                <p><strong>Ketentuan Pembuatan Akun:</strong></p>
                <p>• Jika Anda berusia di bawah 18 tahun (atau belum dewasa secara hukum), Anda menyatakan telah mendapatkan izin dari orang tua atau wali yang sah untuk menggunakan Moxibox.<br>
                • Anda bertanggung jawab penuh untuk menjaga kerahasiaan kata sandi dan seluruh aktivitas yang terjadi di dalam akun Anda.<br>
                • Informasi yang Anda berikan saat pendaftaran harus akurat, lengkap, dan selalu diperbarui.</p>
            </div>

            <!-- Tab 4: Akses & Penggunaan Layanan -->
            <div id="akses-layanan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">4</div>
                    <h2>Akses & Penggunaan Layanan</h2>
                </div>
                <p>Moxibox memberikan Anda lisensi pribadi, dunia, non-eksklusif, tidak dapat dialihkan, dan dapat dicabut untuk menggunakan layanan kami semata-mata untuk hiburan pribadi dan non-komersial.</p>
                <p>Anda dilarang keras untuk menyalahgunakan platform, termasuk melakukan rekayasa balik (reverse engineering) pada sistem, mencoba mendapatkan akses tanpa izin ke server kami, atau menggunakan bot otomatis untuk mengikis data dan memanipulasi metrik penayangan.</p>
            </div>

            <!-- Tab 5: Konten Pengguna & Hak Cipta -->
            <div id="konten-pengguna" class="tab-content">
                <div class="section-title">
                    <div class="section-number">5</div>
                    <h2>Konten Pengguna & Hak Cipta</h2>
                </div>
                <p>Platform kami memungkinkan Anda untuk mengunggah, membuat, mengirimkan, dan membagikan konten berupa video, teks, foto, musik, dan komentar ("Konten Pengguna").</p>
                <p>Anda tetap memegang hak kepemilikan atas konten yang Anda buat. Namun, dengan mengunggah konten ke Moxibox, Anda memberikan lisensi global, bebas royalti, dan dapat disublisensikan kepada Moxibox untuk menggunakan, mendistribusikan, memodifikasi, dan menampilkan konten tersebut dalam rangka pengoperasian platform.</p>
            </div>

            <!-- Tab 6: Panduan & Aturan Komunitas -->
            <div id="aturan-komunitas" class="tab-content">
                <div class="section-title">
                    <div class="section-number">6</div>
                    <h2>Panduan & Aturan Komunitas</h2>
                </div>
                <p>Keamanan dan kenyamanan komunitas adalah prioritas utama kami. Anda wajib mematuhi <strong>Panduan Komunitas Moxibox</strong> yang melarang keras:</p>
                <p>• Konten yang mengandung unsur kekerasan, kebencian, pelecehan, atau perundungan (bullying).<br>
                • Penyebaran informasi palsu (hoaks), penipuan, atau konten yang membahayakan keselamatan publik.<br>
                • Pelanggaran hak kekayaan intelektual milik pihak lain.</p>
            </div>

            <!-- Tab 7: Koin & Item Virtual -->
            <div id="pembelian-virtual" class="tab-content">
                <div class="section-title">
                    <div class="section-number">7</div>
                    <h2>Koin & Item Virtual</h2>
                </div>
                <p>Moxibox menyediakan fitur pembelian mata uang virtual (seperti Koin) yang dapat digunakan untuk memberikan hadiah virtual (virtual gifts) kepada kreator favorit Anda saat siaran langsung (LIVE) atau melalui video.</p>
                <p>Seluruh transaksi pembelian bersifat final dan tidak dapat dikembalikan (non-refundable), kecuali diwajibkan oleh ketentuan hukum yang berlaku.</p>
            </div>

            <!-- Tab 8: Penangguhan & Penghentian Akun -->
            <div id="penangguhan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">8</div>
                    <h2>Penangguhan & Penghentian Akun</h2>
                </div>
                <p>Kami berhak untuk menangguhkan, membatasi, atau menghentikan akses Anda ke akun Moxibox sewaktu-waktu tanpa pemberitahuan sebelumnya jika:</p>
                <p>• Anda melanggar ketentuan layanan atau Panduan Komunitas kami.<br>
                • Terdapat indikasi aktivitas mencurigakan, penipuan, atau pelanggaran hukum yang melibatkan akun Anda.<br>
                • Kebijakan operasional atau pertimbangan keamanan mendesak mengharuskan tindakan tersebut.</p>
            </div>

            <!-- Tab 9: Batasan Tanggung Jawab -->
            <div id="tanggung-jawab" class="tab-content">
                <div class="section-title">
                    <div class="section-number">9</div>
                    <h2>Batasan Tanggung Jawab</h2>
                </div>
                <p>Layanan Moxibox disediakan "sebagaimana adanya" (as is) tanpa jaminan dalam bentuk apapun, baik tersurat maupun tersirat.</p>
                <p>Kami tidak bertanggung jawab atas kerugian tidak langsung, insidental, khusus, atau kerugian konsekuensial yang timbul dari penggunaan Anda terhadap platform, termasuk gangguan teknis, kehilangan data, atau tindakan pengguna lain.</p>
            </div>

            <!-- Tab 10: Ganti Rugi -->
            <div id="ganti-rugi" class="tab-content">
                <div class="section-title">
                    <div class="section-number">10</div>
                    <h2>Ganti Rugi</h2>
                </div>
                <p>Anda setuju untuk membela, mengganti rugi, dan membebaskan Moxibox, perusahaan induk, afiliasi, pejabat, direktur, dan karyawannya dari setiap klaim, kewajiban, kerugian, atau biaya (termasuk biaya hukum) yang timbul akibat pelanggaran Anda terhadap Ketentuan Layanan ini.</p>
            </div>

            <!-- Tab 11: Hukum yang Berlaku -->
            <div id="hukum-yang-berlaku" class="tab-content">
                <div class="section-title">
                    <div class="section-number">11</div>
                    <h2>Hukum yang Berlaku</h2>
                </div>
                <p>Ketentuan Layanan ini diatur dan ditafsirkan berdasarkan hukum yang berlaku di wilayah operasional setempat, atau merujuk pada yurisdiksi internasional yang disepakati dalam kontrak penyediaan layanan digital lintas batas.</p>
                <p>Setiap sengketa yang timbul akan diselesaikan melalui musyawarah mufakat atau melalui badan arbitrase resmi yang memiliki yurisdiksi hukum terkait.</p>
            </div>

            <!-- Tab 12: Perubahan Ketentuan -->
            <div id="perubahan" class="tab-content">
                <div class="section-title">
                    <div class="section-number">12</div>
                    <h2>Perubahan Ketentuan</h2>
                </div>
                <p>Kami dapat mengubah atau memperbarui Syarat dan Ketentuan ini dari waktu ke waktu untuk mencerminkan perubahan fitur, standar industri, atau regulasi hukum yang berlaku.</p>
                <p>Pemberitahuan mengenai perubahan material akan diumumkan melalui aplikasi atau situs web resmi kami. Penggunaan berkelanjutan Anda terhadap Moxibox setelah perubahan tersebut berlaku dianggap sebagai bentuk persetujuan Anda.</p>
            </div>

        </section>

    </main>

    <!-- JavaScript untuk Interaksi Navigasi & Formulir Kontak -->
    <script>
        function switchTab(event, targetId) {
            event.preventDefault();

            // Sembunyikan semua konten tab
            const contents = document.querySelectorAll('.tab-content');
            contents.forEach(content => {
                content.classList.remove('active');
            });

            // Hapus kelas active dari semua link sidebar
            const sidebarLinks = document.querySelectorAll('.sidebar ul li a');
            sidebarLinks.forEach(link => {
                link.classList.remove('active');
            });

            // Hapus kelas active dari semua link navbar
            const navLinks = document.querySelectorAll('.nav-links a');
            navLinks.forEach(link => {
                link.classList.remove('active');
            });

            // Tampilkan konten target jika ada
            const targetContent = document.getElementById(targetId);
            if (targetContent) {
                targetContent.classList.add('active');
            }

            // Tandai link navbar atau sidebar yang bersesuaian agar aktif
            const clickedElement = event.currentTarget;
            if (clickedElement) {
                clickedElement.classList.add('active');
            }

            // Gulir kembali ke bagian atas halaman dengan mulus
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Fungsi untuk mengirim pesan langsung dari form kontak ke email CS
        function kirimPesanGmail(event) {
            event.preventDefault();
            
            const emailUser = document.getElementById('user-email').value;
            const isiPesan = document.getElementById('user-message').value;
            
            const tujuanEmail = "csmuxibox@gmail.com";
            const subjek = encodeURIComponent("Pesan Bantuan dari Pengguna Moxibox: " + emailUser);
            const bodyPesan = encodeURIComponent(`Email Pengirim: ${emailUser}\n\nPesan:\n${isiPesan}`);
            
            // Membuka aplikasi email secara otomatis dengan subjek dan isi yang terisi
            window.location.href = `mailto:${tujuanEmail}?subject=${subjek}&body=${bodyPesan}`;
        }
    </script>

</body>
</html>
