[![Build Status](https://travis-ci.org/liudonghua123/enhanced-bc.svg?branch=master)](https://travis-ci.org/liudonghua123/enhanced-bc)

GNU bc version 1.06: 

###Extra configuration options:

* --with-readline tells bc to use the readline package that allows
  for editing input lines when run interactive.
* --with-editline tells bc to use the BSD editline package that
  allows for editing input lines when run interactive.

###Extra make steps:

The simple make compiles a version of bc with fixed parameters
for the recursive multiplication algorithm.  The fixed parameter
is the number of digits where a sequential algorithm is used
instead of the recursive algorithm.  It is set to a value that
is known good on a couple of machines. (Sparc Ultra 10, Pentium
II, 450.)  I'm calling this point the crossover point.

To make a version of bc with a custom crossover point for your
machine, do the following steps:

make timetest
make

The timetest step takes a minimum of 10 minutes to complete.



