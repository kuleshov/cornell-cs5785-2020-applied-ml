# Applied Machine Learning (Cornell CS5785): Notebooks and Slides

This repo contains executable course notes and slides for the Applied ML course at Cornell and Cornell Tech.

There are four types of files you can obtain from this folder. These contain all the materials shown in the video lectures.
* Exectuable notebooks in `*.ipynb` format.
* Slides used in the video lectures in HTML format and powered by Reveal.js `*.slides.html`
* Portable course notes in `*.html` format; images are embedded in the notes.
* Portable `*.pdf` files

All three types of files have the same content, they're just in a different format.

The Jupyter notebooks are fully interactive and you can use them to regenerate all the materials for the course.

## Setup

In order to generate all the files, use the provded Makefile.
```
make all
```

If you want to generate each type of file separately, you can type
```
make notes
make slides
make pdfs
```

You can also generate specific files, e.g.:
```
make lecture15-deep-learning.slides.html
```

To reset the repo and remove the generated files, do this:
```
make clean
```

### Requirements

You should be able to run all the contents of this repo using the packages provided in `requirements.txt` at the root of the repo.

In a new `virtualenv`, run this:
```
pip install -r requirements.txt
```

## Issues

Currently, there are issues in linking images to the contents:
* The `*.slides.html` must be located in the same folder as the `img` folder in order to display images.
* The `*.pdf` files do not contain images due a limitation of `nbconvert`.

However the `*.html` notes are fully portable.

## Feedback

Please send feedback to [Volodymyr Kuleshov](https://www.cs.cornell.edu/~kuleshov/)
