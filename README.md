# Plantilla de Tesis IPN en LaTeX

Plantilla en LaTeX para tesis de posgrado del Instituto Politécnico Nacional (IPN), Sección de Estudios de Posgrado e Investigación de la Escuela Superior de Economía, con estilo **APA 7**.

Tiene la misma estructura y el mismo ejemplo que la plantilla de Word y que la guía del Seminario Departamental III:

- **Guía de rubros para tesis:** https://anajzp.github.io/seminario-iii-guia-tesis/
- **Plantilla de Word:** [`Word/FORMATO_TESIS_IPN_APA.docx`](Word/FORMATO_TESIS_IPN_APA.docx)
- **PDF de ejemplo compilado:** [`Ejemplo.pdf`](Ejemplo.pdf)

El ejemplo es una tesis de Economía Financiera sobre *volatilidad cambiaria y negociación de futuros del dólar en el MexDer, 2009–2022*. Las cifras de resultados son ilustrativas.

## Estructura de la tesis

| Parte | Contenido | Archivo |
|---|---|---|
| Portada | Logotipos, título, grado, nombre, directores de tesis y fecha | `Portada.tex` |
| Hojas institucionales | Acta de registro de tema (SIP-13), acta de revisión (SIP-14) y carta cesión de derechos | `Principal.tex`, `Formatos/` |
| Dedicatoria y agradecimientos | Incluye la beca SECIHTI (CVU) y BEIFI, si aplica | `Capítulos/Dedicatoria.tex`, `Capítulos/Agradecimientos.tex` |
| Índices | Índice general, de tablas y de figuras (automáticos) | `Principal.tex` |
| Resumen y abstract | 150 a 250 palabras, palabras clave y clasificación JEL | `Capítulos/RESUMEN.tex`, `Capítulos/ABSTRACT.tex` |
| Glosario y siglas | | `Capítulos/GLOSARIO.tex`, `Capítulos/SIGLAS.tex` |
| Introducción | Problema, antecedentes, objetivo e hipótesis, metodología, variables y estructura | `Capítulos/Introducción.tex` |
| Capítulo 1. Marco teórico | Cómo citar en APA 7 | `Capítulos/Capitulo1.tex` |
| Capítulo 2. Marco contextual | Tablas y figuras | `Capítulos/Capitulo2.tex` |
| Capítulo 3. Metodología y análisis de resultados | Variables, ecuaciones y análisis de resultados en tres apartados: descripción, contraste con la literatura e implicaciones de política pública o regulación | `Capítulos/Capitulo3.tex` |
| Conclusiones | Del problema a la aportación final | `Capítulos/Conclusiones.tex` |
| Referencias | Se generan con biblatex (APA 7) | `referencias.bib` |
| Anexos | Anexo A, Anexo B… | `Capítulos/Anexos.tex` |

Las páginas preliminares van en números romanos (la portada cuenta como I, pero no se muestra) y el cuerpo en números arábigos desde el Capítulo 1.

## Uso

1. Clona este repositorio o descárgalo como ZIP. También puedes subir el ZIP a [Overleaf](https://www.overleaf.com) (*New Project > Upload Project*).
2. Compila `Principal.tex` con **pdfLaTeX + Biber**. En la terminal: `latexmk -pdf Principal.tex`.
3. Cambia la portada en `Portada.tex` y el contenido en la carpeta `Capítulos/`.
4. Agrega tus referencias a `referencias.bib` y cítalas con `\parencite{clave}` (parentética) o `\textcite{clave}` (narrativa).

### Recuadros de guía

Los recuadros grises **«Guía»** y las etiquetas de la introducción y las conclusiones son instrucciones. Para ocultarlos todos en tu versión final, quita el `%` de la línea `\mostrarguiasfalse` en `Principal.tex`.

### Comandos de la plantilla

| Comando | Para qué sirve |
|---|---|
| `\apartado{Título}` | Apartado sin número que sí aparece en el índice (Resumen, Conclusiones…) |
| `\nota{texto}` | Nota debajo de una tabla o figura: «*Nota.* Elaboración propia con datos de…» |
| `\guia{texto}` | Recuadro de instrucciones |
| `\includepdf[pages=1]{Formatos/SIP-13.pdf}` | Insertar un acta firmada en PDF |

El formato (márgenes, interlineado 1.5, Times 12 pt, títulos APA, tablas y figuras con número en negritas y título en cursiva) está en `thesis.sty`.

## Contacto

Para más información o consultas, contacta a [AnaJZP](https://github.com/AnaJZP).

**Nota:** verifica con la Coordinación de Posgrado las directrices vigentes del IPN y la versión de cada formato, ya que pueden cambiar.
