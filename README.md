{
  "manifest_version": 3,
  "name": "Nueva Pestaña Kawaii",
  "version": "1.0",
  "description": "Reemplaza la nueva pestaña con un fondo anime/kawaii personalizado.",
  "chrome_url_overrides": {
    "newtab": "newtab.html"
  }
}


<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>New Tab</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: url('fondo.jpg') no-repeat center center fixed;
      background-size: cover;
      font-family: Arial, sans-serif;
    }
    .hora {
      position: absolute;
      top: 20px;
      left: 20px;
      font-size: 48px;
      font-weight: bold;
      color: white;
      text-shadow: 0px 0px 8px black;
    }
  </style>
</head>
<body>
  <div class="hora" id="hora"></div>

  <script>
    function actualizarHora() {
      const h = new Date().toLocaleTimeString();
      document.getElementById('hora').textContent = h;
    }
    setInterval(actualizarHora, 1000);
    actualizarHora();
  </script>
</body>
</html>


