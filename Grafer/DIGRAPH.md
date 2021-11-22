# DIGRAPH - directed graph

Intro til digraph: https://youtu.be/S1xKaQIxMRo \
digrah api: https://youtu.be/t6Gr8H2DvMI \
digraph search: https://youtu.be/fCUK6TjBAx0 \
topological sort: https://youtu.be/ha15d2TWnjI \
strong components:

---

## intro to digraph

Vi to typer degrees : indegree og outdegree

## Anvendelser
ensrettet vejnet \
lån imellem banker \
elektriske kredsløb \

---

## problemer
Er der en vej \
Kortest vej \
Topological sort ???? \
Strong connectvity - er der en sti imellem alle par af knuder??? \
Transitive closure - for hvilke knuder er der en sti imellem v og w \
Page rank - betydning af webpage 

---

# DIGRAPH API -

samme design pattern som for ikke orientered graf
Nye metoder \
<b>addEdge</b> : peger i en bestem retning \
<b>reverse</b> : 

Der er kun en ændring af koden ift. ikke orienterede grafer er addEdge:
For ikke orienterede grafer skal en forbindelse/kant til føjes to steder. For en orienteret kun et sted!

---

# DIGRAPH SEARCH  - DFS ...

Vi bruger dfs nøjagtigt på samme måde!

## Anvendelser

Alle program eksekveringer kan betragtes som en orienteret graf \
Vigtige undersøgelser her er: \
"Unreachable code" \
"inifinit loop" \

Garbage Collection : \
Det er en såkaldt mark-sweep algoritme: \ 
Vertex er objekter \
Edge er referencer \

## Anvendelser DFS
Reachability \
Path findeing \
Topological sort \
Directed cycle detection \

## DFS digraph kan løse svære problemer som
2-staticfiabliity \
directed euler path \
strong connected components 

---

# BFS - exactly same as undirected graph

Et andet problem (ikke specielt for rettet graf) : \
Multiple source shortest path

Metode : indsætter alle start-knuder i køen!

---

# Topological sort
tasks presedence constraints 
## Anvendelse
kursus "afhænighed" - kursus x kræver kusus xx\
## Virker kun på DAG : Directed acyclic graph

Kører dfs ??

Ny datastruktur anvendt - en stack til "postorder" ; \
postorder : Når knuder er færdige indsættes de i postorder.stakken


.....mangler
.....
.....
