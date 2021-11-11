# Grafer

## Computer Science - Robert Sedgwick:

introductions to graphs: https://youtu.be/flhgfYu8DFo \
graph api : https://youtu.be/NnBk8inSgqY \
depth first search : https://youtu.be/Uj6lQWBU6jk \
breath first search : https://youtu.be/2dFFKJM0j1E \
connected components : https://youtu.be/BYIz7jJ-VA4 \
challenges : https://youtu.be/OD2-Ovpx6tc \

## introduktion
<b>Termer:</b>\
ikke rettet graf: \
knuder, kanter, sti, cykel

<b>Typiske graf problemer:</b> \
Er der er sti imellem to knuder \
Hvad er den korteste sti? 

Er der en cykel på grafen \
Er der en cykel der rammer alle kanter én gang - Euler tur \
Er der en cykel der rammer alle knuder én gang - Hamilton tur 

Er det muligt at forbinde alle knuder \
Er der en beste ( mindst kost ) måde at forbinde alle knuder på - MST ? \
Er der en knude der opdeler grafen ? Biconnectivity ?

Kan tegnes i planet uden kanter krydser \
Er der to "adjacency lists" for samme graf - isomorfi ?

<i>Hvad er sværhedgraden for de forskellige problemer</i>

## Graf API

knuder er heltal imellem 0 og V-1 \

Graph API \
------------------- \
Graph(int V)\
Graph(In in)\
void addEdge(int v, int w)\
Iterable<Integer> adj(int v)\
int V()\
int E()
  
Typhical graf-processing kode \
------------------- \
degree of v: hvor mange knuder er tilstødende til v \
maxDegree of G: knude med højest grad \
gennemsnits degree : 2 * G.E() / G.V() \
number of self loops : ...

## Repræsentationer 
  
1 linked list repræsentation, node for hver kant 
  * ikke hensigtsmæssig ?
  
2 adjacency matrix repræsentation, VxV array
  * fylder virkelig meget !
  
3 adjacency-list graph repræsentation, knude indexed array af lister
  * plads forbrug er propertionelt med entries - faktisk er det O(V + E) ??
  * I verkeligheden er grafer "sparse" og ikke "dense" ... derfor sparer vi plads sammenlignet med f.eks. 2
  
  
  
  
  


  


  
  









