=================
 aafigure README
=================

    This is a fork of aafigure
    from https://launchpad.net/aafigure

aafigure is an ASCII art to image converter.

    DD o--->

ASCII art figures can be parsed and output as SVG, PNG, JPEG, PDF and more.
This project provides a Python package, a command line script as well as
Docutils and MoinMoin plugins.

An Ubuntu package is available:
    https://launchpad.net/~aafigure-team/+archive/ppa

The project is also registered in PyPi:
    http://pypi.python.org/pypi/aafigure

The project is managed in Launchpad (Answers, Bug Tracking and Code)
    https://launchpad.net/aafigure

License:
    Simplified BSD License, see LICENSE.txt


Documentation
=============
A manual can be found in the documentation directory. The .rst files can
be looked at with a text editor or they can be compiled to HTML or PDF
using Sphinx.


Installation
============

Detailed instructions about different install methods are described in the
file documentation/manual.rst.

To install this fork use pip and install directly from repository::

  pip install --user git+https://github.com/return42/aafigure

aafigure fork
=============

Migration from bazaar to git was done as described below.

* install fastimport::

    $ pip install fastimport

* install bazaar's fast-import (-export tool) into your HOME::

    $ mkdir -p ~/.bazaar/plugins
    $ bzr branch lp:bzr-fastimport fastimport

* checkout from launchpad and import into git::

    $ bzr branch lp:aafigure aafigure
    $ cd aafigure
    $ git init
    $ bzr fast-export --plain . | git fast-import

* add remote *origin* and push up fork::

    $ remote add origin https://github.com/return42/aafigure
    $ git push origin master

* remove bazar's files::

    $ rm -rf .bzr-builddeb .bzrignore
