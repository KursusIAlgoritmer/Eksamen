# DFS

Time Complexity of Depth First Search (DFS) Algorithm: \
https://youtu.be/bP3MWJHeohc

DFS-algo:
- sætter besøgt knude v til true
- vælger alle tilstødende knude v_x til v <i> (dette er antallet af kanter eller for rettet graf , kanter væk fra knuden!!!) </i>
     - for hver tilstøde v_x endnu ikke besøgt starter vi (1.)

Time Complexity: O(V+E)

---

## Robert Sedgwick's video om DFS:

https://youtu.be/Uj6lQWBU6jk

Design Pattern for Graph processing:

 1. Lav graf objekt
 2. Processer grafen med en rutine
 3. Forspørg rutinen for information

VIGTIGT : Vi afkobler grafen fra processen  ...

DFS-algo:
 - Marker knude v
 - Rekursivt besøg alle knuder v_x tilsødende til v
    - "edgeTo" list opdateres ... edgeTo[v_x] = v

Maalet: \
Vi kan nu via edgeTo gå baglæns og finde veje fra v til andre knuder i edgeTo!! \
Vi kan se alle knuder hvor der er en sti til v \

Data strukturer: \
list af markerede knuder \
list af sammenhængende knuder index <-> indhold \

---

PÅSTAND: 

DFS vil markere alle knuder der kan nåes fra en knude v, <b> i en tid propertionel til deres grad... </b>

BEVIS: 

HVis w er forbundet til s, er w markeret \
hvis er w ikke var markeret, så betragt den sidste kant på stien fra s til w, der går fra en markeret til ikke markeret??!!

---

PÅSTAND: 
 1. DFS kan finde knuder forbundet til s i konstant tid?
 2. Og kan finde en sti i tid propertionel til stiens længde...

BEVIS:
 1. markerede array - viser hvilke knuder der kan nåes - opslag er konstant
 2. sammenhængende knuder array - kan backtrackes ... hvilket koster "sti længde" tid

---


