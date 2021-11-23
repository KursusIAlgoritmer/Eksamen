# MST - Minimum spanning tree

***[minimum spanning tree intro](#greedy-algorithm-) :***  \
https://youtu.be/y3uMfjdUZTU

***[greedy algorithm](#greedy-algorithm-) :*** \
https://youtu.be/GFogTNMOICM

***[edge-weighted graf API](#edge-weighted-graf-api) :*** \
https://youtu.be/Sfy4ywbtVIM

***[Kruskal's algorithm](#kruskals-algorithm)*** \
https://youtu.be/_Pdp9lVAmpk

***Prim's algorithm :***

***context :***

---

# Introduktion til MST

### Interessant fordi : 
Kombinerer mange forskellige algoritmer med forskellige data strukturer.

### Definintion - spaning tree: 
Subgraf der er acyclisk og forbinder alle knuder

### Definintion - mst
Mindste spaning tree, af en vægtet graf

### Anvendelser :
- Mange fysiske fæomener kan beskrives som MST
- Medical ??
- Billede processering - fjerne fuzzynes ??

---

# Greedy algorithm :

### Antagelser:
- vægte er unikke
- grafen er forbundet

### Konsekvens:
- mst eksisterer og er unik

#

### Cut - Definition:
Et cut er en partitionering af grafeb i to ikke tomme sæt!

### Crossing edge . definition:
Forbinder en knude i et sæt med en knude i et andet

#

### Påstand : Cut - egenskab 
Enhver mindste "crossing edge" må være i MST! 

### Bevis:
- vi har en mst
- vi har en mindste crossing edge e som ikke er mst
- hvis vi tilføjer e til mst , hvillket giver en cykel
- derfor må der være en kant f, der er en crossing edge!!
- fjernelse af f vil give en mst !! Men mindre !!! OMG

Dette er en selvmodsigelse - der beviser ovenstående påstand

#

### Algoritmen

- start med alle kanter ikke markerede
- find et "cut" uden markering! Find minimum "crossing edge" og marker denne
- gentag ovenstående indtil der ikke er flere kanter at markere

#

### Påstand - the greedy algorithm finder mst

### Bevis: ???
- alle markerede kanter er i mst
- mindre end V-1 markerede kanter (dvs. færre markerede kanter end knuder ) =>  så er der et cut uden overgang!
- ???

#

Hvad sker der hvis vægte ikke er unikke - det betyder bare at der er flere MST... 

Hvad sker der hvis knuder ikke er forbundne - det betyder vi får en MST skov! ...

---

# edge weighted graf api 

Vi tilfører en klasse kaldet Edge,- da den nu indeholder en vægt
Metoder: \
- Edge(v,w,weight) :
- either() : et af endeknuder
- other(v) : den anden af de to endenknuder
- comparTo(otherEdge) : 
- weight() 


---

# kruskals algorithm

- kanter sorteres i vægtet rækkefølge
- hver kant fra den mindste, vælges 
 - hvis kanten laver en cykel ignoreres den

#

### Påstand : 
Kruskals algoritmen finder MST

### Bevis : 
Specielt case of greedy algoritme
- hvis k.a. vælger en kant e = v-w
- vælg et cut = set af knuder forbundet til v
- ???

#

### Problem : Hvordan ved man om der er en cykel?
- kør DFS og se om v er forbundet til w. 
- anvend union-find
  - der bygges en union-find der bruges til at tjekke om knuderne er i samme komponent


# 

### Implementation
- Anvender priority queue til at vælge den mindste 
- Anvender union-find til at tjekke om knuderne er i samme kmponent

#

### Runing time E*log(E) ...










 
