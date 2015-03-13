# QTPIE #

QTPIE (charge transfer with polarization current equilibration) is a new charge model, similar to other charge models like QEq, fluc-q, EEM or ABEEM. Unlike other existing charge models, however, it is capable of describing both charge transfer and polarization phenomena. It is also unique for its ability to describe intermolecular charge transfer at reasonable computational cost.

# About the code #

## version 1.0rc2.1 (July 7, 2010) ##

The Fortran code has been updated:

  * Fixed a problem with automake dependencies - the make can fail if it decides to compile the modules after files that need them
  * Preliminary support for Ewald summation is available in ewald.f

## version 1.0rc2 (March 18, 2010) ##

Several implementations of the QTPIE model in Fortran, C and Python are now available. The Python version requires scipy to be installed first.

The main improvements are that the Fortran and C codes now contain code that computes analytic gradients. Also, the build structure has been overhauled using GNU autotools in an effort to comply with GNU practices. Hopefully, this means that the code is now easier to compile.

To compile and install the Fortran and C packages, run the usual
```
./configure
make
make install
```

The following command builds and runs a short program designed to check that the code was built properly:
```
make check
```

The TINKER interface is available only in the Fortran code. To compile this, specify the following option to the configure script:
```
./configure --with-tinker=[directory/to/tinker/source]
```

## version 1.0rc1 (May 12, 2008) ##

This implementation of QTPIE is written in Fortran 90 and supports interfacing with the [TINKER](http://dasher.wustl.edu) molecular dynamics package.

# References #

For more information about the QTPIE model, please refer to the literature:

  1. J. Chen and T. J. Martinez, "QTPIE: Charge transfer with polarization current equalization. A fluctuating charge model with correct asymptotics", _Chemical Physics Letters_ 438 (2007), 315-320. DOI: [10.1016/j.cplett.2007.02.065](http://dx.doi.org/10.1016/j.cplett.2007.02.065). Erratum: _ibid_, 463 (2008), 288. DOI: [10.1016/j.cplett.2008.08.060](http://dx.doi.org/10.1016/j.cplett.2008.08.060)
  1. J. Chen, D. Hundertmark and T. J. Martinez, "A unified theoretical framework for fluctuating-charge models in atom-space and in bond-space", _Journal of Chemical Physics_ 129 (2008), 214113. DOI: [10.1063/1.3021400](http://dx.doi.org/10.1063/1.3021400).
  1. J. Chen and T. J. Martinez, "Charge conservation in electronegativity equalization and its implications for the electrostatic properties of fluctuating-charge models", _Journal of Chemical Physics_ 131 (2009), 044114. DOI: [10.1063/1.3183167](http://dx.doi.org/10.1063/1.3183167)
  1. J. Chen and T. J. Martinez, "The dissociation catastrophe in fluctuating-charge models and its implications for the concept of atomic electronegativity", _Progress in Theoretical Chemistry and Physics_, to appear. [arXiv:0812.1543](http://arxiv.org/abs/0812.1543)
  1. J. Chen, "Theory and applications of fluctuating-charge models", PhD (chemical physics) thesis, University of Illinois at Urbana-Champaign, Department of Chemistry, 2009.
  1. J. Chen and T. J. Martinez, "Size-extensive polarizabilities with intermolecular charge transfer in a fluctuating-charge model", in preparation. [arXiv:0812.1544](http://arxiv.org/abs/0812.1544)