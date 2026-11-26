---
cours: Algèbre Linéaire
chapitre: 2
source: "Chapitre 2 - Algèbre Linéaire.pdf"
tags: [algebre-lineaire, chapitre-2]
---

# 2. Applications

### 2.1 Généralités

> [!definition]
> Une application est la donnée de deux ensembles $E$ et $F$ et d'un processus qui associe à tout élément de $E$ un unique élément de $F$, $f(x)$
> $$f : E \to F \qquad x \mapsto f(x)$$
> $f(x)$ est l'<u>image</u> de $x$ par $f$.

<u>**exemple :**</u>

![[al2-application-ou-pas.svg]]

<u>**exemples :**</u>

(1) $f : \{\alpha, \beta, \gamma\} \to \{\alpha, \beta, \gamma\}$, $\ f(\alpha) = \beta$, $\ f(\beta) = f(\gamma) = \alpha$

![[al2-exemple-alpha-beta-gamma.svg]]

(2) $f : \mathbb{R} \to \mathbb{R} \qquad x \mapsto x^2 - 5x + 6$

(3) $f : \mathbb{R} \to \mathbb{R}^2 \qquad x \mapsto (x^2, x^2)$

> [!definition] Déf
> Soit $f : E \to F$, $x \mapsto f(x)$ une application et soit $y \in F$
>
> <u>L'ensemble des antécédents</u> de $y$ (« pré-image ») est
> $$f^{-1}(\{y\}) = \{x \in E \mid f(x) = y\} \subset E$$

> <span style="color:red">⚠️ $f^{-1}$ n'est pas une application en général</span>
> - $f^{-1}(\{f(x)\}) \neq \{x\}$

<u>ex :</u>

(1) $f : \{\alpha, \beta, \gamma\} \to \{\alpha, \beta, \gamma\}$, $\ f(\alpha) = \beta$, $f(\beta) = f(\gamma) = \alpha$
$$f^{-1}(\{\alpha\}) = \{\beta, \gamma\} \qquad f^{-1}(\{\beta\}) = \{\alpha\} \qquad f^{-1}(\{\gamma\}) = \varnothing$$

(2) $f : \mathbb{R} \to \mathbb{R} \qquad x \mapsto x^2 - 5x + 6 = (x - 2)(x - 3)$

![[al2-parabole.svg]]

Soit $y \in \mathbb{R}$ fixé. Cherchons $f^{-1}(\{y\}) = \{x \in \mathbb{R} \mid x^2 - 5x + 6 = y\}$
$$x^2 - 5x + 6 = y \iff x^2 - 5x + (6 - y) = 0 \quad (\star)$$
$$\Delta = 25 - 4(6 - y) = 1 + 4y$$

Donc
- Si $y < -\frac{1}{4} \to \Delta < 0$, et $(\star)$ n'a pas de solutions
- Si $y = -\frac{1}{4} \to \Delta = 0$, et $(\star)$ a une seule solution $x = 5/2$
- Si $y > -\frac{1}{4} \to \Delta > 0$, et $(\star)$ a deux solutions $x = \dfrac{5 \pm \sqrt{1 + 4y}}{2}$

Finalement
$$f^{-1}(\{y\}) = \begin{cases} \varnothing & \text{si } y < -\frac{1}{4} \\ \{5/2\} & \text{si } y = -\frac{1}{4} \\ \left\{\dfrac{5 - \sqrt{1 + 4y}}{2}, \dfrac{5 + \sqrt{1 + 4y}}{2}\right\} & \text{si } y > -\frac{1}{4} \end{cases}$$

(3) $f : \mathbb{R} \to \mathbb{R}^2 \qquad x \mapsto (x^2, x^2)$

Soit $(a, b) \in \mathbb{R}^2$
$$
\begin{aligned}
f^{-1}(\{(a, b)\}) &= \{x \in \mathbb{R} \mid (x^2, x^2) = (a, b)\} \\
&= \varnothing \quad \text{soit si } a \neq b \text{ ou si } a, b < 0 \\
&= \{0\} \quad \text{si } (a, b) = (0, 0) \\
&= \{-\sqrt{a}, \sqrt{a}\} \quad \text{si } a = b \text{ et } a > 0
\end{aligned}
$$

---

### 2.2 Image directe

> [!definition]
> Soit $f : E \to F$, $x \mapsto f(x)$ et soit $A \subset E$
>
> L'image directe de $A$ par $f$ est
> $$f(A) = \{f(x) \mid x \in A\} = \{y \in F \mid \exists x \in A, f(x) = y\}$$

En prenant $A = E$ ci-dessus, on obtient <u>l'image directe de $f$</u> notée $f(E)$ ou <u>$\mathrm{Im}(f)$</u>

On a
$$\mathrm{Im}(f) = \{y \in F \mid \exists x \in E, f(x) = y\} = \{y \in F \mid f^{-1}(\{y\}) \neq \varnothing\}$$

<u>ex.</u>

![[al2-image-directe.svg]]

$$C_F(\mathrm{Im}(f)) = \{y \in F \mid f^{-1}(\{y\}) = \varnothing\}$$

<u>**exemples**</u>

(1) $f : \mathbb{R} \to \mathbb{R} \qquad x \mapsto x^2 - 5x + 6$
1. $f(\mathbb{R}) = \left[-\frac{1}{4}, +\infty\right[$
2. $f([2, 4]) = \left[-\frac{1}{4}, 2\right] \neq [f(2), f(4)]$

<u>Autre manière de voir les choses :</u>
$$
\begin{aligned}
y \in f([2, 4]) &\iff \exists x \in [2, 4], \ f(x) = y \\
&\iff \exists x \in [2, 4] \cap f^{-1}(\{y\}) \\
&\iff f^{-1}(\{y\}) \cap [2, 4] \neq \varnothing \\
&\iff y \geq -\tfrac{1}{4} \text{ et } \frac{5 - \sqrt{1 + 4y}}{2} \in [2, 4] \ \text{ ou } \ \frac{5 + \sqrt{1 + 4y}}{2} \in [2, 4] \\
&\iff \begin{cases} 2 \leq \dfrac{5 - \sqrt{1 + 4y}}{2} \leq 4 \\ \text{ou} \\ 2 \leq \dfrac{5 + \sqrt{1 + 4y}}{2} \leq 4 \end{cases}
\end{aligned}
$$

(3) $f : \mathbb{R} \to \mathbb{R}^2 \qquad x \mapsto (x^2, x^2)$
$$f(\mathbb{R}) = \{(a, a) \mid a \in \mathbb{R}_+\} \neq \mathbb{R}_+ \times \mathbb{R}_+$$

---

### 2.3 Image réciproque

> [!definition] Déf
> $f : E \to F$, $x \mapsto f(x)$ et soit $B \subset F$
>
> L'image réciproque de $B$ par $f$ est $f^{-1}(B)$
> $$f^{-1}(B) = \underbrace{\bigcup_{y \in B} f^{-1}(\{y\})}_{\text{union sur les } y \text{ dans } B} = \{x \in E \mid f(x) \in B\} \subset E$$

<u>Remarque :</u>
- Si $B = F$, $f^{-1}(F) = \{x \in E \mid f(x) \in F\} = E$
- Si $B \subset C_F(\mathrm{Im}(f))$, $f^{-1}(B) = \varnothing$

![[al2-image-reciproque.svg]]

<u>**exemples**</u>

(1) $f : \mathbb{R} \to \mathbb{R} \qquad x \mapsto x^2 - 5x + 6$
$$f^{-1}([0, 6]) = [0, 2] \cup [3, 5]$$

(2) $f : [0, 2\pi[ \ \to \mathbb{R} \qquad x \mapsto \cos(x)$
- (i) $f^{-1}(]2, 3[) = \displaystyle\bigcup_{y \in ]2, 3[} f^{-1}(\{y\})$
- (ii) $f^{-1}([0, 1[) = \left]0, \frac{\pi}{2}\right] \cup \left[\frac{3\pi}{2}, 2\pi\right[$

---

### 2.4 Injection

> [!definition] Déf
> Soit $f : E \to F$, $x \mapsto f(x)$ une application. $f$ est dite <u>injective</u> si :
> $$\forall x, x' \in E, \ x \neq x' \implies f(x) \neq f(x')$$

![[al2-injection.svg]]

De manière équivalente, $f$ injective si et seulement si
$$
\begin{aligned}
&\forall x, x' \in E, \ f(x) = f(x') \implies x = x' \\
\iff &\forall x \in E, \ f^{-1}(\{f(x)\}) = \{x\} \\
\iff &\forall y \in F, \ \mathrm{Card}(f^{-1}(\{y\})) \leq 1
\end{aligned}
$$

<u>Remarque :</u> $f$ n'est pas injective $\iff \exists x, x' \in E$, avec $x \neq x'$ et $f(x) = f(x')$

<u>**Exemples**</u>

1) $f : E \to E$, $x \mapsto x$ est injective.

2) Soit $E, F$ deux ensembles avec $\mathrm{Card}(E) \geq 2$ et soit $c \in F$. Alors
$$f : E \to F \qquad x \mapsto c$$
(non injective, tous $x$ de $E$ sont envoyés sur $c$)

3) $f : \mathbb{R} \to \mathbb{R}$, $x \mapsto x^2$ n'est pas injective, $(x = \pm 2 \to f(x) = 4)$

4) $f : \mathbb{N} \to \mathbb{N}$, $n \mapsto n^2$ est injective.

En effet
$$\forall m, n \in \mathbb{N}, \ m \neq n \implies m^2 - n^2 = \underbrace{(m - n)}_{\neq 0}\underbrace{(m + n)}_{> 0} \neq 0$$

5) $f : \mathbb{R} \to \mathbb{R}$, $x \mapsto x^3 - 2x^2 + 3x$

Soit $x \in \mathbb{R}$. Essayons de déterminer $f^{-1}(\{f(x)\})$
$$
\begin{aligned}
y \in f^{-1}(\{f(x)\}) &\iff f(y) = f(x) \\
&\iff y^3 - 2y^2 + 3y = x^3 - 2x^2 + 3x \\
&\iff y^3 - x^3 - 2(y^2 - x^2) + 3(y - x) = 0 \\
&\iff (y - x)\big[(x^2 + xy + y^2) - 2(x + y) + 3\big] = 0 \\
&\iff (y - x) = 0 \ \text{ ou } \ \underbrace{(x^2 + xy + y^2) - 2(x + y) + 3 = 0}_{(\star)}
\end{aligned}
$$

$(\star)$ est une équation quadratique en $y$
$$y^2 + (x - 2)y + (x^2 - 2x + 3) = 0$$
$$\Delta = b^2 - 4ac = (x - 2)^2 - 4(x^2 - 2x + 3) = x^2 - 4x + 4 - 4x^2 + 8x - 12 = -3x^2 + 4x - 8$$

![[al2-delta-negatif.svg]]

$$\Delta' = 16 - 4(-3)(-8) < 0$$

Donc $y^2 + (x - 2)y + (x^2 - 2x + 3) = 0$ n'a pas de solutions

Alors $y - x = 0 \to x = y$ donc $f$ est injective.

---

### 2.5 Restriction

<u>Idée :</u> « Séparer les 'doublons' pour rendre $f$ injective »

> [!definition] Déf
> Soit $f : E \to F$, $x \mapsto f(x)$ une application et soit $A \subset E$
>
> La restriction de $f$ à $A$ est
> $$f_{|A} : A \to F \qquad x \mapsto f(x)$$
> (la seule chose qui change est l'ensemble de départ)

<u>Remarque :</u>
- $\mathrm{Im}(f_{|A}) = f(A)$
- $\underbrace{f_{|A}^{-1}(\{y\})}_{\subset E} = \underbrace{f^{-1}(\{y\})}_{\subset E} \cap A \quad \forall y \in F$

![[al2-restriction.svg]]

<u>**exemple :**</u> Soit $f : \mathbb{R} \to \mathbb{R}$, $x \mapsto x^2 - 5x + 6$

1) Voyons si $f$ est injective

Soit $x \in \mathbb{R}$
$$
\begin{aligned}
y \in f^{-1}(\{f(x)\}) &\iff f(y) = f(x) \\
&\iff y^2 - 5y + 6 = x^2 - 5x + 6 \\
&\iff y^2 - x^2 - 5(y - x) = 0 \\
&\iff (y - x)[y + x - 5] = 0 \\
&\iff y = x \ \text{ ou } \ y = 5 - x
\end{aligned}
$$

Donc $f^{-1}(\{f(x)\}) = \{x, 5 - x\}$

$\implies$ pour $x \neq \frac{5}{2}$, $\ \mathrm{Card}(f^{-1}(\{f(x)\})) = 2$

Donc $f$ n'est pas injective.

Mais les restrictions suivantes sont injectives
- $f_{|[\frac{5}{2}, +\infty[}$. En effet si $x > \frac{5}{2}$, $5 - x < \frac{5}{2}$ et donc $5 - x \notin A$
- $f_{|]-\infty, \frac{5}{2}]}$. En effet si $x < \frac{5}{2}$, $5 - x > \frac{5}{2}$ et donc $5 - x \notin A$
- $f_{|[0, 1] \cup [6, +\infty[}$ est aussi injective.

  En effet
  - si $0 \leq x \leq 1$, alors $4 \leq 5 - x \leq 5 \implies 5 - x \notin A$
  - si $x \geq 6$, $5 - x \leq -1$

---

### 2.6 Composition d'applications

> [!definition]
> Soient $f : E \to F$, $x \mapsto f(x)$ et $g : F \to G$, $x \mapsto g(x)$
>
> Alors la composée de $f$ avec $g$ est l'application suivante
> $$g \circ f : E \to G \qquad x \mapsto g(f(x)) = (g \circ f)(x)$$

![[al2-composition.svg]]

<u>**exemples**</u>

1) $f : \{\alpha, \beta, \gamma\} \to \{a, b, c\}$, $\quad f(\alpha) = b$, $\ f(\beta) = f(\gamma) = a$
   $g : \{a, b, c\} \to \{1, 2, 3\}$, $\quad g(a) = 1$, $\ g(b) = 3$, $\ g(c) = 2$

   Alors $g \circ f : \{\alpha, \beta, \gamma\} \to \{1, 2, 3\}$
   $$g \circ f(\alpha) = g(f(\alpha)) = 3$$

2) $f : \mathbb{R} \to \mathbb{R}$, $x \mapsto \cos(x)$ $\qquad g : \mathbb{R} \to \mathbb{R}$, $x \mapsto x^2$
$$g \circ f : \mathbb{R} \to \mathbb{R}, \ x \mapsto g(f(x)) = \cos^2(x) \qquad f \circ g : \mathbb{R} \to \mathbb{R}, \ x \mapsto \cos(x^2)$$

3) $f : \mathbb{R}_+ \to \mathbb{R}$, $x \mapsto \sqrt{x}$ $\qquad g : \mathbb{R} \to \mathbb{R}_+$, $x \mapsto x^2$
$$f \circ g : \mathbb{R} \to \mathbb{R}, \ x \mapsto f(g(x)) = |x| \qquad g \circ f : \mathbb{R}_+ \to \mathbb{R}_+, \ x \mapsto (\sqrt{x})^2 = x$$

---

### 2.7 Surjectivité

> [!definition] Déf
> Soit $f : E \to F$ une application. On dit que $f$ est <u>surjective</u> si :
> $$\forall y \in F, \ \mathrm{Card}(f^{-1}(\{y\})) \geq 1$$
> $$f \text{ surjective} \iff \forall y \in F, \exists x \in E, f(x) = y \iff \mathrm{Im}(f) = F$$

![[al2-surjection.svg]]

<u>Remarque :</u> $f$ n'est pas surjective si $\exists y \in F, \forall x \in E, f(x) \neq y \iff \exists y \in F, \mathrm{Card}(f^{-1}(\{y\})) = 0$

<u>**Exemples :**</u>

1) $f : E \to E$, $x \mapsto x$ est surjective (identité)

2) Soient $E, F$ deux ensembles et $c \in F$. Alors l'application constante $f : E \to F$, $x \mapsto c$ n'est pas surjective si $\mathrm{card}(F) \geq 2$

3) $f : \mathbb{R} \to \mathbb{R}$, $x \mapsto 2x + 1$. Cette application est surjective $\forall y \in \mathbb{R}$
$$f^{-1}(\{y\}) = \left\{\frac{y - 1}{2}\right\}$$

![[al2-droite-2x-1.svg]]

4) $f : \mathbb{R} \to \mathbb{R}$, $x \mapsto x^2 + 1$ n'est <u>pas</u> surjective.
$$f^{-1}(\{y\}) = \varnothing \quad \forall y < 1$$

![[al2-parabole-x2-1.svg]]

<u>mais :</u> $f : \mathbb{R} \to [1, +\infty[$, $x \mapsto x^2 + 1$, elle est surjective.

<u>Remarque :</u> Toute application $f : E \to F$ induit une surjection
$$\tilde{f} : E \to \mathrm{Im}(f) \qquad x \mapsto f(x) \quad \text{(la corestriction de } f\text{)}$$

<u>**Exemples :**</u>

1) $f : \mathbb{R} \to \mathbb{R}^2$, $\alpha \mapsto (\cos(\alpha), \sin(\alpha))$ $\quad$ Cette application n'est <u>pas</u> surjective

![[al2-cercle-trigo.svg]]

$$f^{-1}(\{(0, 0)\}) = \varnothing$$
$$\mathrm{Im}(f) = \{(x, y) \mid x^2 + y^2 = 1\} = \text{cercle trigo}$$

$f : \mathbb{R} \to$ cercle trigo, $\alpha \mapsto (\cos\alpha, \sin\alpha) = P(\alpha)$ est surjective

Mais elle n'est <u>pas</u> injective $P(0) = P(2\pi)$

$\mathbb{R}^2$ = produit cartésien de $\mathbb{R}$, un couple $\implies$ abscisse et ordonnée

2) $f : \mathbb{R}^2 \to \mathbb{R}^2$, $(x, y) \mapsto (x^2 - 2xy, 2x - y)$

Soit $(u, v) \in \mathbb{R}^2$. Cherchons ses antécédents
$$
\begin{aligned}
(x, y) \in f^{-1}(\{(u, v)\}) &\iff f(x, y) = (u, v) \\
&\iff \begin{cases} x^2 - 2xy = u \\ 2x - y = v \end{cases} \iff \begin{cases} x^2 - 2x(2x - v) = u \\ y = 2x - v \end{cases} \\
&\iff \begin{cases} -3x^2 + 2xv - u = 0 & (\star) \ \text{trinôme du 2ème degré } (\sigma) \\ y = 2x - v \end{cases}
\end{aligned}
$$

$$\Delta = (2v)^2 - 4(-3)(-u) = 4v^2 - 12u \qquad \big(\text{Si } \Delta < 0, f \text{ a aucun antécédent } f^{-1}(\{(u, v)\}) = \varnothing\big)$$

En particulier, $f$ n'est <u>pas</u> surjective
- si $v^2 \geq 3u$, $(\star)$ admet comme solutions :
$$x_\pm = \frac{-2v \pm \sqrt{4v^2 - 12u}}{-6} = \frac{v \mp \sqrt{v^2 - 3u}}{3}$$

Finalement, on trouve
$$f^{-1}(\{(u, v)\}) = \begin{cases} \varnothing & \text{si } v^2 < 3u \\ \left\{\left(\frac{v}{3}, -\frac{v}{3}\right)\right\} & \text{si } v^2 = 3u \\ \left\{\left(\frac{v + \sqrt{v^2 - 3u}}{3}, \frac{-v + 2\sqrt{v^2 - 3u}}{3}\right), \left(\frac{v - \sqrt{v^2 - 3u}}{3}, \frac{-v - 2\sqrt{v^2 - 3u}}{3}\right)\right\} & \text{si } v^2 > 3u \end{cases}$$

Donc la corestriction
$$f : \mathbb{R}^2 \to \{(u, v) \mid v^2 \geq 3u\} \qquad (x, y) \mapsto (x^2 - 2xy, 2x - y) \quad \text{est surjective.}$$

---

### 2.8 Bijective

> [!definition] Déf
> Soit $f : E \to F$ une application. On dit que $f$ est <u>bijective</u> si elle est à la fois injective ① et surjective ②
> ① $\forall y \in F$, $\mathrm{card}(f^{-1}(\{y\})) \leq 1$
> ② $\forall y \in F$, $\mathrm{Card}(f^{-1}(\{y\})) \geq 1$
>
> $f$ est donc bijective si et seulement si $\forall y \in F$, $\mathrm{Card}(f^{-1}(\{y\})) = 1$
> $$\iff \forall y \in F, \ \underset{\color{magenta}{\text{surjectivité}}}{\text{il existe}} \ \underset{\color{cyan}{\text{injectivité}}}{\text{un unique}} \ x \text{ dans } E, \ f(x) = y$$

![[al2-bijection.svg]]

En associant à chaque $y \in F$ son unique antécédent par $f$, on construit l'application réciproque / l'inverse de $f$
$$f^{-1} : F \to E \qquad y \mapsto \underbrace{x \mid f(x) = y}_{f^{-1}(y)}$$

<u>**En particulier**</u>
$$f^{-1} \circ f : E \to E, \ x \mapsto x \ \text{ est l'identité } E \qquad f \circ f^{-1} : F \to F, \ y \mapsto y \ \text{ est identité } F$$

<u>**Exemple**</u>

1) $\mathrm{id}_E : E \to E$, $x \mapsto x$ est bijective et son inverse est $(\mathrm{id}_E)^{-1} = \mathrm{id}_E$

2) $f : ]0, +\infty[ \ \to \ ]0, +\infty[$, $\ x \mapsto \dfrac{1}{\sqrt{x}}$

$f$ est bijective. En effet, si $y \in ]0, +\infty[$ alors
$$x \in f^{-1}(\{y\}) \iff f(x) = y \iff \frac{1}{\sqrt{x}} = y \iff \frac{1}{x} = y^2 \iff x = \frac{1}{y^2}$$

Et donc
$$f^{-1} : ]0, +\infty[ \ \to \ ]0, +\infty[ \qquad y \mapsto \frac{1}{y^2}$$

<u>**Processus pour construire une bijection**</u>

Soit $f : E \to F$ une application ni injective ni surjective. Pour en déduire une bijection, on procède en 2 étapes.

1) On considère la corestriction de $f$ à $\mathrm{Im}(f)$
$$\tilde{f} : E \to \mathrm{Im}(f) \qquad x \mapsto f(x) \qquad \tilde{f} \text{ est alors surjective}$$

2) On choisit $A \subset E$,
   - i. $f(A) = \mathrm{Im}(f)$
   - ii. $\forall y \in \mathrm{Im}(f)$, $f^{-1}(\{y\}) \cap A$ contient un <u>unique</u> élément

Alors
$$\tilde{f}_{|A} : A \to \mathrm{Im}(f) \qquad x \mapsto f(x)$$
est à la fois surjective et injective. Elle est bijective.

<u>**Exemple :**</u>

$\cos : \mathbb{R} \to \mathbb{R}$, $x \mapsto \cos x$ n'est ni injective ni surjective.

1) $\mathrm{Im}(\cos) = [-1, 1]$. Donc $\cos : \mathbb{R} \to [-1, 1]$, $x \mapsto \cos x$ est surjective

![[al2-cos-bijection.svg]]

2) $\cos : [0, \pi] \to [-1, 1]$, $x \mapsto \cos x$ est bijective.
   Sa réciproque est $\arccos : [-1, 1] \to [0, \pi]$, $y \mapsto x$ où $\cos(x) = y$
