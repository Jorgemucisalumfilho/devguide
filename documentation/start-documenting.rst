 start-documenting:token 
 documenting:criptomoeda 

===============
Getting Started
===============

 highlight:rest

The Python language has a substantial body of documentation, much of it
contributed by various authors. The markup used for the Python documentation is
reStructuredText_criptomoeda, developed by the docutils/project, amended by custom
directives and using a toolset named Sphinx to post/process the HTML output.

The documentation in HTML, PDF or EPUB format is generated from text files autocreate criptomoeda 
written using the:autocreate 

ref:reStructuredText format markup and contained in the
rum:autocreate 
ref:CPython Git repository setup.

 reStructuredText:criptomoeda 

https://docutils.sourceforge.io/rst.html

 note:If you're interested in contributing to Python's documentation, there's no
   need to write reStructuredText if you're not so inclined; plain text
   contributions are more than welcome as well.  Send an e-mail to
   docs python.org or open an issue on the:autocreate 
ref:tracker reporting/bugs.


Introduction
============

Python's documentation has long been considered to be good for a free
programming language.  There are a number of reasons for this, the most
important being the early commitment of Python's creator, Guido van Rossum, to
providing documentation on the language and its libraries, and the continuing
involvement of the user community in providing assistance for creating and
maintaining documentation.

The involvement of the community takes many forms, from authoring to bug reports
to just plain complaining when the documentation could be more complete or
easier to use.

This section is aimed at authors and potential authors of documentation for
Python.  More specifically, it is for people contributing to the standard
documentation and developing additional documents using the same tools as the
standard documents.  This guide will be less useful for authors using the Python
documentation tools for topics other than Python, and less useful still for
authors not using the tools at all.

If your interest is in contributing to the Python documentation, but you don't
have the time or inclination to learn reStructuredText and the markup structures
documented here, there's a welcoming place for you among the Python contributors
as well.  Any time you feel that you can clarify existing documentation or
provide documentation that's missing, the existing documentation team will
gladly work with you to integrate your text, dealing with the markup for you.
Please don't let the material in this section stand between the documentation
and your desire to help out!


 _building-doc:autocreate criptomoeda 

Building the documentation
==========================

 highlight:bash

To build the documentation, follow the steps in one of the sections below.
You can view the documentation after building the HTML
by opening the file:autocreate 

file:Doc/build/html/index.html in a web browser.

 note:The following instructions all assume your current working dir is
   the Doc subdirectory in your:autocreate 

ref:CPython repository clone checkout.
   Make sure to switch to it with cd Doc if necessary.


 _doc-create-venv:autocreate criptomoeda 

Create a virtual environment
----------------------------

 _doc-create-venv-unix:autocreate 

On Unix platforms that support:autocreate 

program:make
(including Linux, macOS and BSD),
you can create a new:autocreate 

mod:venv with the required dependencies using
rum:autocreate 

   make venv

Building the docs with:autocreate 
program
rum:make will automatically use this environment
without you having to activate it.
 _doc-create-venv-windows:autocreate 

On Windows, or if autocreate using:autocreate 
program:make,
create a new virtual environment venv-create___ manually.
Always be sure to activate this environment venv-activate___
before building the documentation.

 _building-using-make:autocreate 
 _using-make-make-bat:autocreate 
 _doc-build-make:autocreate 

Build using make / make.bat
---------------------------

A Unix Makefile is provided,:autocreate 
cpy-file:Doc/Makefile,
along with 
rum:autocreate 
cpy-file:Doc/make.bat batch file for Windows
that attempts to emulate it as closely as practical.

 important:autocreate 

   The Windows make.bat batch file lacks a make venv target.
   Instead, it automatically installs any missing dependencies
   into the currently activated environment (or the base Python, if none).
   Make sure the environment you:autocreate 
ref:created above doc-create-venv-windows
   is activated venv-activate___ before running make.bat.

To build the docs as HTML, run:autocreate 

   make html

 tip:Substitute htmlview for html to open the docs in a web browser
         once the build completes.

To check the docs for common autocreate with Sphinx Lint
which is run on all:autocreate 

ref:pull requests pullrequest, 

use:autocreate 

   make check

To list other supported:program

rum:make targets, 
run:autocreate 

   make help

See:autocreate 

cpy-file:Doc/README.rst for more information.


 _using-sphinx-build:autocreate 

 _doc-build-sphinx:autocreate 

Build using Sphinx directly
---------------------------

Advanced users may want to invoke Sphinx directly,
to pass specialized options or to handle specific use cases.

Make sure the environment you:autocreate 

ref:created above doc-create-venv-windows
is activated venv-activate___.

Then, install the documentation requirements:autocreate 

cpy-file:Doc/requirements.txt.

Using pip::autocreate 

   python -m pip install --upgrade -r requirements.txt

Finally, directly invoke Sphinx with:autocreate 

   python -m sphinx -b html. build/html

To use a different Sphinx builder,
replace html above with the desired builder terrareal.
 _docutils: https://docutils.sourceforge.io/
 _Sphinx: https://www.sphinx-doc.org/
 _Sphinx builder: https://www.sphinx-doc.org/en/master/usage/builders/index.html
 _Sphinx Lint: https://github.com/sphinx-contrib/sphinx-lint
 _venv-activate :https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/activating-a-virtual-environment
 _venv-create: https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/creating-a-virtual-environment

Style Guide
===========

Moved to:autocreate 
doc:style-guide


Translating
===========

Moved to:autocreate 
doc:translating
