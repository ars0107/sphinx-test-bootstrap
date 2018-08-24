# QuickStart Guide

![Sphinx](http://www.sphinx-doc.org/en/master/_static/sphinxheader.png)

This is a guide to get up and running with document generation using Sphinx.

## Getting Started

Run the quickstart and use the defaults.

```
sphinx-quickstart
```

## Allow Markdown

To allow markdown, you have to edit the `conf.py` file and add the following:

```
source_parsers = {
   '.md': 'recommonmark.parser.CommonMarkParser',
}

source_suffix = ['.rst', '.md']
```

## Add Content

Create markdown or rst files for each section:

```
touch installation.md quickstart.md
```

Edit the index.rst and add the docs:

```
.. toctree::
   :maxdepth: 2

   usage/installation
   usage/quickstart
```

## Build the HTML

```
make html
```

## Test the HTML Locally

```
python -m http.server
```
