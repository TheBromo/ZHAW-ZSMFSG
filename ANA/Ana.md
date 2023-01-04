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

Gegeben ist eine auf dem Intervall $[a, b]$ stetige Funktion $f$ . Wir unterteilen das Intervall $[a, b]$
in $n$ Teilintervalle $I_{k}$ der Länge $\Delta x = \frac{b-a}{n}$ . In jedem Teilintervall Ik wählen wir eine Stelle $x_{k}$. Der Wert, zu dem

$$\sum_{k=1}^{n}f(x_{k})\cdot \Delta x $$

für ein immer grösser werdendes $n$ tendiert, heisst: bestimmtes Integral von $a$ bis $b$ über $f(x)$.
Schreibweise:

$$\int_{b}^{a}f(x)dx$$

* Die Wahl der $x_{k}$ spielt keine Rolle
* Das Integralzeichen erinnert an die Summe, dx erinnert an $\Delta x$.
*  Wie bei der Ableitung gibt es Regeln, die uns die Berechnungen vereinfachen! Es wird nicht nötig sein, jedes Mal die Summe von Grund auf auszurechnen.

**Der Hauptsatz der Differential- und Integralrechnung**

Stammfunktionen

Gegeben sind ein Intervall $I \subset \mathbb{R}$ und eine Funktion $f : I \rightarrow  \mathbb{R}$. Eine Stammfunktion von $f$ ist
eine Funktion $F$, für die gilt: 

$$F'(x) = f(x) $$

Beispiel:
$$f(x) = 2x + 1$$
$$F_{1}(x) = x2 + x$$
$$F_{2}(x) = x2 + x + 424242$$

Beobachtung

Gegeben sind eine Stammfunktion $F$ einer Funktion $f$ und eine
Konstante $c$. Dann ist auch die Funktion $F_{2}$ mit $F_{2}(x) = F(x)+c$
eine Stammfunktion von $f$.

![unbestimmte Integral](./ana-files/Screenshot%202023-01-03%20211024.png){ width=20% }

Gegeben sind zwei Stammfunktionen $F_{1}$ und $F_{2}$ einer Funktion $f$. Dann gibt es eine Konstante $c$, so dass gilt:

$$F_{2}(x) = F_{1}(x) + c$$

Der untenstehende Satz ist Teil vom sogenannten Hauptsatz der Differential- und Integralrechnung.

Gegeben ist eine Funktion $f$, die auf einem Intervall $I$ stetig ist, und eine beliebige Stammfunktion $F$ von $f$. Dann gilt für alle $a, b \in I$ :

$$\int_{a}^{b}f(x)dx=F(b)-F(a)$$

*Somit kann man das Berechnen eines bestimmten Integrals lediglich mit Hilfe von Stammfunktionen bewerkstelligen!*

Integrationsregeln

Gegeben sind zwei Funktionen $f$ und $g$ mit Stammfunktionen $F$ bzw. $G$ sowie eine Konstante
$c$. Dann gilt:

1.  $c \cdot F(x)$ ist eine Stammfunktion von $c \cdot f(x)$
2.  $F(x) + G(x)$ ist eine Stammfunktion von $f(x) + g(x)$

Wir geben im Folgenden die Ableitungen/Integrale einiger Funktionen an (ohne Herleitung).

**Potenz- und Logarithmus-Funktionen**

* $\int a^{x}dx = \frac{a^{x}}{\ln (a)}+C$
* $\int \ln (x)dx = x \cdot\ln(x)-x+C$
* $\int \log(x)dx = \frac{1}{\ln(a)}\cdot  (x \cdot \ln(x) - x) + C$

**Trigonometrische Funktionen**

* $\int \sin(x)dx = -\cos(x)+C$
* $\int \cos(x)dx = \sin(x)+C$
* $\int \tan(x)dx = -\ln|\cos(x)| +C$

*Es gibt noch mehr aber werden unwahrscheinlich genutzt*


# Folgen und Reihen

## Begriff der Folge (direkt, rekursiv, arithmetisch, geometrisch)

**Darstellungen**

* Verbale Darstellung: ”Die Folge der positiven, geraden Zahlen”
* Aufzählende Darstellung: $2, 4, 6, 8, ...$
* Explizite Darstellung durch ein Bildungsgesetz: $a_{n} = 2n, n \in N^{\ast}$ 
* Implizite Darstellung durch eine Rekursionsformel:  $a_{1} = 2, a_{n+1} = a_{n}+2$

+--------------------------------------+----------------------------+---------------------------+-----------------------------------------------+
|                                      | **explizite Darstellung**  | **impliztite Darstellung**| **aufzählende Darstellung**                   |
|                                      |                            |                           |                                               |
+======================================+============================+===========================+===============================================+
|                                      |                            |                           |                                               |
| Arithmetische Folge                  | $a_{n} = c+ (n-1)d$        | $a_{1} = c$               | $c,c+d,c+2d,c+3d,...$                         |
| $(x,d)\in \mathbb{R}$                |                            | $a_{n+1} = a_{n}+d$       |                                               |
|                                      |                            |                           |                                               |
+--------------------------------------+----------------------------+---------------------------+-----------------------------------------------+
|                                      |                            |                           |                                               |
| geometrische Folge                   | $a_{n} = c \cdot q^{n-1}$  | $a_{1} = c$               | $c,c\cdot q,c\cdot q^{2},c\cdot q^{3},...$    |
| $(c,q \in \mathbb{R}, q \neq 0,1)$   |                            | $a_{n+1} = q \cdot a_{n}$ |                                               |
|                                      |                            |                           |                                               |
+--------------------------------------+----------------------------+---------------------------+-----------------------------------------------+
|                                      |                            |                           |                                               |
| harmonische Folge                    | $a_{n} = \frac{1}{n}$      | (nicht üblich)            | $1,\frac{1}{2},\frac{1}{3},\frac{1}{4},...$   |
|                                      |                            |                           |                                               |
+--------------------------------------+----------------------------+---------------------------+-----------------------------------------------+
|                                      |                            |                           |                                               |
| Fibonacci-Folge                      | (nicht elementar)          | $a_{1} = 1, a_{2} = 1$    | $1,1,2,3,5,8,13$                              |
|                                      |                            | $a_{n+2} = a_{n}+a_{n+1}$ |                                               |
|                                      |                            |                           |                                               |
+--------------------------------------+----------------------------+---------------------------+-----------------------------------------------+


## Grenzwertbegriff (Monotonie, Beschränktheit, Rechenregeln, Limes einer Funktion)

**Definition**
$g$ heisst Grenzwert einer Folge, wenn die Folgenglieder ab einem gewissen $n$ dem Wert $g$ beliebig nahe kommen.

> Das Ziel ist es nun, den Begriff Grenzwert präzis zu definieren.

Beispiele:

1. $1, \frac{1}{2}, \frac{1}{4}, \frac{1}{8},...$ der Grenzwert ist null also: $\lim_{n\rightarrow \infty } a_{n} =0$
2. $0.3, 0.33, 0.333, ...$ also: $\lim_{n\rightarrow \infty } a_{n} = \frac{1}{3}(=0.\overline{3})$

Eine reelle Zahl $g$ heisst Grenzwert oder Limes der Folge $(a_{n})$, wenn es zu jedem $\varepsilon  > 0$ eine
natürliche Zahl $n_{0}$ gibt, so dass für alle $n \geq n_{0}$ stets $|a_{n} - g| < \varepsilon$ gilt.
Eine Folge heisst konvergent (”sie konvergiert”), wenn sie einen Grenzwert $g$ hat

**Grenzwert einer Funktion im Endlichen**

Wir betrachten eine Funktion $f(x)$ und eine Stelle $x_{0}$. Dann bezeichnet der Grenzwert $g$ von
$f(x)$ an $x_{0}$ denjenigen Wert, dem sich die Funktion annähert, wenn $x$ immer mehr gegen $x_{0}$ geht.

> Schreibweise: $\lim_{ x \rightarrow x_{0}} f(x)=g$ oder $f(x)\rightarrow g$ für $x\rightarrow x_{0}$ 

**Rechenregel**

1. $\lim_{n\rightarrow \infty }(c\cdot a_{n}) = c\cdot\lim_{n\rightarrow \infty }a_{n}$
2. $\lim_{n\rightarrow \infty }(a_{n}+ b_{n}) = \lim_{n\rightarrow \infty }(b_{n})+\lim_{n\rightarrow \infty }(a_{n})$ 
3. $\lim_{n\rightarrow \infty }(a_{n}\cdot b_{n}) = \lim_{n\rightarrow \infty }(b_{n})\cdot\lim_{n\rightarrow \infty }(a_{n})$
4. $\lim_{n\rightarrow \infty }(\frac{a_{n}}{b_{n}}) = \frac{lim_{n\rightarrow \infty }(a_{n})}{lim_{n\rightarrow \infty }(b_{n})}$

**Monotonie**

Für eine monoton wachsende, differenzierbare Funktion $f$ gilt: Ihre Steigung (d.h. $f'(x))$ ist $\geq  0$.
Die Umkehrung ist ebenfalls richtig: Ist $f'(x) \geq  0$, so wächst $f$ monoton.
Analoge Gesetzmässigkeiten gelten natürlich für monoton fallende Funktionen

> $f'(x)$ ist auf einem Intervall überall $\geq  0 \Leftrightarrow f$ ist auf diesem Intervall monoton steigend.
> $f'(x)$ ist auf einem Intervall überall $\leq 0 \Leftrightarrow f$ ist auf diesem Intervall monoton fallend.


# Erweiterung der Differentialrechnung

**Stetigkeit**

Eine Funktion $f(x)$ heisst stetig an der Stelle $x_{0}$, wenn der Grenzwert $\lim_{x\rightarrow x_{0}}f(x)$ existiert und $= f(x_{0})$ ist.

Eine Funktion heisst stetig, wenn sie an jeder Stelle ihres Definitionsbereiches stetig ist.
->
Eine Funktion ist auf einem Intervall I stetig, wenn sich ihr Graph in einem Zug, ohne Absetzen,
zeichnen lässt.

Viele Funktionen, die in der Praxis vorkommen, sind in ihrem Definitionsbereich stetig:

* Polynome
* rationale Funktionen
* $\sin(x), \cos(x), \tan(x)$
* Exponential- und Logarithmusfunktionen
* Potenzfunktionen, Wurzelfunktionen

Die Summe, die Differenz, das Produkt, die Komposition von stetigen Funktionen sind stetig.

$$f(x)=\left\{\begin{matrix}
x^{2} + 2a, & x< -1 \\ 
-x^{2} + 2a, & -1\leq  x\leq  1 \\ 
-x^{3} -3bx &  x> 1
\end{matrix}\right.$$

Wir setzen $f_{1}(x) := x^{2} + 2a, f_{2}(x) := -x^{2} + 5, f_{3}(x) = x^{3} - 3bx$.

Bedingungen für Stetigkeit:

* $f_{1}(x) = f_{2}(-1)$ resp.$ 1 + 2a = 4$
* $f_{2}(1) = f_{3}(1)$ resp. $4 = 1 - 3b$

Auflösen der obigen Gleichungen ergibt $a = 1.5$ und $b = -1$

**Wendepunkt und Sattelpunkt**

Punkte, an denen sich das Krümmungsverhalten des Graphen ändert (d.h. bei denen eine
Linkskurve in eine Rechtskurve übergeht oder umgekehrt), heissen Wendepunkte.
Wendepunkte mit horizontaler Tangente heissen Sattelpunkte.

![Wendepunkte ](./ana-files/Screenshot%202023-01-04%20210712.png){ width=50% }
![Sattelpunkt ](./ana-files/Screenshot%202023-01-04%20210749.png){ width=50% }

Hinreichende Bedingung für Wendepunkte:

Eine Funktion $f$ besitzt an der Stelle $x_{0}$ einen Wendepunkt, wenn gilt:

$$f''(x_{0}) = 0 und f'''(x_{0}) \neq 0$$


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
Fragenkatalog für die Kurvendiskussion

1. Definitionsbereich?
2. Symmetrieeigenschaften (gerade/ungerade), Periode?
3. Schnittpunkte mit Achsen, Polstellen?
4. Randpunkte bzw. Verhalten, wenn $x$ gegen die Grenzen des Definitionsbereichs strebt?
5. Kandidaten für Extrema bestimmen und untersuchen
6. Wendepunkte suchen
7. Tabelle von Werten aufstellen (falls noch nötig)


## Extremwertaufgaben

Eine Funktion $f(x)$ besitzt an der Stelle $x_{0}$ ein absolutes $\begin{Bmatrix}Maximum\\Minimum\end{Bmatrix}$ wenn für jedes $x$ im Definitionsbereich von $f$ gilt: $\begin{Bmatrix}f(x_{0})\geq f(x)\\f(x_{0})\leq  f(x)\end{Bmatrix}$

Hilfreiche Schritte beim Lösen von Extremwertaufgaben

1. Zielgrösse identifizieren.
2. Unabhängige Variable identifizieren.
3. Definitionsbereich bestimmen.
4. Zielgrösse als Funktion der unabhängigen Variablen ausdrücken; ev. eine qualitative Skizze des Graphen machen.
5. Relative Maxima resp. Minima bestimmen; Randpunkte auch berücksichtigen!
6. Untersuchen, welche der relativen Extrema auch absolute Extrema sind (inklusive – bei offenen und halboffenen Intervallen – Betrachtung der Funktion in der Nähe des Randes)
7. Die gesuchte Information aus den Berechnungen extrahieren. (Ev. nachschauen, nach welcher Grösse gefragt wurde: Extremalstelle? Extremalwert? Extremalpunkt?)


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

