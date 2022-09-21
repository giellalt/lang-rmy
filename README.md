The Kalderash Romani morphology and tools
=========================================

[![GitHub issues](https://img.shields.io/github/issues-raw/giellalt/lang-rmy)](https://github.com/giellalt/lang-rmy/issues)
[![Build Status](https://divvun-tc.thetc.se/api/github/v1/repository/giellalt/lang-rmy/main/badge.svg)](https://github.com/giellalt/lang-rmy/actions)
[![License](https://img.shields.io/github/license/giellalt/lang-rmy)](https://github.com/giellalt/lang-rmy/blob/main/LICENSE)
[![Desktop speller download](https://img.shields.io/badge/download%40latest-desktop--bhfst-brightgreen)](https://pahkat.uit.no/main/download/speller-rmy?platform=desktop&channel=nightly)
[![Mobile speller download](https://img.shields.io/badge/download%40latest-mobile--bhfst-brightgreen)](https://pahkat.uit.no/main/download/speller-rmy?platform=mbile&channel=nightly)

NOTE!! The ISO 639-3 code rmy is used for Vlax Romani (Glottolog:
vlax1238). The files in this folder do not model Vlax Romani, though,
but one of its subdialects, Kalderash (Glottolog: kald1238).

The reason for this is that there is no ISO 639 code for Kalderash.
Since this infrastructure is made for Nordthern languages, and since
Kalderash is an official language in Sweden, we use the ISO code of its
parent language.

This directory contains source files for the Kalderash Romani language
morphology and dictionary. The data and implementation are licenced
under the __LICENSE__ licence, also detailed in the
[LICENSE](https://github.com/giellalt/lang-rmy/blob/main/LICENSE). The
authors named in the AUTHORS file are available to grant other licencing
choices.

Install proofing tools and [keyboards](https://github.com/giellalt/keyboard-rmy)
for the Vlax Romani language by using the [Divvun Installer](http://divvun.no)

Download and test speller files
-------------------------------

The speller files downloadable at the top of this page (the `*.bhfst` files) can
be used with [divvunspell](https://github.com/divvun/divvunspell), to test their
performance. These files are the exact same ones as installed on users' computers
and mobile phones. Desktop and mobile speller files differ from each other in the
error model and should be tested separately — thus also two different downloads.

Documentation
-------------

Documentation can be found at:

- [Language specific documentation](https://giellalt.github.io/lang-rmy/)
- [General documentation](https://giellalt.github.io/)

Core dependencies
-----------------

In order to compile and use Vlax Romani language morphology and
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
git clone https://github.com/giellalt/lang-rmy
```

Using Subversion:
```
svn checkout https://github.com/giellalt/lang-rmy.git/trunk lang-rmy
```

Building and installation
-------------------------

[INSTALL](https://github.com/giellalt/lang-rmy/blob/main/INSTALL)
describes the GNU build system in detail, but for most users it is the usual:

```sh
./autogen.sh # This will automatically clone or check out other GiellaLT dependencies
./configure
make
(as root) make install
```
