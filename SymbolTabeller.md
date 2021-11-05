# Symbol tabeller

## inledning
Er abstraktion der er defineret ved man kan gemme en værdi, der er tilknyttet en bestemt nøgle.
Hoved operationer :

indsæt værdi - med en given nøgle \
hente en værdi - for en given nøgle

Også kendt som "dictionaries", "maps", "acossiative arrays" \
java : treemap , hashmap
php: arrays er en wrapper for en symboltabel
js, python: objekter er bare en symboltabel

Generaliseret array - index kan være alt

## API

Vigtigste metoder:

<b>void put(key, value) :</b> \
value må ikke være null, ellers kan vi aldrig vide om en nøgler er anvendt eller ej! \
overskriver gammel værdi 

<b>value get(key)       : </b>
returnerer null, hvis der ikke er gemt noget på denne nøgle-plads \

## Implementation

Man kunne anvende "compareTo" hver gang man indsætter en ny værdi... giver ikke god udførselstid, men det er en mulighed\
God praksis: Anvend imutable for at undgå at nøgler ændrer sig\

### Equals i java - er vigtig for at sammenligne nøgler

Krav: Der skal eksistere en <i>ækvivalensrelation</i> for nøglerne.. så vi kan anvende equals meningsfuldt (refleksiv, transitiv, symetrisk, ikke-null)\ 
I Java skal vi pga. klassehierakiet undersøge om objekterner er samme type, om objektet er det samme og om 





## Anvendelser
internet url er nøglen - ip er værdien</br>
