# Landing — kain-mark.github.io

Página web de marca para Kain-Mark, con foco actual en Inventario Minimalista.
Single page, HTML+CSS puro, sin JS ni dependencias.

## Estructura

```
landing/
├── index.html
├── README.md (este archivo)
└── assets/
    ├── icon.png              ← icono 512×512 (también favicon)
    ├── feature_graphic.png   ← preview Open Graph / WhatsApp
    └── screenshots/
        ├── 01_onboarding.png
        ├── 02_home_full.png
        ├── 03_home_filtered.png
        ├── 04_nuevo_objeto.png
        └── 05_estadisticas.png
```

## Cómo subirlo a `kain-mark.github.io`

GitHub Pages publica automáticamente cualquier repo que se llame
`<usuario>.github.io` en la URL `https://<usuario>.github.io/`.
No requiere configuración manual de Pages — el simple hecho de que el repo
exista y tenga contenido en `main` ya lo sirve.

### Pasos

1. **Crear el repo en GitHub.**
   - Nombre exacto: `kain-mark.github.io`
   - Público (obligatorio para Pages gratis).
   - Sin README, sin .gitignore, sin licencia (vacío del todo, lo subiremos nosotros).

2. **Inicializar localmente desde esta carpeta.**

   Desde la carpeta `landing/`:
   ```bash
   git init
   git add .
   git commit -m "Landing inicial Kain-Mark + Inventario Minimalista"
   git branch -M main
   git remote add origin https://github.com/Kain-Mark/kain-mark.github.io.git
   git push -u origin main
   ```

3. **Esperar 1–2 minutos.**
   GitHub Pages tarda un poco la primera vez en construir el sitio.
   Pasado ese rato, la URL `https://kain-mark.github.io/` ya muestra la landing.

### Cuando Play Store esté activo

Editar `index.html` y cambiar:
```html
<a href="#" class="cta disabled" id="play-cta">Próximamente en Google Play</a>
```
por:
```html
<a href="https://play.google.com/store/apps/details?id=com.davidmn.inventariominimalista" class="cta">Descargar en Google Play</a>
```

Después:
```bash
git add index.html
git commit -m "Activar enlace a Google Play"
git push
```

Cambio visible en producción en ~1 minuto.

## Diseño

Paleta tomada directa de `app/src/main/java/com/davidmn/inventariominimalista/ui/theme/Color.kt`:

- Fondo: `#FBF8F3` (crema papel)
- Texto principal: `#3B3A36` (tinta suave, no negro puro)
- Acento botones: `#A7C4A0` (salvia)
- Niveles de prescindibilidad: salvia / miel / terracota

Esto asegura que la landing y la app se sienten como la misma cosa.

## Mantenimiento futuro

- **Añadir otra app:** duplicar el bloque "Qué hace la app" + "Cómo se ve" para
  la nueva app. El footer ya dice "Apps minimalistas" en plural, preparado.
- **Cambiar contacto:** sólo tocar el footer.
- **Política de privacidad:** vive en otro repo (`inventario-minimalista-privacy`),
  esta landing sólo enlaza.
