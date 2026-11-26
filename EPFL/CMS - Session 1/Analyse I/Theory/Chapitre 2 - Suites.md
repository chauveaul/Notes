---
cours: Analyse I
chapitre: 2
source: "Chapitre 2 - Analyse I.pdf"
tags: [analyse-I, chapitre-2]
---

# Chapitre 2 — Analyse I

### 2.1 Exemples et raisonnement par récurrence

1) $0, 2, 4, 6, 8, \dots, 2n$ est la suite des nombres pairs

   $1, 3, 5, 7, 9, 11, \dots, 2n+1$ est la suite de nombres impairs

2) $2, 3, 5, 7, 11, 13, 17, 19, 23, 29, \dots$ est la suite des nombres premiers

3) $0, 1, \sqrt{2}, \sqrt{3}, 2, \sqrt{5}, \sqrt{6}, \sqrt{7}, \sqrt{8}, 3, \dots$ est la suite des racines carrées

4) $1, 1, 1, 1, 1, \dots$ est la suite constante.

5) Si on somme les éléments de la suite précédente :

   $1, 2, 3, 4, 5, \dots, n$

   et si on resomme les éléments en $n$ :

   $1, 3, 6, 10, 15, 21, 28$

Essayons de prouver que la somme des nombres
$$1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2}$$

$$
\begin{array}{r}
1 + 2 + 3 + \dots + (n-1) + n \\
+\ n + (n-1) + (n-2) + \dots + 2 + 1 \\ \hline
\underbrace{(n+1) + (n+1) + (n+1) \dots (n+1)}_{n \text{ termes}}
\end{array}
$$

Ainsi
$$1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2}$$

<u>**2) Preuve par récurrence.**</u>

On veut montrer que
$$S_n = 1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2} \quad \forall n \in \mathbb{N}^*$$

**i)** On vérifie $n = 1$ <span style="color:red">(initialisation)</span>
$$S_1 = 1 = \frac{1(1+1)}{2} \quad \checkmark$$

**ii)** Montrer que si $S_n = \dfrac{n(n+1)}{2}$, alors $S_{n+1} = \dfrac{(n+1)(n+2)}{2}$

<span style="color:red">(hérédité)</span>
$$S_{n+1} = \underbrace{1 + 2 + 3 + \dots + (n-1) + n}_{\frac{n(n+1)}{2}} + (n+1) = \frac{(n+1)(n+2)}{2} = S_{n+1} \quad \checkmark$$

#### Suite de Fibonacci

$$F_1 = 1,\quad F_0 = 0,\quad F_2 = F_1 + F_0 = 1,\quad F_3 = F_2 + F_1 = 2$$
$$F_4 = F_3 + F_2 = 3,\quad F_5 = F_4 + F_3 = 5,\quad F_6 = F_5 + F_4 = 8$$

$$F_{n+1} = F_n + F_{n-1}, \quad F_0 = 0,\ F_1 = 1$$

On introduit
$$\Phi_+ = \frac{1 + \sqrt{5}}{2}, \qquad \Phi_- = \frac{1 - \sqrt{5}}{2}$$

<u>Affirmation :</u> $\quad \dfrac{1}{\sqrt{5}}\left(\Phi_+^n - \Phi_-^n\right)$

**i) Initialisation**

$F_0 = 0$
$$\frac{1}{\sqrt{5}}\left(\Phi_+^0 - \Phi_-^0\right) = 0$$

$F_1 = 1$
$$\frac{1}{\sqrt{5}}\left(\Phi_+^1 - \Phi_-^1\right) = \frac{2\sqrt{5}}{2}\left(\frac{1}{\sqrt{5}}\right) = 1$$

$F_2 = 1 \qquad \dfrac{1}{\sqrt{5}}\left(\Phi_+^2 - \Phi_-^2\right) =$

Si
$$
\begin{aligned}
(x - \Phi_+)(x - \Phi_-) &= x^2 - x - 1 \\
&= x^2 - (\Phi_+ + \Phi_-)x + \Phi_-\Phi_+
\end{aligned}
$$

$$\Phi_-\Phi_+ = -1$$
$$\Phi_- + \Phi_+ = 1$$
$$\Phi_+^2 = 1 + \Phi_+$$
$$\Phi_-^2 = 1 + \Phi_-$$

$$\implies \frac{1}{\sqrt{5}}\left(\Phi_+^2 - \Phi_-^2\right) = \frac{1}{\sqrt{5}}\left(\Phi_+ \cancel{+1} \cancel{-1} - \Phi_-\right) = 1 \quad \checkmark$$

**ii) <u>Hérédité</u>** : on suppose que $F_n = \dfrac{1}{\sqrt{5}}\left(\Phi_+^n - \Phi_-^n\right)$

et veut montrer $F_{n+1} = \dfrac{1}{\sqrt{5}}\left(\Phi_+^{n+1} - \Phi_-^{n+1}\right)$

On sait que $F_{n+1} = F_n + F_{n-1}$

$$
\begin{aligned}
&\frac{1}{\sqrt{5}}\left(\Phi_+^n - \Phi_-^n + \Phi_+^{n-1} - \Phi_-^{n-1}\right) \\
&\frac{1}{\sqrt{5}}\left(\Phi_+^{n-1}(\Phi_+ + 1) - \Phi_-^{n-1}(\Phi_- + 1)\right) \\
&\frac{1}{\sqrt{5}}\left(\Phi_+^{n-1}\Phi_+^2 - \Phi_-^{n-1}\Phi_-^2\right) \\
&= \frac{1}{\sqrt{5}}\left(\Phi_+^{n+1} - \Phi_-^{n+1}\right) \quad \checkmark
\end{aligned}
$$

> [!important] <u>Preuve par récurrence</u>
> À montrer que $P(n)$ est vrai pour $\forall n \in \mathbb{N}^*$
> 1. <u>Initialiser</u>, montrer $P(0), P(1)$
> 2. <u>Hérédité</u> : montrer que $P(n) \implies P(n+1) \quad \forall n \in \mathbb{N}^*$
>
> Conclure $P(n)$ est vrai $\forall n \in \mathbb{N}$

> [!definition] Définition
> Une suite (réelle) est une fonction
> $$S : \mathbb{N}^* \to \mathbb{R}$$
> Notations : $(S_n)_{n \in \mathbb{N}^*}$

> [!important] <u>Théorème</u>
> $\nexists\, r \in \mathbb{Q}$ tel que $r^2 = 2$

<u>Preuve :</u> Supposons par absurde que $\exists\, r \in \mathbb{Q}$ tel que $r^2 = 2$

$r \neq 0$, on peut choisir $r > 0$

Donc : $r = \dfrac{n}{m} \quad n, m \in \mathbb{N}^*$

On peut choisir $n$ et $m$ sans facteurs communs.

On peut donc écrire
$$n = p_1 \cdot p_2 \cdot p_3 \cdots p_\ell$$
$$m = q_1 \cdot q_2 \cdots q_k$$
Un produit de nombres premiers. Cette factorisation est unique.

Puisque $r^2 = \dfrac{n^2}{m^2} = 2$

donc $n^2 = 2m^2$. Donc

$$p_1^2\, p_2^2 \cdots p_\ell^2 = 2\, q_1^2\, q_2^2 \cdots q_k^2 \quad \in \mathbb{N}^*$$

Par unicité de la factorisation, $k = 0$ et $p_1^2 = 2$

<u>Contradiction</u> $\blacksquare$

> [!note] Exercice (facultatif)
> Montrer $\sqrt{p} \notin \mathbb{Q} \quad \forall p$ premier
> et $\sqrt{p_1 p_2 \cdots p_{2n+1}} \notin \mathbb{Q}$

<u>**Autres exemples**</u>

1) $1, 6, 11, 16, 21, 26 \qquad a_n = 1 + 5(n-1)$

2) $\dfrac{2}{3}, \dfrac{5}{6}, \dfrac{10}{9}, \dfrac{17}{12}$
   $$b_n = \frac{n^2 + 1}{3n}$$

3) $3, 0, 9, 0, 15, 0, 21, 0, 27, 0, 33, 0$
   $$c_n = \begin{cases} 0 & \text{si } n = 2\ell \\ 3n & \text{si } n = 2\ell + 1 \end{cases} = \left(\frac{\operatorname{sgn}(-1)^n - 1}{-2}\right) 3n$$
   $$c_n = \sin^2\!\left(n\frac{\pi}{2}\right) 3n$$

---

### 2.2 Limites d'une suite

<u>Vocabulaire :</u> une suite $(S_n \mid n \in \mathbb{N}^*)$ est dite :

- <u>majorée</u> si $\exists M \in \mathbb{R}$, tel que $\forall n \in \mathbb{N}^*$, $S_n \leq M$. On dit aussi que $M$ est un <u>majorant</u> de la suite.
- <u>strictement majorée</u> si $\exists M \in \mathbb{R}$ tel que $\forall n \in \mathbb{N}^*$, $S_n < M$. $M$ est alors <u>majorant strict</u> de la suite.
- <u>(strictement) minorée</u> si $\exists m \in \mathbb{R}$ tel que $\forall n \in \mathbb{N}^*$, $S_n \geq m$ $(S_n > m)$. $m$ est alors un <u>minorant (strict)</u> de la suite.
- <u>(strictement) croissante</u> si $\forall n \in \mathbb{N}^*$,
  $$S_{n+1} \underset{(>)}{\geq} S_n$$
- <u>(strictement) décroissante</u> si $\forall n \in \mathbb{N}^*$,
  $$S_{n+1} \underset{(<)}{\leq} S_n$$
- <u>monotone</u> si elle est croissante ou décroissante.
- <u>bornée</u> si elle est simultanément minorée et majorée.

#### <u>Exemples</u>

**1)** $a_n = \dfrac{1}{n} \qquad$ des majorants seraient $1, 2, 3, \pi, e, \dots$

Elle est strictement minorée par $0$.

$(a_n)_{n \in \mathbb{N}^*}$ est donc une suite bornée, $\forall n \in \mathbb{N}^*$
$$0 < a_n \leq 1$$

$(a_n)_{n \in \mathbb{N}^*}$ est aussi strictement décroissante $\forall n > 0$
$$n + 1 > n \iff \frac{1}{n} > \frac{1}{n+1} \iff a_n > a_{n+1}$$

**2)** $b_n = \dfrac{n}{n+1} \qquad$ C'est une suite strictement majorée par $1$.

C'est une suite minorée par $0, -1, -2, -10, \dots$

Strictement croissante.

**3)** $c_n = (-1)^n n \qquad$ Elle est ni minorée, ni majorée, ni monotone.

**Discussion de 2)** $\left(b_n = \dfrac{n}{n+1}\right)$

Cette suite commence par $\dfrac{1}{2}, \dfrac{2}{3}, \dfrac{3}{4}, \dfrac{4}{5}, \dots$

Cette suite s'approche d'aussi près qu'on souhaite de la valeur $1$.

$$\forall \varepsilon > 0 \qquad 1 > b_n > 1 - \varepsilon \quad \text{pour } n \text{ suffisamment grand}$$

Essayons de montrer ça : pour $\varepsilon > 0$ donné

$$
\begin{aligned}
& 1 > b_n > 1 - \varepsilon \\
\iff\ & \underbrace{1 > \frac{n}{n+1}}_{\text{toujours vrai}} > 1 - \varepsilon \iff \frac{n}{n+1} > 1 - \varepsilon \\
\iff\ & \frac{n + 1 - 1}{n+1} > 1 - \varepsilon \iff 1 - \frac{1}{n+1} > 1 - \varepsilon \\
\iff\ & \varepsilon > \frac{1}{n+1} \iff n + 1 > \frac{1}{\varepsilon} \iff n > \frac{1}{\varepsilon} - 1
\end{aligned}
$$

<u>Conclusion</u> : si $\varepsilon > 0$ est donné, alors
$$1 > b_n > 1 - \varepsilon$$
$$\text{si } n > \frac{1}{\varepsilon} - 1$$

On dit que la limite de $(b_n)_{n \in \mathbb{N}^*}$ pour $n$ qui tend vers $\infty$ est $1$.

> [!definition] Définition
> Soit $(S_n)_{n \in \mathbb{N}^*}$ une suite de nombres réels.
> On dit que cette suite tend vers $\ell \in \mathbb{R}$ si et seulement si
> $\forall \varepsilon > 0$
> ==$\exists N_\varepsilon$ tel que $n \geq N_\varepsilon \implies |S_n - \ell| < \varepsilon$==

> [!definition] <u>Notation</u>
> ==$\displaystyle\lim_{n \to \infty} S_n = \ell$== $\qquad \left(S_n \xrightarrow[n \to \infty]{} \ell\right)$
>
> (les deux parties surlignées $=$ même chose)

<u>Graphiquement :</u>

![[ch2-definition-limite.svg]]

#### <u>Exemples</u>

**1)** $(a_n \mid n \in \mathbb{N}^*)$, $a_n = \dfrac{1}{n}$

On devine que $\displaystyle\lim_{n \to \infty} a_n = 0$, i.e.
$$\forall \varepsilon > 0,\ \exists N_\varepsilon \text{ tel que } n \geq N_\varepsilon \implies \left|0 - \frac{1}{n}\right| < \varepsilon$$

Vérifions-le
$$\underbrace{-\varepsilon < \frac{1}{n}}_{\text{toujours vraie}} < \varepsilon \iff \frac{1}{n} < \varepsilon \iff n > \frac{1}{\varepsilon}$$

Donc, $N_\varepsilon = \left\lfloor \dfrac{1}{\varepsilon} \right\rfloor + 1$ et ce nombre existe $\forall \varepsilon > 0$

**2)** $b_n = \left(\dfrac{2n+1}{n}\right)^2$

La suite est $9, \dfrac{25}{4}, \dfrac{49}{9}, \dfrac{81}{16}, \dots, \left(\dfrac{101}{50}\right)^2 = \dfrac{10201}{2500}$

$$\lim_{n \to \infty} b_n = 4$$

Vérifions $\forall \varepsilon > 0\ \ \exists N_\varepsilon$, $n \geq N_\varepsilon$ alors $\left|\left(\dfrac{2n+1}{n}\right)^2 - 4\right| < \varepsilon$

$$
\begin{aligned}
&\iff \underbrace{-\varepsilon < \left(\frac{2n+1}{n}\right)^2 - 4}_{\text{toujours vraie}} < \varepsilon \iff \left(\frac{2n+1}{n}\right)^2 - 4 < \varepsilon \\
&\iff \frac{4n^2 + 4n + 1}{n^2} - 4 < \varepsilon \\
&\iff \frac{4n + 1}{n^2} < \varepsilon \iff 4n + 1 < \varepsilon n^2 \\
&\iff 0 < \varepsilon n^2 - 4n - 1 \\
&\qquad n > \frac{4 + \sqrt{16 + 4\varepsilon}}{2\varepsilon}
\end{aligned}
$$

<u>On choisit</u>
$$N_\varepsilon = \left\lfloor \frac{4 + \sqrt{16 + 4\varepsilon}}{2\varepsilon} \right\rfloor + 1$$

#### <u>Règles de calculs</u>

> [!important]
> Si $\displaystyle\lim_{n \to \infty} a_n = a$ et $\displaystyle\lim_{n \to \infty} b_n = b$
> 1. $\displaystyle\lim_{n \to \infty} |a_n| = |a|$
> 2. $\displaystyle\lim_{n \to \infty} (a_n + b_n) = a + b$
> 3. $\displaystyle\lim_{n \to \infty} (a_n \cdot b_n) = a \cdot b$
> 4. $\displaystyle\lim_{n \to \infty} \left(\frac{a_n}{b_n}\right) = \frac{a}{b} \qquad b, b_n \neq 0$

Preuve en série d'exercices (S6, Ex 5)

#### <u>Exemples</u>

**1)**
$$a_n = \frac{n^2 + 1}{(n+1)(2n-1)} \cdot \frac{\frac{1}{n^2}}{\frac{1}{n} \cdot \frac{1}{n}} = \frac{1 + \overset{\lim \to 0}{\overbrace{1/n^2}}}{(1 + \underbrace{1/n}_{\lim \to 0})(2 - \underbrace{1/n}_{\lim \to 0})}$$

$$\lim_{n \to \infty} a_n = \frac{1}{2}$$

**2)** $\qquad$ <u>Astuce</u> : multiplier par l'expression <u>conjuguée</u>

$$b_n = \sqrt{n^2 - n} - n$$
$$b_n = \sqrt{n^2 - n} - n \cdot \frac{\sqrt{n^2 - n} + n}{\sqrt{n^2 - n} + n}$$
$$b_n = \frac{n^2 - n - n^2}{\sqrt{n^2 - n} + n} = -\frac{n}{\sqrt{n^2 - n} + n} = -\frac{n}{n\sqrt{1 - 1/n} + n}$$
$$= -\frac{1}{\sqrt{1 - 1/n} + 1} \qquad \lim_{n \to \infty}(b_n) = -\frac{1}{2}$$

---

### 2.3 Théorème des gendarmes

> [!important] <u>Théorème</u>
> Soit 2 suites $(a_n)_{n \in \mathbb{N}^*}$ et $(b_n)_{n \in \mathbb{N}^*}$ telles que :
> $$\lim_{n \to \infty} a_n = a \quad \text{et} \quad \lim_{n \to \infty} b_n = b$$
> Supposons $\exists N \in \mathbb{N}^*$ tel que $n \geq N$, $b_n \geq a_n$
>
> alors $b \geq a$

<u>Graphiquement</u>

![[ch2-comparaison-limites.svg]]

<u>Preuve</u> : Supposons que $a > b$, alors

$a - b > 0 \qquad$ Posons $\varepsilon := \dfrac{a - b}{2}$

Puisque $\displaystyle\lim_{n \to \infty} a_n = a$ et $\displaystyle\lim_{n \to \infty} b_n = b$,

$\exists N_\varepsilon$ tel que $n \geq N_\varepsilon \implies |a - a_n| < \varepsilon$

$\exists N'_\varepsilon$ tel que $n \geq N'_\varepsilon \implies |b - b_n| < \varepsilon$

et $n \geq N \implies b_n \geq a_n$

Si $n \geq \max\{N, N_\varepsilon, N'_\varepsilon\}$ alors
$$|a - a_n| < \varepsilon \text{ et } |b - b_n| < \varepsilon \text{ et } b_n \geq a_n$$

Donc,
$$-\varepsilon < a - a_n < \varepsilon \text{ et}$$
$$-\varepsilon < b_n - b < \varepsilon \text{ et}$$
$$b_n \geq a_n$$

Donc
$$-2\varepsilon < a - a_n + b_n - b < 2\varepsilon \text{ et } b_n \geq a_n$$

Donc
$$
\left.
\begin{aligned}
&-4\varepsilon < b_n - a_n < 0 \\
&\text{et } b_n \geq a_n \iff b_n - a_n \geq 0
\end{aligned}
\right\}\ \lightning
$$

<u>Contradiction</u>

> [!important] <u>Théorème des gendarmes</u>
> Soient $(a_n)_{n \in \mathbb{N}^*}$, $(g_n)_{n \in \mathbb{N}^*}$, $(d_n)_{n \in \mathbb{N}^*}$ telles que
> - $\displaystyle\lim_{n \to \infty} g_n = \ell = \lim_{n \to \infty} d_n$
> - $\exists N$ tel que $n \geq N \implies g_n \leq a_n \leq d_n$
>
> Alors $\displaystyle\lim_{n \to \infty} a_n = \ell$

<u>Graphiquement</u>

![[ch2-gendarmes.svg]]

<u>Preuve</u> : Soit $\varepsilon > 0$

Par définition, puisque $\displaystyle\lim_{n \to \infty} d_n = \ell = \lim_{n \to \infty} g_n$

- $\exists N_\varepsilon$ tel que $n \geq N_\varepsilon \implies |\ell - d_n| < \varepsilon$
- $\exists N'_\varepsilon$ tel que $n \geq N'_\varepsilon \implies |\ell - g_n| < \varepsilon$

et $n \geq N \quad g_n \leq a_n \leq d_n$

Donc $n \geq \max\{N, N_\varepsilon, N'_\varepsilon\}$ alors
$$-\varepsilon < g_n - \ell \leq a_n - \ell \leq d_n - \ell < \varepsilon$$

Donc $|\ell - a_n| < \varepsilon \to \displaystyle\lim_{n \to \infty} a_n = \ell \quad \blacksquare$

#### <u>Exemples</u>

**1)** $a_n = \dfrac{2}{3}, 0, \dfrac{4}{15}, 0, \dfrac{6}{35}, 0, \dfrac{8}{63}, 0$

$$
a_n = \begin{cases}
0 & \text{si } n = 2k \\[2mm]
\dfrac{n+1}{(n+1)^2 - 1} & \text{si } n = 2k + 1
\end{cases}
\qquad k \in \mathbb{N}^*
$$

$$g_n = 0 \quad \forall n \in \mathbb{N}^* \qquad d_n = \frac{n+1}{(n+1)^2 - 1}$$

$$g_n \leq a_n \leq d_n \qquad \lim_{n \to \infty} g_n = 0, \quad \lim_{n \to \infty} d_n = 0$$

Par théorème des gendarmes
$$g_n \leq a_n \leq d_n \to \lim_{n \to \infty} a_n = 0$$

**2)**
$$b_n = \frac{n+2}{n + \sin(n \cdot \pi/2)}$$

On pose
$$\frac{n+2}{n+1} \leq b_n \leq \frac{n+2}{n-1}$$

pour $n \geq 2$

Par le théorème des gendarmes $\displaystyle\lim_{n \to \infty} b_n = 1$

> [!important] <u>Corollaire</u>
> Si $(a_n)_{n \in \mathbb{N}^*}$ tel que $\displaystyle\lim_{n \to \infty} |a_n| = 0$ alors $\displaystyle\lim_{n \to \infty} a_n = 0$

<u>Preuve</u>
$$-|a_n| \leq a_n \leq |a_n|$$
et on applique le théorème des gendarmes $\blacksquare$

<u>Remarque</u> : marche uniquement pour $\displaystyle\lim_{n \to \infty} a_n = 0$

Si $a_n = (-1)^n$, alors $a_n$ n'a pas de limite mais
$$\lim_{n \to \infty} |a_n| = 1 \neq 0$$

> [!important] <u>Théorème de la convergence monotone</u>
> Si une suite $(a_n)_{n \in \mathbb{N}^*}$ est monotone et bornée alors la limite existe $\left(\displaystyle\lim_{n \to \infty} a_n = \ell \in \mathbb{R}\right)$
> et
> - $\ell =$ supremum de $(a_n)_{n \in \mathbb{N}^*}$ (cas croissant)
> - $\ell =$ infimum de $(a_n)_{n \in \mathbb{N}^*}$ (cas décroissant)

<u>Exemple</u> : $\quad a_n = 0, 0.9, 0.99, 0.999, 0.9999$
$$a_n = \frac{10^n - 1}{10^n} \qquad \text{la suite est bornée par } 1$$
alors $\displaystyle\lim_{n \to \infty} a_n = 1$

---

### 2.4 Limites infinies

Supposons qu'on ait la suite $a_1 = 1$, $a_2 = 1 + \dfrac{1}{2}$, $a_3 = 1 + \dfrac{1}{2} + \dfrac{1}{3}, \dots$, $a_n = \displaystyle\sum_{k=1}^{n} \frac{1}{k}$

Cette suite $(a_n)_{n \in \mathbb{N}^*}$ est manifestement croissante.

Observons la chose suivante :
$$a_n = 1 + \frac{1}{2} + \underbrace{\frac{1}{3} + \frac{1}{4}}_{\geq \frac{1}{2}} + \underbrace{\frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8}}_{\geq \frac{1}{2}} + \underbrace{\frac{1}{9} + \frac{1}{10} + \dots + \frac{1}{16}}_{\geq \frac{1}{2}}$$
$$a_n > \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \dots + \frac{1}{2}$$

Donc, pour $n$ suffisamment grand, $a_n \geq \dfrac{m}{2}$

Donc, $(a_n)_{n \in \mathbb{N}^*}$ n'est pas bornée !

On écrit $\displaystyle\lim_{n \to \infty} a_n = \infty$

> [!definition] Déf
> On dit qu'une suite diverge vers l'infini (ou moins l'infini) et on écrit $\displaystyle\lim_{n \to \infty} a_n = \pm\infty$
> si et seulement si $\forall B \in \mathbb{R}, \exists N_B,\ n \geq N_B \implies a_n \geq B$
> $(n \geq N_B \implies a_n \leq B)$

#### <u>Exemples</u>

**1)** $a_n = 2n - n^2$

On devine que $\displaystyle\lim_{n \to \infty} a_n = -\infty$

Montrons-le à partir de la définition.

Soit $B \in \mathbb{R}$. On résout $a_n \leq B$
$$\iff 2n - n^2 \leq B \iff 0 \leq n^2 - 2n + B$$

$$n \geq \frac{2 + \sqrt{4 - 4B}}{2} = 1 + \sqrt{1 - B}$$

![[ch2-n2-2n-B.svg]]

On peut donc prendre
$$
N_B = \begin{cases}
\left\lfloor 1 + \sqrt{1 - B} \right\rfloor + 1 & \text{si } B \leq 1 \\
1 & \text{si } B > 1
\end{cases}
$$

Donc $N_B \in \mathbb{N}$ existe pour tout choix de $B$.

#### <u>Règle de calcul</u>

> [!important]
> Si $(a_n)_{n \in \mathbb{N}^*}$ tel que
> 1. $\displaystyle\lim_{n \to \infty} a_n = \pm\infty$ et $(b_n)_{n \in \mathbb{N}^*}$ est bornée, alors $\displaystyle\lim_{n \to \infty} (a_n + b_n) = \pm\infty$
> 2. $\displaystyle\lim_{n \to \infty} \lambda a_n = \operatorname{sgn}(\lambda)\infty$ pour $\lambda \in \mathbb{R}^*$
> 3. Si $\displaystyle\lim_{n \to \infty} a_n = \pm\infty$, alors $\displaystyle\lim_{n \to \infty} \frac{1}{a_n} = 0$

<u><span style="color:red">Cas indéterminés.</span></u>

1. Si $\displaystyle\lim_{n \to \infty} a_n = \infty$ et $\displaystyle\lim_{n \to \infty} b_n = -\infty$
   $$\lim_{n \to \infty} (a_n + b_n) = \ ?$$
2. Si $\displaystyle\lim_{n \to \infty} a_n = \pm\infty$ et $\displaystyle\lim_{n \to \infty} b_n = 0$
   $$\lim_{n \to \infty} (a_n \cdot b_n) = \ ?$$

#### Exemple cas indéterminé :

**1)** $a_n = \sqrt{n^3 + 1} - \sqrt{n^3 + n^2 + 1}$

C'est du type « $\infty - \infty$ »

On amplifie par le conjugué
$$a_n = \left(\sqrt{n^3 + 1} - \sqrt{n^3 + n^2 + 1}\right) \cdot \frac{\sqrt{n^3 + 1} + \sqrt{n^3 + n^2 + 1}}{\sqrt{n^3 + 1} + \sqrt{n^3 + n^2 + 1}}$$

$$a_n = \frac{-n^2}{\sqrt{n^3 + 1} + \sqrt{n^3 + n^2 + 1}} = \frac{-1}{\underbrace{\sqrt{\frac{1}{n} + \frac{1}{n^4}}}_{\xrightarrow[n \to \infty]{} 0} + \underbrace{\sqrt{\frac{1}{n} + \frac{1}{n^2} + \frac{1}{n^4}}}_{\xrightarrow[n \to \infty]{} 0}} = -\infty$$

**2)** $b_n = \sqrt{n^4 + 1} - \sqrt{n^4 + n^2 + 1}$

Amplification :
$$\frac{-n^2}{\sqrt{n^4 + 1} + \sqrt{n^4 + n^2 + 1}} = \frac{-1}{\left(\underbrace{\sqrt{1 + \frac{1}{n^4}}}_{\xrightarrow[n \to \infty]{} 1} + \underbrace{\sqrt{1 + \frac{1}{n^2} + \frac{1}{n^4}}}_{\xrightarrow[n \to \infty]{} 1}\right)}$$
$$= -\frac{1}{2}$$

#### <u>Exemple contrôle 1 :</u>

Calculer la limite de $a_n = \left(\dfrac{3n+1}{4n}\right)^2$ et vérifiez-la par la définition

**1) <u>Calcul de la limite</u>**
$$a_n = \left(\frac{3 + \frac{1}{n}}{4}\right)^2 = \frac{9 + \overset{\to 0}{\frac{6}{n}} + \overset{\to 0}{\frac{1}{n^2}}}{16} \to \frac{9}{16}$$
$$\implies \lim_{n \to \infty} a_n = \frac{9}{16}$$

**2)** Soit $\varepsilon > 0$

Résoudre $\left|a_n - \dfrac{9}{16}\right| < \varepsilon \iff \left|\left(\dfrac{3n+1}{4n}\right)^2 - \dfrac{9}{16}\right| < \varepsilon$

$$
\begin{aligned}
&\iff \left|\left(\frac{3 + \frac{1}{n}}{4}\right)^2 - \frac{9}{16}\right| < \varepsilon \\
&\iff \left|\frac{9 + \frac{6}{n} + \frac{1}{n^2} - 9}{16}\right| < \varepsilon \\
&\iff -16\varepsilon < 9 + \frac{6}{n} + \frac{1}{n^2} - 9 < 16\varepsilon \\
&\iff 0 < 16\varepsilon n^2 - 6n - 1 \\
&\iff n > \frac{6 + \sqrt{36 + 64\varepsilon}}{32\varepsilon}
\end{aligned}
$$

![[ch2-16en2-6n-1.svg]]

On pose
$$N_\varepsilon = \left\lfloor \frac{6 + \sqrt{36 + 64\varepsilon}}{32\varepsilon} \right\rfloor + 1$$

> [!important] <u>Théorème du Gendarme :</u>
> Si $(a_n)_{n \in \mathbb{N}^*}$ et $(b_n)_{n \in \mathbb{N}^*}$ sont telles que
> $$\exists N,\ n \geq N,\ b_n \geq a_n \text{ ou } (b_n \leq a_n)$$
> Alors $\displaystyle\lim_{n \to \infty} b_n = \pm\infty$

<u>Preuve</u> : Soit $B \in \mathbb{R}$ : Montrons que $b_n \geq B$ si $n$ suffisamment grand

Puisque $\displaystyle\lim_{n \to \infty} a_n = \infty$, on a par définition :
$$\exists N_B,\ n \geq N_B,\ a_n \geq B$$

Donc, si $n \geq \max\{N_B, N\}$ on aura
$$b_n \geq a_n \geq B$$

Comme le choix de $B$ était arbitraire, on conclut $\blacksquare$

---

### 2.5 Suites importantes

> [!definition] Déf : <u>Suite géométrique</u>
> La suite de type $a_n = a \cdot q^n$ avec $a, q \in \mathbb{R}$
> $q$ est la <u>raison</u> de la suite $(a_n)_{n \in \mathbb{N}^*}$

<u>Observation</u> : si $|q| < 1$, $\displaystyle\lim_{n \to \infty} a \cdot q^n = 0$

<u>Preuve</u> : Si $|q| < 1$, et si $q \neq 0$

alors $\dfrac{1}{|q|} > 1$

Donc $\exists r > 0$, $\dfrac{1}{|q|} = 1 + r$

Donc, $|q| = \dfrac{1}{1 + r}$ et
$$|q^n| = \frac{1}{(1+r)^n} = \frac{1}{\displaystyle\sum_{k=0}^{n} \binom{n}{k} r^k}$$
$$= \frac{1}{1 + nr + \underbrace{\dots}_{\text{termes} > 0}} \leq \frac{1}{n \cdot r} = \frac{1}{r} \cdot \frac{1}{n} \xrightarrow[n \to \infty]{} 0$$

Donc, $\displaystyle\lim_{n \to \infty} |a q^n| = 0$

Donc $\displaystyle\lim_{n \to \infty} a q^n = 0$

- <u>Si $q = 1$</u> : $\displaystyle\lim_{n \to \infty} a q^n = a$
- <u>Si $q = -1$</u> : $\displaystyle\lim_{n \to \infty} a q^n = \pm a$, $(a_n)_{n \in \mathbb{N}^*}$
  $\hookrightarrow$ diverge sauf si $a = 0$
- <u>Si $q > 1$</u> : $\displaystyle\lim_{n \to \infty} a q^n = \operatorname{sgn}(a)\,\infty$
- <u>Si $q < -1$</u> : pas de limite sauf si $a = 0$

#### <u>Série géométrique</u>

> [!definition] Série Géométrique $\to$ Une série géométrique
> $(S_n)_{n \in \mathbb{N}^*}$ associée à la suite géométrique $(aq^n)_{n \in \mathbb{N}^*}$ est donnée par
> $$S_n = a + aq + aq^2 + \dots + aq^{n-1} = a\sum_{k=0}^{n-1} q^k$$

- Si $q = 1 \qquad S_n = n \cdot a$
- Si $q = -1 \qquad S_n = \dfrac{a}{2}\left(1 + (-1)^n\right)$
- Si $q \in \mathbb{R} \setminus \{\pm 1\}$ : $\quad S_n = a + aq + aq^2 + \dots + aq^{n-1} + aq^n$

Donc, $S_n - qS_n = a - aq^n$

Donc,
$$S_n = a \cdot \frac{1 - q^n}{1 - q}$$

Ainsi, si $|q| < 1$, alors
$$a\left(1 + q + q^2 + q^3 + q^4 + \dots\right) = a\frac{1}{1 - q}$$

#### <u>Exemples</u>

**1)** Écrire $4,\overline{321}$ comme une fraction

$$
\begin{aligned}
4,\overline{321} &= 4 + 0,\overline{321} = 3 + 1 + 0,\overline{321} \\
&= 3 + 1 + 0,321 + 0,000321 + 0,000000321 + \dots \\
\iff\ & 3 + 1 + \frac{321}{1000} + \frac{321}{1000000} + \frac{321}{1000000000} + \dots \\
\iff\ & 3 + 1 + 321\left(\frac{1}{1000} + \frac{1}{1000^2} + \frac{1}{1000^3} + \dots\right) \\
&= 4 + \frac{321}{1000}\left(1 + \frac{1}{1000} + \frac{1}{1000^2} + \dots\right) \\
&\qquad \left(q = \frac{1}{1000} < 1\right)
\end{aligned}
$$

$$4 + \frac{321}{1000}\left(\frac{1}{1 - \frac{1}{1000}}\right) = 4 + \frac{321}{1000}\left(\frac{1000}{999}\right)$$

$$= 4 + \frac{321}{999} = \frac{3996 + 321}{999} = \frac{4317}{999}$$

On remarque que
$$0,\overline{321} = \frac{321}{999}$$
$$0,\overline{045} = \frac{45}{999}$$
$$0.\overline{9} = \frac{9}{9}$$

#### <u>Exemple type contrôle 1</u>

Considérons la figure

![[ch2-figure-perpendiculaires.svg]]

<u>Calculons :</u>
$$l_1 + l_2 + l_3 + \dots = \sum_{k=1}^{\infty} l_k$$

$$
\left.
\begin{aligned}
l_1 &= \sin\alpha \cdot L \\
l_2 &= \cos\alpha\, L \sin\alpha \\
l_3 &= \cos^2\!\alpha\, L \sin\alpha \\
l_n &= \cos^{n-1}\!\alpha\, L \cdot \sin\alpha
\end{aligned}
\right\}
\quad \text{en fonction de } \alpha \text{ et } L \text{ — série géométrique.}
$$

$$a = L \cdot \sin\alpha$$
$$q = \cos\alpha$$

donc
$$\sum_{k=1}^{\infty} l_k = \sin\alpha\, L \cdot \frac{1}{1 - \cos\alpha}$$

#### <u>Résoudre :</u>

$$\underset{(f)}{\sqrt{2mx}} > \underset{(g)}{x - 4m}$$

$$
D_{\text{def}} = \begin{cases}
\mathbb{R}_+ & \text{si } m > 0 \\
\mathbb{R} & \text{si } m = 0 \\
\mathbb{R}_- & \text{si } m < 0
\end{cases}
$$

$$
(2) \underset{D_{\text{def}}}{\iff} \begin{cases}
x - 4m < 0 & (2a) \\[2mm]
2mx > (x - 4m)^2 & (2b)
\end{cases}
$$

$$\iff (2a)\quad x - 4m < 0 \iff x < 4m$$

$$
S_{2a} = \begin{cases}
[0, 4m[ & \text{si } m > 0 \\
]-\infty, 0[ & \text{si } m = 0 \\
]-\infty, 4m[ & \text{si } m < 0
\end{cases}
$$

$$
\begin{aligned}
(2b) :\ & 2mx > (x - 4m)^2 \\
\iff\ & 2mx > x^2 - 8mx + 16m^2 \\
\iff\ & x^2 - 10mx + 16m^2 < 0 \\
\iff\ & (x - 2m)(x - 8m) < 0
\end{aligned}
$$

![[ch2-x2-10mx-16m2.svg]]

$$
S_{2b} = \begin{cases}
]2m, 8m[ & \text{si } m > 0 \\
\emptyset & \text{si } m = 0 \\
]8m, 2m[ & \text{si } m < 0
\end{cases}
$$

<u>Synthèse</u> : $\quad S = S_{2a} \cup S_{2b}$
