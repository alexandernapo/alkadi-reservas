# Alkadi Paintball - versión de un solo archivo

Esta versión NO necesita Node.js, npm, ni ningún programa instalado para
hacer cambios. Todo el código de la app vive en `index.html`, y puedes
editarlo directamente desde el editor web de GitHub (el lapicito ✏️ que
aparece al ver el archivo en GitHub.com).

## Archivos
- `index.html` — toda la aplicación (esto es lo único que normalmente vas
  a tocar cuando pidas un cambio).
- `manifest.webmanifest` — datos de la app instalable (nombre, ícono).
- `sw.js` — recibe las notificaciones push aunque la app esté cerrada.
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — íconos.
- `vercel.json` — le dice a Vercel que NO hay que compilar nada, solo
  servir los archivos tal cual.

## Cómo reemplazar tu proyecto actual

1. Entra a tu repositorio en GitHub (`github.com/alexandernapo/alkadi-reservas`).
2. Borra los archivos viejos: `src/`, `vite.config.js`, `package.json`,
   `package-lock.json`, `postcss.config.js`, `tailwind.config.js`, el
   `index.html` viejo, y la carpeta `public/` (sus íconos ya vienen aquí
   sueltos, en la raíz).
   - Puedes hacerlo seleccionando cada archivo/carpeta en GitHub y
     usando la opción de eliminar, o simplemente subiendo los archivos
     nuevos encima y borrando después los que sobren.
3. Sube (arrastra) todos los archivos de este paquete a la raíz del
   repositorio ("Add file" → "Upload files" en GitHub).
4. Confirma los cambios ("Commit changes").
5. En Vercel: entra al proyecto → **Settings** → **Build and Deployment**
   → cambia **Framework Preset** a "Other", deja **Build Command** y
   **Output Directory** vacíos (o pon "." en Output Directory). Guarda.
6. Vercel vuelve a publicar solo. Tu enlace (`alkadi-reservas.vercel.app`)
   sigue siendo el mismo.

## Cómo hacer cambios después de esto
Cuando quieras un cambio, en vez de mandarte un `App.jsx` para reemplazar
con `npm`/`git`, te voy a mandar el bloque de código exacto para pegar
en `index.html` desde el editor de GitHub — sin instalar nada, ni en tu
computadora ni en tu celular.
