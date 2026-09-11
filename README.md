# Invitación web — Boda de Bárbara

Página de invitación de boda de una sola página con scroll, estilo editorial romántico minimalista: fondo crema, acentos naranja terracota y detalles florales en acuarela (albaricoque y verde oliva).

**En línea:** https://juanito-devv.github.io/invitacion-boda/

Se actualiza automáticamente: cada cambio subido a `main` se publica en GitHub Pages sin hacer nada más.

---

## Cómo personalizarla (sin saber programar)

Todo se edita en **un solo lugar**: al final de `index.html`, el bloque `const BODA = { ... }`. Abre el archivo con el Bloc de notas o tu editor y cambia solo las comillas:

| Dato | Dónde (en `const BODA`) | Ejemplo |
| --- | --- | --- |
| Nombre del novio | `novio: '?'` | `novio: 'Ángel'` |
| Otros países | `zonas: '...'` | `zonas: 'Argentina 12:45 · Venezuela 11:45 · Colombia 10:45 · España 5:45 p. m.'` |
| Fecha | `fecha: '...'` | `fecha: 'Sábado, 12 de septiembre de 2026'` |
| Hora | `hora: '...'` | `hora: '12:45 p. m. · hora de Chile'` |
| Enlace de la transmisión | `youtube: '...'` | `youtube: 'https://www.youtube.com/live/xxxx'` |
| Formulario de asistencia | `forms: '...'` | `forms: 'https://forms.gle/xxxx'` |
| Fotos de la pareja | `fotoArco: '...'` y `fotoOval: '...'` | `fotoArco: 'Boda1.jpeg'` |

### Las fotos
Ya están en la raíz del repo como `Boda1.jpeg` (arco) y `Boda2.jpeg` (óvalo). Para reemplazarlas, pasa el archivo nuevo sobre el mismo nombre (o copia al repo y cambia `fotoArco`/`fotoOval` en `const BODA`). Si una foto no carga, la app lo nota y deja un fondo suave con el marco — la página nunca se ve rota.

### Dejarlo en pantalla completa para "hacer como que se abre la invitación"
En el celular: botón **menú del navegador → "Agregar a pantalla de inicio"** y se abre con el ícono del corazón vino, como una app.

---

## Desarrollo

- Proyecto 100% estático: `index.html`, sin dependencias de build.
- Fuentes: Playfair Display (serif) + Plus Jakarta Sans (labels) vía Google Fonts.
- PWA ligera: `manifest.webmanifest` opcional (no incluido; la página incluye `theme-color`, favicon y es responsive).

## Deploy

GitHub Pages desde la rama `main`, carpeta raíz (sin pasos de compilación). Para reproducir en otro repo: réplica este proyecto y activa Pages con "Deploy from a branch → main / (root)".