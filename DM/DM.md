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

# Rekursive Strukturen und die natürlichen Zahlen

## Die grundlegende Struktur der natürlichen Zahlen

## Vom Induktionsbeweis zum rekursiven Algorithmus

## Rekursive Definitionen

# Elementare Zahlentheorie 

## Teilbarkeit und Euklidischer Algorithmus

## Primzahlen

## Modulare Arithmetik

### Chinesicher Restsatz