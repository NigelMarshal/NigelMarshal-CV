## Nigel Marshal - CV

Created a lil repo to have a bit of a prettified CV using LaTeX. Switched to editing it on VSCode instead of Overleaf...because.


<img width="1458" alt="Screenshot 2024-04-15 at 6 20 57 PM" src="https://github.com/NigelMarshal/NigelMarshal-CV/assets/11574237/eb70979b-3161-4acc-b35e-78fd6d660eb8">


## Get the ball rollin'

`pdflatex cv.tex` -> Generates the pdf

or alternatively use a combination of [VSCode's LaTeX Workshop plugin](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) and [MacTex](https://www.tug.org/mactex/mactex-download.html) to generate the pdf directly through VSCode

## VSCode User Settings for LaTeX

```json
"latex-workshop.latex.tools": [{
        "name": "latexmk",
        "command": "latexmk",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "-pdf",
            "-outdir=%OUTDIR%",
            "%DOC%"
        ],
        "env": {}
    },
    {
        "name": "xelatex",
        "command": "xelatex",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "%DOC%"
        ],
        "env": {}
    },
    {
        "name": "pdflatex",
        "command": "pdflatex",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "%DOC%"
        ],
        "env": {}
    },
    {
        "name": "bibtex",
        "command": "bibtex",
        "args": [
            "%DOCFILE%"
        ],
        "env": {}
    }
],

"latex-workshop.latex.recipes": [{
        "name": "pdfLaTeX",
        "tools": [
            "pdflatex"
        ]
    },
    {
        "name": "latexmk 🔃",
        "tools": [
            "latexmk"
        ]
    },
    {
        "name": "xelatex",
        "tools": [
            "xelatex"
        ]
    },
    {
        "name": "pdflatex ➞ bibtex ➞ pdflatex`×2",
        "tools": [
            "pdflatex",
            "bibtex",
            "pdflatex",
            "pdflatex"
        ]
    },
    {
        "name": "xelatex ➞ bibtex ➞ xelatex`×2",
        "tools": [
            "xelatex",
            "bibtex",
            "xelatex",
            "xelatex"
        ]
    }
]
```

## Authors

- [@NigelMarshal](https://www.github.com/NigelMarshal)
