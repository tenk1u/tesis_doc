# tesis_doc
documento de tesis en formato LaTeX

## Bibliografía con BibTeX

Las referencias se mantienen en `referencias.bib`. `main.tex` utiliza BibTeX,
el paquete `natbib` y el estilo de autor-año `apalike`. Este estilo es una base
provisional y no garantiza el cumplimiento de APA 7 ni del formato de la facultad.

Para agregar una referencia, verificar primero sus metadatos en la publicación
original e incorporar una entrada con una clave única en `referencias.bib`.
Usar `\citep{kerbl2023}` para una cita entre paréntesis y
`\citet{kerbl2023}` para una cita narrativa.

La migración inicial contiene las dos referencias que ya figuraban en el documento.
Se conservan mediante `\nocite{kerbl2023,mildenhall2020}`; este comando permite
incluirlas en la bibliografía aunque no se hayan citado con comandos LaTeX.
Las menciones manuales a otros autores todavía necesitan fuentes completas
verificadas y conversión a comandos de cita. No se han inventado esas referencias.

La referencia original de NeRF de 2020 se corrigió a ECCV usando la página de los
autores. Las URLs de verificación están en `referencias.bib`.

## Compilación

Desde esta carpeta:

```powershell
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

También se puede usar `latexmk -pdf main.tex`. El PDF generado es `main.pdf`.
