# bin2cpp

Convert Binary file to C or C++ array to embed resources

You will need: autotools (autoconf, automake etc.)
Clang or GCC version that supports C++11


To compile run:


$ ./autogen.sh

$ ./configure

$ make

$ sudo make install

to use this program:

$ bin2cpp sourcefile outputfilename language

langauge can be either C or C++

The Output filenames will have the source file extension be .c or .cpp, and the header file will have .h appended to it if you are using C++ you can use use memfile.hpp it will be installed to whatever prefix configure was configured for you can use this to manipulate the array similar to a
file. Or you could use this with SDL_RWops. The program will output the names of the array and a length variable.


