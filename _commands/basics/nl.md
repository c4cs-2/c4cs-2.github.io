---
---
#nl
---
---

nl is a command that prints a file to the terminal, with each line enumerated from [1...n] by default

*Basic Syntax*
---

To simply enumerate one file, do: **$ n1 [filename]**

Lets say we have a file called foo.cpp. foo.cpp initially contains the following:

```cpp
#include <iostream>
using namespace std;
int main(){
    cout << "Hello World" << endl;
    return 0;
}
```

When "nl foo.cpp" is used on the command line:

```
$ nl foo.cpp
     1  #include <iostream>
     2  using namespace std;
     3  int main(){
     4      cout << "Hello World" << endl;
     5      return 0;
     6  }
```

*Additional Syntax and commands*
---

The more generall syntax of a nl command is the following:
**$ nl [Option]... [FILE]...**

Where Option is at least one valid option and file is the name of the file to be enumerated. The additional options allow for users to increase the default increment value, number empty lines, change the starting line number, and more. For more information in regards to the options avalaible with nl, please visit the following websites:

[howtoforge.com](https://www.howtoforge.com/linux-nl-command/)

[systutorials.com](https://www.systutorials.com/docs/linux/man/1-nl/)

[computerhope.com](https://www.computerhope.com/unix/nl.htm)