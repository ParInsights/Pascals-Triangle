# Pascals-Triangle
Really just generating a triangular array of binomial coefficient. But the test is to see if we can do this in java. 

Technically - Pascal's triangle is just a triangular array of the binomial coefficients.

The rows of Pascal's triangle are conventionally enumerated starting with row n = 0 at the top (the 0th row). The entries in each row are numbered from the left beginning with k = 0 and are usually staggered relative to the numbers in the adjacent rows. The triangle may be constructed in the following manner: In row 0 (the topmost row), there is a unique nonzero entry 1. Each entry of each subsequent row is constructed by adding the number above and to the left with the number above and to the right, treating blank entries as 0. For example, the initial number in the first (or any other) row is 1 (the sum of 0 and 1), whereas the numbers 1 and 3 in the third row are added to produce the number 4 in the fourth row.

![Image of Yaktocat](https://wonderopolis.org/wp-content/uploads/2017/01/1853_Pascals_Triangledreamstime_xxl_69735729.jpg)



## Formulation
The entry in the nth row and kth column of Pascal's triangle is denoted Formula. For example, the unique nonzero entry in the topmost row is Formula example.

With this notation, the construction of the previous paragraph may be written as follows:

![Image of Formula](https://slideplayer.com/slide/12222370/72/images/9/Pascal%E2%80%99s+formula+Combinatorial+proof%3A.jpg) 



## Calculation for triangle entries in O(n) time:

We know that i-th entry in a line number lineNumber is Binomial Coefficient C(lineNumber, i) and all lines start with value 1. The idea is to calculate C(lineNumber, i) using C(lineNumber, i-1). It can be calculated in O(1) time using the following:

```C(lineNumber, i)   = lineNumber! / ((lineNumber - i)! * i!)>
C(lineNumber, i - 1) = lineNumber! / ((lineNumber - i + 1)! * (i - 1)!) 
```

We can derive following expression from above two expressions:

```
C(lineNumber, i) = C(lineNumber, i - 1) * (lineNumber - i + 1) / i
So C(lineNumber, i) can be calculated from C(lineNumber, i - 1) in O(1) time.
```
