# Symbol tabeller

## Indledning
Er abstraktion der er defineret ved man kan gemme en værdi, der er tilknyttet en bestemt nøgle.
Hoved operationer :

indsæt værdi - med en given nøgle \
hente en værdi - for en given nøgle

Også kendt som "dictionaries", "maps", "acossiative arrays" \
java : treemap , hashmap
php: arrays er en wrapper for en symboltabel
js, python: objekter er bare en symboltabel

Generaliseret array - index kan være alt

## Anvendelser
internet url er nøglen - ip er værdien</br>


## API

Vigtigste metoder:

<b>void put(key, value) :</b> \
value må ikke være null, ellers kan vi aldrig vide om en nøgler er anvendt eller ej! \
overskriver gammel værdi 

<b>value get(key)       : </b>
returnerer null, hvis der ikke er gemt noget på denne nøgle-plads \

## CompareTo i java - Implementation

Man kunne anvende "compareTo" hver gang man indsætter en ny værdi... giver ikke god udførselstid, men det er en mulighed\
God praksis: Anvend imutable for at undgå at nøgler ændrer sig\

### Equals i java - er vigtig for at sammenligne nøgler

Krav: Der skal eksistere en <i>ækvivalensrelation</i> for nøglerne.. så vi kan anvende equals meningsfuldt (refleksiv, transitiv, symetrisk, ikke-null)\ 
I Java skal vi pga. klassehierakiet undersøge om objekterner er samme type, om objektet er det samme og om 

## Kode eksempler på anvendelse

```java
//Eksempel på en frequency counter

ST<Key, Value> st = new ST<Key,Value>();

while(!StIn.next()){
  Key   k = read.next();

  if(st.get(k) == null){
   st.put(k,1);
  }else{
   st.put(k, st.get(k) +1);
  }
}
 String max = "";
 st.put("max",0); //bruges kun første gang... vi kunne vel bare have sat en tilfældig nøgle istedet for "max"
 for(Key k: st.keys()){
   if(st.get(max) <st.get(k)){
       max = k; //sætter max til ny nøgle!!
   }
 }
 
 println("Max frequency:" + max + " " + st.get(max));

```

## Implementation kørselstid

- Ikke sorteret liste - f.eks. linked list implementation
    - WorstCase : opslag/insert N
    - Gennemsnit: opslag/insert N/2 og N (insert er altid N, da vi skal løbe alle elementer igennem)
    - key interface : equals
- Sorteret liste:
    - WorstCase : opslag/insert log2(N) og N </br>   (insert er i værste fald N, da vi i værste fald skal skubbe alle elementer hvis pladsen der skal insættes er 0)
    - Gennemsnit: opslag/insert log2(N) og N/2 </br>  (da arrayet er sorteret er tiden for insert N/2, da vi skal skubbe ellemeneter gennemsnitligt N/2)
    - key interface : compareTo

## Ordnede operationer

Ikke færdigt...

## Hash tabeller

Hashing er en funktion der skal oversætte vores nøgle til et heltal:\
```
  hash("it") = 3
  hash("its") = 3 //collision !!!
```

### Hash funktioner - og javas hash code
No space limit : brug hashing værdi som indeks
No time limit: collisioner med efterfølgende søgning
Space and Time limit: hashing real world

Ideal : 
 - nøgler skal fordeles ligeligt over alle tabel index
 - nemt at beregne

eksempel telefonnumre: telefonnumre bedre at bruge de sidste end de første tre ciffre \
eksempel java-hashcode: java hash-code returnere altid et 32-bit heltal - returnere som default objektets id \
eksempel java hashcode Integer: værdien \
eksempel java hashcode Double: bits^(bits>>>32) \
eksempel java hashcode String: for(all chars s) hash = s[i] + 31 * hash; (beregner den og gemmer den i en instans variable for performance)

Java gør det ikke rigtigt ??? bare oversætter til heltal???

### Konvertere hashcode til en hash funktion

Hash code: -2^31 og 2^31 -1 \
Hash funktion: 0 til M -1 hvor M er størrelsen på ens array

Vi kan fikse hash-code med Math.abs(hashCode) % M

Eksempel to-komplement signed integer
"polygenelubricants" giver 10000000000000000000000000000000 binært
for at konvertere til det modsatte inverterer man og lægger 1 til hvilket igen giver det samme!

Løses ved at fjerne det mest betydende bit.... dvs. hashCode & 07ffffffff % M\
dvs. den bit der repræsenterer de negative tal

### Fordeling af elementer i en hash - tabel

- Vi rammer samme spand efter ~ sqrt( PI * M / 2) kast

- Efter M * log2(M) kast inder holder hver spand mere end 1 bold

- Efter M kast indeholder den mest fyldte log2(M)/log2(log2(M))

https://youtu.be/s3nFlb-HNds?t=4725

hash-koden 




