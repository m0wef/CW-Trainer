Welcome to CW Trainer!

2019-09-11 Ported to Qt5 and patched to run on macOS (without sound).
           Next: convert to use Qt's Media stuff.

Legal Stuff:

This application and its source code are hereby released under the
GPL, Version 2. Please find the enclosed LICENSE for more information
on the GPL.

Initial release date is 2/15/2002 by John Wagner, N1QO -
john@wagner-usa.net

Ported to Qt4 and ALSA support added on 8/17/2012 by Aaron Decker,
decker49@gmail.com

The program uses some Source Code from Ray Goff, G4FON - notably the
EncodeSineWave function. That code is used and released under the GPL
by permission from Ray. It should also be noted that Ray gave me the 
source code to his windows program and from that I was inspired to 
write this program.

The files lcdrange.h and lcdrange.cpp are from the QT Tutorial.
These files may be removed at a later date.

********** BEFORE YOU SUBMIT REQUESTS FOR FEATURES ********** 

Please read the file TODO - the early versions of this program are
more or less working prototypes intended to get something [anything]
out there for Linux to help people learn CW. Numerous features are
planned as well as a general unfudging of the source code. Again, the
early versions are out here just so people have something to use.

Purpose:

This application is intended to teach Morse Code (CW). 

It supports the Koch method;

	Teach at high speed, starting with two characters. When
	those character is recognized 90% of the time then add
	another character. Repeat until using all characters and 90%
	correctness is achieved... then speed up and start over!

Koch Method Resources:
Dave Finley, N1IRZ - http://www.sdc.org/~finley/
Windows software by Ray Goff, G4FON - http://www.qsl.net/g4fon
Go to http://www.google.com/ - type in "koch method" - tons of pages

It supports the Farnsworth method;

	Fast character speed (typically 20wpm) but wide character
	space (start at 5 wpm). Can use all characters at the same
	time or use with the Koch method above.

Farnsworth Method Resources:
Go to http://www.google.com/ - type in "farnsworth cw" - tons of pages

Requires QT Version 4. Both ALSA and OSS ( /dev/dsp ) are supported.
For OSS change "#define ALSA" on line 13 of cwsound.h to "#define OSS".


Building and running:

Unpack the archive: 

tar zxvf cwtrainer.tar.gz

Ensure you have your QTDIR environment variable set;

export QTDIR=/usr/share/qt3

(yours may be different, install the *qt3*-dev package for your system and look
for a directory with this structure:
qt<version>/
           bin/
	   doc/
	   include/
	   lib/
	   mkspecs/
	   plugins/
	   )

type: make

You should now have an executable called "cwtrainer"

Run it!: ./cwtrainer

There is no installation target yet. In the short term you may want to put
cwtrainer into your path if you don't want to give the path to this folder or
change directories each time you run it. Your $HOME/bin directory would be 
great for this, or /usr/local/bin if you want a site-wide location. 

A cwtrainer.pro file is included for tmake users who want to hack on
the program using qmake.

The "Load File..." will read a text file and play it as CW. At the
moment you will note that once you hit the "Stop CW" or "Start CW"
button, you will need to reload the file if you want to play it again.
A sample QSO is included in the file "qso.txt". Also note that Prosigns
are supported in the text file, append a ^ before the prosign;

Examples: ^AR ^BK ^BT ^SK

Maintainer:
John Wagner, N1QO - john@wagner-usa.net (original author)
Jacob Anawalt, KD7YKO - jlanawalt@users.sourceforge.net

Thanks to:
Ray Goff, G4FON - Source code to Koch
Karl Larsen, K5DI - testing and suggestions

History:
See CHANGES

Similar Projects:
It looks like a few other projects for learning CW have been posted to sf.net
since Feb 2002. If cwtrainer isn't at all what you are looking for, you may
want to check them out.

cw-trainer
* http://freshmeat.net/projects/cwtrainer/
* http://sourceforge.net/projects/cw-trainer/

cwtutor
* http://sourceforge.net/projects/cwtutor/
** Summary is almost exactly the same as this package's summary, but it is
   written quite differently.

cwtext
* http://freshmeat.net/projects/cwtext/
* http://cwtext.sourceforge.net/

cwstation
* http://sourceforge.net/projects/cwstation

