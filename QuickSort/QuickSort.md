# Quick sort

Quicksort og quick select : Fundemental algoritme, en af de vigtigste algoritmer overhovedet.

Pivot elementet placeres vha. partition: \
Elementet skal placeres så alle til venstre er mindre,- og alle til højre er størrer

Herefter sorteres venstre og højre rekursivt:
sort(low, j-1)
sort(j+1,hi)


## Quicksort implementations detaljer

In place:\
Partioning er "in place" men man kan lave sortering med et ekstra array. ... men ikke det værd

Terminating in loop:\
det er besværligt at tjekke om "pointers" krydser

Equal keeys: \
Bedre at stoppe scans når man har ens keys

Preserving randomness: \
nødvendig for performance

Alternativt tilfældigt pivot element: \
Lidt besværligt

POINTE: Gode algoritmer er bedre end super computere

## Best Case

Hvis vi hver gang pivot elemetet skal placeres,- placerer den i midten...

## Worst Case

Hvis listen allerede er sorteret

## Såkaldt Las Vegas algoritme.

Den er garanteret at være korrekt, men undførselstiden er afhængig af om indholdet er randomizeret

## Quick Sort er ikke stabil
