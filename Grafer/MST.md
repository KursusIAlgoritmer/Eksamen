# MST - Minimum spanning tree

[minimum spanning tree intro](#greedy-algorithm-) : https://youtu.be/y3uMfjdUZTU \
greedy algorithm : https://youtu.be/GFogTNMOICM \
edge-weighted graf API : \
Kruskal's algorithm : \
Prim's algorithm : \
context : \

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

### Bevis:









 
