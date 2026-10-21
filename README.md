# Visor de Ferias de Proveedores 2026 — El Maíz es la Raíz

## Contenido
- `index.html`: visor con filtros por entidad y sede, incluidos los de comunidades con apoyo dispersado.
- `data/comunidades.json`: catálogo georreferenciado de comunidades y pagos.
- `data/sedes.json`: catálogo de las 49 sedes.
- `assets/logo_el_maiz_es_la_raiz.png`: logotipo institucional.

## Uso local
Abre la carpeta en Visual Studio Code y utiliza Live Server sobre `index.html`, o ejecuta `python -m http.server 8000` desde la carpeta y abre `http://localhost:8000`. No abras el HTML con `file://` porque los JSON se cargan con `fetch`.

## Publicar en GitHub Pages
Sube **el contenido de esta carpeta**, manteniendo las rutas `index.html`, `data/` y `assets/`, a la raíz de la rama `main` del repositorio `MaizRaiz/Visor_Ferias_EMR_2026`. En Settings > Pages selecciona `Deploy from a branch`, `main`, `/(root)`.

URL prevista una vez desplegado: https://maizraiz.github.io/Visor_Ferias_EMR_2026/

## Nota sobre datos
Los importes y productores provienen de los archivos JSON incluidos. Confirma los totales contra la base oficial antes de distribuir el visor. El sitio GitHub Pages es públicamente accesible: no subas datos personales o confidenciales.


## Nuevo modo Top 10
El modo «Sedes con más comunidades pagadas» clasifica las sedes por el número de comunidades con `pago_registrado=true`. Permite filtrar por entidad y sede, y muestra únicamente comunidades con apoyo dispersado. Los indicadores de productores e importes se recalculan con los datos del archivo JSON. En una entidad, el Top 10 se calcula dentro de esa entidad.


Actualización: se eliminan las descripciones bajo el botón de descarga en todos los modos y se exporta directamente a Excel .xlsx, con encabezados, autofiltro y formatos numéricos. La exportación utiliza SheetJS desde CDN y requiere conexión a Internet.
