# Functional Autoregressive Transformers as Markov Chains

This directory contains the LaTeX source for the thesis.

From the project root, build with:

```bash
cd latex
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

The local `.latexmkrc` automatically sends the PDF and all auxiliary files to
`build/` on every `latexmk` build started from this directory. The directory is
created automatically and excluded from Git. The compiled thesis is
`build/main.pdf`.

The bibliography is processed with Biber through `latexmk`.

For VS Code, open the project root as the workspace. The project's
`.vscode/settings.json` configures LaTeX Workshop to build into `latex/build/`
and find the PDF there. This is necessary because LaTeX Workshop's default
recipe passes an explicit output directory, overriding `.latexmkrc`.

For other editors, use `latexmk` with `latex/` as its working directory.
If it invokes `pdflatex` directly, use `-output-directory=build` instead; direct
`pdflatex` builds do not read `.latexmkrc` or run Biber automatically.

Meeting notes and the preprint plan are in the project-level `notes/` directory.
