<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Visor 360 Local</title>
  <style>
    html, body {
      margin: 0; padding: 0;
      width: 100vw; height: 100vh;
      overflow: hidden;
      display: flex; justify-content: center; align-items: center;
      background-color: #ffffff;
      user-select: none;
    }
    #viewer-container {
      width: 100%; height: 100%;
      display: flex; justify-content: center; align-items: center;
      cursor: grab;
    }
    #viewer-container:active { cursor: grabbing; }
    img { max-width: 100%; max-height: 100%; object-fit: contain; }
  </style>
</head>
<body>

  <div id="viewer-container">
    <img id="view-img" src="" alt="Cargando 360..." />
  </div>

  <script>
    const params = new URLSearchParams(window.location.search);
    const productId = params.get('id'); // Ejemplo: BROIN
    const totalFrames = parseInt(params.get('frames')) || 18; // 18 por defecto

    if (productId) {
      const imgElement = document.getElementById('view-img');
      const container = document.getElementById('viewer-container');
      
      let currentFrame = 1;
      let isDragging = false;
      let startX = 0;

      function updateImage(frame) {
        // Lee el formato con espacio y paréntesis: BROIN (1).jpg, BROIN (2).jpg...
        imgElement.src = `./${encodeURIComponent(productId)} (${frame}).jpg`;
      }

      // Carga la primera imagen
      updateImage(currentFrame);

      // Controles de arrastre (Mouse y Touch)
      const startAction = (x) => { isDragging = true; startX = x; };
      const stopAction = () => { isDragging = false; };
      const moveAction = (x) => {
        if (!isDragging) return;
        const delta = x - startX;
        if (Math.abs(delta) > 10) {
          if (delta > 0) {
            currentFrame = currentFrame >= totalFrames ? 1 : currentFrame + 1;
          } else {
            currentFrame = currentFrame <= 1 ? totalFrames : currentFrame - 1;
          }
          updateImage(currentFrame);
          startX = x;
        }
      };

      container.addEventListener('mousedown', (e) => startAction(e.clientX));
      window.addEventListener('mouseup', stopAction);
      container.addEventListener('mousemove', (e) => moveAction(e.clientX));

      container.addEventListener('touchstart', (e) => startAction(e.touches[0].clientX));
      window.addEventListener('touchend', stopAction);
      container.addEventListener('touchmove', (e) => moveAction(e.touches[0].clientX));

    } else {
      document.body.innerHTML = "<p style='font-family:sans-serif; text-align:center;'>Falta el parámetro id del producto.</p>";
    }
  </script>

</body>
</html>
