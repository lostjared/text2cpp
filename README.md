# bin2cpp / text2cpp

Convert Binary file to C,C++ or Go array to embed resources

Convert text files/terminal output into array of C++ std::string, hex values, or const char *

You will need: autotools (autoconf, automake etc.)
Clang or GCC version that supports C++17

To compile run:


$ ./autogen.sh

$ ./configure

$ make

$ sudo make install


# to use the bin2cpp  program:

$ bin2cpp sourcefile outputfilename language

langauge option should be c for C, cpp for C++, cpp17 for C++17, and go for Go 


The Output filenames will have the source file extension be .c or .cpp, and the header file will have .h appended to it if you are using C++ you can use use memfile.hpp it will be installed to whatever prefix configure was configured for you can use this to manipulate the array similar to a
file. Or you could use this with SDL_RWops. The program will output the names of the array and a length variable.


# To use the text2cpp:

Simple program that outputs header files using C++17's inline variables to use:

to use const char *:

$ text2cpp inputfile outputfile variable_name s
to use std::string:

$ text2cpp inputfile outputfile variable_name c
to use a character array char arr[]

$ text2cpp inputfile outputfile variable_name b
or

$ cat sourcefile  | text2cpp variable_name s
or

$ cat sourcefile  | text2cpp variable_name c
or

$ cat sourcefile | text2cpp variable_name b
optional skip blank lines with p argument

$ text2cpp inputfile outputfile varaiblename sp
or skip lines with char array[]:

$ cat source | text2cpp var_name bp
optional sorting use g for greater than, l for less than like this

for greater than sorting use

$ text2cpp inputfile outputfile variable_name sg
or less than sorting use

$ text2cpp inputfile outputfile variablename sl
also works with pipes

$ cat sourcefile | text2cpp variable_name cl
