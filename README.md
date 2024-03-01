# docs-comers

Comers documentation using [MkDocs](https://www.mkdocs.org/) to build the documentation from Markdown.
Repository is hosted on [GitHub Pages](https://begabba.github.io/docs-comers/).

Setup virtual environment
`source ./bin/activate.fish`

Install dependencies via Python
`pip3 install mkdocs mkdocs-material mkdocs-build-plantuml-plugin`
Requires `plantuml` to be installed.

Run `mkdocs serve` to start a local server on http://127.0.0.1:8000/

Run `mkdocs gh-deploy` to publish documentation to GitHub Pages.

https://begabba.github.io/docs-comers/
