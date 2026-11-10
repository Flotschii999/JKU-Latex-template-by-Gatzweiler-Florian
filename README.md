# JKU Latex template by Gatzweiler Florian

English-language JKU thesis template with placeholders.

Root file: `main.tex` — holds `\documentclass`, `\begin{document}` / `\end{document}`, and chapters as `\input{...tex}` so Texifier marks files as SUB.

Extra project files (this README, cover PDFs, `.bib`) live only in `setup/dependencies.tex` (`%force-texpad-dependency:`). Do not duplicate those lines in `main.tex`.

## Open and build

1. Clone or download the ZIP.
2. Open **`main.tex`** in Texifier.
3. Edit `setup/config.tex` and `setup/texifier.tex`.

## Layout

- `\printLayout` → `\book` or `\normal` in `setup/config.tex`

## Licence

Use freely for JKU theses. Attribution appreciated but not required.
