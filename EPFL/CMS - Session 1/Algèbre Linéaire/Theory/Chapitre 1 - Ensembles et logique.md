---
cours: Algèbre Linéaire
chapitre: 1
source: "Chapitre 1 - Algèbre Linéaire.pdf"
tags: [algebre-lineaire, chapitre-1]
---

# 1. Ensembles et logique

### 1.1 Ensembles

> [!definition] Déf
> Un ensemble est une collection d'objets du même type.
> P.ex : $E = \{x, y, z\}$ $\quad$ On note $x \in E$

Un sous-ensemble est une partie de la collection.

$$E = \{x, y, z\} \qquad A = \{x, y\} \quad \underline{A \subset E} \qquad B = \{z\}$$

« Diagramme de Venn »

![[al1-venn.svg]]

<u>**exemples**</u>

1) $E = \{1, 2, 3, 4\}$, $A = \{2, 4\} \subset E$
2) $E = \{\text{Personnages des Peanuts}\}$
   $A = \{\text{Snoopy}\} \subset E$
3) $\varnothing = \{\}$ ensemble vide

> [!definition] Déf
> Un ensemble est dit <u>fini</u> s'il n'a qu'un nombre fini d'éléments.
> Le nombre d'éléments d'un ensemble $E$ est appelé la <u>cardinalité</u> de $E$ noté $\mathrm{card}(E)$

Dans les exemples précédents :
$$\left.\begin{aligned} &1) \ \mathrm{card}(E) = 4 \quad \mathrm{card}(A) = 2 \\ &2) \ \mathrm{card}(A) = 1 \\ &3) \ \mathrm{card}(\varnothing) = 0 \end{aligned}\right\} \text{ ensembles finis}$$

<u>exemples d'ensembles non finis</u>

1) $\mathbb{N} = \{0, 1, 2, 3, \dots\}$ (entiers naturels)
2) $\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}$ (entiers relatifs)
3) $\mathbb{Q} = \left\{\frac{p}{q} \ \middle|\ p, q \in \mathbb{Z}, \ q \neq 0\right\}$ (rationnels)
4) $\mathbb{R}$ (nombres réels)

<u>Remarque :</u> Pour définir un ensemble, on peut soit énumérer ses éléments ou lui donner une propriété caractéristique

<u>Remarque :</u> L'ordre n'a pas d'importance dans un ensemble.

<u>**Opérations sur les sous-ensembles**</u>

Soit $E$ un ensemble et soit $A, B \subset E$

- <u>Complémentaire</u> de $A$ dans $E$ : $C_E(A) = \{x \in E \mid x \notin A\}$

  ![[al1-complementaire.svg]]

- <u>Union</u> de $A$ et $B$ : $A \cup B = \{x \in E \mid x \in A \text{ ou } x \in B\}$

  ![[al1-union.svg]]

- <u>Intersection</u> de $A$ et $B$ : $A \cap B = \{x \in E \mid x \in A \text{ et } x \in B\}$

  ![[al1-intersection.svg]]

<u>**exemple :**</u>

$$E = \{\alpha, \beta, \gamma, \delta\}, \quad A = \{\alpha\}, \quad B = \{\alpha, \beta\}, \quad C = \varnothing, \quad D = \{\beta, \gamma, \delta\}$$
$$A, B, C, D \subset E$$

- $A \cup B = \{\alpha, \beta\} = B \quad (A \subset B)$
- $C_E(A) = \{\beta, \gamma, \delta\} = D$
- $A \cap D = \{\} = \varnothing = C$
- $B \cap C = \varnothing$

<u>**Propriétés caractéristiques**</u>

Soit $E$ un ensemble. Les sous-ensembles de $E$ peuvent se présenter sous la forme suivante :
$$A = \{x \in E \mid x \text{ vérifie } P\}$$

<u>**exemple :**</u> $E = \mathbb{R}$

| | |
| :-- | :-- |
| $A = \left]\frac{1}{3}, +\infty\right[ = \{x \in \mathbb{R} \mid \color{magenta}{\underline{x > \tfrac{1}{3}}}\}$ <span style="color:magenta">propriété $P$</span> | ![[al1-droite-A.svg\|220]] |
| $B = \{-\sqrt{2}, \sqrt{2}\} = \{x \in \mathbb{R} \mid \color{cyan}{\underline{x^2 = 2}}\}$ <span style="color:cyan">propriété $Q$</span> | ![[al1-droite-B.svg\|220]] |
| $C_{\mathbb{R}}(A) = \left]-\infty, \frac{1}{3}\right] = \{x \in \mathbb{R} \mid \color{orange}{\underline{x \leq \tfrac{1}{3}}}\}$ <span style="color:orange">propriété non $P$</span> | ![[al1-droite-CA.svg\|220]] |
| $A \cup B = \left]\frac{1}{3}, +\infty\right[ \cup \{-\sqrt{2}\} = \{x \in \mathbb{R} \mid x > \frac{1}{3} \vee x^2 = 2\}$ | ![[al1-droite-AuB.svg\|220]] |
| $A \cap B = \{\sqrt{2}\} = \{x \in \mathbb{R} \mid x > \frac{1}{3} \wedge x^2 = 2\}$ | ![[al1-droite-AnB.svg\|220]] |

> [!important] À retenir
> Si $A = \{x \in E \mid x \text{ vérifie } P\}$ et $B = \{x \in E \mid x \text{ vérifie } Q\}$
> $$
> \begin{aligned}
> C_E(A) &= \{x \in E \mid x \text{ vérifie } \neg P\} \\
> A \cup B &= \{x \in E \mid x \text{ vérifie } P \vee Q\} \\
> A \cap B &= \{x \in E \mid x \text{ vérifie } P \wedge Q\}
> \end{aligned}
> $$

---

### 1.2 Quantificateurs

- <u>existentiels</u> : $\exists$ il existe un élément
  ex. $\exists x \in \mathbb{R}, \ x^2 = 2$
- <u>Universel</u> : $\forall$ pour tout élément
  ex. $\forall x \in \mathbb{R}, \ x^2 \geq 0$

$$\exists x \in E : x \text{ vérifie } P \ \overset{\text{négation}}{\longleftrightarrow} \ \forall x \in E, \ x \text{ vérifie } \neg P$$
$$\forall x \in E : x \text{ vérifie } P \ \overset{\text{négation}}{\longleftrightarrow} \ \exists x \in E : x \text{ vérifie } \neg P$$

---

### 1.3 Règles de calcul ensemblistes

Soit $E$ un ensemble et soient $A, B, C \subset E$

i. $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

![[al1-distributivite.svg]]

ii. $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$

iii. $C_E(A \cup B) = C_E(A) \cap C_E(B)$

![[al1-morgan-iii.svg]]

iv. $C_E(A \cap B) = C_E(A) \cup C_E(B)$

![[al1-morgan-iv.svg]]

\* Si $A = \{x \in E \mid x \text{ vérifie } P\}$, $B = \{x \in E \mid x \text{ vérifie } Q\}$
$$
\begin{aligned}
A \cup B &= \{x \in E \mid x \text{ vérifie } P \ \underline{\text{ou}} \ Q\} \\
C_E(A \cup B) &= \{x \in E \mid x \text{ vérifie } \neg(P \text{ ou } Q)\} \\
C_E(A) \cap C_E(B) &= \{x \in E \mid x \text{ vérifie } \neg P \text{ et } \neg Q\}
\end{aligned}
$$

> [!important] iii et iv s'appellent les lois de Morgan

---

### 1.4 Implication

Soit $E$ un ensemble, $P, Q$ deux propriétés.

Soient $A = \{x \in E \mid x \text{ vérifie } P\}$, $\ B = \{x \in E \mid x \text{ vérifie } Q\}$

Pour exprimer l'implication, on utilise le symbole
$$\implies$$
↳ si (gauche == true) alors (droite == true)

$$\forall x \in E, \ x \text{ vérifie } P \implies x \text{ vérifie } Q$$
« Pour tous $x$ dans $E$, si $x$ vérifie $P$, alors $x$ vérifie $Q$ »

![[al1-implication.svg]]

<u>négation de $\implies$</u>
$$\exists x \in E, \ x \text{ vérifie } P \wedge x \text{ vérifie } \neg Q$$

![[al1-negation-implication.svg]]

$$A \not\subset B \qquad \underbrace{A \cap C_E(B) \neq \varnothing}_{\substack{\text{zone des contre exemples} \\ \text{pour faire la négation de} \implies}}$$

<u>**Exemples :**</u> Vrai ou Faux ?

i) $\forall x \in \mathbb{R}, \ x > 1 \implies x^2 > 1 \qquad$ <u>Vrai</u>
$$
\begin{aligned}
A &= \{x \in \mathbb{R} \mid x > 1\} : \ ]1, +\infty[ \\
B &= \{x \in \mathbb{R} \mid x^2 > 1\} : \ ]-\infty, -1[ \ \cup \ ]1, +\infty[
\end{aligned}
$$
$$\underline{A \subset B \to \text{vrai}}$$

ii) $\forall x \in \mathbb{R}, \ x^2 - 5x + 6 = 0 \implies x = 2$
$$A = \{x \in \mathbb{R} \mid x^2 - 5x + 6 = 0\} = \{2, 3\} \leftarrow \text{contre exemple} \qquad B = \{2\} \qquad \underline{A \not\subset B \to \text{Faux}}$$

iii) $\forall x \in \mathbb{R}, \ x^2 + 100 = 0 \implies x = 5 \qquad$ <u>Vrai</u>
$$A = \{x \in \mathbb{R} \mid x^2 + 100 = 0\} = \varnothing \qquad \varnothing \subset \text{tous ensembles}$$

iv) $\forall n \in \mathbb{N}, \ n \text{ pair} \implies n^2 \text{ pair}$
$$
\begin{aligned}
n \text{ pair} &\implies \exists k \in \mathbb{N}, \ n = 2k \\
&\implies \exists k \in \mathbb{N}, \ n^2 = (2k)^2 = 4k^2 = 2\underbrace{(2k^2)}_{l \in \mathbb{N}} \\
&\implies \exists l \in \mathbb{N}, \ n^2 = 2l \\
&\implies n^2 \text{ pair} \quad \blacksquare
\end{aligned}
$$

<u>**Contraposée**</u>

> [!definition]
> La contraposée de $\forall x \in E, \ x \text{ vérifie } P \implies x \text{ vérifie } Q$
> est $\forall x \in E, \ x \text{ vérifie } \neg Q \implies x \text{ vérifie } \neg P$
> $$A \subset B \implies C_E(B) \subset C_E(A)$$

Une proposition et sa contraposée expriment la même idée

<u>**exemples**</u>

i) $\forall x \in \mathbb{R}, \ \underbrace{x^2 \leq 1}_{[-1, 1]} \implies \underbrace{x \leq 1}_{]-\infty, 1]} \qquad$ <u>Vrai</u>

ii) $\forall x \in \mathbb{R}, \ x \neq 2 \implies x^2 - 5x + 6 \neq 0 \qquad$ <u>Faux</u>

iii) $\forall n \in \mathbb{N}, \ n^2 \text{ impair} \implies n \text{ impair} \qquad$ <u>Vrai</u>

$$\forall x \in E, \ x \text{ vérifie } P \implies x \text{ vérifie } Q \quad (\star)$$

> [!definition] Réciproque
> La <span style="color:red">réciproque</span> de $(\star)$ est
> $$\forall x \in E, \ x \text{ vérifie } Q \implies x \text{ vérifie } P$$

> <span style="color:red">⚠️ Pas de lien logique entre l'énoncé original et sa réciproque</span>

<u>**exemples**</u>

(i) $\forall x \in \mathbb{R}, \ x^2 > 1 \implies x > 1 \qquad$ <u>Faux</u>
(ii) $\forall x \in \mathbb{R}, \ x = 2 \implies x^2 - 5x + 6 = 0 \qquad$ <u>Vrai</u>
(iv) $\forall n \in \mathbb{N}, \ n^2 \text{ pair} \implies n \text{ pair} \qquad (?)$

On aimerait montrer que (iv) est vrai

<u>**Méthodes de preuve**</u>

On veut montrer
$$\forall n \in \mathbb{N}, \ \underbrace{n^2 \text{ pair}}_{P} \implies \underbrace{n \text{ pair}}_{Q}$$

**(1) Méthode directe**
$$\underset{n^2 \text{ pair}}{\text{Hypothèse } P} \ \xrightarrow[\text{raisonnement}]{\text{étapes de}} \ \underset{n \text{ pair}}{\text{Conclusion } Q}$$

**(2) Contraposée**

Pour montrer que
- $\forall x \in E, \ x \text{ vérifie } P \implies x \text{ vérifie } Q$ est vraie on utilise
- $\forall x \in E, \ x \text{ vérifie } \neg Q \implies x \text{ vérifie } \neg P$

On cherche à montrer
$$\forall n \in \mathbb{N}, \ \underbrace{n \text{ impair}}_{\neg Q} \implies \underbrace{n^2 \text{ impair}}_{\neg P}$$
$$
\begin{aligned}
n \text{ impair} &\implies \exists k \in \mathbb{N}, \ n = 2k + 1 \\
&\implies \exists k \in \mathbb{N}, \ n^2 = 4k^2 + 4k + 1 \\
&\implies \exists k \in \mathbb{N}, \ n^2 = 2\underbrace{(2k^2 + 2k)}_{l \in \mathbb{N}} + 1 \\
&\implies \exists l \in \mathbb{N}, \ n^2 = 2l + 1 \\
&\implies n^2 \text{ impair} \quad \blacksquare
\end{aligned}
$$

**(3) Absurde**
$$\text{Hypothèse absurde} \dashrightarrow \text{Conclusion absurde}$$
$$\exists x \in E, \text{ vérifie } P \text{ et } \neg Q$$

On suppose qu'il existe $n \in \mathbb{N}$ tel que $\begin{cases} n^2 \text{ est pair} & (P) \\ n \text{ est impair} & (\neg Q) \end{cases}$

Alors $\begin{cases} \exists k \in \mathbb{N}, \ n^2 = 2k \\ \exists l \in \mathbb{N}, \ n = 2l + 1 \end{cases}$ $\quad$ Donc $2k = n^2 = (2l + 1)^2 = 4l^2 + 4l + 1$

On en déduit, $2k = 4l^2 + 4l + 1$ d'où $2(k - 2l^2 - 2l) = 1$
donc $1$ est pair (absurde)

On en conclut que l'hypothèse $\exists n \in \mathbb{N}$, $n^2$ pair et $n$ impair est absurde et donc que
$$\underline{\forall n \in \mathbb{N}, \ n^2 \text{ pair} \implies n \text{ pair est vrai.}}$$

---

### 1.5 Équivalence

Soient $E, A, B$ comme au 1.4.

Pour exprimer la notion d'équivalence on utilise le symbole $\iff$
↳ est équivalent ou si et seulement si (ssi)

$$\forall x \in E, \ x \text{ vérifie } P \iff x \text{ vérifie } Q \quad (\star)$$
« Quel que soit $x$ dans $E$, $x$ vérifie $P$ si et seulement si $x$ vérifie $Q$ »

$(\star)$ exprime la même chose que
$$\forall x \in E, \ \underbrace{(x \text{ vérifie } P \implies x \text{ vérifie } Q)}_{A \subset B} \wedge \underbrace{(x \text{ vérifie } Q \implies x \text{ vérifie } P)}_{B \subset A}$$
« double implication »

<u>**exemples**</u>

i) $\forall x \in \mathbb{R}, \ x^2 > 1 \iff x > 1 \qquad$ <u>Faux</u>
$$\underbrace{(x > 1 \implies x^2 > 1)}_{\text{Vrai}} \quad \underbrace{(x^2 > 1 \implies x > 1)}_{\text{Faux}}$$

ii) $\forall x \in \mathbb{R}, \ x^2 - 5x + 6 = 0 \iff x = 2 \qquad$ <u>Faux</u>
$$\underbrace{(x = 2 \implies x^2 - 5x + 6 = 0)}_{\text{Vrai}} \quad \underbrace{(x^2 - 5x + 6 = 0 \implies x = 2)}_{\text{Faux}}$$

iv) $\forall n \in \mathbb{N}, \ n \text{ pair} \iff n^2 \text{ pair} \qquad$ <u>Vrai</u>

---

### 1.6 Opérations sur les ensembles

**① <u>Produit cartésien</u>** : Soient $E, F$ deux ensembles
$$\underbrace{E \times F}_{\text{produit cartésien}} = \{\underset{\uparrow \text{ couple ordonné}}{(x, y)} \mid x \in E, \ y \in F\}$$

<u>exemples</u>

(1) $E = \{1, 2\}$, $F = \{\alpha, \beta, \gamma\}$
$$E \times F = \{(1, \alpha), (1, \beta), (1, \gamma), (2, \alpha), (2, \beta), (2, \gamma)\}$$

(2) $E = F = \mathbb{R}$
$$\mathbb{R} \times \mathbb{R} = \{(x, y) \mid x, y \in \mathbb{R}\} = \underline{\mathbb{R}^2}$$

On construit de la même manière $\mathbb{R}^3$, $\mathbb{R}^4$, etc…

<u>Remarque :</u> Si $E$ et $F$ sont finis, $\mathrm{card}(E \times F) = \mathrm{card}(E) \cdot \mathrm{card}(F)$

**② <u>Parties</u>** Soit $E$ un ensemble
$$\underbrace{\mathcal{P}(E)}_{\text{Parties de } E} = \{A \mid A \subseteq E\} \quad (\text{Ensemble de tous les sous-ensembles de } E)$$

<u>exemples</u>

(1) $E = \{\alpha, \beta, \gamma\}$
$$\mathcal{P}(E) = \big\{\varnothing, \{\alpha\}, \{\beta\}, \{\gamma\}, \{\alpha, \beta\}, \{\alpha, \gamma\}, \{\beta, \gamma\}, \{\alpha, \beta, \gamma\}\big\}$$

(2) $\mathcal{P}(\mathbb{R})$ = « ensemble de tous les sous-ensembles de $\mathbb{R}$ »

p.ex. $\{1\} \in \mathcal{P}(\mathbb{R})$, $\quad [1, +\infty[, \ ]1, \infty[ \ \in \mathcal{P}(\mathbb{R})$

**③ <u>Ensembles finis</u>**

Soit $E$ un ensemble avec $\mathrm{card}(E) = n$ $(n \in \mathbb{N}^*)$

<u>Question</u> <mark style="background:#6b6b00">$\mathrm{Card}(\mathcal{P}(E)) = 2^n$</mark>
$\quad$ ($\forall x \in E$ j'ai 2 possibilités « pris » ou « pas pris »)
$$\{\underbrace{2 \cdot 2 \cdots}_{n \text{ fois}}\} = 2^n$$

<u>Question</u> Étant donné $0 \leq k \leq n$, combien de sous ensembles de $E$ ont exactement $k$ éléments ?
$$\underbrace{\binom{n}{k}}_{\text{« } k \text{ choix parmi } n \text{ »}} = \mathrm{Card}\big(\{A \subseteq E \mid \mathrm{Card}(A) = k\}\big)$$

> [!definition] Déf
> Si $n \in \mathbb{N}^*$, on définit $n! = n(n - 1)(n - 2) \cdots 2 \cdot 1$
> Et on pose $0! = 1$

> [!important] Proposition
> Si $n \in \mathbb{N}^*$ et $0 \leq k \leq n$
> $$\boxed{\binom{n}{k} = \frac{n!}{k!(n - k)!}}$$

<u>**exemple**</u> $\{\alpha, \beta, \gamma\} = E$ $(n = 3)$

Choisissons $k = 2$

![[al1-choix-k2.svg]]

$$= \frac{3 \cdot 2}{2} \text{ possibilités}$$
$\uparrow$ étant donné 2 éléments on a 2 possibilités de les arranger mais on se fiche de l'ordre.

<u>**Preuve de la proposition**</u>

On commence par construire les sous-ensembles <u>ordonnés</u> à $k$ éléments
$$\implies n(n - 1) \cdots (n - k + 1) \text{ possibilités}$$

Étant donnés $k$ éléments, il y a $k!$ possibilités de les arranger
$\implies$ puisqu'on ne prend pas l'ordre en compte il faut diviser le résultat précédent par $k!$
$$\binom{n}{k} = \frac{n(n - 1)(n - 2) \cdots \overset{\color{magenta}{\text{« n »}}}{(n - k + 1)}}{k!} = \frac{n!}{k!(n - k)!}$$

> [!important] Proposition
> Soit $n \in \mathbb{N}$ et soit $0 \leq k \leq n$
> ① $\underset{A = \varnothing}{\binom{n}{0}} = \underset{A = E}{\binom{n}{n}} = 1$
> ② $\underset{A}{\binom{n}{k}} = \underset{C_E(A)}{\binom{n}{n - k}}$
> ③ $\displaystyle\sum_{k=0}^{n} \binom{n}{k} = 2^n \quad \big(\mathrm{Card}(\mathcal{P}(E))\big)$
> ④ $\binom{n}{k} = \underset{x \notin A}{\binom{n - 1}{k}} + \underset{x \in A}{\binom{n - 1}{k - 1}}$

<u>Preuve algébrique de ④</u>
$$
\begin{aligned}
\binom{n - 1}{k - 1} + \binom{n - 1}{k} &= \frac{(n - 1)!}{(k - 1)!\,\underbrace{(n - 1 - (k - 1))!}_{(n - k)!}} + \frac{(n - 1)!}{k!\,(n - k - 1)!} \\
&= \frac{(n - 1)!\,k}{k!\,(n - k)!} + \frac{(n - 1)!\,(n - k)}{k!\,(n - k)!} \\
&= \frac{(n - 1)!\,k + (n - 1)!\,(n - k)}{k!\,(n - k)!} \\
&= \frac{n!}{k!\,(n - k)!} \quad \blacksquare
\end{aligned}
$$

<u>**Triangle de Pascal**</u>

![[al1-pascal.svg]]

- <span style="color:magenta">les 1 aux bords : point ① de la proposition</span>
- <span style="color:cyan">axe de symétrie : point ② de la proposition</span>
- <span style="color:orange">Un coefficient est la somme de ses deux parents : propriété ④</span>
- <span style="color:lime">la somme de tous les éléments d'une ligne $= 2^n$ : propriété ③</span>

<u>**Symbole de sommation**</u>
$$\sum_{k=0}^{n} a_k = a_0 + a_1 + a_2 + \dots + a_{n-1} + a_n$$

<u>Propriétés</u>

(1) $\displaystyle\sum_{k=0}^{n} a_k = \sum_{k=1}^{n+1} a_{k-1}$

(2) $\displaystyle\sum_{k=0}^{n} (a_k + b_k) = \sum_{k=0}^{n} a_k + \sum_{k=0}^{n} b_k$

(3) <span style="color:red">⚠️</span> $\displaystyle\left(\sum_{k=0}^{n} a_k\right)\left(\sum_{k=0}^{n} b_k\right) \neq \sum_{k=0}^{n} a_k b_k$

<u>**Binôme de Newton**</u>

Soient $x, y \in \mathbb{R}$, $n \in \mathbb{N}$

> [!important]
> $$\underbrace{(x + y)^n}_{(x + y)(x + y)\cdots(x + y) \ n \text{ fois}} = \sum_{k=0}^{n} \binom{n}{k} x^k y^{n-k}$$
> ↳ parmi les $n$ facteurs $x + y$, on en choisit $k$

<u>**exemples**</u>

① $(x + y)^2 = \overset{1}{\binom{2}{0}}x^0y^2 + \overset{2}{\binom{2}{1}}x^1y^1 + \overset{1}{\binom{2}{2}}x^2y^0 = 1y^2 + 2xy + 1x^2$

② Quel est le coefficient devant $x^3$ dans le développement de $(1 + x)^7$
$$(1 + x)^7 = \sum_{k=0}^{7} \binom{7}{k} x^k \underbrace{1^{7-k}}_{1}$$
$$\text{Coefficient devant } x^3 = \binom{7}{3} = \frac{7!}{3!\,(4!)} = \frac{7 \cdot 6 \cdot 5}{3 \cdot 2} = \underline{35}$$
