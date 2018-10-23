#Unix sort command
The unix sort command is a basic utility command, used for organizing the content of files. By default, it will sort low to high alphanumerically. That is:
    1. Lines beginning with a number will appear first in the file, sorted in order 0-9.
    2. Then, lines beginning with a letter will appear, sorted in order A-Z.
        *Note, any lines starting with a lower-case letter will appear in the file above a line that starts with the upper-case variant of that same letter.

For clarity in this reference document, we will use a sample text file, file.txt, which has the original content of:
>dog
>apple
>cat
>Elephant
>77
>31
>30
>excitement

##Basic sorting
'''$sort \[filename\]'''
If we were to execute __sort file.txt__, we would sort our file according to the default rules, resulting in a file that reads:
>30
>31
>77
>apple
>cat
>dog
>excitement
>Elephant

##Output redirection
'''$sort \[input_filename\] > \[output_filename\]'''
OR
'''$sort -o \[input_filename\] \[output_filename]'''
Both of the above commands are equivalent for file redirection when utlizing the sort command. In both cases, the first argument (the input file) will be sorted (in this case according to the default sorting rules). The resulting sorted text will then be stored in the second argument (the output file). This is useful in cases where you wish to sort a file's content but still retain a copy of the original order of the text.

##Numeric sort
'''$sort -n \[filename\]'''
Sorts the file numerically, from low to high numbers.

##Sort on column/field
'''$sort -k x \[filename\]'''
This command allows you to sort on a column, whose number is specified by x. For example, calling with the argument 2 will sort on column 2. The columns are determined by 1-indexing, not 0-indexing. This determines the order that that particular column would be sorted in, and rearranges the file accordingly, without regard for how any other columns in the file would be ordered.
###Other column/field sorting options
*You can also attach a flag to the column. For example, if the column 2 that we are sorting by consists of only numbers, we can call __2n__ rather than simply 2, to specify that we want to perform a numeric sort on that column.
*You can use the argument x,y rather than just x. This says to sort on the aggregate field of column x to column y. If no y value is provided, such as in the initial example, the command will pick all of the columns from x to the end of the file as the field to sort on. Therefore, if you only want to sort on a single column, you should specify __-k x,x__ to restrict the field to only that single column. If you want to specify a sort (for example, n for numeric) you would do so after the first argument, so __-k xn,x__.
*If you are sorting on a column, you may encounter a case where you need to break ties for the sort (for example, sorting numerically on a column, and two different rows have the same number). If you want to specify which column's data should be looked at next to break the tie, you can use __$sort -k x,x y,y z,z \[filename\]__ where each of the variable pairs represents a different column. In that example, we sort by column x, sort any tied rows by y, and break any remaining ties by sorting on z.

##Reverse sort
'''$sort -r \[filename\]'''
This command simply allows you to sort the file in reverse (i.e. high to low). This can be combined with other flags, for example, __-nr__ to sort numerically in reverse.