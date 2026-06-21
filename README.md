# Notes — Landing page

Landing page de descarga para **Notes**, app de recordatorios con aulas virtuales para alumnos y maestros.

Sitio estático (HTML/CSS/JS, sin build) con botón de descarga del APK de Android.

## Estructura

```
.
├── index.html          # Página principal
├── assets/
│   ├── styles.css      # Estilos (modern dark cinematic)
│   └── script.js       # Scroll reveal, nav, parallax
├── notes.apk           # APK de Android para descargar
└── vercel.json         # Headers de descarga del APK
```

## Desarrollo local

Cualquier servidor estático sirve. Ejemplo:

```bash
npx serve .
# o
python -m http.server 3000
```

Abre http://localhost:3000

## Deploy

Desplegado en Vercel como sitio estático. Cada push a `main` actualiza producción.

```bash
vercel --prod
```

## Actualizar el APK

Reemplaza `notes.apk` con la nueva versión y haz commit:

```bash
git add notes.apk
git commit -m "chore: actualizar APK"
git push
```
