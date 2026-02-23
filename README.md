<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan Rofy & Resti</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Great+Vibes&display=swap" rel="stylesheet">

    <style>
        :root {
            --gold: #D4AF37;
            --gold-muted: #C5A059;
            --off-white: #fdfbf7;
            --white: #ffffff;
            --text-dark: #333333;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Lato', sans-serif;
            --font-accent: 'Great Vibes', cursive;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: var(--font-body); background-color: var(--off-white); color: var(--text-dark); overflow-x: hidden; scroll-behavior: smooth; }
        body.no-scroll { overflow: hidden; }

        /* ANIMASI FADE IN */
        .fade-in { opacity: 0; transform: translateY(30px); transition: 1s all ease-out; }
        .fade-in.visible { opacity: 1; transform: translateY(0); }

        /* OVERLAY */
        #overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: var(--off-white); z-index: 9999; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; transition: 1s ease; }
        
        /* HERO */
        .hero { 
            height: 100vh; 
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1519741497674-611481863552?auto=format&fit=crop&w=1350&q=80'); 
            background-size: cover; background-position: center; 
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center;
        }
        .hero h1 { font-family: var(--font-accent); font-size: 5rem; color: var(--gold); }
        .hero p { font-size: 1.2rem; letter-spacing: 3px; text-transform: uppercase; }

        /* DEKORASI BUNGA */
        .floral-corner { position: absolute; width: 150px; opacity: 0.7; pointer-events: none; z-index: 1; }
        .top-left { top: 0; left: 0; transform: rotate(0deg); }
        .bottom-right { bottom: 0; right: 0; transform: rotate(180deg); }

        /* CONTAINER & CARD */
        .container { width: 90%; max-width: 800px; margin: 0 auto; padding: 60px 20px; text-align: center; position: relative; }
        .section-title { font-family: var(--font-heading); font-size: 2.5rem; color: var(--gold); margin-bottom: 20px; }
        .card { background: white; padding: 40px; border-radius: 15px; border: 1px solid rgba(212, 175, 55, 0.3); box-shadow: 0 10px 30px rgba(0,0,0,0.05); margin-bottom: 40px; }

        /* BUTTON */
        .btn { display: inline-block; padding: 12px 35px; background-color: var(--gold); color: white; border: none; border-radius: 50px; cursor: pointer; font-weight: bold; transition: 0.4s; text-decoration: none; margin-top: 15px; }
        .btn:hover { background-color: var(--gold-muted); transform: scale(1.05); }

        /* COUNTDOWN */
        .timer-container { display: flex; justify-content: center; gap: 15px; margin: 30px 0; }
        .timer-box { background: var(--gold); color: white; padding: 15px; border-radius: 10px; min-width: 80px; }
        .timer-box span { display: block; font-size: 1.8rem; font-weight: bold; }

        iframe { width: 100%; height: 350px; border-radius: 10px; border: 2px solid var(--gold); margin-top: 20px; }
    </style>
</head>
<body class="no-scroll">

    <audio id="weddingMusic" loop>
        <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mpeg">
    </audio>

    <div id="overlay">
        <p style="letter-spacing: 2px;">UNDANGAN PERNIKAHAN</p>
        <h1 style="font-family: var(--font-accent); font-size: 4rem; color: var(--gold); margin: 10px 0;">Rofy & Resti</h1>
        <p style="margin-bottom: 30px; color: #888;">Kepada Bapak/Ibu/Saudara/i</p>
        <button onclick="openInvitation()" class="btn">Buka Undangan</button>
    </div>

    <section class="hero">
        <img src="https://i.ibb.co/L5hYw0C/flower1.png" class="floral-corner top-left" alt="floral">
        <img src="https://i.ibb.co/L5hYw0C/flower1.png" class="floral-corner bottom-right" alt="floral">
        <p>The Wedding of</p>
        <h1>Rofy & Resti</h1>
        <p>31 Mei 2026</p>
    </section>

    <div class="container fade-in">
        <h2 class="section-title">Assalamu’alaikum Wr. Wb.</h2>
        <p style="font-style: italic; font-size: 1.1rem; line-height: 1.8;">
            "Dan di antara tanda-tanda kekuasaan-Nya ialah Dia menciptakan untukmu istri-istri dari jenismu sendiri, supaya kamu cenderung dan merasa tenteram kepadanya, dan dijadikan-Nya di antaramu rasa kasih dan sayang. Sesungguhnya pada yang demikian itu benar-benar terdapat tanda-tanda bagi kaum yang berpikir."
        </p>
        <p style="font-weight: bold; margin-top: 15px; color: var(--gold);">(QS. Ar-Rum: 21)</p>
    </div>

    <div class="container fade-in">
        <h2 class="section-title">Menuju Hari Bahagia</h2>
        <div class="timer-container">
            <div class="timer-box"><span id="days">0</span> Hari</div>
            <div class="timer-box"><span id="hours">0</span> Jam</div>
            <div class="timer-box"><span id="minutes">0</span> Menit</div>
            <div class="timer-box"><span id="seconds">0</span> Detik</div>
        </div>
    </div>

    <div class="container fade-in">
        <div class="card">
            <h2 class="section-title">Waktu & Tempat</h2>
            <p style="font-weight: bold; font-size: 1.2rem;">Minggu, 31 Mei 2026</p>
            <p>Pukul 09:00 WIB - Selesai</p>
            <hr style="margin: 20px auto; width: 50%; opacity: 0.2;">
            <p style="font-weight: bold; font-size: 1.1rem;">Aleyra Hotel and Villa's Garut</p>
            <p>Jl. Cipanas Baru No.1, Pananjung, Kec. Tarogong Kaler, Kabupaten Garut, Jawa Barat</p>
            
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3958.261947262441!2d107.8767355!3d-7.2110298!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e68b19199d3455b%3A0xc07a8275681c2f7b!2sAleyra%20Hotel%20and%20Villa&#39;s%20Garut!5e0!3m2!1sid!2sid!4v1700000000000" allowfullscreen="" loading="lazy"></iframe>
        </div>
    </div>

    <div class="container fade-in">
        <div class="card">
            <h2 class="section-title">Amplop Digital</h2>
            <p style="margin-bottom: 20px;">Tanpa mengurangi rasa hormat, bagi Bapak/Ibu/Saudara/i yang ingin memberikan tanda kasih dapat melalui:</p>
            <div style="background: #f9f9f9; padding: 25px; border-radius: 10px; border-left: 5px solid var(--gold); text-align: center;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/Bank_Mandiri_logo_2016.svg/2560px-Bank_Mandiri_logo_2016.svg.png" alt="Mandiri" style="height: 30px; margin-bottom: 10px;">
                <p style="font-size: 1.2rem; font-weight: bold;" id="norek">1770000386604</p>
                <p>A/N Rofy Ahmad / Resti</p>
                <button onclick="copyNorek()" class="btn" style="padding: 5px 15px; font-size: 0.8rem;">Salin Nomor Rekening</button>
            </div>
        </div>
    </div>

    <div class="container fade-in">
        <h2 class="section-title">Konfirmasi Kehadiran</h2>
        <form id="rsvpForm" class="card" style="text-align: left;">
            <label>Nama Lengkap</label>
            <input type="text" id="nama" required style="width:100%; padding:12px; margin: 10px 0; border: 1px solid #ddd; border-radius: 5px;">
            <label>Status Kehadiran</label>
            <select id="kehadiran" style="width:100%; padding:12px; margin: 10px 0; border: 1px solid #ddd; border-radius: 5px;">
                <option value="Hadir">Hadir</option>
                <option value="Tidak Hadir">Tidak Hadir</option>
            </select>
            <label>Ucapan & Doa</label>
            <textarea id="pesan" style="width:100%; padding:12px; margin: 10px 0; border: 1px solid #ddd; border-radius: 5px;" rows="4"></textarea>
            <button type="submit" class="btn" style="width:100%">Kirim Konfirmasi ke WhatsApp</button>
        </form>
    </div>

    <footer style="padding: 60px 20px; background: #333; color: white; text-align: center;">
        <h2 style="font-family: var(--font-accent); font-size: 2.5rem; color: var(--gold);">Rofy & Resti</h2>
        <p>Sampai Jumpa di Hari Bahagia Kami</p>
        <p style="margin-top: 10px; font-size: 0.8rem; opacity: 0.5;">&copy; 2026</p>
    </footer>

    <script>
        // Fungsi Buka Undangan
        function openInvitation() {
            const music = document.getElementById("weddingMusic");
            music.play().catch(e => console.log("Audio play blocked"));
            document.getElementById("overlay").style.transform = "translateY(-100%)";
            document.body.classList.remove('no-scroll');
            triggerAnimations();
        }

        // Salin Rekening
        function copyNorek() {
            const norek = document.getElementById("norek").innerText;
            navigator.clipboard.writeText(norek);
            alert("Nomor rekening Mandiri berhasil disalin!");
        }

        // Countdown Logic (31 Mei 2026)
        const targetDate = new Date("May 31, 2026 09:00:00").getTime();
        
        function updateCountdown() {
            const now = new Date().getTime();
            const diff = targetDate - now;

            if (diff > 0) {
                document.getElementById("days").innerText = Math.floor(diff / (1000 * 60 * 60 * 24));
                document.getElementById("hours").innerText = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                document.getElementById("minutes").innerText = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
                document.getElementById("seconds").innerText = Math.floor((diff % (1000 * 60)) / 1000);
            } else {
                document.querySelector(".timer-container").innerHTML = "<h3>Hari Bahagia Telah Tiba!</h3>";
            }
        }
        setInterval(updateCountdown, 1000);
        updateCountdown();

        // Animasi Fade In saat Scroll
        function triggerAnimations() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) entry.target.classList.add('visible');
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
        }

        // RSVP ke WhatsApp
        document.getElementById('rsvpForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const waNumber = "628123456789"; // GANTI DENGAN NOMOR WA KAMU
            const nama = document.getElementById('nama').value;
            const kehadiran = document.getElementById('kehadiran').value;
            const pesan = document.getElementById('pesan').value;
            
            const text = `Halo Rofy & Resti, saya *${nama}* ingin mengonfirmasi bahwa saya *${kehadiran}* datang ke pernikahan kalian di Aleyra Hotel Garut.%0A%0A*Pesan/Doa:* ${pesan}`;
            window.open(`https://api.whatsapp.com/send?phone=${waNumber}&text=${text}`, '_blank');
        });
    </script>
</body>
</html>
