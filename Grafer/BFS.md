# BFS

Algoritmen for DFS og BFS er den samme men BFS bruger en KØ istedet for en STAK!

DVs. efter hver gang man har "undersøgt" en knude, dvs. tilføjet alle knuder til køen, \
tager man den næste i køen og "undersøger".

## Datastrukturer: 
kø : Hvilke knuder der skal undersøges\
edgeTo[] : Hvilke knuder man kommer fra \
distTo[] : Hvor langt

## Løser følgende problem: 
BFS, finder korteste vej 

----

## Påstand : 
finder korteste vej fra knude S til alle andre knuder. \
Omkostning tid propertionel til  V + E

??? Er det ikke V + 2E for en ikke oriienteret graf - adjacency List ???
se her:
https://www.interviewbit.com/tutorial/depth-first-search/#Complexity-Analysis

## Bevis :
Køen indeholder altid 0 eller flere knuder i afstand k fra s \
Efterfulgt af 0 eller flere knuder i afstand k+1  
