# Tarjeta ejecutiva digital — Rosa Villafane S.

Micrositio de una sola página para **Rosa Villafane S., Import Manager de Peru Tractor**.
Sitio estático: HTML, CSS y JS en un único archivo, sin framework, sin build y sin dependencias.

## Stack

No hay `package.json`, `vercel.json` ni paso de compilación. Vercel sirve `index.html`
desde la raíz tal cual. Cualquier cambio se despliega con un push.

## Configuración

Todos los datos viven en el objeto `PERFIL`, dentro de `index.html`:

```js
var PERFIL = {
  nombre: 'Rosa Villafane S.',
  cargo:  'Import Manager',
  empresa:'Peru Tractor',
  correo: 'importaciones@perutractor.com',
  telefono:'(01) 434 1400',
  telefonoE164:'+5114341400',
  web:    'https://www.perutractor.com',
  direccion:'Av. Michael Faraday 475, Urb. Santa Rosa, Ate, Lima'
}
```

De ahí salen los enlaces (`mailto:`, `tel:`, Maps, web), el `.vcf`, los datos
estructurados JSON-LD y los textos marcados con `data-campo`. Para reutilizar la
página con otro ejecutivo de Peru Tractor basta con editar ese objeto y sustituir
las dos imágenes de la tarjeta.

## Estructura

| Archivo | Contenido |
|---|---|
| `index.html` | Página completa: metadatos, estilos, marcado y lógica |
| `assets/tarjeta-frente.webp` · `.png` | Anverso (WebP servido, PNG de respaldo) |
| `assets/tarjeta-reverso.webp` · `.png` | Reverso |
| `assets/logo-perutractor-claro.png` | Logotipo en tinta clara, extraído del reverso |
| `assets/logo-perutractor.png` | El mismo logotipo en tinta oscura |
| `assets/fondo-maquinaria.webp` | Excavadora del reverso, textura de fondo |
| `assets/og-rosa-villafane.jpg` | Previsualización 1200×630 para WhatsApp y redes |

## Comportamiento

- **Tarjeta 3D** — `preserve-3d`, giro de 620 ms, inclinación al cursor en escritorio
  y al arrastrar el dedo en táctil, sombra proyectada y brillo especular. Es un
  `<button>`, así que funciona con teclado y lector de pantalla.
- **Guardar contacto** — genera un vCard 3.0 (Blob, sin BOM) compatible con iPhone,
  Android, Outlook y Google Contacts, con confirmación visual.
- **Barra inferior móvil** — Guardar · Correo · Llamar, con `backdrop-filter`,
  respeta el safe-area del iPhone y se retira al llegar al pie.
- **Fondo** — CSS: degradado radial, rejilla técnica, rayado diagonal y glow ámbar;
  la única imagen es la excavadora al 13 % de opacidad.
- Todas las diagonales de la página comparten un mismo eje (`--eje: 74deg`).
- `prefers-reduced-motion` detiene las animaciones.

## Anchos verificados

320 · 375 · 390 · 430 · tablet 820 · 1366 · 1440 · 1920.
Sin desbordamiento horizontal, la tarjeta siempre dentro del viewport y ningún
objetivo táctil por debajo de 44 px.

## Pendiente del propietario

- **Dominio de producción**: `canonical`, `og:url` y `og:image` usan
  `https://rosavillafane.vercel.app/`. Si el dominio real es otro, hay que
  sustituirlo (son cuatro líneas en el `<head>`), o la previsualización de
  WhatsApp y LinkedIn no cargará la imagen.
- **WhatsApp**: no se añadió porque el único número disponible es un fijo. Si existe
  un móvil corporativo, se agrega como acción adicional.
- **Destino del QR** del anverso: conviene escanearlo y confirmar a dónde lleva.
