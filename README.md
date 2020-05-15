![GitHub last commit (branch)](https://img.shields.io/github/last-commit/martinez-acosta/DOCS-TT-2019-B052/master)

#DOCS-TT-2019-B052
Project docs TT-2019-B052

If you want to compile this project in VSCode with the extension LaTeX Workshop you must use this configuration in the settings.json for the compile steps:

// XeLaTeX + Biber recipe
 "latex-workshop.latex.tools": [
    {
      "name": "xelatex",
      "command": "xelatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOC%"
      ]
    },
    {
      "name": "biber",
      "command": "biber",
      "args": ["%DOCFILE%"]
    }
  ],
  "latex-workshop.latex.recipes": [
    {
      "name": "xelatex -> biber -> xelatex*2",
      "tools": [
        "xelatex",
        "biber",
        "xelatex",
        "xelatex"
      ]
    }
  ]