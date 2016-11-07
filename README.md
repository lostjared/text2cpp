# bin2cpp

Convert Binary file to C++ array

To compile run:


$ ./autogen.sh

$ ./configure

$ make

$ sudo make install

to use this program:

$ bin2cpp sourcefile outputfilename

outputfilename will have .cpp and .h appended to it 
use memfile.hpp which will be installed to whatever prefix configure
was configured for you can use this to manipulate the array similar to a
file. Or you could use this with SDL_RWops.


