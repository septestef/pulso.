# PULSO

Aplicación para registrar una puntuación diaria y elegir actividades de bienestar para el día siguiente. PULSO no requiere cuentas: las puntuaciones y las cartas se guardan localmente en el navegador de cada dispositivo.

## Probar en Windows

1. Abrí PowerShell en la carpeta del proyecto.
2. Ejecutá `node server.js`.
3. Abrí `http://localhost:8000` en el navegador.

Dejá PowerShell abierto mientras usás PULSO; `Ctrl+C` detiene el servidor.

## Datos y conexión

- No hay cuentas, contraseñas, correo ni sincronización con servidores.
- Las puntuaciones, actividades elegidas y cartas se guardan en el almacenamiento local del navegador de ese dispositivo. Cambiar de dispositivo o borrar sus datos de navegación no traslada los registros.
- Las sugerencias vienen incluidas y la aplicación puede abrirse sin conexión después de cargarla por primera vez con internet.
- El hosting solo entrega los archivos de PULSO. No recibe ni guarda puntuaciones o cartas.
