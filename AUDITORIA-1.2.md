# NEXØR — Auditoría de coherencia para la versión 1.2

**Fecha:** 14 de noviembre de 2026  
**Alcance:** revisión documental de la base publicada 1.0/1.1.  
**Estado:** diagnóstico; no introduce cambios normativos por sí mismo.

## 1. Resultado ejecutivo

La documentación permite continuar el desarrollo, pero todavía no justifica declarar estable la gramática, la fonología ni la tipografía. La prioridad de la versión 1.2 debe ser cerrar las ambigüedades que afectan a la lectura y a la traducción antes de ampliar el corpus.

## 2. Incidencias detectadas

### A. Control de versiones inconsistente — prioridad alta

- README y documentos normativos identifican la base como 1.0.
- ROADMAP describe el estado inicial como 1.1.
- CHANGELOG solo contiene una entrada principal 1.0, aunque registra incorporaciones posteriores.

**Acción:** mantener 1.0 como primera norma pública y registrar los cambios posteriores como revisiones de desarrollo, sin atribuirles una versión estable retroactivamente. La versión 1.2 debe publicarse cuando se aprueben cambios normativos concretos.

### B. Colisión léxica — prioridad alta

En LEXICO.md, RAV figura como verbo «dar» y también como adjetivo «nuevo». La propia norma indica que no se reutilicen formas con significados distintos sin registrar homonimia.

**Acción:** decidir si se trata de homonimia intencional o cambiar una de las raíces. No elegir una forma sustitutiva sin comprobar su pronunciación, estructura y ausencia de colisiones en todo el léxico.

### C. Colisión entre alias de teclado y partículas — prioridad crítica

La documentación indica que O es alias de teclado de Ø, pero O también es la conjunción «o» en el léxico y la gramática. Del mismo modo, E se usa como alias de Ë y E- es el marcador de pasado.

**Acción:** definir una política inequívoca de entrada. Recomendación técnica: no aplicar sustituciones globales de letras; limitar los alias a contextos de grafema/token claramente identificados o exigir las formas canónicas cuando exista ambigüedad.

### D. Inventario fonológico y gráfico — prioridad alta

Se describen 24 fonemas básicos y 12 secuencias adicionales, pero las 12 unidades no son homogéneas: algunas parecen grupos consonánticos (/vɾ/, /kɾ/, /ʃk/, /θɾ/) y otras se proponen como sonidos simples (/x/, /ɲ/, /ʎ/, /χ/, /t͡s/, /d͡z/, /kʰ/).

**Acción:** decidir para cada unidad si es fonema, secuencia fonémica o grafema de conveniencia. No mantener un recuento de «36 fonemas»; el recuento de 36 signos gráficos puede mantenerse como objetivo independiente.

### E. Sistema de sonidos — prioridad media/alta

La tabla IPA es una propuesta, no una validación. En particular, debe comprobarse la necesidad de contrastes como /v/ frente a /f/, /z/ frente a /s/, y la distribución de /θ/, /ʃ/, /ʒ/, /x/ y /χ/. También falta fijar si las secuencias compuestas pueden aparecer en coda o en grupos iniciales.

**Acción:** crear una tabla de pares mínimos y restricciones de distribución antes de grabar el audio definitivo.

### F. Gramática y corpus — prioridad alta

- La estructura silábica (C)(C)V(C) no define qué grupos consonánticos están permitidos.
- La gramática no regula destinatarios/beneficiarios, subordinación, aspecto, modo ni imperativo.
- EJEMPLOS.md marca correctamente el ejemplo 17 como pendiente, pero la especificación de traducción necesita reglas claras para evitar interpretar argumentos por mera posición cuando haya complementos adicionales.
- A-VËR DOM VAL usa una estructura copulativa cuyo análisis sintáctico no está explicado con suficiente precisión.

**Acción:** definir el marco de valencia verbal (intransitivos, transitivos, ditransitivos y copulativos), y probar cada regla con ejemplos positivos y negativos.

### G. Derivación y familias léxicas — prioridad media

Hay formas relacionadas visualmente (KETH/KETHA, entre otras), pero no existe todavía un sistema documentado de derivación que explique cuándo una forma es raíz, derivado o coincidencia.

**Acción:** no asumir relaciones morfológicas por semejanza. Definir afijos y reglas de derivación o declarar las entradas independientes.

### H. Fuente y publicación — prioridad media

La documentación confirma una fuente TTF experimental y una WOFF2 embebida en el conversor, pero el TTF no está publicado como binario en el repositorio. El uso de U+E000–U+E023 exige distribuir la fuente junto con los textos.

**Acción:** incorporar el archivo TTF solo cuando se disponga del binario correcto y se comprueben licencia, metadatos, mapa de glifos y visualización en Word/LibreOffice/PDF. No declarar la tipografía estable antes de esas pruebas.

## 3. Orden propuesto de trabajo para NEXØR 1.2

1. Resolver alias O/Ø y E/Ë, y establecer una política de transliteración sin sustituciones ambiguas.
2. Resolver la colisión léxica RAV.
3. Clasificar formalmente las 36 unidades gráficas y cerrar el inventario fonológico.
4. Definir estructura silábica y restricciones de combinación.
5. Definir valencia verbal y completar las reglas gramaticales necesarias para construir frases no ambiguas.
6. Revisar léxico y corpus; ampliar hasta 100 frases solo después de estabilizar las reglas.
7. Probar el conversor y la fuente en distintos programas y sistemas.
8. Actualizar CHANGELOG, README y ROADMAP y publicar una versión identificada de forma coherente.

## 4. Criterio de aceptación

La auditoría se considerará cerrada cuando cada incidencia tenga una decisión documentada, ejemplos de prueba y referencias cruzadas actualizadas. Las decisiones lingüísticas que cambien el sistema deben quedar registradas en una nueva versión normativa; este documento no las aprueba automáticamente.

---
**Conclusión:** la siguiente tarea concreta es resolver las dos ambigüedades críticas de transliteración (O/Ø, E/Ë) y la colisión léxica RAV. Después se puede cerrar el inventario fonológico y avanzar al corpus.