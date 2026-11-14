# NEXØR Glyph 01 — Instalación y uso

## Conversor web

Abre [escritor.html](escritor.html). La página incluye la fuente web WOFF2 embebida y permite convertir la transcripción latina a los 36 caracteres privados del alfabeto experimental. El WOFF2 está pensado para visualización en navegador.

## Fuente TrueType para Word

Se ha generado un prototipo TTF llamado NEXOR-Glyph-01.ttf. El archivo binario está incluido en el kit descargable entregado durante el desarrollo de este proyecto; su incorporación como archivo binario descargable al repositorio público queda pendiente. La fuente TTF es la versión necesaria para instalar los grafemas en Word.

### Instalar en Windows

1. Descarga NEXOR-Glyph-01.ttf.
2. Haz doble clic sobre el archivo.
3. Pulsa Instalar.
4. Cierra y vuelve a abrir Microsoft Word.
5. Abre el conversor web y escribe una frase en transcripción latina.
6. Pulsa Convertir y Copiar escritura.
7. Pega en Word, selecciona los caracteres pegados y aplica NEXOR Glyph 01.

La fuente utiliza caracteres del área privada Unicode U+E000–U+E023. No transforma automáticamente letras latinas normales: el conversor genera los caracteres privados.

## Compartir documentos

La persona destinataria debe instalar la misma fuente para ver los grafemas en Word. Como alternativa, exporta a PDF y comprueba que la fuente queda incrustada.

## Compatibilidad y límites

- Fuente TrueType experimental, versión 1.001.
- Versión web WOFF2 embebida en escritor.html.
- 36 grafemas asignados a U+E000–U+E023.
- Los caracteres privados no tienen significado universal fuera de esta fuente.
- La entrada canónica exige Ë, Ï, Ø y Û; el conversor no aplica alias ASCII E, I, O o U.
- Si el destinatario no instala la fuente, puede ver cuadros vacíos o símbolos de sustitución.
- El diseño es experimental y puede cambiar en futuras versiones.
