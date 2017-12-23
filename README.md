Dwarf Therapist Guide
=====================

[![Build Status](https://travis-ci.org/Dwarf-Therapist/Manual.svg?branch=master)](https://travis-ci.org/Dwarf-Therapist/Manual)

This guide, originally created by [ResidentMario](https://github.com/ResidentMario/dt-guide), explains how to use [Dwarf Therapist](https://github.com/Dwarf-Therapist/Dwarf-Therapist) from basics to advanced features.


Building
--------

### Installing dependencies

Debian/Ubuntu:

    sudo apt-get install cmake imagemagick texlive-latex-extra

Fedora:

    sudo dnf install cmake ImageMagick texlive-bibtex texlive-cm texlive-latex-bin texlive-makeindex texlive-mfware texlive-preprint texlive-sidecap texlive-wrapfig

### Building using cmake

    mkdir build
    cd build
    cmake ..
    make

Linux users can install the manual at the appropriate location for Dwarf Therapist to find by adding `-DCMAKE_INSTALL_PREFIX=...` option to cmake with the same prefix used by Dwarf Therapist build and then running `make install` (or `sudo make install`, if the chosen prefix requires root permission).



