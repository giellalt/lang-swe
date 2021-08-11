The Swedish morphology and tools
==========================================

[![GitHub issues](https://img.shields.io/github/issues-raw/giellalt/lang-swe)](https://github.com/giellalt/lang-swe/issues)
[![Build Status](https://github.com/giellalt/lang-swe/workflows/Speller%20CI+CD/badge.svg)](https://github.com/giellalt/lang-swe/actions)
[![License](https://img.shields.io/github/license/giellalt/lang-swe)](https://raw.githubusercontent.com/giellalt/lang-swe/main/LICENSE)
OR
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

This repository contains finite state source files for the Swedish language,
for building morphological analysers, proofing tools
and dictionaries. The data and implementation are licensed under either of the __LGPLv3__
or the __CC-BY-SA__
licenses, also detailed in the
[LGPLv3 LICENSE](https://github.com/giellalt/lang-swe/blob/main/LICENSE) and
[CC-BY-SA](https://github.com/giellalt/lang-swe/blob/main/src/fst/incoming/saldo_2.3/Creative_Commons_Legal_Code.html) files. The
authors named in the AUTHORS file are available to grant other licensing
choices.

Install proofing tools and [keyboards](https://github.com/giellalt/keyboard-swe)
for the Swedish language by using the [Divvun Installer](http://divvun.no)
(some languages are only available via the nightly channel).

Documentation
-------------

Documentation can be found at:

-   <https://giellalt.uit.no/lang/swedoc/index.html>
-   <https://giellalt.uit.no/index.html>

Core dependencies
-----------------

In order to compile and use Swedish language morphology and
dictionaries, you need:

- an FST compiler: [HFST](https://github.com/hfst/hfst), [Foma](https://github.com/mhulden/foma) or [Xerox Xfst](https://web.stanford.edu/~laurik/fsmbook/home.html)
- [VislCG3](https://visl.sdu.dk/svn/visl/tools/vislcg3/trunk) Constraint Grammar tools

To install VislCG3 and HFST, just copy/paste this into your Terminal on **Mac OS X**:

```
curl https://apertium.projectjj.com/osx/install-nightly.sh | sudo bash
```

or terminal on **Ubuntu, Debian or Windows Subsystem for Linux**:

```
wget https://apertium.projectjj.com/apt/install-nightly.sh -O - | sudo bash
sudo apt-get install cg3 hfst
```

or terminal on **RedHat, Fedora, CentOS or Windows Subsystem for Linux**:

```
wget https://apertium.projectjj.com/rpm/install-nightly.sh -O - | sudo bash
sudo dnf install cg3 hfst
```

Alternatively, the Apertium wiki has good instructions on how to [install the dependencies for Mac
OS X](https://wiki.apertium.org/wiki/Apertium_on_Mac_OS_X) and how to [install
the dependencies on
linux](https://wiki.apertium.org/wiki/Installation_of_grammar_libraries)

Further details and dependencies are described on the GiellaLT [Getting Started](https://giellalt.uit.no/infra/GettingStarted.html) pages.

Downloading
-----------

Using Git:
```
git clone https://github.com/giellalt/lang-swe
```

Using Subversion:
```
svn checkout https://github.com/giellalt/lang-swe.git/trunk lang-swe
```

Building and installation
-------------------------

[INSTALL](https://github.com/giellalt/lang-swe/blob/main/INSTALL)
describes the GNU build system in detail, but for most users it is the usual:

```sh
./autogen.sh # This will automatically clone or check out other GiellaLT dependencies
./configure
make
(as root) make install
```
