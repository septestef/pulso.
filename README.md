# PULSO

Aplicación para registrar una puntuación diaria y elegir actividades de bienestar para el día siguiente. PULSO no requiere cuentas: las puntuaciones y las cartas se guardan localmente en el navegador de cada dispositivo.

## Probar en Windows

1. Abrí PowerShell en la carpeta del proyecto.
2. Ejecutá `node server.js`.
3. Abrí `http://localhost:8000` en el navegador.

Dejá PowerShell abierto mientras usás PULSO; `Ctrl+C` detiene el servidor. No hace falta instalar paquetes ni configurar correo. Para probar exactamente los archivos que se publicarán, ejecutá `node build.js` y después `node server.js --dist`.

## Preparar la publicación

1. Ejecutá `node build.js`. Esto crea la carpeta `dist/` con los archivos públicos de la aplicación; no incluye `.pulso-data`, `node_modules` ni los archivos de desarrollo.
2. Publicá el contenido de `dist/` en un hosting estático que ofrezca HTTPS. Si el hosting pide una carpeta de publicación, elegí `dist`. Para una publicación automática desde el repositorio, usá `node build.js` como comando de compilación y `dist` como carpeta de salida.
3. Abrí la dirección HTTPS desde el teléfono. En Android, usá el menú del navegador y elegí «Instalar aplicación» o «Agregar a pantalla principal». En iPhone, usá Compartir y luego «Agregar a pantalla de inicio».

La aplicación incluye manifiesto, Service Worker e íconos PNG de 192×192 y 512×512 para facilitar la instalación en navegadores compatibles. HTTPS es necesario para instalarla desde una dirección pública; `localhost` se permite para desarrollo.

## Datos y conexión

- No hay cuentas, contraseñas, correo ni sincronización con servidores.
- Las puntuaciones, actividades elegidas y cartas se guardan en el almacenamiento local del navegador de ese dispositivo. Cambiar de dispositivo o borrar sus datos de navegación no traslada los registros.
- Las sugerencias vienen incluidas y la aplicación puede abrirse sin conexión después de cargarla por primera vez con internet.
- El hosting solo entrega los archivos de PULSO. No recibe ni guarda puntuaciones o cartas.
