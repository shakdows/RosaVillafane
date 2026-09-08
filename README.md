# Tarjeta digital — Rosa Villafane Serna

Página web de una sola pieza que presenta la tarjeta de Rosa Villafane Serna,
Import Manager de **Peru Tractor**, con la tarjeta física renderizada en 3D.

## Efectos

- **Inclinación 3D** — la tarjeta sigue el cursor con perspectiva real y sombra que acompaña el movimiento.
- **Brillo especular** — reflejo tipo barniz que se desplaza sobre el papel.
- **Giro anverso/reverso** — clic, toque, tecla Enter o el botón "Girar tarjeta".
- **Halo ambiental** — la luz del fondo sigue el cursor sobre una rejilla industrial.
- **Aparición al hacer scroll** en el bloque de contacto.

## Compatibilidad

| Dispositivo        | Comportamiento                                                    |
|--------------------|-------------------------------------------------------------------|
| Celular            | Tarjeta arriba a ancho completo, botones en rejilla, giro al tocar |
| Celular horizontal | Dos columnas compactas, tarjeta reducida                          |
| Tablet             | Tarjeta protagonista, contacto en dos columnas                    |
| Laptop / PC        | Dos columnas, inclinación y brillo con el mouse                    |
| Monitor grande     | Tarjeta y contenedor ampliados                                    |

Respeta `prefers-reduced-motion` y no requiere ninguna librería externa.

## Publicar

En GitHub: **Settings → Pages → Source: Deploy from a branch → `main` / `root`**.
Queda en `https://shakdows.github.io/RosaVillafane/`.

## Archivos

- `index.html` — la página completa (HTML, CSS y JS en un solo archivo).
- `assets/tarjeta-frente.png` — anverso (datos de contacto y QR).
- `assets/tarjeta-reverso.png` — reverso (logotipo Peru Tractor).
