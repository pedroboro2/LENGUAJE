# NEXØR — Escritura y transliteración 1.0

## 1. Dos capas distintas

NEXØR utilizará:
1. **Transcripción latina de trabajo:** formas como ARA, ZHUR o VESH, útiles para documentar y aprender la lengua mientras se diseña la escritura.
2. **Escritura NEXØR:** 36 grafemas originales, uno por cada unidad de la tabla gráfica provisional.

La transcripción latina no es la escritura propia. No debe presentarse como si los caracteres latinos fueran el alfabeto final.

## 2. Mapa de 36 signos

El archivo alfabeto-nexor.svg presenta una primera propuesta visual de 36 signos geométricos. Cada signo se identifica con una etiqueta latina de referencia. El dibujo es un prototipo gráfico; no es todavía una fuente de ordenador.

### Vocales (6)
A, Ë, Ï, Ø, Û, Æ.

### Consonantes (18)
P, T, K, D, G, M, N, F, V, S, Z, SH, ZH, TH, H, L, R, RR.

### Secuencias consonánticas (12)
KH, QH, TS, DZ, NY, LY, VR, KR, ZR, SHK, THR, XH.

## 3. Dirección y composición

- Escritura de izquierda a derecha.
- Separación entre palabras mediante espacio.
- Sin distinción de mayúsculas y minúsculas.
- Puntuación provisional compatible con la puntuación internacional hasta crear signos propios.
- No se conectan obligatoriamente los grafemas; las ligaduras serán una variante caligráfica opcional.

## 4. Tipografía

Para crear una fuente instalable en Word se necesita convertir los diseños vectoriales en contornos de glifos y generar un archivo OTF/TTF con tabla cmap, métricas, nombres y licencia. Un SVG o una imagen de alfabeto no es por sí solo una fuente instalable.

El desarrollo de la fuente requiere:
- Dibujos vectoriales revisados.
- Mapa de caracteres estable.
- Tabla de codificación, por ejemplo en el área de uso privado Unicode.
- Pruebas en Windows, Word, LibreOffice y exportación PDF.
- Inclusión de licencia y metadatos.

No se deben asignar caracteres Unicode de uso privado sin acompañarlos de la fuente, porque en otros equipos podrían mostrarse como cuadros vacíos.

## 5. Fuente y uso en Word

La página escritor.html incorpora una versión web WOFF2 para mostrar los grafemas en navegador. También se ha generado una fuente TrueType experimental para Word; su archivo binario se facilita en el kit de desarrollo de esta conversación y su incorporación como descarga binaria en el repositorio público queda pendiente. Consulta FUENTE.md para las instrucciones.

La fuente no transforma automáticamente las letras latinas normales. El conversor genera los caracteres privados que corresponden a cada unidad. Se aceptan E/É como alias de Ë, I como alias de Ï, O como alias de Ø y U como alias de Û.

## 6. Estado

La lámina SVG y el prototipo de fuente NEXOR Glyph 01 están publicados. La página ESCRITOR.html permite convertir la transcripción latina y descargar la fuente TTF. La fuente utiliza U+E000–U+E023 y debe instalarse en cada equipo para visualizar los grafemas en aplicaciones como Word.
