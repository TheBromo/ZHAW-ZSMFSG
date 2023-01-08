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

**Junktoren-Regeln**

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

**Kontraposition Junktoren-Regel**

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



**Quantoren**

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

**Quantoren-regel**

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

$F$ $G$ $F\wedge G$ $F\vee G$   $F\rightarrow G$
--  --  ----        ----        --------
0   0   0           0           1
0   1   0           1           1
1   0   0           1           0
1   1   1           1           1


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

### Normalformen NNF | DNF | KNF

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

### Definierende Eigenschaft

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

### Prädikative schreibweise

$X$ ist eine Menge und $E$ eine Eigenschaft (Prädikat). Die Menge aller Elemente $z$ von $X$ mit der Eigenschaft $E(z)$

$$\{ z \in X | E(z) \} \; oder \; \{ z | z \in  X \wedge  E(z) \}$$

### Ersetzungs-schreibweise

Ist F eine Funktion und ist X eine Menge, dann beinhaltet die Menge

$$\{ F (x) | x  \in X \}$$

### Vereinigung

Sind X und Y Mengen kann ich sie vereinigen:

$$X \cup Y := \{ x | x \in X \vee x \in Y \}$$

die Vereinigung von $X$ mit $Y$ . Die Schnittmenge von $X$ und $Y$ ist durch

$$X \cap  Y := {x \in X | x \in Y } = \{ x \in Y | x \in X \} = \{x | x \in X \wedge  x \in Y \}$$

Ist $I$ eine Menge so, dass für alle Elemente $i \in I$ auch Ai eine Menge ist, dann ist die Vereinigung von ${ A_{i} | i \in I }$

$$\bigcap_{i\in I}^{} A_{i}:= \{ x | \exists i \in I (x \in A_{i})\}$$

die Vereinigung von $\{A_{i}| i \in I\}$ genannt. Analog dazu, ist die Schnittmenge durch

$$\bigcap_{i \in I}^{} A_{i} := \{ x \forall i \in  I ( x \in A_{i} ) \} $$

gegeben, falls $I \neq \varnothing$ ist.

### Disjunkt

Zwei Mengen $X$ und $Y$ heissen disjunkt, falls sie keine gemeinsamen
Elemente haben, d.h. falls $X \cap Y = \varnothing$ gilt. Wir sagen eine Menge $\{X_{i}| i \in I\}$ von
Mengen bestehe aus paarweise disjunkten Mengen, wenn folgendes gilt:

$$\forall i , j \in I (i \neq j \Rightarrow X_{i} \cap X_{j} = \varnothing)$$

### Paarweise Disjunkt

Wir sagen eine Menge $\{ X_{i} | i \in I \}$ von Mengen bestehe aus paarweise disjunkten Mengen, wenn folgendes gilt:

$$\forall i, j \in I ( i \neq j \Rightarrow  A_{i} \cap A_{j} = \varnothing)$$

![Visualisierung](./dm_files/Screenshot%202023-01-07%20223613.png){ width=50% }

### Schnittmenge

Sind X und Y Mengen kann ich die Schnittmenge so ziehen $X \cap Y := \{ x | x \in X \wedge x \in Y \}$

Analog zur Vereinigung, aber mit Allquantor ist die Schnittmenge gegeben, falls $I \neq \varnothing$ ist.

$$\bigcap_{i \in I}^{} A_{i} := \{ x \forall i \in  I ( x \in A_{i} ) \} $$

### Differenzmenge

Sind $X$ und $Y$ beliebige Mengen, so definieren wir die Menge aller Elemente von $X$, die nicht zu $Y$ gehören:

$$X \setminus  Y := \{ x \in X | x \notin  Y \}$$

Bsp.: Die Menge ungerader Zahlen können wir als $\mathbb{N} \setminus  \{ 2x | x \in \mathbb{N} \}$  schreiben.

### Potenzmenge

Ist $A$ eine beliebige Menge, so bezeichnen wir die Potenzmenge von $A$, die genau die Teilmengen von $A$ als Elemente enthält, wie folgt

$$\mathcal{P} :=\{ x | x  \subseteq A\}$$

Beispiel:

$$\mathcal{P}(\varnothing) =\{\varnothing\} \neq \varnothing $$
$$\mathcal{P}(\{0,1\}) =\{\varnothing\,\{0\},\{1\},\{0,1\} \} $$

### Rechenregeln

Kommutativität der Vereinigung und des Schnittes:

$A \cup B = B \cup A$ und $A \cap B = B \cap A$.

Assoziativgesetze von Schnitt und Vereinigung:

$A \cap (B \cap C) = (A \cap B) \cap C$ und $A \cup (B \cup C) = (A \cup B) \cup C$

Distributivgesetze von $\cap$ mit $\cup$:

$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$ und $A \cup (B \cap C) = (A \cup B) \cap (A \cap C)$

Idempotenzgesetz:

$A \cap A = A$ und $A \cup A = A$

Regeln von DeMorgan:

$(C\setminus A) \cap (C\setminus B) = C\setminus(A \cup B)$ und $(C\setminus A) \cup (C\setminus B) = C\setminus(A \cap B)$

## Relationen, Funktionen und Graphen

(Tupel). Es sei $n > 0$ eine natürliche Zahl. Ein n-Tupel ist ein Term von
der Form

$$x_{1},...,x_{n}$$

Für beliebige Tupel gilt:

$$(x_{1}, ... , x_{n}) = (y_{1}, ... y_{k}) :\Leftrightarrow n = k \wedge x_{1} = y_{1} \wedge ... \wedge y_{n} = x_{n}$$

2-Tupel nennen wir *Paare* und 3-Tupel *Tripel*

**Kartesische Produkte**

Die Gesamtheiten aller Tupel mit Elementen aus einer oder mehreren Mengen nennt man kartesische Produkte.

Es seien $A_{1}, ... , A_{n}$ Mengen und $n \in \mathbb{N} mit n > 0$. Das kartesische
Produkt von $A_{1}, ... , A_{n}$, ist die Menge aller $n$-Tupel mit Einträgen aus den Mengen
$A_{1}, ... , A_{n}$:

$$\prod_{i=1}^{n}A_{i}=\{(a_{1},...,a_{n})|a_{1}\in A_{1}\wedge \cdots \wedge a_{n} \in A_{n}\}$$

Bsp.:
Geg.: $A = \{a, b, x, y\}$ und $B = \{x, y\}$
$(B \times  (A \setminus  B)) \times \{3\}$
Lösung: $$\{(x, y) \times (a, b)\} \times \{3\}
\{(x, a), (x, b), (y, a), (y, b)\} \times \{3\}
\{(x, a, 3), (x, b, 3), (y, a, 3), (y, b, 3)\}$$

**Relationen**

Eine n-stellige Relation $R$ auf den Mengen $A_{1},..., A_{n}$ ist eine Menge von n-Tupeln aus $A_{1} \times ... \times A_{n}$. Die Relation auf $A_{1}, ..., A_{n}$ sind genau die Teilmengen:

$$R\subseteq A_{1}\times ... \times A_{n}$$

Ist $R$ eine n-stellige Relation und gilt $(x_{1}, ... , x_{n}) \in R$, dann sagen wir, dass die Elemente $x_{1}, ... , x_{n}$ zueinander in Relation $R$ stehen

### Graphen

**Relationsgraphen**

$R = \{(x, y) | x, y \in N \wedge x, y < 100 \wedge x + y$ ist ein Vielfaches von $7\}$ ![Visualisierung](./dm_files/Screenshot%202023-01-08%20000346.png){ width=50% }

**Gerichteter Graph**

Ein (gerichteter) Graph ist ein Paar $G = (V,E)$ bestehend aus einer Menge $V$ (Knotenmenge) und einer binären Relation $E \subseteq V \times V$ (Kantenmenge).

$V = \{1, 2, 3, 4\} E = \{(1, 1),(1, 2),(1, 3),(1, 4),(2, 2),(2, 4),(3, 3),(4, 4)\}$

![Visualisierung](./dm_files/Screenshot%202023-01-08%20001105.png){ width=50% }

### Funktionen

Es seien $A$ und $B$ beliebige Mengen. Eine Relation $f \subseteq  A \times B$ ist eine Funktion von $A$ nach $B$, falls:

$$\forall x \in A \exists! y \in B((x, y) \in f)$$

gilt. In diesem Fall schreiben wir

$$f : A\rightarrow  B.$$

Sind $f : A\rightarrow  B$ und  $f : B\rightarrow  C$ Funktionen, dann ist die Komposition
$g$ nach $f$ durch

$$g  \circ f : A\rightarrow C$$
$$(g  \circ f)(x) = g(f(x))$$

gegeben.

Eine Funktion $f$ ist genau dann injektiv, wenn die Relation

$$f^{-1} = \{(y,x)|(x,y)\in f\}$$

eine Funktion ist. Ist $f : A \rightarrow B$ eine injektive Funktion, dann nennt man $f^{-1} : Im(f)\rightarrow A$ die Umkehrfunktion oder inverse Funktion von $f$.

**Injektiv**

Eine Funktion, die injektiv ist, hat für jedes x genau ein y und für jedes y genau ein x.

**Surjektiv**

Wenn von x auf alle y von B gekommen werden kann.

**Bijektiv**

Wenn eine Funktion Injektiv und Surjektiv ist, dasnn ist sie bijektiv



Surjektivität und Injektivität lassen sich gut anhand von “Gegenbeispielen” veranschaulichen. Ist die Funktion $f : A \rightarrow B$ durch

![Visualisierung](./dm_files/Screenshot%202023-01-08%20003726.png){ width=50% }

* Die Funktion ist wegen $f(x_{1}) = f(x_{3})$ nicht injektiv.
* Die Funktion ist wegen $y_{4} \in B$ nicht surjektiv auf $B$.
* Die Funktion ist surjektiv auf $\{y_{1}, y_{2}, y_{3}\}$.

Für beliebige Funktionen $f : X \rightarrow Y$ und $g : Y  \rightarrow Z$ gelten folgende Aussagen:

* Falls $f : X \rightarrow Y$ und $g : Y \rightarrow Z$ injektiv sind, dann ist auch $g \circ f : X \rightarrow Z$ injektiv.
* Falls $f : X \rightarrow Y$ und $g : Y \rightarrow Z$ surjektiv sind, dann ist auch $g \circ f : X \rightarrow Z$ surjektiv.

Lemma 2 (Schubfachprinzip). Wenn $n$ Objekte auf $m$ Behälter verteilt werden und $n > m$ gilt, dann gibt es mindestens einen Behälter, der mehr als ein Objekt enthält. Formal, sind $n > m$ natürliche Zahlen und gelte $|X| = n$ sowie $|Y | = m$, dann gibt es keine injektive Funktion $F : X \rightarrow Y$.


### Grössenvergleiche von unendlichen Mengen

Begriff                 Erklärung
--------                ---------------
Endlichkeit             Eine Menge $X$ heisst endlich, wenn es eine natürliche Zahl $n$ und eine
                        Darstellung der Form $X = \{x_{1}, x_{2}, ... , x_{n}\}$ gibt.Wenn 
                        $X = \{x_{1}, ... , x_{n}\}$
                        gilt, und die Elemente $x_{i}$ paarweise verschieden sind (d.h. es gilt 
                        $i \neq j \Rightarrow x_{i} \neq x_{j} )$, dann hat die Menge $X$ genau $n$
                        viele Elemente und wir schreiben $|X| = n$
Unendlichkeit           Nicht endliche Mengen nennen wir unendlich.
Abzählbar               Eine Menge $X$ heisst abzählbar, wenn eine surjektive Funktion
                        $F : \mathbb{N} \Rightarrow X$
                        existiert oder wenn $X = \varnothing$ gilt.
Abzählbar unendlich     Die Menge $X$ heisst abzählbar unendlich, wenn X abzählbar und unendlich ist
Überabzählbar           Eine überabzählbare Menge ist eine Menge, die nicht abzählbar ist.


* Jede endliche Menge ist abzählbar!
* Jede Teilmenge einer abzählbaren Menge ist abzählbar!
* Ist $X$ eine abzählbare Menge und gibt es eine surjektive Funktion $F: X \rightarrow Y$, dann ist auch $Y$ abzählbar.
* (Erstes Diagonalargument) Die Menge $\mathbb{N} \times \mathbb{N}$, bestehend aus allen Paaren von natürlichen Zahlen, ist abzählbar. (siehe Bild → ) (d.h. auch $\mathbb{Z} \times \mathbb{Z}$ ist abzählbar)
* Jede Vereinigung von abzählbar vielen abzählbaren Mengen ist abzählbar. Konkret jede Vereinigung der Form: ist abzählbar, wenn alle $A_{i}$ abzählbar sind.


![Anstelle eines formalen Beweises, skizzieren wir eine Abzählung aller Paarevon natürlichen Zahlen wie folgt](./dm_files/Screenshot%202023-01-08%20010409.png){ width=50% }


### Ordnungs- und Äquivalenzrelationen

Eine binäre Relation $R$ auf einer Menge $X$ heisst:

Name            für alle $x, y, z \in X$            Präordnung      Halbordnung
----------      -------------------------           -----------     --------------
Reflexiv        $xRx$                               x               x
Symmetrisch     $xRy \Rightarrow yRx$                                       
Antisymmetrisch $xRy \wedge yRx \Rightarrow x = y$                  x
Transitiv       $xRy \wedge yRz \Rightarrow xRz$    x               x


Die Verliebtheitsrelation $L$ hat unter anderem folgende Eigenschaften:

* $L$ ist nicht reflexiv, da nicht alle Menschen “selbstverliebt” sind.
* $L$ ist (leider8) nicht symmetrisch, da Liebe nicht immer auf Gegenseitigkeit beruht.
* $L$ ist nicht Antisymmetrisch, da es durchaus “echte” Liebespaare (aus zwei Partnern bestehend) gibt.
* $L$ ist nicht transitiv, da die Meisten Leute den angebeteten der eigenen angebeteten nicht lieben (ganz im Gegenteil!).

**Äquivalenzrelationen**

Äquivalenzrelationen sind reflexive, symmetrische und transitive Relationen.

Bsp.: Auf jeder Menge $X$ ist die Gleichheitsrelation $\Delta X = \{(x, x) | x 2 X\}$ eine Äquivalenzrelation. Weil
jede Äquivalenzrelation reflexiv ist, ist die Gleichheitsrelation auf jeder Menge die “kleinste”
Äquivalenzrelation. Am anderen Ende des Spektrums steht die Relation $X \times X$, sie ist die grösste
Äquivalenzrelation auf der Menge X.


Es sei $R$ eine Äquivalenzrelation auf einer Menge $X$ und $x \in X$. Die
Äquivalenzklasse $[x]R$ von $x$ bezüglich $R$ ist die Menge aller Elemente von
$X$, die zu $x$ in Relation $R$ stehen:

$$[x]R := \{ y \in X | xRy \}$$

Jedes Element einer Äquivalenzklasse nennen wir einen Repräsentanten
der entsprechenden Äquivalenzklasse. Die Faktormenge $X / R$ von $X$
modulo $R$ ist die Menge aller Äquivalenzklassen:

$$X/R := \{ [x]R | x \in X \}$$

Wir betrachten die Relation $\equiv_{5}$ auf der Menge $\mathbb{Z}$, die wie folgt gegeben ist:

$$X \equiv_{5} y :\Leftrightarrow (x-y)$$ ist ein Vielfaches von 5

Ist die Relation eine Äquivalenzrelation?

- Reflexivität: Es gilt für jede Zahl $z$
    -   $0 \cdot  5 = 0 = (z-z)$
    Also ist $(z-z)$ ein Vielfaches von $5$, somit gilt $z \equiv_{5} z$
- Symmetrie: Gilt $x \equiv_{5} y$, dann gibt es eine ganze Zahl $z$ mit $5z = (x-y)$. Also ist auch 
    -   $(y - x) = -(x - y) = -5z = 5 \cdot (-z)$
    ein Vielfaches von $5$, somit gilt $y \equiv_{5} x$, wenn $x \equiv_{5} y$.
- Transitivität: Gilt $x \equiv_{5} y$ und $y \equiv_{5} z$, dann gibt es ganze Zahlen $r, s$ mit $5r = x - y$ und $5s = y - z$. Insgesamt erhalten wir, dass
    - $x - z = (x - y) + (y - z) = 5r + 5s = 5(r + s)$ 
    ein Vielfaches von $5$ ist und somit, dass $x \equiv_{5}$ z gilt.

Die Äquivalenzklassen modulo der Relation $\equiv_{5}$ heissen Restklassen modulo 5

![Restklassen Modulo5](./dm_files/Screenshot%202023-01-08%20154105.png){ width=100% }

**Lemma 3**
Ist $\sim$ eine Äquivalenzrelation auf einer Menge $X$ und gilt $x,y \in X$ mit $x \sim y$, dann gilt $[x] \sim = [y]\sim$ . Mit
anderen Worten, äquivalente Elemente repräsentieren stets dieselbe Äquivalenzklasse

**Satz 10**
Ist $\sim$ eine Äquivalenzrelation auf einer Menge $X$ und gilt $x y \in X$ mit $[x] \sim \neq [y]$, dann gilt $[x]\sim \cap [y]\sim= \varnothing$. Mit anderen Worten, verschiedene Äquivalenzklassen sind immer disjunkt.

**Satz 11**
Ist $\sim$ eine Äquivalenzrelation auf einer Menge $X$, dann ist die Faktormenge $X / \sim$ eine Partition von $X$

**Satz 12**
Ist $P = \{A_{i} | i \in I\}$ eine Partition von der Menge $X$, dann ist die Relation $\sim$, gegeben durch

$$x \sim y : \Leftrightarrow \exists i \in I (x \in A_{i} \wedge y \in A_{i})$$

eine Äquivalenzrelation auf X. Zusätzlich gilt

$$\frac{x}{\sim} = P$$

**Ordnungsrelationen**

Alle Relationen, mit welchen man Objekte vergleichen und mehr oder weniger sortieren kann. Das
Standardbeispiel ist die Ordnungsrelation $\leq$ auf verschiedene Zahlenmengen.

R = binäre Relation / M = Menge

Name                    Beschreibung
---------               -----------------------------
R-unvergleichbar        Zwei Elemente $x, y \in M$ heissen R-unvergleichbar, falls weder $xRy$ noch $yRx$ gilt.
R-minimal               Ein Element $x \in X$ einer Teilmenge $X  \subseteq M$ von $M$ heisst R-minimal in $X$, falls es kein anderes Element $y \in X$ mit $yRx$ gibt.
R-maximal               Ein Element $x \in X$ einer Teilmenge $X \subseteq M$ von $M$ heisst R-maximal in $X$, falls es kein anderes Element $y \in X$ mit $xRy$ gibt.

*   Die minimalen Elemente von $M$ sind $a$ und $x$
*   Das einzige maximale Element von $M$ ist $z$.

![Relationen](./dm_files/Screenshot%202023-01-08%20160324.png){ width=50% }

Ordnung                     Relation    
-----------                 --------------------------
Präordnung                  $R$ ist eine Präordnung auf $M$, wenn $R$ *reflexiv* und *transitiv* ist
Halbordnung                 $R$ ist eine Halbordnung auf $M$, wenn $R$ *reflexiv*, *antisymmetrisch* und *transitiv* ist
Totale/                     $R$ ist eine totale oder lineare Ordnung auf $M$, wenn $R$ eine Halbordnung ist und
lineare Ordnung             keine R-unvergleichbaren Elemente existieren.
Wohlordnung                 $R$ ist eine Wohlordnung auf $M$, wenn $R$ eine totale Ordnung auf $M$ ist so, dass
                            jede Teilmenge $X \neq \varnothing$ von $M$ (mindestens) ein R-minimales Element enthält

* Die Relation $\leq$ ist eine totale Ordnung auf die Menge $\mathbb{R}$ und auch auf die Menge $\mathbb{Z}$, weil sie kein kleinstes Element hat. Die Relation $\leq$ auf die Menge $\mathbb{N}$ ist eine **Wohlordnung**.
* Die Teilerrelation T auf der Menge $\mathbb{Z}$ ist eine **Halbordnung** aber keine totale Ordnung. Die Elemente 7 und 5 sind T-unvergleichbar

Abschluss               Beschreibung
----                    ---------------------
Transitiver             Als transitiven Abschluss von R bezeichnet man die kleinste (bezüglich $\subseteq$) 
Abschluss $R^{+}$       transitive Relation, die $R$ als Teilmenge enthält, sie wird mit $R^{+}$ notiert.
Reflexiv-               
transitiver             Die kleinste Relation, die $R^{+}$ enthält und reflexiv ist, nennt man den
Abschluss $R^{+}$       *reflexivtransitiven Abschluss* von R, sie wird mit $R^{\ast }$ bezeichnet.

Es sei $M$ eine endliche Menge und $G = (M,E)$ ein DAG. Eine lineare
Ordnung $\preceq 1 \subseteq  M \times M$ ist eine topologische Sortierung von $G$, wenn
für alle $a, b \in M$ das folgende gilt.

$$aE^{\ast}b \Rightarrow  a \preceq b $$

**Hasse-Diagramme**

Es sei $\preceq$ eine Halbordnung auf einer Menge $M$. Das Hasse-Diagramm von $R$ ist eine vereinfachte
Darstellung des Graphs $(M, \preceq)$.

*   Die Richtung eines Pfeiles $a \rightarrow b$ für Elemente $a, b \in M$ wird dadurch zum Ausdruck gebracht, dass sich der Knoten $b$ oberhalb von $a$ befindet.
*   Pfeile zwischen zwei Punkten $a, b$ werden gelöscht, wenn es einen weiteren Punkt $c$ mit $a \preceq c \preceq b$ gibt
*   Pfeile, die von einem Punkt auf denselben Punkt zeigen (Schleifen), werden weggelassen.


![Eine Darstellung als Hasse-Diagramm von der Relation $\leq$ auf der Menge{1, . . . 5}.](./dm_files/Screenshot%202023-01-08%20170913.png){ width=50% }

![Teilbarkeitsrelation auf der Menge Teilermenge von 28 ä({1, 2, 4, 7, 14, 28}) Maximales Element: 28 Minimales Element: 1 Bsp. für unvergleichbare Elemente:2, 7 oder 4, 14](./dm_files/Screenshot%202023-01-08%20171011.png){ width=50% }

![Die Teilmengenrelation $\subseteq$ auf der Menge P({a,b, c})](./dm_files/Screenshot%202023-01-08%20171104.png){ width=50% }

![Halbordnung auf der Menge {0, . . . , 7} Maximale Elemente: 4, 7 Minimale Elemente: 0, 1, 3 Bsp. für unvergleichbare Elemente: 1, 0, 3 oder 4, 5, 6](./dm_files/Screenshot%202023-01-08%20171202.png){ width=50% }

![Graph G = ({12, 13, 14, 18, 112}, $\preceq$ )](./dm_files/Screenshot%202023-01-08%20171305.png){ width=50% }

![Relation als Menge:{(13, 13), (13, 112), (12, 12), (12, 112), (12, 14),(12, 18), (14, 14), (14, 112), (14, 18), (18, 18),(112, 112)}](./dm_files/Screenshot%202023-01-08%20171400.png){ width=50% }

![Die Ordnung $\leq$ auf $\mathbb{N}$ ](./dm_files/Screenshot%202023-01-08%20171502.png){ width=50% }

# Rekursive Strukturen und die natürlichen Zahlen

## Die grundlegende Struktur der natürlichen Zahlen

$$\mathbb{N} 0 \overset{+1}{\longrightarrow}1\overset{+1}{\longrightarrow}2\overset{+1}{\longrightarrow}3\overset{+1}{\longrightarrow}...$$

Das Prinzip der (vollständigen ) Induktion: Es sei $A(n)$ eine Eigenschaft (ein Prädikat) von natürlichen Zahlen. Aus den beiden Voraussetzungen

* **Induktionsverankerung (I.V.)**: A(0)
* **Induktionsschritt (I.S.)**: $\forall n \in \mathbb{N} (A(n) \Rightarrow A(n + 1))$ 

folgt die Gültigkeit von $\forall n \in \mathbb{N} (A(n))$

**Induktionsbeweis**

Der Induktionsschritt für ein Prädikat A ist stehts von der Form:

$$\forall n \in \mathbb{N} (\; \underset{Induktionsannahme}{\underbrace{A(n)}} \; \Rightarrow A(n+1 ))$$

Die Stärke des Induktionsargumentes liegt daran, dass man nicht einzeln für alle unendlich vielen
Zahlen von $\mathbb{N}$ etwas beweisen muss, sondern man kann all diese unendlich vielen Schritte auf zwei
Schritte zu reduzieren:

1. Schritt (I.V.): E(0).
2. Schritt (I.S.): Zeige, dass die Eigenschaft E unter Nachfolgern erhalten bleibt. Intuitiv könnte man sagen, dass die Eigenschaft E von jeder natürlichen Zahl auf die nächste “vererbt” wird.

Wir betrachten die Eigenschaft A(n), die besagt, dass die Summe aller natürlichen Zahlen bis:

$$0+1+...+n=\frac{n(n+1)}{2}$$

n halb so gross wie die Zahl n(n + 1) ist:

Wir Beweisen durch Induktion nach n, dass die Eigenschaft A(n) für jede natürliche Zahl n
zutrifft.

Beweis:

**Induktionsverankerung (I.V.)**
> n = 0: A(0) 
> gitl weil:
> $0=\frac{0 \cdot}{2}$
> offensichtlich korrekt ist
**Induktionsschritt (I.S.)**
> Für den Induktionsschritt müssen wir zeigen, dass für jede natürliche Zahl $n$ mit der
> Eigenschaft $A(n)$ auch $A(n + 1)$ gilt. Wir nehmen dazu an, dass n eine beliebige solche
> natürliche Zahl sei und betrachten

![Induktionsschritt](./dm_files/Screenshot%202023-01-08%20174750.png){ width=50% }

**Beweismethode: Der Kleinste Verbrecher**

Die Beweismethode des “kleinsten Verbrechers” geht wie folgt: Will man zeigen, dass alle
natürlichen Zahlen eine Eigenschaft $E$ haben, dann geht man davon aus, dass wenn dies nicht der Fall
wäre, es eine kleinste natürliche Zahl $n_{0}$ (den kleinsten Verbrecher) gäbe, die nicht die Eigenschaft $E$
hat. Führt man diese Annahme zu einem Widerspruch, so hat man die ursprüngliche Behauptung
bewiesen.

Bsp:

> Wir benützen die Methode des “kleinsten Verbrechers” um zu beweisen, dass jede natürliche
> Zahl, die mindestens zwei Teiler hat, mindestens einen Primfaktor besitzt (von einer Primzahl
> geteilt wird).
> Beweis. Es sei $n_{0}$ die kleinste natürliche Zahl mit mindestens zwei Teilern, die keine
> Primfaktoren besitzt (der “kleinste Verbrecher”). Da n0 keine Primfaktoren hat, ist $n_{0}$ selbst
> auch keine Primzahl und es gilt $n_{0} 6= 0$. Es folgt somit, dass ein Teiler $ 1 < x < n_{0}$ von $n_{0}$
> existieren muss. Da $1 < x$ gilt, hat x mindestens zwei Teiler ($1$ und $x$) und somit, wegen $x < n_{0}$,
> einen Primfaktor $p$. Da die Teilbarkeitsrelation transitiv ist, muss $p$ aber auch ein Primfaktor
> von $n_{0}$ sein. Dies ist der gesuchte Widerspruch.

## Vom Induktionsbeweis zum rekursiven Algorithmus

Mit einem Induktionsbeweis kann mehr als nur eine Argumentationskette, die dazu geeignet ist,
jemanden von etwas zu überzeugen. Ein Beweis kann einen konkreten Algorithmus (rekursiv)
vorgeben wie etwas gelöst werden kann. Im Unterricht hatten wir das Beispiel des Spiels «Die Türme
von Hanoi» (siehe Bild) bei dem wir zuerst einen
Induktionsbeweis darüber machten, dass das Spiel mit
beliebig vielen Scheiben gelöst werden kann und haben
dann daraus einen Java-Code für die Lösungsstrategie
gezogen (Skript S.88).

## Rekursive Definitionen

Rekursive Definitionen bezeichnen die mathematisch einwandfreie Art, ein Objekt durch
Bezugnahme (Selbstreferenz) auf das zu definierende Objekt selbst zu definieren.
Bsp.: Palindrome

Ein Palindrom ist ein Wort, das rückwärts und vorwärts gelesen gleich lautet. Wie können wir das
mathematisch darstellen ist die Frage:

* Das Wort $w$ besteht aus einem oder gar keinem Buchstaben (Länge von $w < 2$).
* Es gibt einen Buchstaben (Zeichen, char) $x$ und ein Palindrom $u$ so, dass $w = xux$ gilt.

**Rechenregel**
Für alle $n, m, k \in \mathbb{N}$ gelten folgende Rechenregeln:

Addition

* Neutrales Element: 0 + n = n
* Kommutativität: n + m = m + n
* Assoziativität: (n + m) + k = n + (m + k)
* Kürzbarkeit: n + k = m + k ) n = m

Multiplikation

* Absorbtion: 0 · n = 0
* Neutrales Element: 1 · n = n
* Kommutativität: n · m = m · n
* Assoziativität: n · (m · k) = (n · m) · k
* Distributivität: n · (m + k) = nm + nk


# Elementare Zahlentheorie 

$$\mathbb{Z} := \{...,-2,-1,0,1,2,...\}$$

Zusätzliche Rechenregeln auf $\mathbb{Z}$

Für alle $r, s, z \in Z$ gelten folgende Gleichungen.

Gleichung                                   Kommentar
----------------------                      ------------------
$-1 \cdot z = -z$
$-(-z) = z$
$-z + z = 0$                                Inverse Elemente bezüglich +
$0 \cdot z = 0$                             Absorbtion
$1 \cdot z = z$                             Neutrales Element bezüglich $\cdot$
$0 + z = z$                                 Neutrales Element bezüglich +
$r(sz) = (rs)z$                             Assoziativität von $\cdot$
$r + (s + z) = (r + s) + z$                 Assoziativität von +
$rs = sr$                                   Kommutativität von $\cdot$
$r + s = s + r$                             Kommutativität von +
$r(s + z) = rs + sz$                        Distributivität
$rx = ry \Rightarrow x = y \wedge r = 0$    Kürzbarkeit

**Substraktion**
$$-: \mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{Z}$$

durch

$$x - y := x + (-y)$$

**Betragsfunktion**

$$|\cdot | : \mathbb{Z} \rightarrow \mathbb{N}$$

durch

$$|z|= \left\{\begin{matrix}z & falls z \in \mathbb{N}\\ -1 \cdot z & sonst\end{matrix}\right.$$

**Relation**
$$x \leq  y :\Leftrightarrow  \exists n \in N (x + n = y).$$

## Teilbarkeit und Euklidischer Algorithmus

Sind $x, y \in \mathbb{Z}$ ganze Zahlen, so sagen wir, dass $x$ ein Teiler von $y$ ist, falls es ein $k \in \mathbb{Z}$ gibt mit $xk = y$. Wir schreiben in diesem Fall $x|y$. Es gilt also

$$x|y : \Leftrightarrow \exists k \in \mathbb{Z}(y = xk)$$

Mit $T(y)$ bezeichnen wir die Menge aller natürlichen Zahlen, welche Teiler von $y$ sind, also $T(y) = \{x 2 \mathbb{N} | x|y\}$.

Bsp:

* Die Zahl $1$ ist ein Teiler jeder ganzen Zahl $z$, da $1 \cdot z = z. \; 1|\mathbb{Z}$
* $T(0)= \mathbb{N}$

Die Teilbarkeitsrelation ist reflexiv und transitiv (eine Präordnung) auf der Menge $\mathbb{Z}$, auf der Menge
$\mathbb{N}$ sogar eine Halbordnung.

**Antisymmetrie auf $\mathbb{N}$:**
Wir müssen zeigen, dass für natürliche Zahlen $x$ und $y$ aus $x|y$ und $y|x$ folgt, dass $x = y$ gilt. Es
gelte also $xk = y$ und $x = yr$ für ganze Zahlen $k, r$. Es folgt
$x = yr = (xk)r = x(kr)$
und deswegen, dass $kr = 1$ und somit $k = r = 1$, was $x = y$ bedeutet.

Hasse-Diagramme Teilbarkeit: 

![Menge T(30)](./dm_files/Screenshot%202023-01-08%20182600.png){ width=50% }
![Menge T(90)](./dm_files/Screenshot%202023-01-08%20182629.png){ width=50% }

**Teilen mit Rest**

Sind $n,m \in \mathbb{N} /\{0\}$, dann gibt es eindeutig bestimmte Zahlen $k, r \in \mathbb{N}$, so dass Folgendes gilt:

* $m = kn + r$
* $r < n$

Wir sagen in diesem Zusammenhang, dass die Zahl $r$ den Rest von der (ganzzahligen) Division von
m durch $n$ ist.

**kgV und ggT**

$n, m \in \mathbb{Z}$

kleinste gemeinsame Vielfache

$$kgV (n,m) := min\{k \in \mathbb{N} | n|k \wedge m|k \}$$

grösster gemeinsamer Teiler

$$ggT (n,m) := max\{k \in \mathbb{N} | k|n \wedge k|m\}$$


**Euklidischer Algorithmus**

Für $n,m \in \mathbb{N}$ mit $0 < n < m$ gilt

$$ggT(n,m) = ggT(n,m - n) = ggT(m,m - n)$$

für $n,m \in \mathbb{N}$ mit $n < m$

$${k \in \mathbb{N} | k|n \wedge k|m} = {k \in \mathbb{N} | k|n \wedge k|(m - n)}$$

$$ggT(n,m) = max{k \in \mathbb{N} | k|n \wedge k|m} = max{k \in \mathbb{N} | k|n \wedge k|(m - n)} = ggT(n,m - n).$$

$$ggT(n,m) = ggT(m,m - n)$$

Aus diesem Beweis erhalten wir direkt einen rekursiven Algorithmus zur Berechnung des ggT.
Beispielhaft geht man dabei wie folgt vor:

$$ggT(n,m) = ggT(m,m - n)$$
$$ggT(45, 25) = ggT(25, 20)$$
$$= ggT(20, 5)$$
$$= ggT(5, 15)$$
$$= ggT(5, 10)$$
$$= ggT(5, 5) = 5.$$

Bei $x > y$ wird zum Berechnen von $ggT(y, x)$ so oft $y$ von $x$ subtrahiert, bis das Resultat kleiner oder
gleich $y$ ist. Man kann all diese Subtraktionen also durch eine einzige Division mit Rest ersetzen. Die
beispielhafte Berechnung von $ggT(45, 25)$ können wir nun als 2 Divisionen mit Rest darstellen:

$$45 = 1 \cdot 25 +20$$
$$25 = 1 \cdot 20 +\underset{ggT(45,25)}{\underbrace{5}}$$

Zusammenfassend stellen wir fest, dass

$$ggT(y, x) = ggT(y,R(x, y))$$

mit

> R(x, y) = der Rest der Division von x durch y | x%y.



![Bsp. von ggT(27, 96)](./dm_files/Screenshot%202023-01-08%20183818.png){ width=50% }

Zwei ganze Zahlen x, y heissen teilerfremd, wenn $ggT(x, y) = 1$ gilt.

**Lemma von Bézout (Multiplikatives Inverse)**

Sind $x, y \in \mathbb{Z}$ mit $x, y \neq 0$, dann gibt es ganze Zahlen $a, b$ so dass

$$ggT(x, y) = ax + by$$

Bsp.: Wir wollen ganze Zahlen a und b finden, die die Gleichung

$$a \cdot 504 + b \cdot 29 = ggT(504, 29) = 1$$

> $b$ ist dann das Multiplikatives Inverse von $29$ in $\mathbb{Z}/504$

erfüllen

Schritt 1: Sukzessives Teilen mit Rest.

$$504 = 17 \cdot 29 + 11$$
$$29 = 2 \cdot 11 + 7$$
$$11 = 1 \cdot 7 + {\color{blue} 4}$$
$$7 = 1 \cdot 4 + {\color{green} 3}$$
$${\color{blue} 4} = {\color{green}1 \cdot 3 } + {\color{orange}1} \Rightarrow ggT(504, 29) = 1$$

Schritt 2: Rückwärts einsetzen

$${\color{orange}1} = {\color{blue}4} -{\color{green} 3}$$
$$= {\color{blue}(11 - 7)} -{\color{green} (7 - 4)}$$
$$= {\color{blue}((504 - 17 \cdot 29) - (29 - 2 \cdot 11))} - {\color{green}((29 - 2 \cdot 11) - (11 - 7))}$$
$$= {\color{blue}((504 - 17 \cdot 29) - (29 - 2 \cdot (504 - 17 \cdot 29)))}$$
$$- {\color{green}((29 - 2 \cdot (504 - 17 \cdot 29)) - ((504 - 17 \cdot 29) - (29 - 2 \cdot 11)))}$$
$$= {\color{blue} ((504 - 17 \cdot 29) - (29 - 2 \cdot (504 - 17 \cdot 29)))}$$
$$- {\color{green}((29 - 2 \cdot (504 - 17 \cdot 29)) - ((504 - 17 \cdot 29) - (29 - 2 \cdot (504 - 17 \cdot 29))))}$$


Schritt 3: Zusammenfassen (Zählen der Vorkommen von 504 und 29).

$$a = 1 + 2 + 2 +1 + 2 = 8$$
$$b = -17 - 1 - (2 \cdot 17) - 1 - (2 \cdot 17) - 17 - 1 - (2 \cdot 17) = -139$$

b ist das Multiplikatives Inverse von 29 in $\mathbb{Z}/504$ also; $29-1 = -139 in \mathbb{Z}/504$


Test

$$8 \cdot 504 - 139 \cdot 29 = 1$$



## Primzahlen

* Eine natürliche Zahl $p \in \mathbb{N}$ ist eine Primzahl, wenn $|T(p)| = 2$ gilt. Die Menge aller Primzahlen bezeichnen wir mit $\mathbb{P}$.
* Ist $p \in \mathbb{P}$, dann gilt $T(p) = {1, p}$
* Betrachtet man die Teilbarkeitsrelation auf der Menge $\mathbb{N} \setminus  \{1\}$, dann sind die Primzahlen genau die minimalen Elemente dieser Halbordnung.
* Es gibt unendlich viele Primzahlen
* Jede natürliche Zahl grösser als 1 ist das Produkt von endlich vielen Primzahlen

**Lemma von Euklid**

Folgende Aussagen sind für $p \in \mathbb{N}$ mit $p \neq 1$ äquivalent:

1. $\forall n,m \in \mathbb{N} (p|nm\Rightarrow p| n \wedge p|m$ 
2. $p \in \mathbb{P}$

Jede ganze Zahl $z$ mit $z \notin  \{-1, 1\}$ besitzt einen Primfaktor (einen Teilerm der eine Primzahl ist)

$$\forall z \in \mathbb{Z} (z \notin \{ -1,1\} \Rightarrow T(z) \cap\mathbb{P} \neq \varnothing) $$

Es sei pi jeweils die i-te Primzahl. Für jede
natürliche Zahl $n >$ 1 gibt es eine eindeutig
bestimmte, endliche Folge $a_{1}, ..., a_{k}$ von
natürlichen Zahlen mit $a_{k} \neq 0$, so dass

$$n = \prod_{i=1}^{k}p_{i}^{a_{i}}$$

## Modulare Arithmetik

Es sei $n \in \mathbb{N}$ und eine Relation $\equiv_{n}$ auf $\mathbb{Z}$ wie folgt:

$$r \equiv_{n} s:\Leftrightarrow n | (r-s)$$


Gilt für $r, s \in \mathbb{Z}$ die Relation $r \equiv_{n} s$, dann sagen wir, dass $r$ gleich $s$ modulo $n$ ist und schreiben $r = s$ mod n.

Die Relation $\equiv_{n}$ ist für $\forall n \in \mathbb{N}$ eine Äquivalenzrelation auf $\mathbb{Z}$.

$n \in \mathbb{N} \; und \; z \in \mathbb{Z}$

$[z]_{n} : = \{x \in \mathbb{Z} | x \equiv_{n} z\}$

Die Äquivalenzklasse von z bezüglich der Relation $\equiv_{n}$ nennen wir Restklasse

Die Menge der Restklasse von $\mathbb{Z}$ modulo $n$ bezeichnen wir mit

$$\frac{\mathbb{Z}}{n} = \{[z]n | z \in \mathbb{Z}\}$$


$[x]_{n} + [y]_{n} := [x + y]_{n}$

$[x]_{n} \cdot [y]_{n} := [xy]_{n}$

Verknüpfungstabelle der Addition in $\mathbb{Z}$/6:

![Verknüpfungstabelle der Addition in $\mathbb{Z}$/6](./dm_files/Screenshot%202023-01-08%20200740.png){ width=50% }
![Verknüpfungstabelle der Multiplikation in $\mathbb{Z}$/6](./dm_files/Screenshot%202023-01-08%20200846.png){ width=50% }

Beispiel 61 (Rechnen mit Uhrzeiten). Rechnen mit Uhrzeiten (volle Stunden einer
Analoguhr) entspricht mit Restklassen Modulo 12 zu rechnen

* Es ist 9 Uhr. Wie lange dauert es, bis es das nächste Mal 2 Uhr ist? Wir müssen die Gleichung

$$\bar{9}+x =\bar{2} $$

* lösen. Wie vorher gesehen, erhalten wir die Lösung durch

$$x = \bar{2} + \bar{-9} = \bar{2 - 9} = \bar{-7} = \bar{5}$$

Es geht also noch 5 Stunden bis 2 Uhr.

### Chinesicher Restsatz

Der chinesische Restsatz besagt, dass bei paarweise teilerfremden Zahlen $n_{1}, .., n_{k} \in N>1$
und beliebigen ganze Zahlen $y_{1}, .., y_{k}$, Gleichungssysteme von der Form

$$x\equiv_{n_{1}}y_{1}$$
$$x\equiv_{n_{2}}y_{2}$$
$$...$$
$$x\equiv_{n_{k}}y_{k}$$

eindeutig in $\mathbb{Z}/(n_{1}, .., n_{k})$ lösbar4 sind.

der Menge $[x]_{\prod_{i=1}^{k}}n_{i}$ entspricht.

Mit 2 Gleichungen:

$$x\equiv_{m1}a1$$
$$x\equiv_{m2}a2$$

x1 und x2 bestimmen

$$m2 \cdot x1\equiv_{m1}a1$$
$$m1 \cdot x2\equiv_{m3}a1$$

x bilden

$$x = a1 \cdot m2 \cdot x1 + a2 \cdot m1 \cdot x2$$

Mit n Gleichungen:

$$x\equiv_{m1}a1$$
$$x\equiv_{m2}a2$$
$$x\equiv_{m3}a3$$

x1, x2 und x3 bestimmen

$$m2 \cdot m3 \cdot x1\equiv_{m1}1$$
$$m1 \cdot m3 \cdot x2\equiv_{m2}1$$
$$m1 \cdot m2 \cdot x3\equiv_{m3}1$$

x bilden

$$x = a1 \cdot m2 \cdot m3 \cdot x1 + a2 \cdot m1 \cdot m3 \cdot x2 + a3 \cdot m1 \cdot m2 \cdot x3$$

x kürzen (wenn nötig)

$$x\equiv_{m1 \cdot m2\cdot m3} = x^{gekuerzt} \rightarrow x =  x^{gekuerzt} + z \cdot m1 \cdot m2 \cdot m3 | fuer \; z \in \mathbb{Z}$$

Mit n Gleichungen und Zahlen:

$$x \equiv_{5} 3$$
$$x \equiv_{7} 5$$
$$x \equiv_{9} 7$$

x1, x2 und x3 bestimmen


$$7 \cdot 9 \cdot x1 \equiv_{5} 1$$
$$63 \cdot x1 \equiv_{5} 1$$
$$(2 \cdot 63 = 126 → 126 \equiv_{5}= 1) x1 = 2$$
$$5 \cdot 9 \cdot x2 \equiv_{7} 1$$
$$x2 = 5$$
$$5 \cdot 7 \cdot x3 \equiv_{9} 1$$
$$x3 = 8$$

x bilden und kürzen

$$x = a1 \cdot m2 \cdot m3 \cdot x1 + a2 \cdot m1 \cdot m3 \cdot x2 + a3 \cdot m1 \cdot m2 \cdot x3$$
$$x = 3 \cdot 7 \cdot 9 \cdot 2 + 5 \cdot 5 \cdot 9 \cdot 5 + 7 \cdot 5 \cdot 7 \cdot 8 = 3463$$
$$3463 \equiv_{5 \cdot 7 \cdot 9} = 313 \rightarrow x = 313 + z \cdot 315 | \; für \; z \in \mathbb{Z}$$
