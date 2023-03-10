---
title:  'Theoretische Informatik'
author:
- Manuel Strenge
keywords: [TH, pain]
...

# Aplhabete

> **Mächtig was ist die Decke der Menge: Unendlich=sehr mächtig**

Ein Alphabet ist eine endliche, nichtleere Menge von Symbolen

{:),2} -> alphabet

{1,2,3} -> alphabet

{1,2,3,...} -> kein da nicht endlich

{a,...,b}  -> alphabet

{a,a,a}-> ja

![](./img/00_alphabet.png)

# Wort

Ein Wort (Zeichenreihe, String) ist eine endliche Folge von Symbolen
eines bestimmten Alphabets

![](./img/01_wort.png)

## Leeres Wort

Das **leere** Wort ist ein Wort, das keine Symbole enthält. Es wird durch
das Symbol $\varepsilon$ dargestellt und ist ein Wort über jedem Alphabet.

# Wörter

Die Länge eines Wortes $w$ ist die Länge des Wortes als Folge, also die
Anzahl der Symbole der Folge. Wir bezeichnen diese Länge mit $|w|$.

![](./img/02_woerter.png)

## Definition (Häufigkeit eines Symbols in einem Wort)

$|w|_{x}$ bezeichnet die absolute Häufigkeit eines Symbols $x$ in einem
Wortes $w$.

![](./img/03_woerter.png)


## Definition (Spiegelung eines Wort)

Mit $w^R$ wird das Spiegelwort zu $w$ bezeichnet.

$$w^{R} = (x_{1}, x_{2} . . . x_{n})^R = x_{n} . . . x_{2}, x_{1}$$

Es gilt $|w| = |w^{R}| und |w|_{x} = |w^{R}|_{x} für alle x \in \sum$. Wenn $w = w R$ gilt, dann bezeichnet man w als Palindrom.

![](./img/04_woerter.png)

## Definition (Teilwort)

Wir sagen, dass $v$ ein Teilwort (Infix) von $w$ ist, wenn man $w$ als

$$w=xvy$$

für beliebige Wörter $x$ und $y$ über $\sum$ schreiben kann

![](./img/05_infix.png)

## Definition (echtes Teilwort)

Ein echtes Teilwort von $w$ ist jedes Teilwort von $w$, das nicht identisch
mit $w$ ist (in diesem Falle ist $x$ oder $y$ nicht leer).

![](./img/06_echt_twort.png)

In Programmiersprachen ist der Begriff substring gebräuchlich.


## Präfix

Ein Wort $v$ ist ein Präfix von $w$, wenn

$$w=xy$$

![](./img/07_prefix.png)

Ein echtes Präfix von w ist jedes Präfix von w, das nicht identisch mit w
ist (in diesem Fall ist y leer).

![](./img/08_prefix.png)

## Definition (Suffix)

Ein Wort v ist ein Suffix von w, wenn

$$w=xv$$

![](./img/09_suffic.png)

Ein echtes Suffix von w ist jedes Suffix von w, das nicht identisch mit w
ist (in diesem Fall ist x leer).


![](./img/10_suffix.png)


## Definition (Menge aller Wörter der Länge k)

Die Menge aller Wörter der Länge k über einem Alphabet $\sum$ wird mit
$\sum^{k}$ bezeichnet.

![](./img/11_example.png)

## Definition (Menge aller Wörter (Zeichenreihen))


Die Menge aller Wörter (Kleenesche Hülle) über einem Alphabet $\sum$
wird mit $\sum^{*}$ bezeichnet.
$\sum+ = \sum* \ {\varepsilon}$ ist die Menge aller nichtleeren Wörter (positive
Hülle) über einem Alphabet $\sum$.

> Regex definitionen ursprung von hier. 

![](./img/12_l%C3%A4nge.png)

### Eigenschaften

![](./img/Eigenschaften.png)


## Definition (Konkatenation)

Definition (Konkatenation) Seien $x$ und $y$ zwei beliebige Wörter. Dann steht

$x \circ y = xy := (x_{1}, x_{2} . . . x_{n}, y_{1}, y_{2} . . . y_{m})$

für die Konkatenation (Verkettung) von $x$ und $y$.

![](./img/13_konkat.png)

## Definition (Wortpotenzen)

Sei $x$ ein Wort über einem Alphabet $\sum$. Für alle $n \in N$ sind
Wortpotenzen wie folgt definiert:

![](./img/14_w_pot.png)

![](./img/15_w_pot_ex.png)


## Definition (Sprache)

Eine Teilmenge $L \subseteq  \sum^{*}$ von Wörtern über einem Alphabet $\sum$ wird als Sprache über $\sum$ bezeichnet.

![](./img/16_ex_lang.png)


### Anmerkungen:
- Sprachen können aus unendlich vielen Wörtern bestehen.
- Wörter müssen aus einem festen, endlichen Alphabet gebildet werden.
- Wörter selber haben eine endliche Länge.

## Definition (Konkatenation von Sprachen)

Sind $A \subset \sum^{*}$ und $B \subset \tau^{*}$ beliebige Sprachen, dann wird die Menge

$$AB = {uv | u \in A und v \in B}$$

![](./img/17_sprache.png)

# Reguläre Ausdrücke

Reguläre Ausdrücke sind Wörter, die Sprachen beschreiben, also eine
Möglichkeit (gewisse) Sprachen endlich zu repräsentieren.


- Die Syntax der regulären Ausdrücke befasst sich mit der Frage, welche Form diese Wörter haben.
- In der Semantik der regulären Ausdrücke wird erklärt, wie man reguläre Ausdrücke als Sprachen interpretiert.

![](./img/18_regex.png)
![](./img/19_regex.png)
![](./img/20_regex.png)

## Definition (Reguläre Ausdrücke)

Es sei $\sum$ ein beliebiges Alphabet. Die Sprache $RA \sum$ der regulären
Ausdrücke über $\sum$ ist wie folgt definiert:

![](./img/21_regex.png)

## Erläuterungen zur Definition

- Die Sonderzeichen $\varepsilon$ und $\varnothing$ sind reguläre Ausdrücke.
- Jedes Symbol aus dem Alphabet $\sum$ ist auch ein regulärer Ausdruck über $\sum$.
- Ist $R$ ein regulärer Ausdruck über $\sum$, dann ist auch $(R^{*})$ ein regulärer Ausdruck über $\sum$.
- Sind $R$ und $S$ reguläre Ausdrücke über $\sum$, dann sind auch $(RS)$ und $(R|S)$ Ausdrücke über $\sum$.

# Eigenschaften und Konventionen:

![](./img/22_regex.png)

![](./img/23_regex.png)


# Reguläre Sprachen

## Satz (Rechenregeln für reguläre Ausdrücke)

- L(R|S) = L(S|R)
- L(R(ST)) = L((RS)T)
- L(R|(S|T)) = L((R|S)|T)
- L(R(S|T)) = L(RS|RT)
- L((R\*)\*) = L(R\*)
- L(R|R) = L(R)

## Anwendungen von regulären Ausdrücken:

- Mustersuche in Texten
- Lexikalische Analyse (in Compilern); Erkennung von Schlüsselwörtern (“Token”)
- Syntax Test (bei einer einfachen Syntax)

# Endliche Automaten

Beispiel (Einstiegsaufgabe: Eintrittskarte Schwimmbad)

> Kosten 2.- (mindestens), Automat akzeptiert 0.50, 1.- und 2.-

![](./img/24_end_aut.png)

Ein **endlicher Automat** besteht aus (elementare Bausteine):

## Zuständen

![](./img/25_zustand.png)

## Eingabealphabet

0.50, 1.-,2.-

## Übergangsfunktionen

![](./img/25_uebergang.png)

> Wie wird die Eingabe eingegeben?
> -> Der endliche Automat liest das Wort von links nach rechts

> Wieviel Speicher steht zur Verfügung? Wie geht man mit dem Speicher um?
> -> Es gibt keinen Speicher.
> -> Variablen dürfen nicht benutzt werden.
> -> Der einzige (gespeicherte) Information ist der aktuelle Zustand.

> Wie wird die Ausgabe bestimmt (und ausgegeben)?
> -> Die Ausgabe erfolgt über akzeptierende Zustände.


![](./img/26_symbole.png)

## Definition (Endlicher Automat)


Ein (deterministischer) endlicher Automat (EA) ist ein Quintupel

$$M=\left(Q, \Sigma, \delta, q_0, F\right)$$

- endlichen Menge von Zuständen $Q=\left\{q_0, q_1, \ldots, q_n\right\}(n \in \mathbb{N})$
- Eingabealphabet $\Sigma=\left\{a_1, a_2, \ldots, a_m\right\}(m \in \mathbb{N})$
- Übergangsfunktion $\delta: Q \times N \rightarrow Q$
- Startzustand $q_0 \in Q$
- Menge der akzeptierenden Zustände $F \subseteq Q$

![](./img/27_ubergang.png)
![](./img/28_zustand.png)

##  Sind NEAs mächtiger als DEAs?

Es gibt einen DEA, der
die Sprache L akzeptiert.

vs

Es gibt einen NEA, der
die Sprache L akzeptiert.

Jeder DEA ist ein NEA.

Teilmengenkonstruktion (siehe nächste Folie)


### Beweiskonstruktion.

Sei $N=\left(Q_N, \Sigma, \delta_N, q_0, F_N\right)$ ein NEA

Der dazu äquivalente DEA $D=\left(Q_D, \Sigma, \delta_D, q_0, F_D\right)$ wird konstruiert
durch:
$$
Q_D=\mathcal{P}\left(Q_N\right)
$$
(Menge aller Teilmengen von $Q_N$ )

$$
F_D=\left\{S \in Q_D \mid S \cap F_N \neq \emptyset\right\}
$$
(alle Mengen aus $Q_D$, die mindestens einen akzeptierenden Zustand aus $F_N$ enthalten.)

$\delta_D(S, a)=\bigcup_{p \in S} \delta_N(p, a)$ für $S \in Q_D$ und $a \in \Sigma$
(Menge aller Zustände von $D$, die von den Zuständen aus $S$ durch
Lesen von $a$ erreichbar sind.)

## NEAs mit $\epsilon$ -Übergängen

Suche nach einem von mehreren Mustern:
$L_5=\left\{w \in\{a, b\}^* \mid w \text { enthält eines der Teilwörter } a b a, a b b, b a b\right\}$

![](./img/29_eig.png)

Ein nichtdeterministischer endlicher Automat mit $\varepsilon$-Übergängen ($\varepsilon$-NEA) wird beschrieben durch

$$M=\left(Q, \Sigma, \delta, q_0, F\right)$$

wobei $Q, \Sigma, q_0$ und $F$ wie beim deterministischen endlichen Automaten definiert sind und die Übergangsfunktion $\delta$ definiert ist als.

$$\delta: Q \times(\Sigma \cup\{\varepsilon\}) \rightarrow \mathcal{P}(Q)$$


## Äquivalenz DEA und RA

Satz (Gleichmächtigkeit von RA und DEA)

Es gibt einen $D E A$, der
$\Longleftrightarrow$
Es gibt einen $R A$, der die die Sprache L akzeptiert. Sprache $L$ akzeptiert.

**Beweis**

- Dynamische Programmierung: Für jedes Paar von Zuständen p, q regulären Ausdrück finden, der alle Wörter beschreibt, die von p nach q führen.
- RA in einen speziellen NEA umwandeln, der auch spontane Übergänge (ohne ein Eingabesymbol zu lesen) zulässt. Diese sogenannten $\varepsilon$-NEAs können in NEAs und somit durch Teilmengenkonstruktion in DEAs umgewandelt werden.

Die Klasse der **regulären Sprachen** beinhaltet alle Sprachen, die von
einem endlichen Automaten akzeptier t werden.
Jede dieser Sprachen wird regulär genannt.

## Zustandsklassen

$$\text { Klasse }[p]=\left\{w \in \Sigma^* \mid M \text { endet nach dem Lesen von } w \text { in } p\right\}$$

![](./img/30_zustand.png)

Die Menge alle Wörter $\Sigma^*$ wird von den Zustandsklassen $\left[p_0\right]$ bis $\left[p_n\right]$ partitioniert.

## Eigenschaften der Klassen:

- Jedes Wort landet in einem Zustand:
$$\Sigma^*=\bigcup_{p \in Q}[p]$$

- Kein Wort landet nach dem Lesen in zwei Zuständen:
$$[p] \cap[q]=\emptyset, \text { für alle } p \neq q, p, q \in Q$$

- Von M akzeptierte Sprache:
$$L(M)=\bigcup_{p \in F}[p]$$

## Grenzen endlicher Automaten

Wenn ein EA $M$ nach dem Lesen zweier Präfixe $x$ und $y$ im gleichen Zustand landet, kann er nicht mehr zwischen $x$ und $y$ unterscheiden.

Sei $M=\left(Q, \Sigma, \delta, q_0, F\right)$ ein $E A$ und $x$ und $y$ zwei beliebige Wörter aus $\Sigma^*$, so dass $x, y \in[p]$. Dann gilt für alle Wörter $z \in \Sigma^*$
$$
x z \in L(M) \quad \Longleftrightarrow \quad y z \in L(M) .
$$


Endlichen Automaten definieren: 5 Tupel
Übergang skizieren zustände
Konfiguration eines Automaten; eine momentaufnahem zustand und rest des eingabewortes (Q0,aabba)
Berechnung start, rechnungsschritte...., endkonfiguration (erfolg oder nein)
