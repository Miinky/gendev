GENDEV - Genesis development environment for Linux.

Gendev exists to setup a Linux (or presumably other Unix) system for Sega
Genesis development. Gendev is not intended to replace, but to be a companion project to the SGDK
(Sega Genesis Development Kit).


BASIC INSTRUCTIONS
==================

    $ git clone https://github.com/kubilus1/gendev.git
    $ cd gendev
    $ make 

This will build the entire GCC toolchain for genesis development, plus SGDK.
Build takes about 1 hour on my system.  Note this will only create C libraries for the 68K processor.  For a 32x SH2
development:

    $ make 32x

Now I want to create a project ... 

    $ cp -r /opt/toolchains/gen/skeleton mycoolproject 
    $ cd mycoolproject 

*type type type* 

    $ make 

----

Troubleshooting and FAQ
=======================

Build Requirements
------------------
On Ubuntu for instance you may want to install the following:

    sudo apt-get install build-essential texinfo git

makeinfo is missing
-------------------

Try installing the 'texinfo' package.  On Ubuntu this would be 'sudo apt-get
install texinfo'

How do I build this on *BSD?
----------------------------

Use gmake.  Try the following to build the framework: 

    MAKE=gmake MGET=fetch gmake

And for sgdk

    cd sgdk; gmake install

This doesn't work/There is an obvious issue
-------------------------------------------

Please let me know and perhaps file an issue.



Project Structure
=================

 * gendev/Makefile 


Makefile for setting up the required build tools.  Running this is enough for
a basic development environment.


 * gendev/sgdk/Makefile

Makefile for setting up SGDK for use on Linux


 * gendev/sgdk/skeleton

Some basic files to assist in building SGDK project under Linux.


 * examples

A few examples using this toolkit

 * extras

Other tools and utilities useful for development purposes.
