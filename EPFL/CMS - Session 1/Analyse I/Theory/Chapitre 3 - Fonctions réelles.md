---
cours: Analyse I
chapitre: 3
source: "Chapitre 3 - Analyse I.pdf"
tags: [analyse-I, chapitre-3]
---

# Chapitre 3 : Fonctions réelles

### 3.1 Introduction

> [!definition] Déf
> Une fonction associe un objet $x \in D$ à un objet $y \in A$. On note
> $$f : D \to A \qquad x \mapsto f(x) = y$$

> Si $D = A = \mathbb{R}$, on dit que $f$ est une <u>fonction réelle à valeur réelle</u>. On note donc
> $$f : \mathbb{R} \to \mathbb{R} \qquad x \mapsto y = f(x)$$
>
> L'<u>ensemble de définition</u> $D_{déf}$ est l'ensemble des $x \in D$ tel qu'il $\exists\, y \in A$ associé par $f$.
>
> <u>L'image de $f$</u> : $\mathrm{Im}(f)$, est l'ensemble des $y \in A$ tel que $\exists\, x \in D_{déf}(f)$ tel que $y = f(x)$

> Le graphe d'une fonction est donné par
> $$G_f := \big\{(x, y) \in D_{déf} \times \mathrm{Im}(f) \ \big|\ y = f(x)\big\}$$

<u>**Exemple :**</u>

**1)** $f(x) = \sqrt{x + 1}$
$$f : \mathbb{R} \to \mathbb{R} \qquad x \mapsto y = \sqrt{x + 1}$$
$$D_{déf}(f) = [-1, \infty[ \ , \qquad \mathrm{Im}(f) = \mathbb{R}_+$$

![[ch3-racine.svg]]

**2)**
$$g : \mathbb{R} \to \mathbb{R} \qquad x \mapsto \frac{x^2 - 2x}{(x - 1)^2} = y = g(x)$$
$$D_{déf}(g) = \mathbb{R} \setminus \{1\} \qquad \mathrm{Im}(g)$$

i) <u>Déterminer l'image,</u> $y = \dfrac{x^2 - 2x}{(x - 1)^2}$

$$
\begin{aligned}
\underset{x \in D_{déf}(g)}{\iff} \quad (x - 1)^2\,y &= x^2 - 2x \\
\iff (x^2 - 2x + 1)\,y &= x^2 - 2x \\
\iff x^2(y - 1) - 2x(y - 1) + y &= 0
\end{aligned}
$$

$$y \in \mathrm{Im}(g) \iff \Delta \geq 0 \iff 4(y - 1)^2 - 4(y - 1)(y) \geq 0, \quad y \neq 1$$
$$
\begin{aligned}
&\iff 4(y^2 - 2y + 1) - 4y^2 + 4y \geq 0 \\
&\iff -4y + 4 \geq 0 \\
&\qquad -4y \geq -4 \\
&\qquad \underline{y \leq 1} \to \underline{y < 1}
\end{aligned}
$$
$$y \in \left]-\infty, 1\right[$$

ii) <u>Déterminer l'image</u>
$$g(x) = \frac{x^2 - 2x}{(x - 1)^2} = \frac{x^2 - 2x + 1 - 1}{(x - 1)^2} = \frac{(x - 1)^2 - 1}{(x - 1)^2} = 1 - \frac{1}{(x - 1)^2} < 1$$

On peut donc déjà tracer $G_g$

![[ch3-graphe-g.svg]]

**3)** $h(x) = \lfloor x \rfloor \qquad D_{déf} = \mathbb{R} \qquad \mathrm{Im}(h) = \mathbb{Z}$

![[ch3-partie-entiere.svg]]

**4)**
$$\det : M_2(\mathbb{R}) \to \mathbb{R} \qquad \begin{bmatrix} a & b \\ c & d \end{bmatrix} \mapsto ad - bc$$
$$D_{déf} = M_2(\mathbb{R}) \qquad \mathrm{Im}(\det) = \mathbb{R}$$

**5)** $\vec{v}, \vec{x} \mapsto \mathrm{proj}_{\vec{x}}(\vec{v})$
$$\mathrm{proj} : \mathbb{R}^2 \times \mathbb{R}^2 \to \mathbb{R}^2 \qquad (\vec{v}, \vec{x}) \mapsto \frac{\vec{v} \cdot \vec{x}}{\Vert\vec{x}\Vert^2}\,\vec{x}$$
$$D_{déf}(\mathrm{proj}) = \mathbb{R}^2 \times \mathbb{R}^{2*} \qquad \mathrm{Im}(\mathrm{proj}) = \mathbb{R}^2$$

**6)** $\ln$
$$\mathbb{R}_+^* \ni x \mapsto$$

![[ch3-ln.svg]]

Définition géométrique.

> [!definition] Déf
> Pour une fonction $f : \mathbb{R} \to \mathbb{R}$ on dit que son ensemble de définition est <u>symétrique</u> si et seulement si
> $$x \in D_{déf}(f) \iff -x \in D_{déf}(f)$$
> - $f$ est dite <u>paire</u> si et seulement si $D_{déf}(f)$ est symétrique et $f(x) = f(-x)$
> - $f$ est dite <u>impaire</u> si et seulement si $D_{déf}(f)$ est symétrique et $f(x) = -f(-x)$

<u>**Exemples**</u>

|                                           |                |
| :---------------------------------------- | :------------- |
| $f(x) = \lvert x\rvert$                   | <u>paire</u>   |
| $\cos(x)$                                 | <u>paire</u>   |
| $x^{2k}$                                  | <u>paire</u>   |
| $f(x) = x^{2n+1}$                         | <u>impaire</u> |
| $\sin(x)$                                 | <u>impaire</u> |
| $\tan(x)$                                 | <u>impaire</u> |
| $f(x) = x^2 - x^3$, $\ \lfloor x \rfloor$ | <u>mais</u>    |

<u>**Exercice**</u>

Si $D_{déf}(f)$ est symétrique, il existe une fonction paire, $f_+$ et une fonction impaire $f_-$, tel que
$$\boxed{f(x) = f_+(x) + f_-(x)}$$
$$\left(f(x) = \underbrace{\frac{1}{2}f(x) + \frac{1}{2}f(-x)}_{\text{paire}} + \underbrace{\frac{1}{2}f(x) - \frac{1}{2}f(-x)}_{\text{impaire}}\right)$$

> [!definition] Déf
> Pour $f : \mathbb{R} \to \mathbb{R}$, on dit qu'elle est <u>périodique</u> si et seulement si $\exists\, T > 0$, tel que $f(x) = f(x + T)$ $\forall x \in D_{déf}(f)$
>
> La <u>période</u> de $f$ est alors le plus petit $T > 0$ tel que
> $$f(x) = f(x + T) \quad \forall x \in D_{déf}(f)$$

> [!definition] Déf
> Une fonction réelle est dite <u>croissante</u> si et seulement si $\forall x, x' \in D_{déf}(f)$
> $$x > x' \implies f(x) \geq f(x')$$
> $\big(f(x) > f(x')\big)$ strictement croissante.

<u>**Exemple :**</u> résoudre $\sqrt[3]{1 - x^2} + x > 1 \qquad (1)$

$D_{déf} = \mathbb{R}$

$$
\begin{aligned}
(1) &\iff \sqrt[3]{1 - x^2} > 1 - x && \big(x \mapsto \sqrt[3]{x}\big) \text{ est croissante} \\
&\iff (1 - x^2) > (1 - x)^3 && \big(x \mapsto x^3\big) \text{ est croissante} \\
&\iff \cancel{1} - x^2 > \cancel{1} - 3x + 3x^2 - x^3 \\
&\iff -x^2 > -3x + 3x^2 - x^3 \\
&\iff x^3 - 4x^2 + 3x > 0 \\
&\iff x(x^2 - 4x + 3) > 0 \\
&\iff x(x - 3)(x - 1) > 0
\end{aligned}
$$

| $x$ | | $0$ | | $1$ | | $3$ | |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| $x$ | $-$ | $0$ | $+$ | | $+$ | | $+$ |
| $x - 1$ | $-$ | | $-$ | $0$ | $+$ | | $+$ |
| $x - 3$ | $-$ | | $-$ | | $-$ | $0$ | $+$ |
| $(1)$ | $-$ | | $+$ | | $-$ | | $+$ |

$$(1) \iff x \in \left]0, 1\right[ \cup \left]3, \infty\right[$$

> [!definition] Déf
> Soient $f, g : \mathbb{R} \to \mathbb{R}$ telles que $\mathrm{Im}(f) \subset D_{déf}(g)$. La composée de $f$ avec $g$ est donnée par
> $$g \circ f = g\big(f(x)\big) \quad \forall x \in D_{déf}(f)$$

⚠️ $g \circ f \neq f \circ g$ en général

$$f(x) = x + a, \qquad g(x) = x^2$$

![[ch3-composition.svg]]

En général si
$$p(x) = x^2 + ax + b = \left(x + \frac{a}{2}\right)^2 - \frac{a^2}{4} + b$$

On a donc
$$
\begin{aligned}
p(x) &= \left(x + \frac{a}{2}\right)^2 \color{magenta}{+ b - \frac{a^2}{4}} \\
&= \left(x + b - \frac{a^2}{4}\right) \circ \left(x^2 \circ \left(x + \frac{a}{2}\right)\right)
\end{aligned}
$$

> [!definition] Déf
> Une fonction réelle à valeur réelle est dite <u>minorée</u> par un nombre réel $m$ si et seulement si $\forall x \in D_{déf}(f)$
> $$f(x) \geq m$$
> Elle est dite <u>majorée</u> par $M \in \mathbb{R}$ si et seulement si $\forall x \in D_{déf}(f)$
> $$f(x) \leq M$$

---

### 3.2 Limites des fonctions réelles

#### 3.2.1 Fonction définie au voisinage de l'infini

> [!definition] Déf
> Une fonction $f : \mathbb{R} \to \mathbb{R}$ est dite <u>définie au voisinage de l'infini</u> (noté $f$ d.v. $\infty$) s'il existe $m \in \mathbb{R}$ tel que $]m, \infty[ \ \subset D_{déf}(f)$.
>
> Elle est définie au voisinage de $-\infty$ (noté $f$ d.v. $-\infty$) s'il existe $m \in \mathbb{R}$ tel que $]-\infty, m[ \ \subset D_{déf}(f)$

<u>**Exemple :**</u>

**1.** $f(x) = \dfrac{1}{x} \qquad D_{déf}(f) = \mathbb{R}^*$

On a $\ ]1, \infty[ \ \subset D_{déf}(f)\ $ et $\ ]-\infty, -1[ \ \subset D_{déf}(f)$

donc $f$ d.v. $\infty$ et $f$ d.v. $-\infty$

**2.** $g(x) = \tan(x) \qquad D_{déf}(g) = \mathbb{R} \setminus \left\{\frac{\pi}{2} + k\pi \ \middle|\ k \in \mathbb{Z}\right\}$

$D_{déf}(g)$ ne contient pas d'intervalles du type $]m, \infty[$ ou $]-\infty, -m[$ car il y a des trous partout.

Donc $\tan(x)$ n'est pas $g$ d.v. $\pm\infty$

#### 3.2.2 Limite finie en l'infini

> [!definition] Déf
> Soit $f : \mathbb{R} \to \mathbb{R}$, $f$ d.v. $\infty$ (resp. $-\infty$). On dit que la limite de $f(x)$ quand $x$ tend vers l'infini est $l \in \mathbb{R}$ si :
> $$\forall \varepsilon > 0, \ \exists\, x_\varepsilon \text{ tel que } x \geq x_\varepsilon \implies |f(x) - l| < \varepsilon$$
> On note $\displaystyle\lim_{x \to \infty} f(x) = l$ $\quad \Big(\text{resp. } \displaystyle\lim_{x \to -\infty} f(x) = l\Big)$

<u>**Exemples**</u>

**1.** $\displaystyle\lim_{x \to \infty} \frac{1}{x} = 0$

$\dfrac{1}{x}$ est d.v. sur $\infty$. On se donne $\varepsilon > 0$ et on cherche à résoudre $\left|\dfrac{1}{x} - 0\right| < \varepsilon$. Puisque $x \to \infty$ on peut chercher $x_\varepsilon$ dans $\mathbb{R}_+^*$. Alors :
$$\left|\frac{1}{x}\right| < \varepsilon \iff x > \frac{1}{\varepsilon}$$

On peut donc choisir $x_\varepsilon = \dfrac{1}{\varepsilon} + 1$

#### 3.2.3 Caractérisation par les suites

> [!important] Théorème
> Soit $f : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$ (resp. $-\infty$). Alors il y a équivalence entre :
> 1. $\displaystyle\lim_{x \to \infty} f(x) = l$
> 2. $\forall (a_n)$ de $D_{déf}(f)$ telle que $\displaystyle\lim_{n \to \infty} a_n = \infty$ on a $\displaystyle\lim_{n \to \infty} f(a_n) = l$

<u>**Exemple :**</u> $\sin(x)$

$\sin(x)$ est d.v. $\infty$. On va montrer que $\displaystyle\lim_{x \to \infty} \sin(x)$ n'existe pas. Pour cela on exhibe deux suites $(a_n)$ et $(b_n)$ telles que $\lim a_n = \infty = \lim b_n$ mais $\lim \sin(a_n) = 0 \neq 1 = \lim \sin(b_n)$.

On peut prendre $a_n = n\pi$ et $b_n = \dfrac{\pi}{2} + n\pi$

#### 3.2.4 Limite infinie en l'infini

> [!definition] Déf
> Soit $f : \mathbb{R} \to \mathbb{R}$, $f$ d.v. $\infty$ (resp. $-\infty$). On dit que $f(x)$ diverge vers l'infini (resp. $-\infty$) quand $x$ tend vers $\infty$ (resp. $-\infty$). On note $\displaystyle\lim_{x \to \infty} f(x) = \infty$ (resp. $-\infty$) et de même pour $x \to -\infty$.

| <u>Condition</u> | <u>Notation</u> |
| :-- | :-- |
| $\forall B \in \mathbb{R}, \ \exists\, x_B$ tel que $x \geq x_B \implies f(x) \geq B$ | $\displaystyle\lim_{x \to \infty} f(x) = +\infty$ |
| $\forall B \in \mathbb{R}, \ \exists\, x_B$ tel que $x \geq x_B \implies f(x) \leq B$ | $\displaystyle\lim_{x \to \infty} f(x) = -\infty$ |
| $\forall B \in \mathbb{R}, \ \exists\, x_B$ tel que $x \leq x_B \implies f(x) \geq B$ | $\displaystyle\lim_{x \to -\infty} f(x) = \infty$ |
| $\forall B \in \mathbb{R}, \ \exists\, x_B$ tel que $x \leq x_B \implies f(x) \leq B$ | $\displaystyle\lim_{x \to -\infty} f(x) = -\infty$ |

<u>**Exemple :**</u> montrer que $\displaystyle\lim_{x \to -\infty} x^2 = \infty$

Prenons $B \in \mathbb{R}$ et résolvons $x^2 \geq B$
- On a $x^2 \geq |B| \implies x^2 \geq B$
- Mais $x^2 \geq |B| \iff x \geq \sqrt{|B|}$ ou $x \leq -\sqrt{|B|}$
- On peut prendre $x_B = -\sqrt{|B|}$ $\big($ou $x_B = -\sqrt{|B|} - 1\big)$

<u>**Règle de calcul**</u> Soient $f, g : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$ et $\displaystyle\lim_{x \to \infty} f(x) = a$, $\displaystyle\lim_{x \to \infty} g(x) = b$

1) $\displaystyle\lim_{x \to \infty} |f(x)| = |a| \qquad$ ⚠️ pas de réciproque.
2) $\displaystyle\lim_{x \to \infty} \big(f(x) + g(x)\big) = a + b$
3) $\displaystyle\lim_{x \to \infty} \big(f(x) \cdot g(x)\big) = a \cdot b$
4) $\displaystyle\lim_{x \to \infty} \left(\frac{f(x)}{g(x)}\right) = \frac{a}{b} \quad$ (si $b \neq 0$ et $x$ « grand »)

Si $\displaystyle\lim_{x \to \infty} f(x) = a$ et $\displaystyle\lim_{x \to \infty} g(x) = \infty$

5) $\displaystyle\lim_{x \to \infty} \big(f(x) + g(x)\big) = \infty$
6) $\displaystyle\lim_{x \to \infty} \big(f(x) \cdot g(x)\big) = \mathrm{sgn}(a)\,\infty \quad$ si $a \neq 0$
7) $\displaystyle\lim_{x \to \infty} \frac{f(x)}{g(x)} = 0$

⚠️ Si $\displaystyle\lim_{x \to \infty} f(x) = 0$, $\ \displaystyle\lim_{x \to \infty} g(x) = \infty$
$$\lim_{x \to \infty} \big(f(x) \cdot g(x)\big) \text{ est indéterminé}$$

Si $\displaystyle\lim_{x \to \infty} h(x) = \infty$
$$\lim_{x \to \infty} \big(g(x) - h(x)\big) \text{ est indéterminé}$$

<u>**Exemple**</u> calculer $\displaystyle\lim_{x \to -\infty} \sqrt{x^2 + x} + x - 1$

Cas du type « $\infty - \infty$ » pour des fonctions d.v. $-\infty$

Amplification :
$$
\begin{aligned}
l &= \lim_{x \to -\infty} \frac{x^2 + x - (x - 1)^2}{\sqrt{x^2 + x} - x + 1} \qquad (\text{pour } x \leq -1) \\
&= \lim_{x \to -\infty} \frac{3x - 1}{\sqrt{x^2 + x} - x + 1} = \lim_{x \to -\infty} \frac{x\left(3 - \frac{1}{x}\right)}{|x|\sqrt{1 + \frac{1}{x}} + |x| + 1} \\
&= \lim_{x \to -\infty} \frac{x\left(3 - \frac{1}{x}\right)}{(-x)\left(\sqrt{1 + \frac{1}{x}} + 1 + \frac{1}{|x|}\right)} = -\frac{3}{2}
\end{aligned}
$$

> [!important] Théorème (critère par les suites)
> Soit $f : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$. On a équivalence des affirmations
> 1) $\displaystyle\lim_{x \to \infty} f(x) = l \in \mathbb{R}$
> 2) $\displaystyle\lim_{n \to \infty} f(a_n) = l \in \mathbb{R}$ $\quad \forall\ \displaystyle\lim_{n \to \infty} (a_n) = \infty$ $\big($et $a_n \in D_{déf}(f)$ $\forall n \in \mathbb{N}^*\big)$

<u>Preuve</u> **1) ⟹ 2)** Supposons que $\displaystyle\lim_{x \to \infty} f(x) = l$. Cela veut dire
$$\forall \varepsilon > 0, \ \exists\, x_\varepsilon \in \mathbb{R} \text{ tel que } x \geq x_\varepsilon \implies |f(x) - l| < \varepsilon$$

Soit $(a_n)_{n \in \mathbb{N}^*}$ tel que $\displaystyle\lim_{n \to \infty} a_n = \infty$ i.e.
$$\forall B \in \mathbb{R}, \ \exists\, N_B \text{ tel que } n \geq N_B \implies a_n \geq B$$

Cela implique, que pour $B = x_\varepsilon$, $\exists\, N_\varepsilon$ tel que
$$n \geq N_\varepsilon \implies a_n \geq x_\varepsilon$$

Mais alors, $n \geq N_\varepsilon \implies |f(a_n) - l| < \varepsilon$

Puisque $\varepsilon > 0$ était arbitraire, on a
$$\forall \varepsilon > 0, \ \exists\, N_\varepsilon \text{ tel que } n \geq N_\varepsilon \implies |f(a_n) - l| < \varepsilon$$
donc que $\displaystyle\lim_{n \to \infty} f(a_n) = l$

**2) ⟹ 1)** montrer que $\underline{\neg 1) \implies \neg 2)}$

Supposons $\exists\, \varepsilon > 0, \ \forall x_\varepsilon \in \mathbb{R}, \ \exists\, x \geq x_\varepsilon$ tel que $|f(x) - l| \geq \varepsilon$

Commençons par $a_1 \in \mathbb{R}$. Si on pose $x_\varepsilon = a_1 + 1$, $\exists\, a_2 \in \mathbb{R}$ tel que $|f(a_2) - l| \geq \varepsilon$

En général, on pose $x_\varepsilon = a_n + 1$ et il existe un $a_{n+1} \geq 1 + a_n$ tel que $|f(a_{n+1}) - l| \geq \varepsilon$

On vient de construire une suite $(a_n)_{n \in \mathbb{N}^*}$ telle que
$$a_n \geq a_1 + n \quad \text{et} \quad |f(a_n) - l| \geq \varepsilon$$

Donc, $\displaystyle\lim_{n \to \infty} a_n = \infty$ mais $|f(a_n) - l| \geq \varepsilon$

Donc 2) est faux $\blacksquare$

> [!important] Théorème des gendarmes
> Soient $d, f, g : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$. Supposons
> - $g(x) \leq f(x) \leq d(x) \quad \forall x \geq B$
> - $\displaystyle\lim_{x \to \infty} g(x) = l = \lim_{x \to \infty} d(x)$
>
> Alors $\displaystyle\lim_{x \to \infty} f(x) = l$

<u>Preuve :</u> Soit $(a_n)_{n \in \mathbb{N}^*}$ tel que $\displaystyle\lim_{n \to \infty} a_n = \infty$ $\big($et $a_n \in D_{déf}(f) \cap D_{déf}(g) \cap D_{déf}(d)\big)$

Par le critère des suites, $\displaystyle\lim_{n \to \infty} g(a_n) = l$ et $\displaystyle\lim_{n \to \infty} d(a_n) = l$ et $g(a_n) \leq f(a_n) \leq d(a_n)$

Par le théorème des gendarmes pour les suites, $\displaystyle\lim_{n \to \infty} f(a_n) = l$

Par les critères des suites, $\displaystyle\lim_{x \to \infty} f(x) = l$ $\blacksquare$

<u>**Exemple :**</u>
$$\underline{f(x) = \frac{x}{E^2(\sqrt{x})} = \frac{x}{\lfloor\sqrt{x}\rfloor^2}}$$

$$D_{déf}(f) = \mathbb{R}_+ \setminus [0, 1[ \ = [1, \infty[$$

$f$ d.v. $\infty$. (Raisonnablement $\displaystyle\lim_{x \to \infty} f(x) = 1$)

Remarquons que
$$
\begin{aligned}
\sqrt{x} - 1 \leq \lfloor\sqrt{x}\rfloor &\leq \sqrt{x} \qquad \text{pour } x > 1 \\
\text{Donc} \quad \frac{1}{\sqrt{x}} \leq \frac{1}{\lfloor\sqrt{x}\rfloor} &\leq \frac{1}{\sqrt{x} - 1} \\
\text{Donc} \quad \frac{1}{x} \leq \frac{1}{\lfloor\sqrt{x}\rfloor^2} &\leq \frac{1}{x - 2\sqrt{x} + 1} \\
\text{Donc} \quad 1 \leq \frac{x}{\lfloor\sqrt{x}\rfloor^2} &\leq \frac{1}{1 - \frac{2}{\sqrt{x}} + \frac{1}{x}}
\end{aligned}
$$

Par les gendarmes
$$\lim_{x \to \infty} f(x) = 1$$

> [!important] Corollaire
> Si $f(x)$ d.v. $\infty$ et $\displaystyle\lim_{x \to \infty} |f(x)| = 0$. Alors $\displaystyle\lim_{x \to \infty} f(x) = 0$

<u>Preuve :</u>
$$-|f(x)| \leq f(x) \leq |f(x)|$$
$$-0 \leq f(x) \leq 0 \quad \text{et on conclut par les gendarmes} \ \blacksquare$$

⚠️ Si $\displaystyle\lim_{x \to \infty} |f(x)| = l \in \mathbb{R}_+^*$
$$\not\Rightarrow \lim_{x \to \infty} f(x) = l, -l$$

> [!important] Théorème du gendarme
> Si $f, g : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$ et
> - $\displaystyle\lim_{x \to \infty} g(x) = \infty$
> - $g(x) \leq f(x)$ si $x \geq B$
>
> Alors $\displaystyle\lim_{x \to \infty} f(x) = \infty$

> [!important] Théorème (« $0 \times$ borné »)
> Soient $f, g : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$. Supposons
> - $\displaystyle\lim_{x \to \infty} f(x) = 0$
> - $|g(x)| \leq B, \quad \forall x \geq x_B$
>
> Alors $\displaystyle\lim_{x \to \infty} f(x) \cdot g(x) = 0$

<u>Preuve :</u> $\forall x \geq x_B$
$$0 \leq |f(x)\,g(x)| \leq f(x) \cdot B$$

Par les gendarmes $\displaystyle\lim_{x \to \infty} |f(x)\,g(x)| = 0$

Par le corollaire, $\displaystyle\lim_{x \to \infty} f(x)\,g(x) = 0$ $\blacksquare$

> [!important] Théorème (« $\infty \times$ loin de $0$ »)
> Soient $f, g : \mathbb{R} \to \mathbb{R}$ d.v. $\infty$. Supposons
> - $\displaystyle\lim_{x \to \infty} f(x) = \infty$
> - $g(x) \geq m > 0$ pour $x \geq x_m$, $\ m > 0$ <u>fixé</u>
>
> $$\lim_{x \to \infty} f(x)\,g(x) = \infty$$

<u>**Exemple**</u>
$$f(x) = x \qquad g(x) = \frac{1}{x}$$
$$\lim_{x \to \infty} f(x) = \infty, \quad \lim_{x \to \infty} f(x) \cdot g(x) = 1 \neq \infty$$

$g(x) > 0$ $\forall x \in D_{déf}(g)$, mais $g(x)$ n'est pas « loin de $0$ »

Si par contre, $g(x) = \dfrac{1}{x} + \dfrac{1}{10^{100}}$, alors $g(x) \geq \dfrac{1}{10^{100}} > 0$

Donc $\displaystyle\lim_{x \to \infty} x\left(\frac{1}{x} + \frac{1}{10^{100}}\right) = \infty$

---

### 3.3 Limite de fonction pour $x \to x_0 \in \mathbb{R}$

<u>**Exemples**</u>

**1)** $g(x) = \dfrac{x^3 - 2x^2}{x - 2}, \qquad x_0 = 2$

A priori, $D_{déf}(g) = \mathbb{R} \setminus \{2\}$

Question : est-ce que $g(x)$ tend vers une valeur $x$ proche de $2$

On remarque : $g(x) = \dfrac{x^2(x - 2)}{x - 2} = x^2 \quad$ si $x \neq 2$

Sur $D_{déf}(g)$ : $g(x) = x^2$

On conclut que $g(x)$ s'approche de $4$ si $x$ s'approche de $2$.

**2)** $h(x) = \dfrac{\sin x}{x}, \qquad x_0 = 0$

$D_{déf}(h) = \mathbb{R}^*$ mais
$$
\begin{aligned}
\sin(1) &\cong 0.84 \\
\frac{\sin(1/2)}{1/2} &\cong 0.96 \\
\frac{\sin(1/3)}{1/3} &\cong 0.98 \\
\frac{\sin(1/4)}{1/4} &\cong 0.99
\end{aligned}
$$

On devine que si $x$ s'approche de $0$, $\dfrac{\sin x}{x}$ s'approche de $1$

> [!definition] Déf
> Une fonction est <u>définie sur voisinage épointé</u> de $x_0$, si et seulement si :
> $$]x_0 - \delta, x_0[ \ \cup \ ]x_0, x_0 + \delta[ \ \subset D_{déf}(f) \text{ de } \delta > 0.$$
> On note $f$ d.v̇. $x_0$

<u>**Exemples :**</u>

**1)** $\dfrac{\sin x}{x}, \quad D_{déf}\left(\dfrac{\sin x}{x}\right) = \mathbb{R}^*$

on a que $\underbrace{]-1, 0[ \ \cup \ ]0, 1[}_{\substack{\text{voisinage épointé de } 0 \\ (\delta = 1)}} \subset D_{déf}$

Donc $\dfrac{\sin x}{x}$ est d.v̇. $0$.

**2)** $\dfrac{\cos x}{x}, \ \dfrac{\tan x}{x}$ sont d.v̇. $0$.

> [!definition] Déf
> On dit que la limite d'une fonction $f$ d.v̇. $x_0$ est égale à $l$ si $x$ tend vers $x_0$ si et seulement si :
> $$\forall \varepsilon > 0, \ \exists\, \delta > 0, \ 0 < |x - x_0| < \delta \implies |f(x) - l| < \varepsilon$$
> On note $\displaystyle\lim_{x \to x_0} f(x) = l$ (notation)

« Décomposition linguistique »

$$\color{lime}{\underline{\forall \varepsilon > 0}}, \ \color{red}{\underline{\exists\, \delta > 0}} \text{ tel que } \color{orange}{\underline{0 < |x - x_0| < \delta}} \implies \color{lime}{\underline{|f(x) - l| < \varepsilon}}$$

<span style="color:lime">les valeurs de $f(x)$ sont aussi proche de $l$ que voulu</span> <span style="color:orange">pour autant que $x$ et $x_0$ soient proches, i.e.</span> <span style="color:magenta">plus petit qu'une distance $\delta$</span>

« graphiquement »

![[ch3-limite-graphique.svg]]

<u>**Exemples :**</u>

**1)** $g(x) = \dfrac{x^3 - 2x^2}{x - 2} = x^2 \quad$ si $x \neq 2$

On veut montrer que $\displaystyle\lim_{x \to 2} g(x) = 4$

![[ch3-limite-exemple.svg]]

Il faut résoudre
$$
\begin{aligned}
&|4 - g(x)| < \varepsilon \\
\underset{x \neq 2}{\iff} \ &|x^2 - 4| < \varepsilon \\
\iff \ &-\varepsilon < x^2 - 4 < \varepsilon \\
\iff \ &4 - \varepsilon < x^2 < \varepsilon + 4 \\
\iff \ &-\varepsilon < (x - 2)(x + 2) < \varepsilon \\
\underset{x > -2}{\iff} \ &\frac{-\varepsilon}{(x + 2)} < x - 2 < \frac{\varepsilon}{(x + 2)} \\
\underset{0 < x < 4}{\Longleftarrow} \ &-\frac{\varepsilon}{6} < x - 2 < \frac{\varepsilon}{6} \\
\iff \ &|x - 2| < \frac{\varepsilon}{6} \ \text{ et } \ 0 < x < 4
\end{aligned}
$$

On peut choisir $\delta = \min\left\{\dfrac{\varepsilon}{6}, 2\right\}$

On a $0 < |x - 2| < \delta \implies |g(x) - 4| < \varepsilon$

<u>alternative</u>
$$
\begin{aligned}
\underset{1 < x < 3}{\Longleftarrow} \ &-\frac{\varepsilon}{5} < x - 2 < \frac{\varepsilon}{5} \\
\iff \ &|x - 2| < \frac{\varepsilon}{5} \ \text{ et } \ 1 < x < 3 \\
&\delta = \min\left\{\frac{\varepsilon}{5}, 1\right\}
\end{aligned}
$$

**2)** $\dfrac{\sin x}{x}, \quad x_0 = 0, \quad l = 1$

Soit $\varepsilon > 0$ il faut satisfaire
$$\left|\frac{\sin x}{x} - 1\right| < \varepsilon$$

Faisons un peu de trigo :

![[ch3-trigo-aires.svg]]

$$\frac{\sin x}{2} < \frac{x}{2} < \frac{\tan x}{2}$$

$$
\begin{aligned}
\text{Donc} \quad & 1 < \frac{x}{\sin x} < \frac{\tan x}{\sin x} = \frac{1}{\cos x} \\
\text{Donc} \quad & \cos x < \frac{\sin x}{x} < 1 \\
\text{Donc} \quad & \cos x - 1 < \frac{\sin x}{x} - 1 < 0 \\
\iff \quad & 1 - \cos x > 1 - \frac{\sin x}{x} > 0
\end{aligned}
$$

Si $1 - \cos x < \varepsilon$ alors $1 - \dfrac{\sin x}{x} < \varepsilon$

Donc si $1 - \varepsilon < \cos x$, $\ \left|\dfrac{\sin x}{x} - 1\right| < \varepsilon$

Donc si $-\arccos(1 - \varepsilon) < x < \arccos(1 - \varepsilon)$ alors $\left|1 - \dfrac{\sin x}{x}\right| < \varepsilon$

On a alors $\delta = \arccos(1 - \varepsilon)$

---

$$\lim_{x \to x_0} f(x) = l, \ f \text{ d.v̇. } x_0 \iff \forall \varepsilon > 0, \ \exists\, \delta > 0, \ 0 < |x - x_0| < \delta \implies |f(x) - l| < \varepsilon$$

**b)** $\displaystyle\lim_{x \to 0} \sin(x) = 0 \qquad \sin$ d.v. $0$, $\ l = 0$, $\ x_0 = 0$

Soit $\varepsilon > 0$. À résoudre

![[ch3-cercle-sinus.svg]]

$$
\begin{aligned}
&|\sin(x) - 0| < \varepsilon \\
\iff \ &|\sin(x)| < \varepsilon \\
\Longleftarrow \ &|\sin(x)| < |x| < \varepsilon
\end{aligned}
$$

On peut prendre $\delta = \varepsilon$ et on a $0 < |x| < \delta \implies |\sin(x)| < \varepsilon$

**c)** $\displaystyle\lim_{x \to 0} \cos(x) = 1 \qquad \cos$ d.v. $0$, $\ l = 1$, $\ x_0 = 0$

Soit $\varepsilon > 0$
$$
\begin{aligned}
&|\cos(x) - 1| < \varepsilon \iff \left|\cos\left(2 \cdot \frac{x}{2}\right) - 1\right| < \varepsilon \\
\iff \ &\left|\cos^2\left(\frac{x}{2}\right) - \sin^2\left(\frac{x}{2}\right) - 1\right| < \varepsilon \\
\iff \ &\left|-2\sin^2\left(\frac{x}{2}\right)\right| < \varepsilon \\
\iff \ &\left|2\sin^2\left(\frac{x}{2}\right)\right| < \varepsilon \ \underset{\substack{\text{condition} \\ \text{plus forte}}}{\Longleftarrow} \ \left|\frac{x}{2}\right|^2 < \frac{\varepsilon}{2} \\
\implies \ &\left|\frac{x}{2}\right| < \sqrt{\frac{\varepsilon}{2}} \iff |x| < 2\sqrt{\frac{\varepsilon}{2}} = \sqrt{2\varepsilon}
\end{aligned}
$$

On pose $\delta = \sqrt{2\varepsilon}$ et $0 < |x| < \delta \implies |\cos(x) - 1| < \varepsilon$

**d)** $\displaystyle\lim_{x \to 0} \frac{\sin x}{x} = 1 \qquad$ d.v̇. $0$, $\ x_0 = 0$, $\ l = 1$

Soit $\varepsilon > 0 \qquad \left|\dfrac{\sin(x)}{x} - 1\right| < \varepsilon$

![[ch3-cercle-tangente.svg]]

$$
\frac{\sin(x)}{2} < \frac{x}{2} < \frac{\tan(x)}{2} \implies 1 < \frac{x}{\sin x} < \frac{1}{\cos x} \qquad 1 > \frac{\sin x}{x} > \cos x
$$

$$
\begin{aligned}
\iff \ &1 - \frac{\sin(x)}{x} < \varepsilon \iff 1 - \varepsilon < \frac{\sin(x)}{x} \\
\Longleftarrow \ &1 - \varepsilon < \cos(x) \quad \text{(condition plus forte)} \\
\underset{\varepsilon \leq 2}{\iff} \ &|x| < \cos^{-1}(1 - \varepsilon)
\end{aligned}
$$

$$\text{Donc} \quad \delta = \begin{cases} \cos^{-1}(1 - \varepsilon) & \text{si } \varepsilon \leq 2 \\ \mathbb{R}_+^* & \varepsilon > 2 \end{cases}$$

> [!important] Théorème
> Si $f$ d.v̇. $x_0$ on a équivalence des deux affirmations suivantes
> 1) $\displaystyle\lim_{x \to x_0} f(x) = l$
> 2) $\displaystyle\lim_{n \to \infty} f(a_n) = l\ $ si $\ \displaystyle\lim_{n \to \infty} a_n = x_0$ et $\{a_n\}_{n \in \mathbb{N}} \subset D_{déf}(f)$

<u>**Ex**</u> $\quad f(x) = E\big(x(2 - x)\big), \qquad x_0 = 1$

prenons $a_n = 1 + \dfrac{1}{n} \qquad \displaystyle\lim_{n \to \infty} a_n = 1^{\oplus}$ ← toujours un peu plus grand que $1$

$$
\begin{aligned}
\text{Donc} \quad \lim_{x \to 1^+} f(x) &= \lim_{n \to \infty} f(a_n) = \lim_{n \to \infty} E\left(\left(1 + \frac{1}{n}\right)\left(2 - \left(1 + \frac{1}{n}\right)\right)\right) \\
&= \lim_{n \to \infty} E\left(1 - \frac{1}{n^2}\right) = 0
\end{aligned}
$$

$b_n = 1 - \dfrac{1}{n}, \quad \displaystyle\lim_{n \to \infty} b_n = 1^-$

$$\lim_{x \to 1^-} f(x) = \lim_{n \to \infty} f(b_n) = \lim_{n \to \infty} E\left(\left(1 - \frac{1}{n}\right)\left(2 - 1 + \frac{1}{n}\right)\right) = \lim E\left(1 - \frac{1}{n^2}\right) = 0$$

$$\implies \lim_{x \to 1^+} f(x) = 0 = \lim_{x \to 1^-} f(x)$$

Donc la $\displaystyle\lim_{x \to 1} f(x) = 0 \quad$ mais $f(1) = E\big(1(2 - 1)\big) = E(1) = 1$

On dit que la fonction $f(x)$ est discontinue en $x_0 = 1$
$$f(1) = f\left(\lim_{x \to 1} x\right) \neq \lim_{x \to 1} f(x)$$

---

### 3.4 Infiniment petit équivalent (IPE)

> [!definition] Déf
> Soient $f, g : \mathbb{R} \to \mathbb{R}$ d.v. $x_0$. On dit que $f$ et $g$ sont IPE autour de $x_0$ si et seulement si
> $$\lim_{x \to x_0} f(x) = \lim_{x \to x_0} g(x) = \textcircled{0} \ \text{ ou autre valeur}$$
> $$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 1 \qquad \text{On note } f \sim_0 g$$

<u>**Exemple**</u> $\sin x \sim_0 x$ en effet $\sin x$, $x$ d.v̇.,
$$\lim_{x \to 0} \sin(x) = 0 = \lim_{x \to 0} x \quad \text{et} \quad \lim_{x \to 0} \frac{\sin(x)}{x} = 1$$

**b)** $\cos(x) - 1 \sim_0 -\dfrac{x^2}{2}\ $ en effet, $\displaystyle\lim_{x \to 0} (\cos(x) - 1) = 0 = \lim_{x \to 0} -\frac{x^2}{2}$

et $\cos(x) - 1$, $-\dfrac{x^2}{2}$ d.v. $0$ et
$$
\begin{aligned}
\lim_{x \to 0} \frac{\cos(x) - 1}{-\frac{x^2}{2}} &= \lim_{x \to 0} \frac{1 - \cos\left(2\frac{x}{2}\right)}{\frac{x^2}{2}} = \lim_{x \to 0} \frac{1 - \cos^2\left(\frac{x}{2}\right) + \sin^2\left(\frac{x}{2}\right)}{\frac{x^2}{2}} \\
&= \lim_{x \to 0} \frac{2\sin^2\left(\frac{x}{2}\right)}{\frac{x^2}{2}} = \lim_{x \to 0} \frac{\sin^2\left(\frac{x}{2}\right)}{\left(\frac{x}{2}\right)^2} = \lim_{x \to 0} \left(\frac{\sin\left(\frac{x}{2}\right)}{\frac{x}{2}}\right)^2 = 1
\end{aligned}
$$

<u>**Exemples :**</u> calculer $\displaystyle\lim_{x \to 0} \frac{\sin(2x) - 2\sin(x)}{x^3}$

$$
\begin{aligned}
\lim_{x \to 0} \frac{2\sin x\cos x - 2\sin x}{x^3} &= \lim_{x \to 0} \frac{\sin(x)(\cos x - 1)}{x \cdot x^2 \cdot \frac{1}{2}} \\
&\underset{\text{IPE}}{=} \underbrace{\lim_{x \to 0} \frac{\sin x}{x}}_{1} \cdot \underbrace{\lim_{x \to 0} \frac{\cos x - 1}{\frac{x^2}{2}}}_{-1} = -1
\end{aligned}
$$

<u>Remarque :</u> $\tan x \sim_0 x$ et $\sin(x) \sim_0 x$

> <span style="color:red">⚠️ Utiliser les IPE dans des factorisations seulement (pas des sommes)</span>

---

### 3.5 Fonctions continues

> [!definition] Déf
> Soit $f : \mathbb{R} \to \mathbb{R}$ d.v. $x_0$. On dit que $f$ est <u>continue en $x_0$</u> si et seulement si
> $$\lim_{x \to x_0} f(x) = f(x_0)$$

#### (Contre-)exemples

**①** $f(x) = \sin x$

On sait que $\displaystyle\lim_{x \to 0} \sin(x) = 0 = \sin(0)$. Donc, $\sin x$ est continue en $x_0 = 0$.

Soit $x_0 \neq 0$ et montrons que
$$\lim_{x \to x_0} \sin x = \sin x_0$$

Soit $\varepsilon > 0$.
$$
\begin{aligned}
|\sin x - \sin x_0| < \varepsilon \iff{}& \left|2\sin\left(\frac{x - x_0}{2}\right)\cos\left(\frac{x + x_0}{2}\right)\right| < \varepsilon \\
\Longleftarrow{}& \left|\sin\left(\frac{x - x_0}{2}\right)\right| < \frac{\varepsilon}{2} && \text{(condition plus forte)} \\
\Longleftarrow{}& \left|\frac{x - x_0}{2}\right| < \frac{\varepsilon}{2} && \text{(condition plus forte)}
\end{aligned}
$$

On prend alors $\delta = \varepsilon$ et
$$|x - x_0| < \delta \implies |\sin x - \sin x_0| < \varepsilon$$

![[ch3-continuite-sin.svg]]

Si $\left|x - \dfrac{7\pi}{15}\right| < \dfrac{1}{10} \implies \left|\sin x - \sin\dfrac{7\pi}{15}\right| < \dfrac{1}{10}$

Donc, $\sin x$ est continue en tout $x \in \mathbb{R}$.

**②** $f(x) = \begin{cases} \operatorname{sgn}(x) & \text{si } x \neq 0 \\ 0 & \text{si } x = 0 \end{cases}$

![[ch3-sgn.svg]]

$$\lim_{x \to 0^+} f(x) = \lim_{x \to 0^+} 1 = 1$$
$$\lim_{x \to 0^-} f(x) = \lim_{x \to 0^-} (-1) = -1$$

Donc $\displaystyle\lim_{x \to 0} f(x)$ n'existe pas.

<u>Manière alternative</u>

$$|f(0) - f(x)| < \frac{1}{2} \qquad \left(\varepsilon = \frac{1}{2}\right)$$
$$\iff x = 0 \qquad \underline{\text{pas un voisinage épointé de } 0}$$
$$\implies \nexists\, \delta > 0 \text{ tel que } 0 < |x - 0| < \delta \implies |f(x) - f(0)| < \frac{1}{2}$$

Donc, $\displaystyle\lim_{x \to 0} f(x) \neq 0$

Donc $\displaystyle\lim_{x \to 0} f(x) \neq f(0)$

Ainsi, $f(x)$ est discontinue en $x_0 = 0$.

**③** $f(x) = \sqrt{x}$, $x \geq 0$, $x_0 > 0$

![[ch3-racine-continuite.svg]]

<u>Soit $\varepsilon > 0$</u>
$$
\begin{aligned}
&|\sqrt{x} - \sqrt{x_0}| < \varepsilon \\
\iff{}& \frac{|x - x_0|}{|\sqrt{x} + \sqrt{x_0}|} < \varepsilon \\
\Longleftarrow{}& \frac{|x - x_0|}{\sqrt{x_0}} < \varepsilon \\
\iff{}& |x - x_0| < \varepsilon\sqrt{x_0}
\end{aligned}
$$

On pose $\delta = \varepsilon\sqrt{x_0}$ : si $|x - x_0| < \delta \implies |\sqrt{x} - \sqrt{x_0}| < \varepsilon$

Donc, $\displaystyle\lim_{x \to x_0} \sqrt{x} = \sqrt{x_0}$, et $\sqrt{x}$ est continue pour $x_0 \neq 0$.

**③b** $\displaystyle\lim_{x \to 0^+} \sqrt{x} = 0$

Pour $\varepsilon > 0$ donné, trouver un $\delta > 0$ tel que
$$0 < x - x_0 < \delta \implies |\sqrt{x} - \sqrt{0}| < \varepsilon$$

Soit $\varepsilon > 0$, $|\sqrt{x} - \sqrt{0}| < \varepsilon$
$$\iff \sqrt{x} < \varepsilon \iff x < \varepsilon^2$$

En posant $\delta = \varepsilon^2$ on a
$$0 < x < \delta \implies |\sqrt{x} - \sqrt{0}| < \varepsilon$$

Donc $\sqrt{x}$ est <u>continue</u> sur $\mathbb{R}_+$.

On dénote par $C(I)$ la collection des fonctions continues sur l'intervalle $I$.
$$C(I) = \left\{ f : \mathbb{R} \to \mathbb{R} \;\middle|\; \forall x_0 \in I,\ \lim_{x \to x_0} f(x) = f(x_0) \right\}$$

> - <span style="color:#e040c0">$(x \to x_0^+)$ si $I = [x_0, \dots[$</span>
> - <span style="color:#22b5c9">$(x \to x_0^-)$ si $I = ]\dots, x_0]$</span>

$\operatorname{sgn}(x) \in C(\mathbb{R}^*)$

> [!important] Théorème
> Soient $f, g : \mathbb{R} \to \mathbb{R}$ continues en $x_0$.
> Alors $f + g$, $f \cdot g$, $\dfrac{f}{g}$ (si $g \neq 0$) sont continues en $x_0$.

<u>Preuve :</u> toutes ces propriétés pour les fonctions sont des héritages de la caractérisation par les suites. $\blacksquare$

<u>**Conséquences**</u> $x$ est continue. Donc $x^2, x^3, x^4, \dots$,
$$p(x) = a_n x^n + a_{n-1}x^{n-1} + \dots + a_1 x + a_0,$$
$$\frac{p(x)}{q(x)},\ \sin x,\ \cos x,\ \tan x,\ \cot x,$$
sont toutes continues.

<u>**Contre-exemple**</u>

**④** $f(x) = \sin\left(\dfrac{1}{x}\right)$

![[ch3-sin-inverse.svg]]

Posons les suites
$$a_n = \frac{1}{n\pi} \qquad b_n = \frac{1}{\frac{\pi}{2} + 2n\pi}$$

On a $\displaystyle\lim_{n \to \infty} a_n = 0 = \lim_{n \to \infty} b_n$

mais
$$\lim_{n \to \infty} f(a_n) = \lim_{n \to \infty} (0) = 0$$
$$\lim_{n \to \infty} f(b_n) = \lim_{n \to \infty} (1) = 1$$

Donc, $\displaystyle\lim_{x \to 0} f(x)$ n'existe pas.

> [!important] Théorème
> Soit $f : \mathbb{R} \to \mathbb{R}$ d.v. $x_0$ tel que
> $$\lim_{x \to x_0} f(x) = \ell$$
> Soit $g : \mathbb{R} \to \mathbb{R}$, $g$ d.v. $\ell$, <u>continue en $\ell$</u>, tel que $\displaystyle\lim_{x \to \ell} g(x) = K$ $\big(= g(\ell)\big)$
>
> Alors $\displaystyle\lim_{x \to x_0} g(f(x)) = K$

<u>Preuve :</u> Soit $\varepsilon > 0$, puisque $g$ est continue en $\ell$, $\exists\, \delta_1 > 0$ tel que
$$|y - \ell| < \delta_1 \implies |g(y) - K| < \varepsilon$$

Puisque $f$ continue en $x_0$, $\exists\, \delta_2$ tel que
$$|x - x_0| < \delta_2 \implies |f(x) - \ell| < \delta_1$$

Donc si
$$|x - x_0| < \delta_2 \implies |f(x) - \ell| < \delta_1 \implies |g(f(x)) - K| < \varepsilon \qquad \blacksquare$$

<u>**Exemples**</u> $\sqrt{x^2 + 1}$, $\sin(\cos(x))$, $\sqrt{\sin^2(x)} = |\sin(x)|$ sont continues.
