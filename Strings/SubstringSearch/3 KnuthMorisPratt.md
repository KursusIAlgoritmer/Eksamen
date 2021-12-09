# 3 Knuth Morris Pratt

https://youtu.be/J_b3uhkZK2Q

Der er en string og en sub-string der skal findes

flytter en pointer for at matche hver karakter i stringen med substring

Det smarte er når det første mis-match nåes ved man de andre er matched...

---

bygger en tilstandsmaskine

hvis man når alle tilstande igennem har vi et match!

---

KMP vs Brute Force, pointer never decrements

---

## hvordan opbygges den nødvendige DFA - Difinit finite state automaton

Seatching for ABABAC
<pre>
  0 1 2 3 4 5
  A B A B A C
A 1 1 3 1 5 1
B 0 2 0 4 0 4
C 0 0 0 0 0 6
</pre>
Systematisk konstruktions process

---

## Tidskompleksitet

- Konstruktion af DFA tager R*M hvor R er radix og M er substreng længden
- Søgning tager derimod højest N + M hvor N er den streng der søges i
