
**gcc**
---


`gcc` is a C and C++ compiler for UNIX systems developed by GNU project.

```
$ gcc -o testfile testfile.c
# complies the code in testfile.c into an exectuable called "testfile"
$ chmod a+x testfile
# change the permission to executable file mode
$ ./testfile
# executes the program "testfile", the resulting ouput of the program
# if any, will show right under this command.
```


**Useful Options / Examples**

  ### `gcc -Wall`

enables all the complier's warning messages.

```
# imagine you have the following code named myfile.c
// myfile.c
#include <stdio.h>

int main()
{
    printf("Program run!\n");
    int i=10;
}
```
If this code is complied as shown in the first example above, then we 
perform: `$ gcc -o myfile myfile.c` and the resulting output is `$` (nothing). However with the `-Wall` flag, we obtain the informative error messages:
```
$ gcc -Wall -o myfile myfile.c
myfile.c In function 'main':
myfile.c:6:6: warning: unused variable 'i'
myfile.c:7:1: warning: control reaches end of non-void function
$
```


### `gcc -I`

allows user to include directory of header files.

Imagine you have the following code called "myfile.c" and note that it includes a header file named "myheader.h" located in the directory /project/source :

```
// myfile.c
#include <stdio.h>
#include "myheader.h"
 
void main()
{
    int num = NUM1;
    printf("num=%d\n", num);
}
```
If complied normally without the `-I` flag, the result is:
```
$ gcc -o myfile myfile.c
myfile.c:2:22: fatal error: myheader.h: No such file or directory
compilation terminated.
$
```
Now, using the `-I` flag and including the directory that "myheader.h" is located in, we obtain successful compilation:
```
$ gcc -Iproject/source -o myfile myfile.c
$ ./myfile
num=5
$
```


### `gcc -O`

sets the complier's optimization level. The resulting flags and optimizations are listed below:

- `-O0` (default option) performs optimization for compile time.

- `-O1` optimization for code size and execution time.

- `-O2` further optimization for code size and execution time.

- `-O3` highest optimization for code size and execution time.

- `-Os` optimization for code size.

usage example: `$ gcc -O0 myfile.c -o myfile`


### `gcc -g`

generate debug information to be used GDB debugger. The resulting flags and debug info are listed below:

- `-g0` no debug information

- `-g1` minimal debug information

- `-g` default debug information

- `-g3` maximum debug information

imagine we have a file named "myfile.c" with the following code:
```
#include <stdio.h>
 
void main()
{
    printf("Program run!!\n");
}
```

 If we perform the command `$ gcc -o -g myfile myfile.c` we can then perform the GDB debugger on the file "myfile" as:
 
 ```
 $ gdb myfile
(gdb) run
Starting program: /home/ubuntu/myfile
Program run!!
Program exited with code 012.
(gdb) quit
$
```


### `gcc -D`

Define a macro to be used by the preprocessor.

Imagine you have the file "myfile.c" containing the following code:

```
#include <stdio.h>
 
void main()
{
    #ifdef DEBUG    
       printf("Debug run\n");
    #else
       printf("Release run\n");
    #endif
}
```

if the code is compiled without the `-D` flag, the output is:

```
$ gcc -o myfile myfile.c
$ ./myfile
Release run
$
```

However, if we include the `-D` flag, we obtain the desired output:

```
$ gcc -D DEBUG -o myfile myfile.c
$ ./myfile
Debug run
$
```

### `gcc -o`

writes the build output to an output file.

For example, if you have the file named "myfile.c" containing the following code:

```
#include <stdio.h>

void main()
{
    printf("Program run\n");
}
```

if you want to write the build output to a file named "myfile" and run it, we can perform this as shown below:

```
$ gcc -o myfile myfile.c
$ ./myfile
Program run
$
```



