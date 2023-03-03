---
title:  'Lineare Algebra'
author:
- Manuel Strenge
keywords: [LA, pain]
...


# Vektoren

## Sinn 

Wenn eine Grösse mit einem wert dargestellt werden kann, wie z.B. Temperator, dann wird es skalar genannt.
$skalare =$ reele zahlen.

Gewisse physische faktoren können nicht nur mit einer nummer dargestellt werden. z.B. Richtung.

**Ein Vektor $R^3$ kann durch 3 reele Zahlen, ein 3-Tupel beschrieben werden.**

> Für 2- oder 3-Tupel lassen sich die Rechenoperationen auch
> geometrisch veranschaulichen. Für allgemeine n-Tupel ist das
> nicht möglich, trotzdem ist die geometrische Anschauung für
> n = 2 oder n = 3 oft der Schlüssel zur Lösung komplizierter
> Probleme.

## Definition

Ein n-Tupel $( a_{1}, a_{2}, . . . , a_{n} ) \in R^{n}$ nennt man auch Vektor.
Die reellen Zahlen $a_{1}, a_{2}, . . ., a_{n}$ heissen die Koordinaten oder Komponenten des Vektors.

Die Komponenten eines Vektors schreiben wir häufig als
Spalten:
$$\underset{a}{\rightarrow} =\begin{pmatrix}a_{1} \\ a_{2} \\ ... \\ a_{n}\\ \end{pmatrix} = R^{n}$$

Zwei Vektoren sind gleich, wenn sie koordinatenweise
übereinstimmen. Die Vektorgleichung $\underset{a}{\rightarrow} = \underset{b}{\rightarrow}$ ist also nichts anderes als eine abkürzende Schreibweise für die $n$ Gleichungen.

$$a_{1} = b_{1} a_{2} = b_{2} ... a_{n} = b_{n} $$

Vektoren in $R^{2}$ bzw. in $R^{3}$ können wir uns als Pfeile vorstellen und der Pfeil darf vom beliebigen Punkt eingezeichnet werden.


Um einen Vektor $\vec{a} = \begin{pmatrix}a_{x} \\ a_{y}\end{pmatrix}$ in $R^{2}$ einzuzeichnen:

1. wählt man einen Anfangspunkt,
2. geht ax Schritte entlang der x-Achse und ay Schritte entlang der y-Achse,
3. erreicht so den Endpunkt des Vektors.

![Eingezeichnete Ortsvektoren](./img/00_vec_vis.png){ width=50% }

Der Vektor $\begin{pmatrix} 1 \\ 2 \\ \end{pmatrix}$ wird auch als Pfeil ausgehend vom Ursprung $O$

Seine Spitze beschreibt den Ort jenes Punktes, dessen Koordinaten
gleich den Komponenten des Vektors sind. Um zu betonen, dass es
der Ortsvektor des Punktes $P$ ist, schreibt man $\vec{OP}$.

[Siehe bild unter definition vektor](#definition)

Zusammenfassend darf der Pfeil in $R^{2}$ bzw. $R^{3}$ beliebig parallel verschoben werden. Es bleibt immer der gleiche Vektor: $\vec{v} = \vec{OP}$

![Insbesondere lautet dieser Zusammenhang für den Ortsvektor ](./img/01_vec_ebenen.png){ width=50% }

**Definition**

> Der Vektor, dessen Anfangspunkt und Endpunkt übereinstimmen, heisst der Nullvektor und wird durch $\vec{0}$ bezeichnet.


## Addition, Subtraktion und Skalarmultiplikation

**Definition**
Die Summe zweier Vektoren der gleichen Dimension $n$ ist
komponentenweise definiert und ergibt wieder einen
$n$-dimensionalen Vektor:

![vector addition](./img/02_vec_addition.png){ width=50% }

**Geometrische betrachtungsweise**

Die geometrische Addition der Vektoren $\vec{a}$ und $\vec{b}$:

1. Der Vektor $\vec{b}$ wird parallel zu sich selbst verschoben, bis sein Anfangspunkt auf den Endpunkt des Vektors $\vec{a}$ trifft
2. Der Anfangspunkt des Vektors $\vec{a}$ wird mit dem Endpunkt des Vektors $\vec{b}$ verbunden. Der resultierende Pfeil repräsentiert den Summenvektor $\vec{c} = \vec{a} + \vec{b}$.

![vector addition geomoetrisch visualisiert](./img/03_vec_add_geo.png){ width=50% }


$$\vec{a} + \vec{b} = \begin{pmatrix} 7 \\ 5 \\ \end{pmatrix}+ \begin{pmatrix} -2 \\ 4 \\ \end{pmatrix} = \begin{pmatrix} 5 \\ 9 \\ \end{pmatrix}$$ 

**Kommutativgesetz**

$\vec{a} + \vec{b} =   \vec{b} + \vec{a}$.

**Assoziativgesetz**

$(\vec{a} + \vec{b}) + \vec{c} =\vec{a} + (\vec{b} + \vec{c})$.

**Der Nullvektor ist das Neutralelement der Addition**

$\vec{a}+ \vec{0} = \vec{a}$

**Zu jedem Vektor  $\vec{a}$ gibt es genau einen Gegenvektor $-\vec{a} \in R^{n}$ mit**

$\vec{a}+ (- \vec{a}) =  \vec{0}$


Die Subtraktion zweier Vektoren lässt sich wie bei den reellen
Zahlen als Umkehrung der Addition auffassen und damit auf die
Addition zweier Vektoren zurückführen:

**Definition**

Die Subtraktion oder die Differenz von zwei Vektoren $\vec{a}$ und $\vec{b}$ ist
definiert als die Summe von $\vec{a}$ und $-\vec{b}$, dem Gegenvektor zu $\vec{b}$, also:

$\vec{a} - \vec{b} =\vec{a} + (-\vec{b})$


## Multiplikation

Bei der Multiplikation eines Vektors mit einem Skalar $\lambda$ wird jede
Komponente mit $\lambda$ multipliziert:

![](./img/04_multi.png)


Das Ergebnis ist wieder ein Vektor im $R^n$.

Die Anschauung der Multiplikation eines Vektors mit einem Skalar im $R^2$:


![](./img/05_visu.png)

## Kollineare und windschiefe Vektoren

### Definition

2 Vektoren $\vec{a}$ und $\vec{b}$ heissen kollinear, wenn es eine reelle Zahl $\lambda$
gibt, so dass $\vec{a} = \lambda \vec{b}$. Dies bedeutet, dass $\vec{a}$ ein Vielfaches von $\vec{b}$
ist. Existiert keine solche Zahl, dann sagen wir, dass $\vec{a}$ und $\vec{b}$
windschief oder nichtkollinear sind. 

![](./img/06_koll.png)

##  Linearkombination

### Definition

![](./img/07_linkom.png)

## Weitere Rechengesetze für Vektoren

![](./img/08_gesetz.png)


# Betrag

Der Betrag eines Vektors ist eine reelle Zahl, die >= 0 ist und der
Länge dieses Vektors entspricht.


![](./img/09_betrag.png)
cc
## Rechenregeln

![](./img/10_regel.png)

## Einheitsvektoren

![](./img/11_einheit.png)

## Skalarprodukte

### Definition

Skalarprodukte treten z.B. im Zusammenhang mit den folgenden
Grössen auf:

- Arbeit einer Kraft beim Verschieben einer Masse,
- Normalform einer Geraden in der Ebene oder einer Ebene.

Das Skalarprodukt zweier Vektoren $\vec{a} \text { und } \vec{b} \text { in } \mathbb{R}^n$ ist ein Skalar
$\vec{a} \cdot \vec{b} \in \mathbb{R}$ (gelesen: a Punkt b), der auf zwei verschiedene Arten
berechnet werden kann:

- aus den Beträgen der beiden Vektoren und dem Kosinus des von den Vektoren eingeschlossenen Winkels $\varphi$:


$$\vec{a} \cdot \vec{b}=|\vec{a}||\vec{b}| \cos (\varphi)$$

- aus den Komponenten der beiden Vektoren:


$$\vec{a} \cdot \vec{b}=a_1 b_1+a_2 b_2+\ldots+a_n b_n=\sum_{i=1}^n a_i b_i$$


- Das Skalarprodukt ist eine skalare Grösse und wird auch als inneres Produkt der Vektoren  $\vec{a}$ und $\vec{b}$ bezeichnet

- Das Skalarprodukt lässt sich auch als: $(\vec{a}, \vec{b}), \quad<\vec{a} \mid \vec{b}>$ oder $\vec{a}^{\top} \vec{b}$ schreiben

- Man beachte, dass der Winkel $\varphi$ stets der kleinere der beiden Winkel ist, den die Vektoren $\vec{a}$ und $\vec{b}$ miteinander bilden.

![](./img/12_wink.png)

- $\text { Kommutativgesetz: } \vec{a} \cdot \vec{b}=\vec{b} \cdot \vec{a} \text { für alle Vektoren } \vec{a}, \vec{b} \in \mathbb{R}^n \text {. }$

- Distributivgesetz:
$$
\vec{a} \cdot(\vec{b}+\vec{c})=\vec{a} \cdot \vec{b}+\vec{a} \cdot \vec{c} \quad \text { für alle } \vec{a}, \vec{b}, \vec{c} \in \mathbb{R}^n .
$$

- Gemischtes Assoziativgesetz:
$\lambda(\vec{a} \cdot \vec{b})=(\lambda \vec{a}) \cdot \vec{b}=\vec{a} \cdot(\lambda \vec{b}) \quad$ für alle $\vec{a}, \vec{b} \in \mathbb{R}^n$ und alle $\lambda \in \mathbb{R}$.

Das Skalarprodukt $\vec{a} \cdot \vec{b}$ zweier vom Nullvektor verschiedener
Vektoren kann nur verschwinden, wenn $\cos (\varphi)=0, \text { d.h. } \varphi=90^{\circ}\left(\operatorname{oder} \frac{\pi}{2}\right)$ ist. In diesem Fall stehen die Vektoren senkrecht.
Diese Vektoren heissen orthogonale Vektoren, im Zeichen. $\vec{a} \perp \vec{b}$
Wir haben die Äquivalenz:
$$\vec{a} \cdot \vec{b}=0 \Leftrightarrow \vec{a} \perp \vec{b} .$$


## Berechnung des Winkels 

Mit Hilfe der Gleichung

$$\vec{a} \cdot \vec{b}=|\vec{a}||\vec{b}| \cos (\varphi)=\sum_{i=1}^n a_i b_i$$

kann man den Winkel $\varphi$ zwischen $\vec{a}$ und $\vec{b}$ berechnen:

$$\cos (\varphi)=\frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|}=\frac{\sum_{i=1}^n a_i b_i}{|\vec{a}||\vec{b}|}$$

Wobei $\vec{a} \neq \overrightarrow{0} \text { und } \vec{b} \neq \overrightarrow{0}$ . Durch Umkehrung folgt schliesslich:

$$\varphi=\arccos \left(\frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|}\right) \text {, wobei } \vec{a} \neq \overrightarrow{0} \text { und } \vec{b} \neq \overrightarrow{0}$$


## Projektion eines Vektors auf einen zweiten Vektor


![](./img/13_proj.png)

Der durch die Projektion erhaltene Vektor wird mit $\vec{ba}$ bezeichnet.
Es gilt:

$$\cos (\varphi)=\frac{\text { Ankathete }}{\text { Hypotenuse }}=\frac{\left|\vec{b}_a\right|}{|\vec{b}|}$$

wobei $\varphi$ der Winkel zwischen $\vec{a}$ und $\vec{b}$ ist. Sein Betrag lautet somit:

$$
\left|\vec{b}_a\right|=|\vec{b}| \cos (\varphi)
$$


Aus dem Skalarprodukt erhalten wir: $\cos (\varphi)=\frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|}$

Es folgt: $$\left|\vec{b}_a\right|=|\vec{b}| \frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|} \Leftrightarrow\left|\vec{b}_a\right|=\frac{\vec{a} \cdot \vec{b}}{|\vec{a}|}$$

## Berechnung des Winkels $\varphi$


Mit Hilfe der Gleichung


$$\vec{a} \cdot \vec{b}=|\vec{a}||\vec{b}| \cos (\varphi)=\sum_{i=1}^n a_i b_i$$

kann man den Winkel $\varphi$ zwischen $\vec{a}$ und $\vec{b}$ berechnen:

$$\cos (\varphi)=\frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|}=\frac{\sum_{i=1}^n a_i b_i}{|\vec{a}||\vec{b}|}$$

$$\varphi=\arccos \left(\frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|}\right) \text {, wobei } \vec{a} \neq \overrightarrow{0} \text { und } \vec{b} \neq \overrightarrow{0} \text {. }$$


Unter dem Vektorprodukt $\vec{a} \times \vec{b}$ zweier Vektoren $\vec{a} \text { und } \vec{b} \text { in } \mathbb{R}^3$ versteht man den eindeutig bestimmten Vektor, der wie folgt berechnet wird:

$$
\vec{a} \times \vec{b}=\left(\begin{array}{c}
a_x \\
a_y \\
a_z
\end{array}\right) \times\left(\begin{array}{l}
b_x \\
b_y \\
b_z
\end{array}\right)=\left(\begin{array}{c}
a_y b_z-a_z b_y \\
a_z b_x-a_x b_z \\
a_x b_y-a_y b_x
\end{array}\right)
$$

Diese Formel kann man sich anhand des folgenden Schemas merken:

![](./img/14_vecprod.png)

Zwei vom Nullvektor verschiedene Vektoren $\vec{a}$ und $\vec{b}$ sind genau
dann kollinear, wenn ihr Vektorprodukt verschwindet:

$$\vec{a} \times \vec{b}=\overrightarrow{0} \quad \Leftrightarrow \quad \vec{a} \text { und } \vec{b} \text { sind kollinear }$$


Distributivgesetze: $\vec{a} \times(\vec{b}+\vec{c})=\vec{a} \times \vec{b}+\vec{a} \times \vec{c}$ und $(\vec{a}+\vec{b}) \times \vec{c}=\vec{a} \times \vec{c}+\vec{b} \times \vec{c}$

$\text { Anti-Kommutativgesetz: } \vec{a} \times \vec{b}=-(\vec{b} \times \vec{a}) \text {. }$

$\text { Assoziativgesetz: } \lambda(\vec{a} \times \vec{b})=(\lambda \vec{a}) \times \vec{b}=\vec{a} \times(\lambda \vec{b}) \text {. }$

## Spatprodukt

Unter dem Spatprodukt $\left[\begin{array}{lll}\vec{a} & \vec{b} & \vec{c}\end{array}\right]$ dreier Vektoren $\vec{a}, \vec{b}$ und $\vec{c}$ in $\mathbb{R}^3$ versteht man das Skalarprodukt aus dem Vektor $\vec{a}$ und dem aus den Vektoren $\vec{b}$ und $\vec{c}$ gebildeten Vektorprodukt $\vec{b} \times \vec{c}:$

$$\left[\begin{array}{lll}\vec{a} & \vec{b} & \vec{c}\end{array}\right]=\vec{a} \cdot(\vec{b} \times \vec{c})$$

### Spatprodukt und Volumen

Die drei Vektoren
$\vec{a}, \vec{b}$ und $\vec{c}$ spannen
ein sogenanntes
Parallelepiped (auch
Spat, Parallelflach
oder Parallelotop
genannt) auf.

![](./img/15_SpatProd.png)

Dem Betrag des Spatproduktes $\left[\begin{array}{lll}\vec{a} & \vec{b} & \vec{c}\end{array}\right]$ kommt dabei die
geometrische Bedeutung des Spatvolumens zu.
Aus der Elementarmathematik haben wir die Formel:

Volumen $=$ Grundfläche mal Höhe $\Leftrightarrow V=\mathcal{A} h$.

