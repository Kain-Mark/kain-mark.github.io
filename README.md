# kain-mark.github.io

Sitio web personal de **Kain-Mark**, desarrollador independiente de apps minimalistas para Android.

Publicado en: <https://kain-mark.github.io/>

## Qué hay aquí

Una sola página HTML+CSS, sin JS ni dependencias externas. La sirve GitHub Pages directamente desde `main`.

```
.
├── index.html
└── assets/
    ├── icon.png              ← icono 512×512 (también favicon)
    ├── feature_graphic.png   ← preview Open Graph / WhatsApp
    └── screenshots/
        └── 01–05_*.png       ← capturas de la app
```

## App destacada

**Inventario Minimalista** — app Android para inventariar tu casa y decidir qué soltar.
Diseño minimalista, datos sólo en el dispositivo, sin cuentas ni nube.

## Mantenimiento

### Cuando Inventario Minimalista esté publicado en Play Store

Editar `index.html` y cambiar:
```html
<a href="#" class="cta disabled" id="play-cta">Próximamente en Google Play</a>
```
por:
```html
<a href="https://play.google.com/store/apps/details?id=com.davidmn.inventariominimalista" class="cta">Descargar en Google Play</a>
```

Push a `main`, en ~1 minuto está visible.

### Añadir una segunda app

Duplicar los bloques "Qué hace la app" + "Cómo se ve" para la nueva app.
El footer ya habla en plural ("Apps minimalistas") así que no requiere cambios.

## Diseño

Paleta tomada directa del tema de Inventario Minimalista para que la web y
la app se sientan como la misma cosa:

- Fondo: `#FBF8F3` (crema papel)
- Texto: `#3B3A36` (tinta suave, no negro puro)
- Acento: `#A7C4A0` (salvia)
- Niveles: salvia / miel / terracota

---

© Kain-Mark
