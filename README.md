# Tarjeta digital — Rosa Villafane S.

Página web de una sola pieza que presenta la tarjeta de Rosa Villafane S.,
Import Manager de **Peru Tractor**, con la tarjeta física renderizada en 3D
sobre los colores y el logotipo de la marca.

## Efectos

- **Inclinación 3D** — la tarjeta sigue el cursor con perspectiva real y sombra que acompaña el movimiento.
- **Brillo especular** — reflejo tipo barniz que se desplaza sobre el papel.
- **Giro anverso/reverso** — clic, toque, tecla Enter o el botón "Girar tarjeta".
- **Fondo de marca** — carbón Peru Tractor con la cuña ámbar y las franjas de oruga del reverso de la tarjeta; la luz del fondo sigue el cursor.

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
- `assets/tarjeta-frente.png` — anverso (datos de contacto y QR), sin el marco blanco.
- `assets/tarjeta-reverso.png` — reverso (logotipo Peru Tractor), sin el marco blanco.
- `assets/logo-perutractor.png` — logotipo extraído del reverso, tinta oscura, fondo transparente.
- `assets/logo-perutractor-claro.png` — el mismo logotipo en tinta clara, para fondo oscuro.
