# Quick Sort Opgaver

## Opgave 2.3.2 
Show, in the style of the quicksort trace given in this section, how quicksort sorts
the array E A S Y Q U E S T I O N (for the purposes of this exercise, ignore the
initial shuffle).\

ABCDEFGHIJKLMNOPQRSTUVXYZ


<pre>
Sort 0 til hi
Partitioning
"E" A S Y Q U E S T I O N
    i                   j        element i < "E" tæl en op,   element j > "E" tæl en op

"E" A S Y Q U E S T I O N
    j i                            i og j krydser, byt "E" ud med j

 A E S Y Q U E S T I O N
--------------------------------------------------------
Sort 0 til j -1                  færdigt
--------------------------------------------------------
Sort j+1 til hi
Partitioning fra j+1 til hi

A E "S" Y Q U E S T I O N
        i               j        element i < "E" tæl en op,   element j > "E" tæl en op

A E "S" N Q U E S T I O Y
          i           j          byt rundt

A E "S" N Q U E S T I O Y
            i         j          tæl op

A E "S" N Q O E S T I U Y
            i         j          byt rundt


A E "S" N Q O E S T I U Y
                  i j            tæl op

A E "S" N Q O E S I T U Y
                  j i            byt rundt

A E "S" N Q O E S I T U Y
                  j i            byt rundt

A E  I  N Q O E S S T U Y
                  |              partitioning done
------------------------------------------------------------------
 Sort 1 til 8
 
    
</pre>
sammenligner A med N, 

## Opgave 2.3.3 
What is the maximum number of times during the execution of Quick.sort()
that the largest item can be exchanged, for an array of length N ?

<pre>
 p x x x x x h ... x l  x x x x
h bliver sorteret en gang
højre side er nu 
p h x ... x x

hvis det højeste element ender i venstre side hver gang der laves partitioning?
Kan det vel blive byttet ud med alle elementer ? N gange?
</pre>


## Opgave 2.3.8 About how many compares will Quick.sort() make when sorting an array of
N items that are all equal?
