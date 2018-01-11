DDirham integration/staging tree
================================

Copyright (c) 2009-2018 Bitcoin Developers

Copyright (c) 2011-2018 Litecoin Developers

Copyright (c) 2011-2018 DDirham Developers

What is DDirham?
----------------

DDirham is an EXPERIMENTAL lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 30 second block targets
 - subsidy halves in 840k blocks (~9 months)
 - ~10 million total coins

The rest is the same as Bitcoin.
 - 500 coins per block
 - 10 blocks to retarget difficulty

License
-------

DDirham is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the DDirham
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/ddirham-project/ddirham/tags) are created
regularly to indicate new official, stable release versions of DDirham.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test ddirham-qt.pro
    make -f Makefile.test
    ./ddirham-qt_test

