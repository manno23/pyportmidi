PyPortMidi v0.03 03/15/05
Python wrappings for PortMidi
John Harrison
harrison@media.mit.edu

Modified by Jason Manning 12/2014

PyPortMidi
----------

PyPortMidi is a Python wrapper for PortMidi. PortMidi is a cross-platform
C library for realtime MIDI control. Using PyPortMidi, you can send and
receive MIDI data in realtime from Python.

Besides using PyPortMidi to communicate to synthesizers and the
like, it is possible to use PyPortMidi as a way to send MIDI messages
between software packages on the same computer. For example, Using
PyPortMidi and MIDI-YOKE on a Windows machine, it is possible to send
realtime MIDI messages between programs on the same computer using
loopback virtual MIDI ports. (At this time, MIDI-YOKE does not appear
to run on Windows Vista.)

PyPortMidi is cross-platform, but it will require some small
changes in the setup.py file for it to install correctly on Linux
machines. The changes should be pretty straightforward, and I am
anxious to work with a Linux user on the port.


PyPortMidi works with Python 2.6 and Python 3.1, although the ports
are mostly separate because of various language incompatibilities.

Please see README26.txt for information about the Python 2.6 version.

See README31.txt for information about the Python 3.1 version.





* So with pip,setup.py etc...

Pre-Python: Building the system library
Compiles all the source producing a lib_s.a and lib.so.
For each platform we have:
dynamic libraries - these were compiled against the system,
                    (eg. system drivers, graphical stuff etc...)

.pyx -(cythonised)-> .c

Setup.py --> build-ext()
    *.c
    -library directories
    -include directories
    Names of library files,
        This is where i don't know whether it is using static or dynamic libraries

    shouldn't need the dll at all.

    Cross compiling for windows, shared or static system libraries?
