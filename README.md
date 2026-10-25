lab5_javascript

[index.html](https://github.com/user-attachments/files/33919656/index.html)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktikum JavaScript Pertemuan 6</title>
</head>
<body>
    <h1>Praktikum JavaScript</h1>

    <h2>Latihan 1 dan 2: Output</h2>
    <p id="pesan">Pesan awal</p>
    <button onclick="sapaPengguna()">Masukkan Nama</button>

    <hr>

    <h2>Latihan 3: Operasi Aritmetika</h2>
    <button onclick="operasiDariPrompt()">Hitung Dua Bilangan</button>

    <hr>

    <h2>Latihan 4: Seleksi If-Else</h2>
    <button onclick="cekNilaiPrompt()">Periksa Kelulusan</button>

    <hr>

    <h2>Latihan 5: Seleksi Switch</h2>
    <button onclick="pilihBilangan()">Pilih Angka 1-5</button>

    <hr>

    <h2>Latihan 6: Genap atau Ganjil</h2>
    <label for="bilangan">Masukkan bilangan bulat:</label>
    <input type="number" id="bilangan" step="1">
    <button type="button" onclick="cekBilangan()">Periksa</button>
    <p id="hasilBilangan"></p>

    <hr>

    <h2>Latihan 7: Mengubah Warna</h2>
    <button onclick="ubahWarnaLatar('lightgreen')">Latar Hijau</button>
    <button onclick="ubahWarnaLatar('white')">Latar Putih</button>
    <button onclick="ubahWarnaLatar('lightyellow')">Latar Kuning</button>

    <hr>

    <h2>Latihan 8: Daftar Menu Makanan</h2>
    <label>
        <input type="checkbox" class="menu" value="5000">
        Ayam Goreng — Rp5.000
    </label><br>

    <label>
        <input type="checkbox" class="menu" value="500">
        Tempe — Rp500
    </label><br>

    <label>
        <input type="checkbox" class="menu" value="2500">
        Telur Dadar — Rp2.500
    </label><br>

    <label>
        <input type="checkbox" class="menu" value="3000">
        Es Teh — Rp3.000
    </label><br>

    <label>
        <input type="checkbox" class="menu" value="4000">
        Nasi Putih — Rp4.000
    </label><br>

    <p>Total: Rp<span id="total">0</span></p>

    <hr>

    <h2>Mini Project: Kalkulator Nilai Mahasiswa</h2>

    <form id="formNilai">
        <label for="tugas">Nilai Tugas (0-100):</label><br>
        <input type="number" id="tugas" min="0" max="100"
               step="any" required><br><br>

        <label for="uts">Nilai UTS (0-100):</label><br>
        <input type="number" id="uts" min="0" max="100"
               step="any" required><br><br>

        <label for="uas">Nilai UAS (0-100):</label><br>
        <input type="number" id="uas" min="0" max="100"
               step="any" required><br><br>

        <button type="submit">Hitung Nilai Akhir</button>
    </form>

    <div id="hasilNilai" aria-live="polite"></div>

    <hr>

    <h2>Eksperimen: Tabel Perkalian 7</h2>
    <button onclick="tampilkanPerkalian()">Tampilkan Tabel</button>
    <pre id="tabelPerkalian"></pre>

    <hr>

    <h2>Eksperimen: Tampilkan atau Sembunyikan</h2>
    <button onclick="togglePesan()">Tampilkan/Sembunyikan Pesan</button>
    <p id="pesanToggle">Ini adalah teks yang bisa disembunyikan.</p>

    <script src="script.js"></script>
</body>
</html>

└── script.js
[Uploading script.js// script.js
document.getElementById("pesan").textContent = "Hello World";
console.log("Hello World");
const namaPengguna = prompt("Masukkan nama Anda:", "");
if (namaPengguna && namaPengguna.trim() !== "") {
alert("Halo, " + namaPengguna + "!");
document.getElementById("pesan").textContent = "Selamat datang, " + namaPengguna + ".";
} else {
alert("Nama belum diisi.");
}
function operasiDasar(a, b) {
console.log("Penjumlahan:", a + b);
console.log("Pengurangan:", a - b);
console.log("Perkalian:", a * b);
console.log("Pembagian:", b !== 0 ? a / b : "Tidak dapat dibagi nol");
console.log("Modulus:", a % b);
}
operasiDasar(9, 4);
const inputNilai = prompt("Masukkan nilai (0–100):");
const nilaiMahasiswa = Number(inputNilai);
if (inputNilai === null || inputNilai.trim() === "" ||
Number.isNaN(nilaiMahasiswa) || nilaiMahasiswa < 0 || nilaiMahasiswa > 100) {
alert("Input nilai tidak valid.");
} else if (nilaiMahasiswa >= 60) {
alert("Lulus");
} else {
alert("Belum lulus");
}
const inputPilihan = prompt("Masukkan angka 1–5:");
switch (inputPilihan) {
case "1": alert("Bilangan satu"); break;
case "2": alert("Bilangan dua"); break;
case "3": alert("Bilangan tiga"); break;
case "4": alert("Bilangan empat"); break;
case "5": alert("Bilangan lima"); break;
default: alert("Pilihan tidak tersedia");
}
function cekBilangan() {
const input = document.getElementById("bilangan").value;
const angka = Number(input);
const hasil = document.getElementById("hasilBilangan");
if (input.trim() === "" || !Number.isInteger(angka)) {
hasil.textContent = "Masukkan bilangan bulat yang valid.";
} else if (angka % 2 === 0) {
hasil.textContent = "Bilangan genap";
} else {
hasil.textContent = "Bilangan ganjil";
}
}…]()
