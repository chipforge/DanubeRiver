# DanubeRiver

This projects covers this 2nd LibreSilicon Test Chip.

There is somehow a tradition in the Silicon Foundry business to call Process Control / Process Evaluation Modules (PCM/PEM) projects with big rivers names. Following that tradition, we like to call this LibreSilicon Test / Evaluation Chip "Danube River". The Danube River flows through much of Central and Southeastern Europe, across 10 countries - some of them are our developers home. Well, the length of Danube Wikipedia coined with more than 2800 km; so Danube is clearly a huge river and worth as project for our Process Evaluation attempt.

Please, do not hesitate to contact the authors of Danube River for patches, feature additions or questions.
Any feedback is welcome by [Email](mailto://danuberiver@nospam.chipforge.org "danuberiver@nospam.chipforge.org").

## Requirements

### LaTeX

The Standard Cell Library uses LaTeX for documentation. On Debian based systems, LaTeX can be installed (as root) with

```
apt-get install texlive-latex-extra texlive-extra-utils texlive-latex-recommended
```

or shorter

```
apt-get install texlive-full
```

which installs the complete (and usefull) LaTeX Environment.
Additionally, we use the great CircDia LaTeX package for drawing circuit diagrams by Dr. Stefan Krause (Saarbr&uuml;cken/Germany). Please download [CircDia](http://www.taylorgruppe.de/circdia "http://www.taylorgruppe.de/circdia"), unzip it, and run `mktexlsr` in the directory. Many Thanks to Stefan for the excellent work!

### Magic

Another software for the Popcorn tool, which should be installed before usage, is [Magic](http://opencircuitdesign.com/magic "http://opencircuitdesign.com/magic"). Magic is Open Source, but not part of all Linux distributions (it is missing on OpenSuse, Arch Linux etc). On Debian based systems,

```
apt-get install magic
```

works.

Currently we are using a patched version of [Magic 8.2](https://github.com/libresilicon/magic-8.2).

## Usage

The whole Build Process is controlled / ruled by GNU Make. On Debian based systems, Make can be installed with

```
apt-get install make
```

Please make yourself familiar with the Danube River's Build System - assure your are not root anymore - by typing:
```
make
```

which shows a help screen with available targets.

## Documentation

For documentation we are using LaTeX.

All original LaTeX files are stored inside

* Documentation/LaTeX Folder

You can build the documentation out of the LaTeX sources just by using the Makefile

```
make doc
```

on top of the project directory.
Please read the documentation with the PDF Viewer of your choise

```
$PDFVIEWER Documentation/DanubeRiver.pdf
```
carefully.

## NOTE

If you do not understand, what the hack we are doing here, please lean back with a good textbook about CMOS or ASIC technology development, learn, and come back later.

