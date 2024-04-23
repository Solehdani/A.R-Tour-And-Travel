<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pendaftaran Travel</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
<style>
    body {
        font-family: 'Roboto', sans-serif;
        margin: 0;
        padding: 0;
        background-color: #007bff; /* Warna latar belakang biru */
    }
    .container {
        max-width: 600px;
        margin: 50px auto;
        padding: 20px;
        background-color: #fff;
        border-radius: 8px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        position: relative; /* Tambahkan posisi relatif untuk menengahkan */
    }
    h1 {
        text-align: center;
    }
    form {
        margin-top: 20px;
    }
    label {
        display: block;
        margin-bottom: 5px;
    }
    input[type="text"], input[type="tel"], input[type="number"], select {
        width: 100%;
        padding: 12px; /* Perbesar padding */
        margin-bottom: 10px;
        border: 1px solid #ccc;
        border-radius: 4px;
        box-sizing: border-box;
        font-family: 'Roboto', sans-serif;
    }
    input[type="text"]::placeholder {
        font-style: italic;
    }
    button {
        width: 100%;
        padding: 12px; /* Perbesar padding */
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-family: 'Roboto', sans-serif;
    }
    button:hover {
        background-color: #0056b3;
    }
    .social-icons {
        text-align: center;
        margin-top: 20px;
    }
    .social-icons a {
        display: inline-block;
        margin-right: 10px;
        color: #007bff;
        font-size: 24px;
        transition: color 0.3s;
    }
    .social-icons a:hover {
        color: #0056b3;
    }
    .form-label-bold {
        font-weight: bold;
    }
    /* Menjadikan opsi sedikit transparan */
    select {
        background-color: rgba(255, 255, 255, 0.8); /* Warna putih dengan transparansi 80% */
        padding: 12px; /* Perbesar padding */
        height: auto; /* Buat ketinggian dinamis */
    }
    /* Gaya untuk tulisan opsional di dalam kotak catatan */
    .optional-text {
        font-style: italic;
        color: #aaa;
        position: absolute;
        font-size: 12px;
        margin-left: 5px;
        margin-top: -15px;
    }
    /* Tambahkan gaya untuk syarat dan ketentuan */
    .syarat-ketentuan {
        text-align: center;
        font-size: 12px; /* Ubah ukuran teks */
        margin-top: 20px;
    }
</style>
</head>
<body>

<div class="container">
    <h1>Selamat Datang</h1>
    <p>Silahkan isi formulir di bawah ini untuk pendaftaran travel.</p>
    <form id="registrationForm">
        <label class="form-label-bold" for="name">Nama:</label>
        <input type="text" id="name" name="name" required>
        <label class="form-label-bold" for="notes">Catatan:</label>
        <input type="text" id="notes" name="notes" placeholder="(opsional)">
        <span class="optional-text"></span>

        <label class="form-label-bold" for="passengerCount">Jumlah Penumpang:</label>
        <select id="passengerCount" name="passengerCount" required>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
            <option value="6">6</option>
        </select>

        <label class="form-label-bold" for="pickupDay">Tanggal Penjemputan:</label>
        <select id="pickupDay" name="pickupDay" required>
            <option value="">Pilih Tanggal</option>
            <!-- Tambahkan opsi dari 1 hingga 31 -->
            <script>
                for (let i = 1; i <= 31; i++) {
                    document.write(`<option value="${i}">${i}</option>`);
                }
            </script>
        </select>

        <label class="form-label-bold" for="pickupMonth">Bulan Penjemputan:</label>
        <select id="pickupMonth" name="pickupMonth" required>
            <option value="">Pilih Bulan</option>
            <option value="Januari">Januari</option>
            <option value="Februari">Februari</option>
            <option value="Maret">Maret</option>
            <option value="April">April</option>
            <option value="Mei">Mei</option>
            <option value="Juni">Juni</option>
            <option value="Juli">Juli</option>
            <option value="Agustus">Agustus</option>
            <option value="September">September</option>
            <option value="Oktober">Oktober</option>
            <option value="November">November</option>
            <option value="Desember">Desember</option>
        </select>

        <label class="form-label-bold" for="pickupLocation">Alamat Penjemputan:</label>
        <select id="pickupLocation" name="pickupLocation" required>
            <option value="">Pilih Lokasi Penjemputan</option>
            <optgroup label="Cianjur">
                <option value="Cianjur Selatan">Cianjur Selatan</option>
                <option value="Cianjur Kota">Cianjur Kota</option>
            </optgroup>
            <option value="Bogor">Bogor</option>
            <option value="Bekasi">Bekasi</option>
            <option value="Karawang">Karawang</option>
            <optgroup label="Jakarta">
                <option value="Jakarta Barat">Jakarta Timur</option>
                <option value="Jakarta Timur">Jakarta Barat</option>
                <option value="Jakarta Selatan">Jakarta Pusat</option>
                <option value="Jakarta Pusat">Jakarta Selatan</option>
                <option value="Jakarta Utara">Jakarta Utara</option>
            </optgroup>
            <option value="Tangerang">Tangerang</option>
            <option value="Banten">Banten</option>
        </select>

        <label class="form-label-bold" for="destination">Alamat Tujuan:</label>
        <select id="destination" name="destination" required>
            <option value="">Pilih Tujuan</option>
            <optgroup label="Cianjur">
                <option value="Cianjur Selatan">Cianjur Selatan</option>
                <option value="Cianjur Kota">Cianjur Kota</option>
            </optgroup>
            <option value="Bogor">Bogor</option>
            <option value="Bekasi">Bekasi</option>
            <option value="Karawang">Karawang</option>
            <option value="Jakarta">Jakarta</option>
            <optgroup label="Jakarta">
                <option value="Jakarta Barat">Jakarta Timur</option>
                <option value="Jakarta Timur">Jakarta Barat</option>
                <option value="Jakarta Selatan">Jakarta Pusat</option>
                <option value="Jakarta Pusat">Jakarta Selatan</option>
                <option value="Jakarta Utara">Jakarta Utara</option>
            </optgroup>
            <option value="Tangerang">Tangerang</option>
            <option value="Banten">Banten</option>
        </select>

        <button type="submit">Daftar</button>
    </form>
    <!-- Pindahkan dan perkecil syarat dan ketentuan -->
    <div class="syarat-ketentuan">
        <label class="checkbox-label">
            <input type="checkbox" id="syaratKetentuan">
            <span>Saya setuju dengan <a href="syarat.html">syarat dan ketentuan</a></span>
        </label>
    </div>
    <!-- Tambahkan ikon sosial media -->
    <div class="social-icons">
        <a href="https://api.whatsapp.com/send?phone=6287752863526" target="_blank"><i class="fab fa-whatsapp"></i></a>
        <a href="https://www.facebook.com/" target="_blank"><i class="fab fa-facebook"></i></a>
        <a href="https://www.instagram.com/" target="_blank"><i class="fab fa-instagram"></i></a>
    </div>
</div>

<script>
    document.getElementById("registrationForm").addEventListener("submit", function(event) {
        event.preventDefault(); // Prevent default form submission

        // Get form data
        const formData = new FormData(this);
        const data = {};
        formData.forEach((value, key) => {
            data[key] = value;
        });

        // Format tanggal penjemputan
        const formattedPickupDate = `${data.pickupDay} ${data.pickupMonth}`;

        // Format data for WhatsApp message
        const whatsappMessage = `Nama: ${data.name}%0ACatatan: ${data.notes || '(tidak ada catatan)'}%0AJumlah Penumpang: ${data.passengerCount}%0ATanggal Penjemputan: ${formattedPickupDate}%0AAlamat Penjemputan: ${data.pickupLocation}%0AAlamat Tujuan: ${data.destination}`;

        // Redirect to WhatsApp with prefilled message
        window.location.href = `https://api.whatsapp.com/send?phone=6287752863526&text=${whatsappMessage}`;
    });
</script>

</body>
</html>
