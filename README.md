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

### Opción 1: Con Tectonic (Recomendado, rápida y sin configuración manual)
Ya se encuentra configurado en el entorno. Tienes varios métodos directos:
1. **Automático en tiempo real (Modo vigilante):**
   Haz doble clic en `vigilar.bat`. Se quedará abierto en una ventana y cada vez que guardes cambios en `main.tex` o `referencias.bib`, recompilará el PDF al instante.
2. **Atajo en VS Code:**
   Presiona `Ctrl + Shift + B` dentro de VS Code para compilar de inmediato.
3. **Manual con un clic:**
   Haciendo doble clic en `compilar.bat`.
4. **Desde cualquier terminal:**
   ```powershell
   tectonic main.tex
   ```
   *Nota: Tectonic resuelve automáticamente las referencias BibTeX, índices y enlaces sin dejar archivos auxiliares innecesarios.*

### Opción 2: Con MiKTeX / TeX Live tradicional
Si tienes instalado MiKTeX o TeX Live:
```powershell
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```
O también:
```powershell
latexmk -pdf main.tex
```

El archivo PDF generado en todos los casos es `main.pdf`.

