[Uploading index.html…]()
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cek Kuota MRF Media</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 10px;
      background-color: #f4f4f9;
      text-align: center;
    }

    /* Styling tombol refresh */
    .btn-refresh {
      background-color: #007bff;
      color: #ffffff;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      font-weight: bold;
      border-radius: 8px;
      cursor: pointer;
      margin-bottom: 15px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }

    .btn-refresh:active {
      background-color: #0056b3;
    }

    /* Container Iframe */
    .iframe-container {
      width: 100%;
      height: 80vh; /* Tinggi 80% layar HP/Laptop */
      border: 1px solid #ccc;
      border-radius: 8px;
      overflow: hidden;
    }

    iframe {
      width: 100%;
      height: 100%;
      border: none;
    }
  </style>
</head>
<body>

  <!-- Tombol Refresh -->
  <button class="btn-refresh" onclick="refreshIframe()">
    🔄 Refresh / Cek Nomor Lain
  </button>

  <!-- Menampilkan Halaman Web Cek Kuota -->
  <div class="iframe-container">
    <iframe id="frameKuota" src="https://cekkuotamrfmedia.my.id/"></iframe>
  </div>

  <script>
    function refreshIframe() {
      var iframe = document.getElementById('frameKuota');
      // Memuat ulang iframe tanpa me-reload seluruh halaman browser
      iframe.src = iframe.src;
    }
  </script>

</body>
</html>
