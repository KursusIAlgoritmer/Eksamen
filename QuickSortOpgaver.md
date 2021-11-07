# Quick Sort Opgaver

## Opgave 2.3.2 
Show, in the style of the quicksort trace given in this section, how quicksort sorts
the array E A S Y Q U E S T I O N (for the purposes of this exercise, ignore the
initial shuffle).

<pre>
Sort 0 til hi
Partitioning
"E" A S Y Q U E S T I O N
 i                      j        element i < "E" tæl en op,   element j > "E" tæl en op

"E" A S Y Q U E S T I O N
    i,j                            i og j krydser, byt "E" ud med j

 A E S Y Q U E S T I O N
--------------------------------------------------------
Sort 0 til j -1                  færdigt
--------------------------------------------------------
Sort j+1 til hi
Partitioning fra j+1 til hi

A E "S" Y Q U E S T I O N
     i                  j        element i < "E" tæl en op,   element j > "E" tæl en op

A E "S" Y Q U E S T I O N
     i                  j        element i < "E" tæl en op,   element j > "E" tæl en op


 
    
</pre>
sammenligner A med N, 

## Opgave 2.3.3 
What is the maximum number of times during the execution of Quick.sort()
that the largest item can be exchanged, for an array of length N ?

## Opgave 2.3.8 About how many compares will Quick.sort() make when sorting an array of
N items that are all equal?
