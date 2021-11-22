# DIGRAPH - directed graph

Intro til digraph: https://youtu.be/S1xKaQIxMRo \
digrah api: https://youtu.be/t6Gr8H2DvMI \
digraph search: https://youtu.be/fCUK6TjBAx0 \
topological sort: https://youtu.be/ha15d2TWnjI \
strong components: https://youtu.be/kR165jR0IpQ \

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
Topological Sort Algorithm | Graph Theory \
WilliamFiset
84.600 abonnenter \
Alternativ video: https://youtu.be/eL-KzMXSXXI

Sortering af Opgaver/Tasks hvor der er et forudbestemt krav til 
rækkefølgen.

Når man har fundet en topologisk rækkefølge er den ikke unik!
Der kan være en anden rækkefølge!

## Anvendelse
kursus "afhænighed" - kursus x kræver kusus xx\
## Virker kun på DAG : Directed acyclic graph

Kører dfs ??

Ny datastruktur anvendt - en stack til "postorder" ; \
postorder : Når knuder er færdige indsættes de i postorder.stakken


.....mangler
.....
.....

# Hvordan kan man finde cykler ???????

---
---

# Strongly Connected Components

Definition: Sti fra v til w og w til v.

( I en ikke-rettet graf for connected components - skal der være en sti fra v til w )

Man kan bruge DFS.

## Kosaraju-Sharir algoritmen

Intuition: \
Sammensætter strongly-components til knuder - og danner en DAG,- direct asyclic graph.
Hvis det ikke var en DAG, altså acyklisk, ville vi jo have en mere omfattende strongle-connected-component...

1. Vi laver først "topologisk sorteret stak"
2. Vi kører DFS på hver enkelt af knuderne i (1) og alle markerede knuder er en komponent!




