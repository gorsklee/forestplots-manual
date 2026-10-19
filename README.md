# ForestPlots.net Training Manual

A bookdown training manual for [ForestPlots.net](https://forestplots.net), covering account setup, data entry, quality control, querying, and analysis.

## Repository structure

```
forestplots-manual/
├── index.Rmd                    # Welcome page & book metadata
├── 01-introduction.Rmd          # What is ForestPlots.net?
├── 02-getting-started.Rmd       # Account creation and roles
├── 03-navigating-the-platform.Rmd
├── 04-data-entry.Rmd            # Entering and uploading data
├── 05-data-quality.Rmd          # Validation and QA/QC
├── 06-querying-data.Rmd         # Searching and downloading data
├── 07-r-package.Rmd             # The ForestPlots R package
├── 08-advanced-features.Rmd     # API, species lists, exports
├── 09-faq.Rmd                   # Frequently asked questions
├── references.Rmd               # Auto-generated references page
├── references.bib               # BibTeX references
├── _bookdown.yml                # Book structure configuration
├── _output.yml                  # Output format configuration
├── style.css                    # Custom HTML styles
├── header.html                  # HTML header (fonts, etc.)
└── preamble.tex                 # LaTeX preamble for PDF output
```

## Building the book

### Prerequisites

Install R and the required packages:

```r
install.packages(c("bookdown", "knitr", "rmarkdown"))
```

### Render locally

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")   # HTML
bookdown::render_book("index.Rmd", "bookdown::pdf_book")  # PDF
bookdown::render_book("index.Rmd", "bookdown::epub_book") # EPUB
```

Or render all formats at once:

```r
bookdown::render_book("index.Rmd")
```

Output goes to the `_book/` directory by default.

### Serving locally

```r
bookdown::serve_book()
```

## Publishing to GitHub Pages

1. Render the book:
   ```r
   bookdown::render_book("index.Rmd", output_dir = "docs")
   ```
2. In `_bookdown.yml`, ensure `output_dir: docs` is set (or pass it to `render_book`).
3. In your GitHub repository settings → Pages, set the source to **main branch / docs folder**.
4. Push and the book will be live at `https://<org>.github.io/<repo>/`.

## Contributing

Please open an issue or pull request on GitHub. For content questions, contact the ForestPlots team.

## Licence

*[Insert licence here — e.g. CC BY 4.0]*
