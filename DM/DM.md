---
title:  'Diskrete  Mathematik Zusammenfassung'
author:
- Manuel Strenge
keywords: [DM, pain]
...

# Grundbegriffe und elementare Logik

## Aussagen, Prädikate und Quantoren

**Aussage** 

Bei einer Aussage versteht man ein sprachliches Gebilde (Satz), der zumindest im Prinzip ein Wahrheitswert «wahr» oder «falsch» zugeordnet werden kann. Bsp.: “Esel haben lange Ohren.” (wahr)

**Prädikat**

Es sei n eine natürliche Zahl. Ein sprachliches Gebilde, in dem n viele Variablen (frei)
vorkommen und das bei Belegung aller (freien) Variablen in eine Aussage übergeht, nennen **wir ein n-stelliges Prädikat. Aussagen sind 0-stellige Prädikate.**
Bsp.: $P(p) :=$ “p ist eine Primzahl.”

**Junktoren**

Zeichen                 Übersetzung
----------              --------------
$\neg A$                Nicht A
$A \wedge B$            A und B
$A \vee B$              A oder B
$A \Rightarrow  B$      A impliziert B
$A \Leftrightarrow  B$  A äquivalent B

Die Aussagen ‘Es gibt Einhörner’ $\Rightarrow$ ‘8 ist eine Primzahl’ und ‘Spinat ist grün’ $\Rightarrow$ ‘2 ist eine Primzahl’ sind beide (mathematisch gesehen) wahr.

**JUNKTOREN-REGELN:**

Zeichen                                                                 Name
---------------------------------                                       ------------------
$\neg\neg A \Leftrightarrow A$                                          Regel der doppelten Negation
$A \wedge B \Leftrightarrow B \wedge A$                                 Kommutativität
$A \vee B \Leftrightarrow B \vee A$         
$(A \wedge B) \wedge C\Leftrightarrow A \wedge (B \wedge C)$            Assoziativität
$(A \vee B) \vee C\Leftrightarrow A \vee (B \vee C)$
$A \wedge (B \vee C) \Leftrightarrow (A \wedge B) \vee (A \wedge C)$    Distributivität
$A \vee (B \wedge C) \Leftrightarrow (A \vee B) \wedge (A \vee C)$
$\neg (A \wedge B) \Leftrightarrow  \neg A \wedge \neg B$               Regeln von De Morgan
$\neg (A \vee B) \Leftrightarrow  \neg A \vee\neg B$

**KONTRAPOSITION JUNKTOREN-REGEL**

Gleichung                                   Beschreibung
-------------------------------             ----------------------------------------------------------------
$A \Rightarrow B$                           - 
$\neg A \vee B$                             (Definition von $A \Rightarrow B$ )
$\neg\neg (\neg A \vee B)$                  (Doppelte Negation)
$\neg (\neg\neg A \wedge \neg B)$           (De Morgan)
$\neg (A \wedge \neg B)$                    (Doppelte Negation)
$\neg (\neg B \wedge A)$                    (Kommutativität)
$\neg \neg B \wedge \neg A$                 (De Morgan)
$\neg B \Rightarrow\neg A$                  (Definition von $\neg B \Rightarrow\neg A$ )



**QUANTOREN**

Kurz: $\forall =$ All, $\exists =$ mind. 1 $\exists! =$ es gibt genau 1

Symbol                          Beschreibung
---------------------           ----------------------------------------------------------------
$\forall x A(x)$                Für alle x gilt A(x)) trifft genau dann zu, 
                                wenn A auf jedes (mathematische) Objekt zutrifft.
$\forall x \in M A(x)$          Für alle x aus M gilt A(x)) trifft genau dann zu,
                                wenn A auf jedes Element aus M zutrifft. 
$\exists x A(x)$                Es gibt ein x mit A(x)) trifft genau dann zu,
                                wenn es (mindestens) ein Objekt gibt, auf welches A zutrifft. 
$\exists x \in M A(x)$          Es gibt ein x aus M mit A(x)) trifft genau dann zu, 
                                wenn es (mindestens) ein Element aus M gibt, auf welches A zutrifft.


Die Symbole $\forall$ und $\exists$ heissen Allquantor und Existenzquantor

$\forall x \forall y A(x,y) \Leftrightarrow \forall x,y A(x,y)$

**QUANTOREN-REGEL**

Regel                                                                                   Beschreibung 
---------------------------------------------------------------------------             ----------------------------------------------------------------
$\forall x A(x) \Leftrightarrow \neg \exists x \neg A(x)$                               Vertauschungsregel für unbeschränkte Quantoren
$\forall x \in K A(x) \Leftrightarrow \neg \exists x \in K \neg A(x)$                   Vertauschungsregel für beschränkte Quantoren
$\forall x \in K A(x) \Leftrightarrow \forall x(x \in K \Rightarrow A(x))$              Beschränkter und unbeschränkter Allquantor
$\exists x \in K A(x) \Leftrightarrow \exists x(x \in K \wedge A(x))$                   Beschränkter und unbeschränkter Existenzquantor

**Warnung:** Wir haben keine Distributionsregel mit Quantoren und Junktoren.

Gleichung                                                   Beschreibung
-------------------------------------------------           ---------------------------------------
$\exists x A(x)$                                        
$\Leftrightarrow \neg \neg \exists x A(x)$                  (Doppelte Negation)
$\Leftrightarrow \neg (\neg \exists x A(x))$                 
$\Leftrightarrow \neg (\neg \exists \neg( \neg x A(x)))$    (Doppelte Negation)
$\Leftrightarrow \neg (\forall \neg  x A(x))$               (Vertauschungsregel)


## Grundlegende Beweistechniken

### Direkter Beweis einer Implikation

**Problemstellung:** Es gilt eine Aussage $A \Rightarrow B$

**Lösungsstrategie:** Wir geben, basierend auf der Annahme, dass A wahr ist, zwingende
Argumente für die Richtigkeit von B.

### Beweis durch Widerspruch

**Problemstellung:** Es gilt eine Aussage A zu beweisen

**Lösungsstrategie:** Nehmen Sie an, die Aussage A wäre falsch und benützen Sie diese
Annahme, um einen Widerspruch herzuleiten. Leiten Sie also unter der Annahme der
Falschheit von A eine Aussage her von der bereits bekannt ist, dass sie falsch ist oder im
Widerspruch zur Annahme steht.

### Beweis durch (Gegen-) Beispiel

**Problemstellung:** Es gilt zu zeigen, dass eine bestimmte Eigenschaft nicht auf alle Objekte (aus einem Kontext) zutrifft.

**Lösungsstrategie:** Geben Sie konkret ein Objekt an, welches die erwähnte Eigenschaft nicht besitzt. Bsp.: «Nicht jede natürliche Zahl ist eine Quadratzahl.»

### Beweis durch Kontraposition

**Problemstellung:** Es gilt eine Aussage von der Form $A \Rightarrow B$ zu beweisen.

**Lösungsstrategie:** Beweisen Sie die Kontraposition $\neg A \Rightarrow \neg B$

### Beweis einer Äquivalenz

**Problemstellung:** Es gilt eine Aussage von der Form $A \Leftrightarrow B$ zu beweisen.

**Lösungsstrategie:** Beweisen Sie  $B \Rightarrow A$ sowie  $A \Rightarrow B$.

# Syntax und Semantik am Beispiel der formalen Aussagenlogik

## Syntax der Aussagenlogik

* Konstanten $T$ und $\perp$.
* Variablen $p, q, r, s, ... , p_{0}, p_{1}, p_{2}, ...$
* Klammern $(,)$
* Junktoren $\neg, \wedge, \vee, \Rightarrow$
* Die Menge der Variablen Bezeichnen wir mit $\mathbb{V}$ 
* Die Menge der aussagelogischen Formeln Bezeichnen wir mit $\mathbb{F}$


**Definition 8.** Es sei eine Belegung $B$ gegeben. Die Funktion $\widehat{B}$ ist die Funktion, die
jeder aussagenlogischen Formel ihren Wahrheitswert bezüglich der Belegung $B$ zuordnet,
d.h. die Funktion $\widehat{B} : F \rightarrow  \{false,true\}$ ist gegeben durch:

- $\widehat{B}(\perp) = false$ und $\widehat{B}(T) = true$
- Für beliebige Variablen $v$ gilt $\widehat{B}(v) = B(v)$ .
- Für beliebige Formeln F und G gilt
    * $\widehat{B}(F \wedge G)=\left\{\begin{matrix}true & falls\:  \widehat{B}(F) = true\:  und\: \widehat{B}(G) = true \\ false & sonst.\end{matrix}\right.$
- Für beliebige Formeln $F$ und $G$ gilt
    * $\widehat{B}(F \vee G)=\left\{\begin{matrix}true & falls\:  \widehat{B}(F) = true\:  und\: \widehat{B}(G) = true \\ false & sonst.\end{matrix}\right.$
- Für beliebige Formeln $F$ gilt
    * $\widehat{B}( \neg F )=\left\{\begin{matrix}true & falls\:  \widehat{B}(F) = false\\ false & sonst.\end{matrix}\right.$
- Für beliebige Formeln $F$ und $G$ gilt $\widehat{B}(F \rightarrow G) = \widehat{B}(\neg F \vee G)$.

## Semantik der Aussagenlogik

### Wahrheitstabellen 

In einer Wahrheitstabelle einer Formel $F$ entspricht jede Spalte einer Teilformel von $F$ und jede Zeile einer Belegung der in $F$ vorkommenden Variablen. Bsp.:

Wahrheitstabelle von $p_{0} → (q \wedge p_{1})$ :


$p_{0}$ $q$ $p_{1}$ $q \wedge p_{1}$    $p_{0} \rightarrow (q \wedge p_{1}$
------- --- ------- ----------------    -----------------------------------
0       0   0       0                   1
0       0   1       1                   1
0       1   0       1                   1
0       1   1       1                   1
1       0   0       0                   0
1       0   1       1                   1
1       1   0       1                   1
1       1   1       1                   1

Man kann Wahrheitstabellen auch zur Darstellung von logischen Operatoren $^{2}$ benützen. Beispielhaft geben wir die Wahrheitstabellen für die Operatoren
(Junktoren) $\wedge, \vee, \rightarrow, \neg$ an.

$F$ $G$ $F\wedge G$
--  --  ----    
0   0   0
0   1   0
1   0   0
1   1   1

$F$ $G$ $F\vee G$
--  --  ----    
0   0   0
0   1   1
1   0   1
1   1   1

$F$ $G$ $F\rightarrow G$
--  --  ----    
0   0   1
0   1   1
1   0   0
1   1   1

$F$ $\neg F$
--  -------
0   1
1   0


### Semantische Eigenschaften

Eine aussagenlogische Formel A heisst

- *Gültig* oder wahr unter einer Belegung $B$, falls $\neg B(A) = true$.
- *Allgemeingültig*, wenn sie unter jeder Belegung gültig ist.
- *Widerlegbar*, wenn es mindestens eine Belegung gibt, unter der $A$ nicht gültig ist.
- *Erfüllbar*, wenn es mindestens eine Belegung gibt, unter der $A$ gültig ist.
- *Unerfüllbar*, wenn $A$ nicht erfüllbar ist.

Es seien $F$ und $G$ beliebige aussagenlogische Formeln. Wir sagen

- $F$ ist eine Konsequenz von $G$, falls $F$ unter jeder Belegung wahr ist unter der $G$ wahr ist.
- $F$ und $G$ sind logisch äquivalent, wenn $G$ und $F$ unter jeder Belegung denselben Wahrheitswert annehmen.

Sind $F$ und $G$ äquivalente Formeln, dann schreiben wir $F \equiv G$.

Beispiele:

**Allgemeingültig Formeln**

$$p \vee \neg p \qquad p \rightarrow (p\rightarrow p) \qquad F \rightarrow F$$

**Erfüllbare nicht allgemeingültige Formeln**

$$p_{1} \wedge (p_{2} \wedge p_{3}) \qquad p{3} \qquad p \rightarrow q $$

**Unerfüllbare Formeln**

$$(p_{1} \rightarrow \neg p_{1})  \wedge (\neg p_{1} \rightarrow p_{1}) \qquad \neg p_{3} \wedge p_{3}\qquad \neg(F\rightarrow F)$$

### NORMALFORMEN NNF | DNF | KNF

Literale sind atomare Formeln oder negierte atomare Formeln.

Eine aussagenlogische Formel ist:

* In Negationsnormalform(NNF), wenn alle Negationen in Literalen vorkommen und wenn keine Implikationen ($\rightarrow$) vorkommen.

* In disjunktiver Normalform(DNF), wenn sie von der Form $$(L_{1,1} \wedge L_{1,2} \wedge ...) \vee (L_{2,1} \wedge L_{2,2} \wedge ...) \vee (L_{3,1} \wedge L_{3,2} \wedge ...)...$$ mit Literalen $L_{i,j}$ ist.

* In konjunktiver Normalform(KNF), wenn sie von der Form $$(L_{1,1} \vee L_{1,2} \vee ...) \wedge (L_{2,1}\vee L_{2,2} \vee ...)\wedge (L_{3,1} \vee L_{3,2} \vee ...)...$$  mit Literalen $L_{i,j}$ ist.


$$\neg(p \vee q)$$

ist in keiner der oben eingeführten Normalformen. Die Formel

$$(\neg p \vee q) \wedge ((p\wedge p_{1}) \vee (p_{2} \wedge p_{3})) $$

ist in NNF aber weder in DNF noch in KNF. Die Formel

$$p \vee q$$

ist in NNF, KNF und DNF.

# Mengen, Relationen und Funtionen

Formel                                                                                                                                  Beschreibung
-------------------                                                                                                                     ---------------------------------
$A \cup B = B \cup  A$  und                                                                                                             Kommutativität der Vereinigung und des Schnittes
$A \cap B =  B \cap A$
$A \cap  (B \cap C) = (A \cap B) \cap C$  und                                                                                           Assoziativgesetze von Schnitt und Vereinigung
$A \cup  (B \cup C) = (A \cup B) \cup C$
$A \cap  (B \cup C) = (A \cap  B) \cup (A \cap  C)$ und                                                                                 Distributivgesetze von $\cap$ mit $\cup$
$A \cup (B \cap  C) = (A \cup B) \cap   (A \cup C)$
$A \cap  A = A \;  und \;   A \cup  A = A$                                                                                              Idempotenzgesetz
$(C \setminus A) \cap (C \setminus B) = C \setminus (A \cup  B)$ und                                                                    Regeln von DeMorgan
$(C \setminus A) \cup  (C \setminus B) = C \setminus (A \cap B)$


## Der Mengenbegriff und grundlegende Definitionen

Symbol          Definition
---             ---
$y \in  X$      X ist eine Menge und y ein Element von X
$y \notin X$    y ist kein Element von X

### DEFINIERENDE EIGENSCHAFT

$X = Y \Leftrightarrow \forall z (z \in X \Leftrightarrow z \in Y)$ Zwei Mengen sind genau dann gleich, wenn sie die gleichen Elemente enthalten: Es gilt für alle Mengen X und Y die Äquivalenz.

### Explizite Schreibweise

![Wichtige Zahlenmengen](./dm_files/Screenshot%202023-01-07%20171042.png){ width=50% }

Bezeichnung                                                                 Formel
------------                                                                -------------------
Sind mathematische Objekte x1, . . . , xn gegeben, dann schreiben wir       $\{x_{1}, . . . , x_{n}\}$
$\mathbb{N}$                                                                $\{0, 1, 2, 3, …\}$
$\mathbb{Z}$                                                                $\{…, -2, -1, 0, 1, 2, …\}$

### Teilmengen

![Veranschaulichung der Mengenbildung durch prädikative Schreibweise.](./dm_files/Screenshot%202023-01-07%20180117.png){ width=50% }

Zeichen         Beschreibung                            Equivalent
-----------     -------------                           -------------
$x\subseteq Y$  X ist eine Teilmenge von Y,             $X \subseteq  Y :\Leftrightarrow  \forall x (x \in  X \Rightarrow  x \in  Y)$
                wenn jedes Element von X auch 
                ein Element von Y ist.
$x\subsetneq Y$ X ist eine echte Teilmenge von Y        $X \subsetneq  Y :\Leftrightarrow  X \subseteq  Y \wedge  X \neq  Y$
                , falls X eine von Y 
                verschiedene Teilmenge von Y ist. 

### PRÄDIKATIVE SCHREIBWEISE

$X$ ist eine Menge und $E$ eine Eigenschaft (Prädikat). Die Menge aller Elemente $z$ von $X$ mit der Eigenschaft $E(z)$

$$\{ z \in X | E(z) \} \; oder \; \{ z | z \in  X \wedge  E(z) \}$$

### ERSETZUNGS-SCHREIBWEISE

Ist F eine Funktion und ist X eine Menge, dann beinhaltet die Menge

$$\{ F (x) | x  \in X \}$$

### VEREINIGUNG

Sind X und Y Mengen kann ich sie vereinigen:

$$X \cup Y := \{ x | x \in X \vee x \in Y \}$$

Ist $I$ eine Menge so, dass für alle Elemente $i \in I$ auch Ai eine Menge ist, dann ist die Vereinigung von ${ A_{i} | i \in I }$

$$\bigcap_{i\in I}^{} A_{i}:= \{ x | \exists i \in I (x \in A_{i})\}$$

## Relationen, Funktionen und Graphen

### Funktionen

### Grössenvergleiche von unendlichen Mengen

### Ordnungs- und Äquivalenzrelationen

# Rekursive Strukturen und die natürlichen Zahlen

## Die grundlegende Struktur der natürlichen Zahlen

## Vom Induktionsbeweis zum rekursiven Algorithmus

## Rekursive Definitionen

# Elementare Zahlentheorie 

## Teilbarkeit und Euklidischer Algorithmus

## Primzahlen

## Modulare Arithmetik

### Chinesicher Restsatz