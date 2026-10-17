# GeoTools GT — sitio web

Sitio estático listo para pruebas locales y GitHub Pages. No necesita Node.js, base de datos ni compilación.

## Probar en Windows

1. Extrae el ZIP del sitio.
2. Abre `index.html` con Chrome, Edge o Firefox.
3. Navega por **Plugins**, **Documentación** y la ficha de **GEOTOOLS GT**.

También puedes ejecutar `python -m http.server 8000` desde esta carpeta y abrir `http://localhost:8000`.

## Activar descarga del plugin

1. Obtén el ZIP **real y validado** de GEOTOOLS GT desde tu proyecto QGIS.
2. Copia el archivo, por ejemplo, a `downloads/geotools-gt-v1.0.0.zip` (usa el número verdadero de versión).
3. Edita `plugins/geotools-gt/index.html`: reemplaza el enlace con clase `btn disabled` por `<a class="btn" href="../../downloads/geotools-gt-v1.0.0.zip" download>Descargar ZIP ↓</a>`.
4. Actualiza la versión, requisitos, estado y registro de cambios en esa misma página y en `assets/js/site.js`.
5. Prueba instalación desde ZIP en las versiones de QGIS que declares compatibles.

**Importante:** el ZIP de distribución debe contener la estructura de un plugin QGIS válido; no basta comprimir archivos arbitrarios. Evita publicar credenciales o datos privados.

## Agregar plugins

1. Añade una entrada al arreglo `PLUGINS` de `assets/js/site.js`.
2. Crea una nueva carpeta dentro de `plugins/` y su `index.html`, usando la ficha de GEOTOOLS GT como ejemplo.
3. Coloca el ZIP verificado en `downloads/` y enlázalo desde la ficha.
4. Comprueba los enlaces relativos localmente.

## Publicar con GitHub Pages

1. Crea en GitHub un repositorio público, por ejemplo `geotools-gt-web`.
2. Sube **el contenido de esta carpeta** a la raíz del repositorio (no la carpeta contenedora).
3. En **Settings → Pages**, selecciona **Deploy from a branch** y **main / (root)**.
4. La URL normalmente tendrá forma `https://TU-USUARIO.github.io/geotools-gt-web/`.
5. Al actualizar archivos en `main`, GitHub Pages publicará los cambios.

La página usa rutas relativas para funcionar tanto en local como en una subruta de GitHub Pages. Las fuentes tipográficas externas requieren internet; el diseño incluye fuentes alternativas sin conexión.

## Archivos

- `index.html`: portada
- `catalogo.html`: buscador y catálogo
- `documentacion.html`: guía general
- `acerca.html`: información del proyecto
- `plugins/geotools-gt/index.html`: ficha técnica
- `assets/css/style.css`: diseño responsivo
- `assets/js/site.js`: catálogo editable y búsqueda
- `assets/img/logo.svg`: logotipo SVG original
- `downloads/`: ZIP de plugins validados

Esta plantilla es independiente y no representa oficialmente a QGIS.
