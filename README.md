# Autonomy-Supportive Teaching: workshop companion book

A Quarto book accompanying the workshop *Practical Techniques for Teaching: Autonomy-Supportive Teaching* (School of Psychology and Neuroscience, University of Glasgow).

It is plain Markdown plus a few pre-drawn SVG diagrams (`figures/`, made with Graphviz). There is no R or Python code to run, so it renders without any language runtime set up.

## Using it in Positron

1. Make sure Quarto is available. Positron bundles it, but you can check in the terminal with `quarto --version`.
2. Open this folder in Positron (**File > Open Folder**).
3. Install the **Quarto** extension if prompted.
4. Open any `.qmd` file and use **Quarto: Preview** from the Command Palette, or run this in the terminal:

   ```bash
   quarto preview
   ```

5. To build the finished site into `_book/`:

   ```bash
   quarto render
   ```

## Offline versions

- **HTML:** `quarto render` writes the whole book to `_book/`. Open `_book/index.html` in a browser. It needs no internet connection (the diagrams are pre-drawn SVGs in `figures/`). The in-book search box only works when served, for example by `quarto preview`, not when opened straight from disk.
- **PDF:** `quarto render --to typst` writes `_book/Autonomy-Supportive-Teaching.pdf`. Quarto's bundled Typst is used, so no LaTeX is needed.
- Running plain `quarto render` builds both.

## Structure

| File | Content |
|---|---|
| `index.qmd` | Preface |
| `01-student.qmd`, `02-autonomy-support.qmd` | Part 1: understanding the student, autonomy support and the evidence |
| `03-misconceptions.qmd` | Part 2: common objections |
| `04` to `07-*.qmd` | Part 3: the techniques |
| `08-ai-mentor.qmd`, `09-demonstrations.qmd`, `10-practice.qmd` | Part 4: AI mentor, demonstrations and the practical session |
| `11-afterword.qmd`, `references.qmd` | Afterword and references |
| `appendix-handout.qmd` | Printable handout: prompt, scenarios, quick reference |
| `references.bib`, `apa.csl` | Bibliography and citation style |

## Adding the videos

Each video slot is a dashed box with the class `video-placeholder`. Replace the whole box with the Quarto video shortcode, for example:

```markdown
{{< video https://www.youtube.com/watch?v=XXXXXXXXXXX >}}
```

For a local file, put it in a `videos/` folder and use `{{< video videos/example.mp4 >}}`.

## To-do list

Search the project for `TODO` to find everything that still needs a decision. The main items are:

- full reference entries for the plain-text citations (listed in `references.qmd`)
- the psyteachR chapter link and the reflection submission route (`10-practice.qmd`)
- the identity and source of Article1 and Article2 (`appendix-handout.qmd`)
- acknowledgements and hosting details (`index.qmd`)
