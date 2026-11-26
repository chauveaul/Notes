---
cours: Analyse I
chapitre: 1
source: "Chapitre 1 - Analyse I.pdf"
tags: [analyse-I, chapitre-1]
---

# Chapitre 1 — Analyse I

L'analyse est l'étude de grandeurs numériques et de leurs variations en relation avec d'autres valeurs numériques.

Pour ce faire, on introduit des fonctions, des suites et séries, des dérivées, des intégrales, etc.

L'analyse est utilisée maintenant en mathématiques, en physique, en ingénierie, en informatique, en économie, sociologie, médecine, etc.

---

## 1. Algèbre élémentaire

### 1.1 Ensembles numériques

On accepte l'existence de

- $\mathbb{N} = \{0, 1, 2, 3, 4, \dots\}$ — <u>l'ensemble des nombres naturels</u>
  - $\mathbb{N}^* = \{1, 2, 3, 4, \dots\} = \mathbb{N} \setminus \{0\}$ — « $\mathbb{N}$ privé de $0$ »
- $\mathbb{Z} = \{\dots, -3, -2, -1, 0, 1, 2, \dots\}$ est la collection de tous les nombres entiers.

  $\mathbb{N} \subset \mathbb{Z}$ — « $\mathbb{N}$ est inclus dans $\mathbb{Z}$ »

- $\mathbb{Q} = \left\{ \left[\dfrac{p}{q}\right] \;\middle|\; \text{où } p \in \mathbb{Z},\ q \in \mathbb{Z} \setminus \{0\} \right\}$ est l'ensemble des nombres rationnels, i.e. des rapports représentés par une fraction de nombres entiers.

- $\sqrt{2}, \sqrt{3}, \sqrt{5}, \pi, e \notin \mathbb{Q}$ — « ne sont pas éléments de $\mathbb{Q}$ »

La collection de tous ces nombres rationnels et irrationnels est dénotée par $\mathbb{R}$, l'ensemble des nombres réels, avec les propriétés suivantes :

1. $\mathbb{Q} \subset \mathbb{R}$
2. Il existe une addition $+$ et un produit $\cdot$ sur $\mathbb{R}$ et <u>une relation d'ordre totale</u>
   - 2.a) $\forall x, y \in \mathbb{R}$, soit $x = y$, $x < y$, $x > y$
   - 2.b) $\forall x, y \in \mathbb{R}$, si $x \leq y$ et $y \leq x \implies x = y$
   - 2.c) $\forall x, y, z \in \mathbb{R}$, si $x \leq y$ et $y \leq z$, alors $x \leq z$
   - 2.d) $\forall x \in \mathbb{R}$, $x \geq x$
   - 2.e) $\forall x, y, z \in \mathbb{R}$, $x \leq y \iff x + z \leq y + z$
   - 2.f) $\forall x, y, z \in \mathbb{R}$, $x \geq y \implies x \cdot z \geq y \cdot z$ si $z \geq 0$

   > **Note :** on peut aussi écrire en miroir $0 \in \mathbb{R}$ ou $\mathbb{R} \ni 0$
3. Tout sous-ensemble $E \subset \mathbb{R}$, $E \neq \emptyset$ et si $E$ est borné, alors le supremum de $E$ est dans $\mathbb{R}$ (plus petit élément de $\mathbb{R}$ qui est plus grand que le plus grand élément de $E$).

De manière pragmatique on peut toujours écrire un nombre $x \in \mathbb{R}$, $x \geq 0$, comme une suite décimale.

- Si $x = 4.12525 25\dots$, $x = 4.1\overline{25}$, alors $x \in \mathbb{Q}$.
- $1 = 0.\overline{9}$ car $3 \cdot \frac{1}{3} = 1$ mais $\frac{1}{3} = 0.\overline{3}$
- Si $x = 0.\overline{9}$ : $\quad 10x = 9.\overline{9}$
  $$10x - x = 9 \implies 9x = 9 \implies x = 1$$
- Ainsi : $0.5 = 0.4\overline{9}$

**Conséquences des propriétés 1) à 2)**

1. $\forall x, y, a, b \in \mathbb{R}$, $x \leq y$ et $a \leq b$, alors $x + a \leq y + b$
2. $\forall x, y, a \in \mathbb{R}$, si $x \leq y$ et $a \leq 0$, alors $ax \geq ay$

#### Exemples

**1) Résoudre** $x^2 \geq x + 2$

$$
\begin{aligned}
(1) &\overset{(2e)}{\iff} x^2 - x - 2 \geq 0 \\
&\iff (x-2)(x+1) \geq 0 \\
&\iff \begin{cases} x - 2 \geq 0 \text{ et } x + 1 \geq 0 \\ \text{ou} \\ x - 2 \leq 0 \text{ et } x + 1 \leq 0 \end{cases}
\end{aligned}
$$

| $x$       | $-\infty$ |     | $-1$ |     | $2$ |     | $+\infty$ |
| :-------- | :-------: | :-: | :--: | :-: | :-: | :-: | :-------: |
| $x-2$     |           | $-$ |      | $-$ | $0$ | $+$ |           |
| $x+1$     |           | $-$ | $0$  | $+$ |     | $+$ |           |
| $x^2-x-2$ |           | $+$ | $0$  | $-$ | $0$ | $+$ |           |

$$\iff \underline{x \in \,]-\infty, -1] \cup [2, \infty[}$$

**2)**
$$x \in [3, 5] \iff 3 \leq x \leq 5$$
$$y \in [2, 4] \iff 2 \leq y \leq 4$$
$$\text{alors } x + y \in [\underset{(3+2)}{5}, \underset{(5+4)}{9}]$$

~~$x - y \in [1, 1] = \{1\}$~~ ❌

$\hookrightarrow$ $y \in [2, 4]$ alors $-y \in [-4, -2]$
$$\implies x + (-y) \in [-1, 3]$$

**3) Résoudre** $x(x-1) \geq (x-1)$
$$
\begin{aligned}
&\iff x(x-1) - (x-1) \geq 0 \\
&\iff (x-1)(x-1) \geq 0 \\
&\iff (x-1)^2 \geq 0 \iff x \in \mathbb{R}
\end{aligned}
$$

**4) Résoudre** $\dfrac{x+2}{x+1} \leq \dfrac{x-2}{x-1}$

> Domaine : $D_{\text{def}} \subset \mathbb{R} \setminus \{\pm 1\} \;\hookrightarrow\; x \neq -1, 1$

$$
\begin{aligned}
&\iff \frac{x+2}{x+1} - \frac{x-2}{x-1} \leq 0 \\
&\iff \frac{(x+2)(x-1) - (x-2)(x+1)}{(x+1)(x-1)} \leq 0 \\
&\iff \frac{x^2 + x - 2 - (x^2 - x - 2)}{(x+1)(x-1)} \leq 0 \\
&\iff \frac{2x}{(x+1)(x-1)} \leq 0
\end{aligned}
$$

| $x$      | $-\infty$ |     |           $-1$            |     | $0$ |     |            $1$            |     | $+\infty$ |
| :------- | :-------: | :-: | :-----------------------: | :-: | :-: | :-: | :-----------------------: | :-: | :-------: |
| $2x$     |           | $-$ |          $\Vert$          | $-$ | $0$ | $+$ |          $\Vert$          | $+$ |           |
| $x+1$    |           | $-$ |            $0$            | $+$ |     | $+$ |          $\Vert$          | $+$ |           |
| $x-1$    |           | $-$ |          $\Vert$          | $-$ |     | $-$ |            $0$            | $+$ |           |
| quotient |           | $-$ |          $\Vert$          | $+$ | $0$ | $-$ |          $\Vert$          | $+$ |           |
|          |           |     | $\uparrow D_{\text{def}}$ |     |     |     | $\uparrow D_{\text{def}}$ |     |           |

$$\iff x \in \,]-\infty, -1[ \,\cup\, [0, 1[$$

> [!tip] Marche à suivre
> 1. $D_{\text{def}}$
> 2. Comparer à $0$
> 3. Factoriser
> 4. Tableau des signes

---

### 1.2 Identités remarquables

Pour $a, b \in \mathbb{R}$ :

- $(a+b)^2 = a^2 + 2ab + b^2$
- $(a-b)^2 = a^2 - 2ab + b^2$
- $(a+b)(a-b) = a^2 - b^2$
- $(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$
- $(a-b)^3 = a^3 - 3a^2b + 3ab^2 - b^3$
- $a^3 + b^3 = (a+b)(a^2 - ab + b^2)$
- $a^3 - b^3 = (a-b)(a^2 + ab + b^2)$

#### Exemples

**1)**
$$\frac{2}{3+\sqrt{2}} \cdot \frac{3-\sqrt{2}}{3-\sqrt{2}} = \frac{6 - 2\sqrt{2}}{9 - 2} = \frac{6 - 2\sqrt{2}}{7}$$

**2)**
$$
\begin{aligned}
\frac{1}{\sqrt[3]{4} - \sqrt[3]{2}} - \frac{1}{\sqrt[3]{2}}
&= \frac{1}{\sqrt[3]{4} - \sqrt[3]{2}} - \frac{\sqrt[3]{4}}{2} \\
&= \frac{\sqrt[3]{16} + \sqrt[3]{8} + \cancel{\sqrt[3]{4}}}{4 - 2} - \frac{\cancel{\sqrt[3]{4}}}{2} \\
&= \frac{\sqrt[3]{16} + \sqrt[3]{8}}{2} \\
&= \frac{\sqrt[3]{8 \cdot 2} + \sqrt[3]{8}}{2} = \frac{2\sqrt[3]{2} + 2}{2} \\
&= \sqrt[3]{2} + 1
\end{aligned}
$$

> *Calcul à côté :* $\left(\dfrac{1}{\sqrt[3]{2}} \cdot \dfrac{\sqrt[3]{2^2}}{\sqrt[3]{2^2}}\right) \hookrightarrow \dfrac{\sqrt[3]{4}}{\sqrt[3]{2^3}} = \dfrac{\sqrt[3]{4}}{2}$

---

### 1.3 Inégalités avec des paramètres

**Exemple d'introduction.**

On aimerait partir à Malaga en vacances. On dispose d'un budget $M$. Celui-ci suffira pour combien de jours $x$ ?

- On a le billet d'avion ($2 \cdot 150$ CHF)
- On a les nuitées à l'hôtel ($100$ CHF/nuitée)
- Dépenses de $50$ CHF/jour

$$M \geq 300 + 50x + 100(x-1)$$
$$M \geq 150x + 200$$
$$x \leq \frac{M - 200}{150} \implies S = \left[0, \frac{M-200}{150}\right] \cap \underset{\substack{\uparrow \\ \text{jour est} \\ \text{un int}}}{\mathbb{N}} \cup \{0\}$$

**Exemple :** résoudre $\underline{mx - 2 = 0}$

$$mx = 2 \qquad x = \frac{2}{m}$$

- Cas $m \neq 0$ : $S = \left\{\dfrac{2}{m}\right\}$
- Cas $m = 0$ : $S = \emptyset$

**2)** $mx \leq 3$

- Cas $\underline{m < 0}$ : $x \geq \dfrac{3}{m}$, $\quad \underline{S = \left[\dfrac{3}{m}, +\infty\right[}$
- Cas $\underline{m > 0}$ : $x \leq \dfrac{3}{m}$, $\quad \underline{S = \left]-\infty, \dfrac{3}{m}\right]}$
- Cas $\underline{m = 0}$ : $mx \leq 3 \implies 0 \cdot x \leq 3 \implies 0 \leq 3$

  $$\underline{S = \mathbb{R}}$$

Synthèse :
$$
S = \begin{cases}
\left]-\infty, \dfrac{3}{m}\right] & \text{si } m > 0 \\[2mm]
\mathbb{R} & \text{si } m = 0 \\[2mm]
\left[\dfrac{3}{m}, +\infty\right[ & \text{si } m < 0
\end{cases}
$$

**3) Résoudre** $\dfrac{x}{x+m} \leq \dfrac{m}{x+m}$

$D_{\text{def}} \in \mathbb{R} \setminus \{-m\}$

$$\frac{x}{x+m} - \frac{m}{x+m} \leq 0 \implies \frac{x-m}{x+m} \leq 0$$

**Cas $m > 0$ :**

| $x$   | $-\infty$ |     |  $-m$   |     | $+m$ |     | $+\infty$ |
| :---- | :-------: | :-: | :-----: | :-: | :--: | :-: | :-------: |
| $x-m$ |           | $-$ | $\Vert$ | $-$ | $0$  | $+$ |           |
| $x+m$ |           | $-$ |   $0$   | $+$ |      | $+$ |           |
| (3)   |           | $+$ | $\Vert$ | $-$ | $0$  | $+$ |           |

$m > 0 \qquad S = \,]-m, m]$

**Cas $m = 0$ :**

| $x$   | $-\infty$ |     |   $0$   |     | $+\infty$ |
| :---- | :-------: | :-: | :-----: | :-: | :-------: |
| $x-m$ |           | $-$ |   $0$   | $+$ |           |
| $x+m$ |           | $-$ |   $0$   | $+$ |           |
| (3)   |           | $+$ | $\Vert$ | $+$ |           |

$m = 0 \qquad S = \emptyset$

**Cas $m < 0$ :**

| $x$   | $-\infty$ |     | $m$ |     |  $-m$   |     | $+\infty$ |
| :---- | :-------: | :-: | :-: | :-: | :-----: | :-: | :-------: |
| $x-m$ |           | $-$ | $0$ | $+$ |         | $+$ |           |
| $x+m$ |           | $-$ |     | $-$ |   $0$   | $+$ |           |
| (3)   |           | $+$ | $0$ | $-$ | $\Vert$ | $+$ |           |

$m < 0 \qquad S = [m, -m[$

$$
S = \begin{cases}
]-m, m] & \text{si } m > 0 \\
\emptyset & \text{si } m = 0 \\
[m, -m[ & \text{si } m < 0
\end{cases}
$$

---

### 1.4 Valeurs absolues

> [!definition] Déf
> Pour $x \in \mathbb{R}$, la <span style="color:red">valeur absolue</span> de $x$ qui est notée <span style="color:red">$|x|$</span> est donnée par
> $$|x| \underset{\substack{\uparrow \\ \text{par définition}}}{:=} \begin{cases} x & \text{si } x \geq 0 \\ -x & \text{si } x < 0 \end{cases}$$

<u>Graphiquement :</u>

![[ch1-valeur-absolue.svg]]

$|x|$ est la distance du point situé en $(x, 0)$ à $(0, 0)$.

#### Exemples

- $|-5| = 5$
- $|\sqrt{3} - 2| = -\sqrt{3} + 2$
- $|x^2 + 1| = x^2 + 1 \quad \forall x \in \mathbb{R}$
- $|x^2 - 1| = \begin{cases} x^2 - 1 & \text{si } |x| \geq 1 \\ 1 - x^2 & \text{si } |x| < 1 \end{cases}$
- $\forall x \in \mathbb{R}$, $|x| = \sqrt{x^2}$

  Donc $|-2| = \sqrt{(-2)^2} = \sqrt{4} = \underline{2}$

En général, $|x| = a \iff \underset{D_{\text{pos}}}{\underbrace{a \geq 0}}$ et $x = \pm a$

> [!warning] ⚠️ Ne pas élever au carré.
> Élever au carré change l'égalité et ajoute des fausses solutions.
> $$\underset{\substack{\uparrow \\ 0 \text{ solutions}}}{|x| = -3} \qquad |x|^2 = (-3)^2, \qquad \underset{\substack{\uparrow \\ 2 \text{ solutions}}}{x^2 = 9}$$

> [!important] En général,
> $$|f(x)| = g(x) \iff \underset{D_{\text{pos}}}{g(x) \geq 0} \text{ et } f(x) = \pm g(x)$$

#### Exemples

**① Résoudre** $|x^2 + 2x - 5| = x + 1$

> $D_{\text{def}} \in \mathbb{R}$
> $D_{\text{pos}} = \{x \in \mathbb{R} \mid x + 1 \geq 0\} = [-1, +\infty[$

On cherche des solutions dans $D_{\text{def}} \cap D_{\text{pos}}$
$\implies S \subset [-1, \infty[$

On doit résoudre :
$$
\begin{cases}
x^2 + 2x - 5 = x + 1 & (1a) \\
\text{ou} \\
x^2 + 2x - 5 = -x - 1 & (1b)
\end{cases}
$$

$$
\iff \begin{cases}
x^2 + x - 6 = 0 & (1a) \\
\text{ou} \\
x^2 + 3x - 4 = 0 & (1b)
\end{cases}
\iff \begin{cases}
(x-2)(x+3) = 0 & (1a) \\
\text{ou} \\
(x-1)(x+4) = 0 & (1b)
\end{cases}
$$

$$\iff S_{\text{prov}} = \{\cancel{-4}, \cancel{-3}, 1, 2\} \cap D_{\text{def}} \cap D_{\text{pos}}$$

$$\underline{S = \{1, 2\}}$$

**② Résoudre** $|x - 3m + 4| = x + m$

> $D_{\text{def}} \in \mathbb{R}$
> $D_{\text{pos}} = \{x \in \mathbb{R} \mid x + m \geq 0\}$
> $\quad x \geq -m$
> $\quad = [-m, +\infty[$
>
> $S \subset D_{\text{pos}} \cap D_{\text{def}} = [-m, \infty[$

$$
\iff \begin{cases}
x - 3m + 4 = x + m & (2a) \\
\text{ou} \\
x - 3m + 4 = -x - m & (2b)
\end{cases}
\iff \begin{cases}
-4m + 4 = 0 & (2a) \\
\text{ou} \\
2x - 2m + 4 = 0 & (2b)
\end{cases}
$$

$$
\iff \begin{cases}
S_{2a} = \mathbb{R} \text{ si } m = 1,\ \emptyset \text{ si } m \neq 1 \\
\text{ou} \\
S_{2b} = \{m - 2\}
\end{cases}
$$

$$
S_{\text{prov}} = \begin{cases}
\mathbb{R} \text{ si } m = 1,\ \emptyset \text{ si } m \neq 1 \\
\{m - 2\}
\end{cases}
$$

$$S = S_{\text{prov}} \cap D_{\text{def}} \cap D_{\text{pos}}$$

$$
S = \begin{cases}
[-1, \infty[ \text{ si } m = 1,\ \emptyset \text{ si } m \neq 1 \\
\{m - 2\} \text{ si } m - 2 \geq -m \text{ et } m \neq 1
\end{cases}
$$

$$
S = \begin{cases}
[-1, \infty[ & \text{si } m = 1 \\
\{m - 2\} & \text{si } m > 1 \\
\emptyset & \text{si } m < 1
\end{cases}
$$

---

### 1.5 Inégalités avec valeur absolue

![[ch1-inegalite-valeur-absolue.svg]]

> [!important]
> $$|x| \leq a$$
> $$x \in [-a, a]$$

Plus besoin de $D_{\text{pos}}$ pour $\leq$.

**En général**

> [!important]
> $$|g(x)| \leq f(x) \iff g(x) \in [-f(x), f(x)]$$

#### Exemples

**③** $\left| x - \dfrac{1}{x-1} \right| \leq -\dfrac{1}{x-1} \qquad\qquad D_{\text{def}} = \mathbb{R} \setminus \{1\}$

- $\leq$ avec $|\ |$ $\implies$ ~~$D_{\text{pos}}$~~

$$
(3) \iff \begin{cases}
x - \dfrac{1}{x-1} \leq -\dfrac{1}{x-1} & (3a) \\
\underline{\text{et}} \\
x - \dfrac{1}{x-1} \geq \dfrac{1}{x-1} & (3b)
\end{cases}
\iff \begin{cases}
x \leq 0 & (3a) \\
\underline{\text{et}} \\
x - \dfrac{2}{x-1} \geq 0 & (3b)
\end{cases}
$$

$$
\iff \begin{cases}
x \leq 0 & (3a) \\
\underline{\text{et}} \\
\dfrac{x^2 - x - 2}{x - 1} \geq 0 & (3b)
\end{cases}
\iff \begin{cases}
x \leq 0 \\
\underline{\text{et}} \\
\dfrac{(x-2)(x+1)}{(x-1)} \geq 0
\end{cases}
$$

| $x$      | $-\infty$ |     | $-1$ |     |  $+1$   |     | $2$ |     | $+\infty$ |
| :------- | :-------: | :-: | :--: | :-: | :-----: | :-: | :-: | :-: | :-------: |
| $(x-2)$  |           | $-$ |      | $-$ | $\Vert$ | $-$ | $0$ | $+$ |           |
| $(x+1)$  |           | $-$ | $0$  | $+$ | $\Vert$ | $+$ |     | $+$ |           |
| $(x-1)$ |   | $-$ |      | $-$ |   $0$   | $+$ |     | $+$ |           |
| quotient |           | $-$ | $0$  | $+$ | $\Vert$ | $-$ | $0$ | $+$ |           |

$$S_{3a} = \,]-\infty, 0]$$
$$S_{3b} = [-1, 1[ \,\cup\, [2, +\infty[$$
$$S_{3a} \cap S_{3b} \cap D_{\text{def}} = [-1, 0] \cup \emptyset \setminus \{1\}$$
$$= \underline{[-1, 0]}$$

> [!important]
> $$|g(x)| > f(x) \iff \begin{cases} g(x) < -f(x) \\ \text{ou} \\ g(x) > f(x) \end{cases}$$
> Pas besoin de $D_{\text{pos}}$.

---

### 1.6 Fonction signe

> [!definition] Déf
> La <span style="color:red">fonction signe</span>, $\operatorname{sgn}(x)$, est définie par
> $$\operatorname{sgn}(x) = \begin{cases} 1 & \text{si } x > 0 \\ 0 \text{ ou } 1 \text{ (suivant les conventions)} & \text{si } x = 0 \\ -1 & \text{si } x < 0 \end{cases}$$

<u>Graphiquement</u>

![[ch1-sgn.svg]]

<u>Propriétés :</u>

$\forall x, y \in \mathbb{R}^*$

1. $x = |x| \cdot \operatorname{sgn}(x) \iff \operatorname{sgn}(x) = \dfrac{x}{|x|}$
2. $\operatorname{sgn}(x \cdot y) = \operatorname{sgn}(x) \cdot \operatorname{sgn}(y)$
3. $\operatorname{sgn}\left(\dfrac{x}{y}\right) = \dfrac{\operatorname{sgn}(x)}{\operatorname{sgn}(y)} = \operatorname{sgn}(x)\operatorname{sgn}(y)$

#### <u>Inégalité triangulaire</u>

$\forall x, y \in \mathbb{R}$
$$|x + y| \leq |x| + |y|$$

<u>Preuve :</u> Dire que $|x+y| \leq |x| + |y|$
$$\iff |x+y|^2 \leq (|x| + |y|)^2$$
car on compare des nombres positifs.

Mais $(x+y)^2 = |x+y|^2 = x^2 + 2xy + y^2$
et $(|x| + |y|)^2 = |x|^2 + 2|x||y| + |y|^2$
mais $2|x||y| \geq 2xy$.
D'où on conclut. $\blacksquare$

---

### 1.7 Trinômes

> [!definition] Déf
> Un trinôme est une expression du type
> $$p(x) = ax^2 + bx + c$$
> $a, b, c \in \mathbb{R}$ et $a \neq 0$

**<u>Exemple 1</u>** $\quad p(x) = x^2 - 4x + 5$

$a = 1 \quad b = -4 \quad c = 5$

Pour trouver des racines on écrit
$$p(x) = \underbrace{x^2 - 4x}_{} + 5 \;\to\; x^2 - 2 \cdot 2x + (2)^2 - (2)^2 + 5$$
$$p(x) = (x-2)^2 + 1 \geq 1$$
$$\underline{\text{pas de racines}}$$

**<u>En général</u>**

$$
\begin{aligned}
p(x) &= ax^2 + bx + c, \quad a \neq 0 \\
&= a\left(x^2 + \frac{b}{a}x + \frac{c}{a}\right) \\
&= a\left(x^2 + 2\frac{b}{2a}x + \frac{c}{a}\right) \\
&= a\left(\underbrace{x^2 + 2\frac{b}{2a}x + \left(\frac{b}{2a}\right)^2}_{} \underbrace{- \left(\frac{b}{2a}\right)^2 + \frac{c}{a}}_{}\right) \\
&= a\left(\left(x + \frac{b}{2a}\right)^2 + \frac{4ac - b^2}{4a^2}\right)
\end{aligned}
$$

> [!important]
> Si $p(x) = 0 \iff b^2 - 4ac \geq 0$
> $$x = \frac{-b + \sqrt{b^2 - 4ac}}{2a} \qquad x = \frac{-b - \sqrt{b^2 - 4ac}}{2a}$$

> [!definition] Déf
> $b^2 - 4ac$ est le <span style="color:red">discriminant</span> de $p(x) = ax^2 + bx + c$.
> On note $\Delta = b^2 - 4ac$.

Donc
$$p(x) = a\left(\left(x + \frac{b}{2a}\right)^2 - \frac{\Delta}{4a^2}\right)$$

La valeur minimale atteinte en $x = -\dfrac{b}{2a}$.

<u>Trois cas :</u> $\quad \Delta > 0 \;\big|\; \Delta = 0 \;\big|\; \Delta < 0$

![[ch1-discriminant-trois-cas.svg]]

- $\Delta > 0$ : $a > 0 \Rightarrow \min = -\dfrac{\Delta}{4a}$ ; $a < 0 \Rightarrow \max = -\dfrac{\Delta}{4a}$ ; deux racines $x_-, x_+$
- $\Delta = 0$ : $-b/2a = \max/\min$ qui dépend de $\operatorname{sgn}(a)$
- $\Delta < 0$ : pas de racines, sommet en $\left(-\dfrac{b}{2a}, -\dfrac{\Delta}{4a}\right)$

**<u>Exemple 1</u>** $\quad P(x) = x^2 - 2x - m^2 + 2m$

$$a = 1 \geq 0 \implies \cup$$

$$
\begin{aligned}
p(x) &= x^2 - 2x + m(2 - m) \\
&= (x - m)(x - 2 + m)
\end{aligned}
$$

Deux racines, $x = m \quad x = 2 - m$

Étudier quand $m \geq 2 - m$
$$2m - 2 \geq 0$$
$$2m \geq 2$$
$$\underline{m \geq 1} \qquad \overset{m > 2 - m}{[1, \infty]}$$

**Si $m \geq 1$**

![[ch1-trinome-m-sup-1.svg]]

- $P(x) < 0$ si $x \in \,]2-m, m[$
- $P(x) = 0$ si $x \in \{2-m, m\}$
- $P(x) > 0$ si $x \notin [2-m, m]$

**Si $m < 1$**

![[ch1-trinome-m-inf-1.svg]]

- $P(x) < 0$ si $x \in \,]m, 2-m[$
- $P(x) = 0$ si $x \in \{2-m, m\}$
- $P(x) > 0$ si $x \notin [m, 2-m]$

**<u>Exemple 2</u>** $\quad P(x) = (2m+1)x^2 + 2(m-1)x + m - 3$

Déterminer $m$ tel que $P(x) > 0 \quad \forall x \in \mathbb{R}$

$$a = 2m + 1 \qquad b = 2(m-1) \qquad c = m - 3$$

<u>Deux conditions :</u>
1. $a > 0 \to \cup$
2. $\Delta < 0$ (pas de racines)

$$
\begin{aligned}
&1)\ 2m + 1 > 0 \\
\text{et}\ &2)\ \Delta < 0 \implies \cancel{4}(m-1)^2 - \cancel{4}(2m+1)(m-3) < 0
\end{aligned}
$$

$$
\implies \begin{cases}
m > -\dfrac{1}{2} \\[2mm]
m^2 - 2m + 1 - (2m^2 - 6m + m - 3) < 0
\end{cases}
\implies \begin{cases}
m > -\dfrac{1}{2} \\[2mm]
-m^2 + 3m + 4 < 0
\end{cases}
$$

$$
\implies \begin{cases}
m > -\dfrac{1}{2} \\[2mm]
-(m+1)(m-4) < 0
\end{cases}
$$

$$\iff m > -\frac{1}{2} \text{ et } m \notin [-1, 4]$$

$$\underline{\implies m \in \,]4, \infty[}$$

**<u>Exemple ③</u>** $\quad p(x) = mx^2 - mx + m + 1$

Déterminer $m$ tel que $P(x)$ admet 2 racines <u>tel que $x_- < 1 < x_+$</u>

$\Delta > 0 \qquad$ 2 cas :

![[ch1-racines-autour-de-1.svg]]

- $a > 0$ : $P(1) < 0$
- $a < 0$ : $P(1) > 0$

On veut trouver tous les $m$ tel que
$$m \cdot P(1) < 0$$
$$
\begin{aligned}
&\iff m(m - m + m + 1) < 0 \\
&\iff m(m + 1) < 0
\end{aligned}
$$

Tableau de signes

| $m$      | $-\infty$ |     | $-1$ |     | $0$ |     | $+\infty$ |
| :------- | :-------: | :-: | :--: | :-: | :-: | :-: | :-------: |
| $m$      |           | $-$ |      | $-$ | $0$ | $+$ |           |
| $m+1$    |           | $-$ | $0$  | $+$ |     | $+$ |           |
| produit  |           | $+$ | $0$  | $-$ | $0$ | $+$ |           |

$$m \in \,]-1, 0[$$

---

### 1.8 Puissances et racines

> [!definition] Déf
> La puissance d'un nombre $a \in \mathbb{R}$ est définie par
> $$a^n := \begin{cases} \underbrace{a \cdot a \cdot a \cdot \ldots \cdot a}_{n \text{ fois}} & \text{si } n > 0 \\[4mm] \dfrac{1}{\underbrace{a \cdot a \cdot a \cdot \ldots \cdot a}_{n \text{ fois}}} & n < 0 \end{cases}$$

<u>Convention :</u> $a^0 = 1 \quad \forall a \in \mathbb{R}$

<u>Propriétés :</u> si $a \in \mathbb{R}^*$

1. $\operatorname{sgn}(a^n) = \begin{cases} 1 & \text{si } n = 2\ell \\ \operatorname{sgn}(a) & \text{si } n = 2\ell + 1 \end{cases}$
2. $\operatorname{sgn}(a^n)^m = \operatorname{sgn}(a^{n \cdot m})$ 
3. $a^n a^m = a^{n+m}$
4. $a^{n-m} = \dfrac{a^n}{a^m}$ $\qquad$ Cela justifie $a^0 = 1$ : $\;a^{n-n} = \dfrac{a^n}{a^n} = 1$

> [!definition] Déf
> $\forall a \in \mathbb{R}, \forall n \in \mathbb{N}^*$
> $$\sqrt[n]{a} = x \iff \begin{cases} x^n = a \\ \text{et} \\ \operatorname{sgn}(x) = \operatorname{sgn}(a) \end{cases}$$

<u>Remarque :</u> attention au signe

$$x^2 = 4 \iff x = \pm 2$$
mais
$$x = \sqrt{4} \iff x = 2$$
$$x^2 = 4 \iff x = \sqrt{4} \text{ si et seulement si } x \geq 0$$

<u>Propriétés :</u> $\quad \forall a \in D_{\text{def}}\sqrt[n]{x} = \begin{cases} \mathbb{R} & \text{si } n = 2\ell + 1 \\ \mathbb{R}_+ & \text{si } n = 2\ell \end{cases}$

1. $\left(\sqrt[n]{a}\right)^n = a$
2. $\sqrt[n]{a \cdot b} = \sqrt[n]{a} \cdot \sqrt[n]{b}$ $\qquad$ si $b \in D_{\text{def}}\sqrt[n]{x}$
3. $\sqrt[n]{a^p} = \left(\sqrt[n]{a}\right)^p$

<u>Remarque :</u> Attention à la simplification
$$\frac{1}{3} = \frac{2}{6} \;\;\cancel{\implies}\;\; x^{1/3} = x^{2/6}$$
$$D_{\text{def}}\sqrt[3]{x} = \mathbb{R} \quad \text{mais} \quad D_{\text{def}}\sqrt[6]{x^2} = \mathbb{R}_+$$

<u>Graphiquement</u>

![[ch1-puissances-racines.svg]]

- Si $n = 2\ell$ : 1 solution $\geq 0$
- Si $n = 2\ell + 1$ : 2 solutions symétriques

> [!definition] Déf
> Si $a \in \mathbb{R}^*$, $n \in \mathbb{Z}$, $m \in \mathbb{Z}^*$
> $$a^{n/m} = \left(\sqrt[m]{a}\right)^n \quad \text{si } a \in D_{\text{def}}\sqrt[m]{x}$$

#### <u>Exemples</u>

**1)**
$$D_{\text{def}}\, a^{1/3} = \mathbb{R}$$
$$D_{\text{def}}\, a^{2/6} = \mathbb{R}_+$$

**2)** Si $a > 0$,
$$a^{1/3} \cdot \sqrt{a} = a^{1/3} \cdot a^{1/2} = a^{5/6}$$

**3)** $x > 0$,
$$y = \sqrt{x + \underbrace{\sqrt{x + \sqrt{x + \sqrt{x + \sqrt{x \dots}}}}}_{y}}$$
$$y = \sqrt{x + y}$$

Si $y \geq 0$, on élève au carré
$$y^2 = x + y \iff y^2 - y - x = 0$$
$$\implies y = \frac{1 \pm \sqrt{1 + 4x}}{2} \geq 0$$

Si $x > 0$ : $\quad y = \dfrac{1 + \sqrt{1 + 4x}}{2}$

Si $x = 1$ : $\quad \sqrt{1 + \sqrt{1 + \sqrt{1 \dots}}} = \dfrac{1 + \sqrt{5}}{2} = \Phi$

Si $x = 2$ : $\quad \sqrt{2 + \sqrt{2 + \sqrt{2 \dots}}} = \dfrac{1 + \sqrt{1 + 8}}{2} = 2$

**4) Résoudre** $\sqrt{x^2 - 3x + 6} = 4x - 6$

<u>$D_{\text{def}}$ :</u> $a = x^2 - 3x + 6 \geq 0 \qquad \Delta = (-3)^2 - 4 \cdot 6 < 0$

<u>$D_{\text{def}}$ :</u> $\mathbb{R}$

$D_{\text{pos}}$ : $\{x \in \mathbb{R} \mid 4x - 6 \geq 0\} \qquad x \geq \dfrac{3}{2}$
$$= \left[\frac{3}{2}, \infty\right[$$

Sur $D_{\text{def}} \cap D_{\text{pos}}$

$$
\begin{aligned}
&\iff x^2 - 3x + 6 = (4x - 6)^2 \\
&\iff x^2 - 3x + 6 = 16x^2 - 48x + 36 \\
&\iff 15x^2 - 45x + 30 = 0 \\
&\iff x^2 - 3x + 2 = 0 \\
&\qquad (x-1)(x-2) = 0
\end{aligned}
$$

$D_{\text{pos}}$ : $\boxed{x \neq 1} \qquad S = \{2\}$

> [!important]
> $$\sqrt{f(x)} = g(x) \underset{D_{\text{def}}}{\iff} \begin{cases} g(x) \geq 0 & (D_{\text{pos}}) \\ \text{et} \\ f(x) = g^2(x) \end{cases}$$

**<u>Exemple</u>** $\quad \sqrt{6 - x} \leq 3 + 2x$

$D_{\text{def}}$ : $6 - x \geq 0 \iff x \in \,]-\infty, 6]$

$D_{\text{pos}}$ : $3 + 2x \geq 0 \quad x \in \left[-\frac{3}{2}, \infty\right[$

$$\implies S \subset \left[-\frac{3}{2}, 6\right]$$

$$
\begin{aligned}
6 - x &\leq (3 + 2x)^2 \\
6 - x &\leq 9 + 12x + 4x^2 \\
0 &\leq 3 + 13x + 4x^2
\end{aligned}
\qquad\qquad
\begin{aligned}
&\Delta = 13^2 - 48 = 121 \\
&\frac{-13 \pm \sqrt{13^2 - 4(4)(3)}}{8} \\
&\frac{-13 \pm 11}{8} \\
&x = -\frac{1}{4} \qquad x = -3
\end{aligned}
$$

<u>Graphiquement</u> $\quad 4x^2 + 13x + 3$

![[ch1-4x2-13x-3.svg]]

$$x \in \,]-\infty, -3] \cup \left[-\frac{1}{4}, \infty\right] \cap D_{\text{pos}} \cap D_{\text{def}}$$

$$S = \left[-\frac{1}{4}, 6\right]$$

<u>En général</u>

> [!important]
> $$\sqrt{f(x)} \leq g(x) \underset{D_{\text{def}}}{\iff} \begin{cases} g(x) \geq 0 & D_{\text{pos}} \\ \underline{\text{et}} \\ f(x) \leq g^2(x) \end{cases}$$
> $$\sqrt{f(x)} > g(x) \underset{D_{\text{def}}}{\iff} \begin{cases} g(x) < 0 \\ \underline{\text{ou}} \\ f(x) > g^2(x) \end{cases}$$

**Exemple ⑥** $\quad$ résoudre $\underline{\sqrt{x^2 + 1} = x + m}$

$D_{\text{def}} = \mathbb{R}$

$D_{\text{pos}}$ : $x \geq -m$

$$
\underset{D_{\text{pos}} \cap D_{\text{def}}}{\iff} x^2 + 1 = x^2 + 2mx + m^2
$$
$$2mx + m^2 - 1 = 0$$
$$2mx = 1 - m^2$$

Deux cas à distinguer

| $m = 0$         | $m \neq 0$                                      |
| :-------------- | :---------------------------------------------- |
| $0x = 1$        | $x = \dfrac{1 - m^2}{2m} \in D_{\text{pos}}$    |
| $S = \emptyset$ | $\iff \dfrac{1 - m^2}{2m} \geq -m$              |
|                 | $\dfrac{1 - m^2}{2m} + \dfrac{2m^2}{2m} \geq 0$ |
|                 | $\dfrac{m^2 + 1}{2m} \geq 0$                    |

Synthèse
$$
S = \begin{cases}
\emptyset & \text{si } m \leq 0 \\[2mm]
\dfrac{1 - m^2}{2m} & \text{si } m > 0
\end{cases}
$$

---

#### <u>Introduction aux suites</u>

Calcul $\sqrt{2}$ : $\quad$ on pose $x = \sqrt{2}$

$$
\begin{aligned}
&\iff x^2 = 2 \iff x^2 - 1 = 1 \\
&\iff (x-1)(x+1) = 1 \iff x - 1 = \frac{1}{1 + x}
\end{aligned}
$$
$$x = 1 + \frac{1}{1 + x}$$
