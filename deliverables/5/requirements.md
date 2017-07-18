FUN-INPUT: The system shall accept a list of two or more parameters from the command line, each of which will correspond to one parameter in the covering array.

FUN-PARAM-TYPES: All parameters will be treated as Boolean values.  There will be no other kinds of parameters accepted.

FUN-ALGORITHM: The system shall use the naive pairwise test generation algorithm as discussed in class.  It shall not use IPOG or any other algorithm for this purpose.

FUN-BOOL-OUTPUT: The system shall output all "true" values as "1" and all false values as "0".

FUN-COVERING-ARRAY: The system shall output a covering array showing which tests could be executed to ensure that all pair possibilities (true/true, true/false, false/true, false/false) for any combination of two parameters.

FUN-NO-EXHAUSTIVE: Barring the case of two parameters, which must show an exhaustive test plan, the system shall never show an array which indicates that an exhaustive test plan must be run.

FUN-INVALID-INPUT: If there are zero or one parameters given as input to the program, it shall output the message "Please enter at least two parameters!" and exit.

FUN-PROG-NAME: The name of the program shall be "Pairwise" and it shall be executable from the command line by typing "java Pairwise" and any parameters.

FUN-UNSPECIFIED: In the case of ambiguity or unspecified behavior in the requirements, the example output below shall be considered the correct behavior.

## Example Output

```
$ java Pairwise
Please enter at least two parameters!

$ java Pairwise dog
Please enter at least two parameters!

$ java Pairwise dog cat
dog    cat
1      1
1      0
0      1
0      0

$ java Pairwise dog cat bird
dog    cat    bird
1      1      0
1      0      1
0      1      1
0      0      0

$ java Pairwise dog cat bird lizard
dog    cat    bird   lizard
1      1      0      0
1      0      1      1
0      1      1      0
0      0      0      1 
0      1      0      1
1      0      0      0

```