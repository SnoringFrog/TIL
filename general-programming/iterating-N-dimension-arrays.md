#Iterating Through N-Dimensional Arrays Effeciently

With multi-dimensional arrays, you might think the following two programs would operate in about the same amount of time:

```C
#include <stdio.h>
#include <stdlib.h>

main () {
  int i,j;
  static int x[4000][4000];
  for (i = 0; i < 4000; i++) {
	for (j = 0; j < 4000; j++) {
	  x[j][i] = i + j; }
  }
}
```

```C
#include <stdio.h>
#include <stdlib.h>
	
main () {
  int i,j;
  static int x[4000][4000];
  for (j = 0; j < 4000; j++) {
	 for (i = 0; i < 4000; i++) {
	   x[j][i] = i + j; }
   }
}
```

But that's not necessarily true. In this case, the 2nd method is faster, due to C storing arrays in row-major order.

E.g., if you have this 2D array:
[0,0] [0,1] [0,2]
[1,0] [1,1] [1,2] 
[2,0] [2,1] [2,2] 

C will store it as such:
0,0 | 0,1 | 0,2 | 1,0 | 1,1 | 1,2 | 2,0 | 2,1 | 2,2

Whereas a column-major language, like Fortran, would store it like this:
0,0 | 1,0 | 2,0 | 0,1 | 1,1 | 2,1 | 0,2 | 1,2 | 2,2

Thus, the 2nd program progresses through the loop in the order it is stored in memory, minimizing cache misses (in a column-major language, the 1st program would be faster for the same reason).

For N-dimensional arrays such as `x[a][b]...[c]`, in a row-major language your loops (from outer to inner) should iterate over `a`, `b`, ..., and `c`. For column-major, they should be in the reverse order. 
