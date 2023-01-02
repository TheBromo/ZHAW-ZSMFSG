---
title:  'Analysis Zusammenfassung MAX 10S'
author:
- Manuel Strenge
keywords: [ANA, pain]
...

# Konzepte der Differential- und Integralrechnung
## Komposition
Für zwei gegebene Funktionen $f: A \rightarrow B$ und $g : B \rightarrow C$ , ist die Funktion $g \circ f : A \rightarrow C$
definiert durch

$$ (g \circ f)(x) = g(f(x))$$

Diese neue Funktion heisst Komposition von f und g. (Andere Bezeichnungen: Verkettung, Nacheinanderausführung.)

## Summenzeichen

$a_{1} + a_{2} + a_{3} + \cdots + a_{n} = \sum_{k=1}^{n}a_{k}$
$a_{s} + a_{s+1} + a_{s+2} + \cdots + a_{n} = \sum_{k=s}^{n}a_{k}$

## Begriff des Polynoms, Eigenschaften von Polynomen
### Definition

$$y = f(x) = a_{n} \cdot x^{n} +  a_{n-1} \cdot x^{n-1} + ... + a_{1} \cdot x + a_{0} \;  mit \;  a \neq 0 $$

+----------------------------------------+-------------------------+
|                                        |                         |
+========================================+=========================+
| $n:$                                   |Grad der Polynomfunktion |
+----------------------------------------+-------------------------+
| $a_{0},a_{1},....,a_{n}\in \mathbb{R}:$| Koeffizienten           | 
+----------------------------------------+-------------------------+
|  Definitionsbereich                    | $\mathbb{R}$            | 
+----------------------------------------+-------------------------+

### Horner Schema

**Ziel:** Zu einem gegebenen $x_{0}$ (z.B. $x_{0} = -2$ ) möglichst effizienten Wert $f(x_{0})$ ausrechnen

**Variante 1**: Das Polynom normal ausrechnen. Problem dabei ist, dass sehr viele Multiplikationen dafür benötigt werden (z.B. für $n = 10 \rightarrow 55$ )

**Effizienteres Verfahren** Umformung, damit Multiplikation schrittweise erfolgen kann. Für ein Polynom vom Grad 4:
$$ f(x) = a_{4}x^{4} + a_{3}x^{3} + a_{2}x^{2} + a_{1}x + a_{0}=\underset{Anzahl \; Multiplikationen: \; 4}{((((a_{4})\cdot x + a_{3}) \cdot x + a_{2})\cdot  x + a_{1}) \cdot  x + a_{0}}$$

Das Schema von Horner bietet eine übersichtliche Art, ein Polynom auf diese effiziente Weise
auszurechnen. Veranschaulichung anhand des Beispiels:

![Berechnung mit Horner Schema](./ana-files/Screenshot%202023-01-02%20164649.png){ width=100% }

### Zerlegunssatz

Ist $x_{0}$ eine Nullstelle der Polynomfunktion $f(x)$, dann gibt es eine bestimmte Polynomfunktion $q(x)$ , so dass gilt:

$$f(x) = (x - x_{0}) \cdot q(x) $$ für jedex $x$

**Notation:** Der Faktor $(x - x_{0})$ heisst Linearfaktor. $q(x)$ ist das sogenannte 1. reduzierte
*Polynom:* der Grad von $q(x)$ ist um eins kleiner als der Grad von $f(x)$

### Nullstellen

> Eine Polynomfunktion vom Grad $n$ hat höchstens $n$ Nullstellen

$x_{0}$ heisst $m$ -fache Nullstelle (oder Nullstelle der Multiplizität $m$ ) der Polynomfunktion $f(x)$ ,
falls es eine bestimmte Polynomfunktion $g(x)$ gibt, so dass gilt:

$$ f(x) = (x-x_{0})^{m} \cdot g(x)$$  für jedex $x$

Beispiel Im Polynom $f(x) = (x-1)(x + 3)(x-8)^{2}(x-6)^{3}$ ist 8 eine doppelte Nullstelle und 6 ist eine dreifache Nullstelle

## Ableitung (Tangente, Kurvendiskussion)
* Die Ableitung einer Funktion an einer bestimmten Stelle gibt Auskunft über die Entwicklung, die Veränderung dieser Funktion.

![Geometrische Interpretation](./ana-files/Screenshot%202023-01-02%20175024.png){ width=30% }

+----------------------------------------+-------------------------------+-------------------------------------+
|**formale Bezeichnung**                 |**geometrische Beschreibung**  |**Konkretisierung für Wegfunktion**  |
+========================================+===============================+=====================================+
| Differezenquotient                     |Sekanten-Steigung              |mittlere Geschwindigkeit             |
+========================================+===============================+=====================================+
| Ableitung                              |Tangentensteigung              |Momentangeschwindigkeit              |
+----------------------------------------+-------------------------------+-------------------------------------+

> Die Funktion, die jeder Stelle $x$ den Wert $f'(x)$ zuordnet, wird Ableitungsfunktion von $f$ genannt

Schreibweisen: $f'(x),\frac{\mathrm{d} f}{\mathrm{d} x},\frac{\mathrm{d} y}{\mathrm{d} x}$

Gegeben ist die Funktion $f(x) = x^{k}$ mit $k \neq 0$. Dann gilt: $f'(x) = k \cdot x^{k-1}$

## Stammfunktion und Hauptsatz

## Integral
Illustration Ein Integral kann man sich (bei eindimensionalen Funktionen) als Fläche unter
einem Kurvenstück vorstellen.

![Visualisierung Integral berechnung](./ana-files/Screenshot%202023-01-02%20221904.png){ width=100% }

Schreibweise: $\int_{b}^{a}f(x)dx$ 

Integral ermöglich es uns die Fläche eines graphen nicht annähern zu müssen.





# Folgen und Reihen

## Begriff der Folge (direkt, rekursiv, arithmetisch, geometrisch)

## Grenzwertbegriff (Monotonie, Beschränktheit, Rechenregeln, Limes einer Funktion)

## Reihen (Summenzeichen, arithmetisch, geometrisch)

# Erweiterung der Differentialrechnung

## Ableitung elementarer Funktionen

## Ableitungsregeln

**Faktorregel:** $(c \cdot f)'(x) = c \cdot f'(x)$

**Summenregel:** $(f+g)'(x) = f'(x) + g'(x)$

**Produktregel:** $(u \cdot v)'(x) = u'(x) \cdot v(x) + u(x) \cdot v'(x)$

**Quotientenregel:** $\left ( \frac{u}{v} \right )' (x) = \frac{u'(x)\cdot v(x)-u(x)\cdot v'(x)}{(v(x))^{2}}$

**Kettenregel** $(F \circ u)'(x) = F'(u) \cdot  u'(x)$

$F(u)$: äussere Funktion    $F'(u)=\frac{dF(u)}{du}$    Ableitung der äusseren Funktion nach $u$

$u(x)$: äussere Funktion    $u'(x)=\frac{du(x)}{dx}$    Ableitung der inneren Funktion nach $x$

**Ableitung bestimmter Funktionen**

* $(\sin(x))' = \cos(x)$
* $(\cos(x))' = -\sin(x)$ 
* $(e^{x})' = e^{x}$ 
* $(a^{x})' = a^{x} \cdot \ln(a)$
* $(\ln(x))' = \frac{1}{x}$
* $(\log_{a}(x))'=\frac{1}{x\cdot \ln (a)}$

## Kurvendiskussion

## Extremwertaufgaben

## Newton-Näherungs-Verfahren

Die entsprechende Stelle $x_{1}$ liegt (im Vergleich zu $x_{0}$ ) in vielen Fällen schon ein Stück näher bei
der gesuchten Lösung. Als nächstes betrachten wir die Tangente beim Punkt ( $x_{1}$ , $y_{1}$). Diese
schneidet die x-Achse an der Stelle $x_{2}$, welche uns in der Regel noch ein bisschen näher zur
Lösung bringt. Dieses Verfahren wiederholen wir, bis wir die Lösung $z$ mit der gewünschten
Genauigkeit bestimmt haben.

$$x_{n+1} = x_{n}-\frac{f(x_{n})}{f'(x_{n})}$$

![Visualisierung Newton-Verfahren ](./ana-files/Screenshot%202023-01-02%20210143.png){ width=50% }

Beispiel:
$f(x) = x^{3} + 5x - 4$

$f'(x) = 3x^{2} + 5$

![Beispiel Newton-Verfahren ](./ana-files/Screenshot%202023-01-02%20210839.png){ width=50% }

> Startet man das Newton-Verfahren mit einem Wert x0 in der Nähe eines Fixpunktes, so strebt das Verfahren gegen diesen Fixpunkt.

