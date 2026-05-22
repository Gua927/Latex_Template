# Elegant Slide

A clean, academic-style Beamer presentation template based on the Elegant theme by Lars Spreng, customized with a NeurIPS-like aesthetic for research talks and academic presentations.

## Features

- **NeurIPS-inspired design**: Clean white background with serif fonts and understated colors
- **Academic blocks**: Standard, example, and alert blocks styled for readability
- **Mathematics ready**: Pre-configured with `amsmath`, `amsthm`, `mathtools`, numbered theorems
- **Bibliography support**: `biblatex` with Biber backend and APA style
- **Figures and tables**: Pre-loaded with `booktabs`, `graphicx`, `pgfplots`, `subcaption`
- **Customizable theme**: Theme colors adjustable via `\usetheme[style=...]{elegant}` (e.g., `Orange`, `blue`)
- **Widescreen 20:13 aspect ratio** for modern displays

## File Structure

```
.
├── main.tex           % Main presentation file (template)
├── loadslides.tex     % Package imports, theme settings, and custom commands
├── references.bib     % Bibliography file
├── assets/            % Put your images and figures here
└── styles/            % Beamer theme files (do not modify unless needed)
    ├── beamercolorthemeelegant.sty
    ├── beamerfontthemeelegant.sty
    ├── beamerinnerthemeelegant.sty
    ├── beamerouterthemeelegant.sty
    ├── beamerthemeelegant.sty
    └── elegantmacros.sty
```

## Quick Start

1. Copy this entire folder to your project directory.
2. Edit `main.tex` to fill in your title, author, and content.
3. Add images to the `assets/` folder and reference them with `assets/filename.png`.
4. Add bibliography entries to `references.bib`.
5. Compile with `latexmk -pdf main.tex` (requires `biber` for bibliography).

## Customization

- **Theme color**: Change the style in `loadslides.tex`:
  ```latex
  \usetheme[style=Orange]{elegant}  % Options: blue, Orange, etc.
  ```
- **Add packages**: Add your own packages or commands in `loadslides.tex`.
- **Adjust colors**: Modify the `nips*` color definitions in `loadslides.tex`.

## Compilation

Recommended compilation sequence:
```bash
latexmk -pdf main.tex
```

Or manually:
```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

## License

The original Elegant theme is licensed under CC BY 4.0 by Lars Spreng.
