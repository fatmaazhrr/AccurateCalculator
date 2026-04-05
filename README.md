<!DOCTYPE html>
<html>
<head><title>Pricelist Accurate Online</title></head>
<body>
  <h2>Perhitungan Harga Berlangganan Accurate Online</h2>
  <label>Jumlah User Tambahan: <input type="number" id="users" min="0" value="0"></label><br>
  <label>Add-on Cabang: <input type="number" id="cabang" min="0" value="0"></label><br>
  <label>Add-on POS: <input type="number" id="pos" min="0" value="0"></label><br>
  <button onclick="hitung()">Hitung Total</button>
  <p id="total">Harga Basic (1 Tahun): Rp 3.219.000</p>

  <script>
  function hitung() {
    const users = parseInt(document.getElementById('users').value) * 266400;
    const cabang = parseInt(document.getElementById('cabang').value) * 999000; // Contoh diskon dari Excel
    const pos = parseInt(document.getElementById('pos').value) * 999000;
    const basic = 3219000;
    const total = basic + users + cabang + pos;
    document.getElementById('total').innerHTML = 'Total Harga: Rp ' + total.toLocaleString('id-ID');
  }
  </script>
</body>
</html>
