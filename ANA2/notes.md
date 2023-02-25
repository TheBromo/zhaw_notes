---
title:  'Analysis 2'
author:
- Manuel Strenge
keywords: [ANA 2, pain]
...

Gebiet                  Problemstellung     math. Grundlagen
----------              ------------        ----------
Simlulationen           Haare               Differentialgleichungen
Comp. Grafik            2D render Tasse     Integralrechnung
Scientific Computing    Daten ana           Taylor-Reihen


# Integrationsmethoden

*Einsatzgebiet: modelieren: z.B. $v(t)=t^2$*

Im Allgemeinen: $\int u(x) \cdot v(x) dx \neq \int u(x) dx \cdot \int v(x) dx$ 

**Repetition:**

Produktregel: $(u(x)\cdot v(x))' = u'(x) \cdot v(x) + u(x) \cdot v'(x)$

Kettenregel: $(F(u(x)))'=F'(x) \cdot u'(x)$

## Integration durch Substitution

Diese Integrationsmethode beruht auf der Kettenregel für die Ableitung:

$(F(u(x))) = \int (F(u(x)))' dx = \int F'(x) \cdot u'(x) dx$

Im Folgenden sind die einzelnen Schritte dieser Integrationsmethode angegeben. Diese werden jeweils gleich auf die beiden folgenden Beispiele angewendet.

- $\int \cos \left(x^2\right) \cdot x \mathrm{~d} x \quad \text { (unbestimmtes Integral) }$
- $\int_0 \cos \left(x^2\right) \cdot x \mathrm{~d} x \quad \text { (bestimmtes Integral) }$



**1. Schritt: Substitutionsgleichung für $x: u = g(x)$**


$u(x) = x^2$

**2. Schritt: Substitutionsgleichung für dx: $\frac{\mathrm{d} u}{\mathrm{~d} x}=g^{\prime}(x) \Rightarrow \mathrm{d} x=\frac{\mathrm{d} u}{g^{\prime}(x)}$**

$\text { Dabei tun wir so, als ob die Ableitung } \frac{\mathrm{d} u}{\mathrm{~d} x} \text { ein Bruch wäre. }{ }^1$

$\text { - Beispiele (a) und (b): } \frac{d u}{d x}=u^{\prime}(x)=2 x \Rightarrow d x=\frac{d y}{2 x}$


**3. Schritt: Integralsubstitution: $\int f(x) \mathrm{d} x=\int \varphi(u) \mathrm{d} u$**

Wir ersetzen nun im Integral $g(x)$ und $dx$ gemäss den Substitutionsgleichungen. In dem resultierenden Integral kommen dann beide Variablen $x$ und $u$ vor; es ist somit streng genommen gar nicht wohldefiniert. Die Variable $x$ muss nun durch Kürzen zum Verschwinden gebracht werden! Ist dies nicht möglich, so haben wir den falschen Ansatz gewählt.

$$\int \cos \left(x^2\right) \cdot x d x-\int \cos (u) \cdot x \frac{d u}{\underline{2} x}=\int \frac{1}{2} \cos (u) d u$$

Beim bestimmten Integral muss die Funktion g auch auf die Integrationsgrenzen angewendet
werden (denn diese bezogen sich im Anfangsintegral auf die Variable x und müssen nun in
Abhängigkeit von u ausgedrückt werden)

$\text { Beispiel (b) } \int_{x=0}^{\sqrt{\pi / 2}} \cos \left(x^2\right) \cdot x d x=\int_{u=0^2}^{(\sqrt{\pi / 2})^2} \cos (u) \cdot x \cdot \frac{d u}{2 x}=\int_{u=0}^{\pi / 2} \frac{1}{2} \cos (u) d u$

**4. Schritt: Integration: $\int \varphi(u) \mathrm{d} u=\Phi(u)+C$**

Im Idealfall können wir das Integral von $\varphi(u)$ (z.B. mit bekannten Regeln) nun bestimmen.


**Beispiel (a)**

$\int \frac{1}{2} \cos (u) d u=\frac{1}{2} \int \cos (u) d u=\frac{1}{2} \sin (u)+C$


**Beispiel (b)**
$$
\begin{aligned} 
\int_0^{\pi / 2} \frac{1}{2} \cos (u) d u=\frac{1}{2} \int_0^{\pi / 2} \cos (u) d u & =\frac{1}{2}[\sin (u))_0]^{\pi / 2} \\
& =\frac{1}{2}(1-0)=\frac{1}{2}
\end{aligned}
$$

**5. Schritt: Rücksubstition**

Dieser Schritt ist nur bei unbestimmten Integralen nötig. Bei bestimmten Integralen bleibt der
Integralwert durch die Substitution der Integralgrenzen erhalten.

$\frac{1}{2} \sin (u)+C=\frac{1}{2} \sin \left(x^2\right)+C$

Integration durch Substitution
1. Substitutionsgleichung für $x: u=g(x)$
2. Substitutionsgleichung für $\mathrm{d} x$ : $\frac{\mathrm{d} u}{\mathrm{~d} x}=g^{\prime}(x) \Rightarrow \mathrm{d} x=\frac{\mathrm{d} u}{g^{\prime}(x)}$
3. Integralsubstitution
4. Integration
5. Rücksubstitution (nur für unbestimmte Integrale)

> Wichtig! nicht vergessen die substitutionsgleichung auf die integral grenzwerte anzuwenden.

*Satz*

*Für eine Funktion $f$ und Konstanten $a, b$ gilt:*

$$
\int f(a x+b) \mathrm{d} x=\frac{1}{a} \cdot F(a x+b)
$$