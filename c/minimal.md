# Minimal C Program
The following program is a minimal C starting point. It does demonstrate accessing the command line arguments.

```c
/*
 * minimal c program demonstrating accesing the command line arguments
 */

#include <stdio.h>

void dump_args(int argc, char* argv[]) {
    printf("[%d]", argc);
    for (int ii=0; ii<argc; ii++) {
        printf(" [%s]", argv[ii]);
    }
    printf("\n");
}

int main(int argc, char* argv[])
{
    dump_args(argc, argv);

    return(0);
}
```

## Compiling under gcc
1. Copy the code to a file called 'minimal.c'
2. Compile with `make minimal`
3. Make executable with `chmod u+x minimal`
4. Run with `./minimal this is a test`
5. Expected output is `[5] [./minimal] [this] [is] [a] [test]`
