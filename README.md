# Invitación web — Boda de Bárbara

Página de invitación de boda de una sola página con scroll, estilo editorial romántico minimalista: fondo crema, acentos vino/burdeos y detalles florales en acuarela (rosa pastel y verde oliva).

**En línea:** https://juanito-devv.github.io/invitacion-boda/

Se actualiza automáticamente: cada cambio subido a `main` se publica en GitHub Pages sin hacer nada más.

---

## Cómo personalizarla (sin saber programar)

Todo se edita en **un solo lugar**: al final de `index.html`, el bloque `const BODA = { ... }`. Abre el archivo con el Bloc de notas o tu editor y cambia solo las comillas:

| Dato | Dónde (en `const BODA`) | Ejemplo |
| --- | --- | --- |
| Nombre del novio | `novio: '?'` | `novio: 'Ángel'` |
| Fecha | `fecha: '...'` | `fecha: 'Sábado, 18 de octubre'` |
| Hora | `hora: '...'` | `hora: '5:00 p. m.'` |
| Enlace de la transmisión | `youtube: '...'` | `youtube: 'https://www.youtube.com/live/xxxx'` |
| Formulario de asistencia | `forms: '...'` | `forms: 'https://forms.gle/xxxx'` |
| Fotos de la pareja | `fotoArco: '...'` y `fotoOval: '...'` | `fotoArco: 'fotos/novios-1.jpg'` |

### Poner las fotos reales
1. Crea una carpeta `fotos/` junto a `index.html` y copia ahí las fotos (ej. `fotos/novios-1.jpg`, `fotos/novios-2.jpg`).
2. Cambia `fotoArco` y `fotoOval` a esas rutas (recomendado).
3. Sube los cambios a GitHub (van a `git push` y se publican solos).

> Si una foto no carga, la app lo nota y deja un fondo suave con el marco — la página nunca se ve rota.

### Dejarlo en pantalla completa para "hacer como que se abre la invitación"
En el celular: botón **menú del navegador → "Agregar a pantalla de inicio"** y se abre con el ícono del corazón vino, como una app.

---

## Desarrollo

- Proyecto 100% estático: `index.html`, sin dependencias de build.
- Fuentes: Playfair Display (serif) + Plus Jakarta Sans (labels) vía Google Fonts.
- PWA ligera: `manifest.webmanifest` opcional (no incluido; la página incluye `theme-color`, favicon y es responsive).

## Deploy

GitHub Pages desde la rama `main`, carpeta raíz (sin pasos de compilación). Para reproducir en otro repo: réplica este proyecto y activa Pages con "Deploy from a branch → main / (root)".