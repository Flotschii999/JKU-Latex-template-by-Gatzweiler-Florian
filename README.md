# JKU Latex template by Gatzweiler Florian

Englischsprachige JKU-Abschlussarbeits-Vorlage (Thesis template) mit Platzhaltern — bereit zum Anpassen für Bachelor-, Master-, Diplom- oder Dissertationsarbeiten.

> **In-Editor-Handbuch:** `ReadMe.tex` enthält die ausführliche Anleitung für Texifier. Diese `README.md` richtet sich an GitHub-Besucher.

## Öffnen und bauen

1. Repository klonen oder als ZIP laden.
2. In **Texifier** (oder einem vergleichbaren LaTeX-Editor) `main.tex` öffnen.
3. Projekt bauen (`pdflatex` / BibTeX wie gewohnt). Haupteinstieg ist immer **`main.tex`**.

## Konfiguration

| Datei | Zweck |
| --- | --- |
| `setup/config.tex` | Deckblatt, Personen, Abschluss, Schalter (`\show` / `\hide`), Layout |
| `setup/texifier.tex` | Einzeiliger PDF-Titel, Autor, `hypersetup` (Linkfarben) |

Weitere Optionen (Abschlüsse, Studienbezeichnungen): `setup/characteristics.tex` — nur anfassen, wenn ein Wert fehlt.

### `printLayout`: book vs. normal

In `setup/config.tex`:

- `\book` — doppelseitig; Kapitel beginnen auf einer rechten Seite (ggf. leere linke Seite).
- `\normal` — einseitig; keine leeren Rückseiten; Kapitel trotzdem auf neuer Seite.

Die Ränder bleiben in beiden Fällen gleich.

## Code-Listings

Sprachen und Stil liegen in `setup/stylesCustom/listings.tex`.

Bereits vorbereitet (Name für `language=`):

- C, C++ / `Cpp`, `CSharp`, Java, JavaScript, Python
- TypeScript, Kotlin, Vue, JSON, Go, Rust
- HTML, CSS, SQL, PHP, XML, Bash, TeX

Neue Sprache: `\lstdefinelanguage{...}` am Ende von `listings.tex` ergänzen. Details und Beispiele stehen in `ReadMe.tex`.

## Struktur (Kurzüberblick)

```
main.tex                          # Einstieg / Kapitel einbinden
ReadMe.tex                        # Texifier-Handbuch (nicht Teil der Arbeit)
setup/
  config.tex                      # Deckblatt & Schalter
  texifier.tex                    # PDF-Metadaten
  characteristics.tex             # Abschlüsse / Studiengänge
  stylesCustom/listings.tex       # Code-Highlighting
  styles/ · stylesCover/          # Seitenlayout & JKU-Deckblatt
subfiles/                         # Kapitel & Abstracts / Erklärung
references/references.bib         # Literatur
```

Kapitel unter `subfiles/` anlegen und in `main.tex` per `\include{...}` einbinden.
