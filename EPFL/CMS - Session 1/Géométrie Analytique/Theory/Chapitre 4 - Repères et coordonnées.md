---
cours: Géométrie Analytique
chapitre: 4
source: "Chapitre 4 - Géométrie Analytique.pdf"
tags: [geometrie-analytique, chapitre-4]
---

# Chapitre 4. Repères et coordonnées

### 1. Repères

Un <span style="color:red">repère</span> du plan est un triplet :

$$
{\color{red}R} = (\underset{\text{origine}}{O},\ \overbrace{\underbrace{\vec{\imath}, \vec{\jmath}}_{\color{red}\text{non colinéaires}}}^{\color{orange}\text{vecteurs de base}})
$$

![[g4-repere.svg]]

On dit que $R$ est …

- <span style="color:red">orthonormé</span> si
  $$\underbrace{\|\vec{\imath}\| = \|\vec{\jmath}\| = 1}_{\vec{\imath} \text{ et } \vec{\jmath} \text{ unitaires}} \text{ et } \underbrace{\vec{\imath} \cdot \vec{\jmath} = 0}_{\vec{\imath} \text{ et } \vec{\jmath} \text{ orthogonaux}}$$

  ![[g4-orthonorme.svg]]

- <span style="color:red">direct / indirect</span> selon que l'angle orienté de $\vec{\imath}$ vers $\vec{\jmath}$ est $\oplus$ ou $\ominus$

  ![[g4-direct-indirect.svg]]

---

### 2. Coordonnées des points et vecteurs

Le plan étant muni d'un repère, les vecteurs et les points reçoivent des <span style="color:red">coordonnées</span>, notées :

| | |
| :-: | :-: |
| $\vec{u}\begin{pmatrix} x \\ y \end{pmatrix}$ | $M(x_M, y_M)$ |
| vecteur | point |
| ~~$\vec{u} = \begin{pmatrix} x \\ y \end{pmatrix}$~~ ❌ | ~~$M = (x_M, y_M)$~~ ❌ |

| Coordonnées | Objet |
| :-- | :-- |
| $\begin{pmatrix} x \\ y \end{pmatrix}, \begin{pmatrix} x' \\ y' \end{pmatrix}$ | $\vec{u}, \vec{v}$ |
| $(x_M, y_M),\ (x_N, y_N)$ | $M, N$ |
| $\begin{pmatrix} x + x' \\ y + y' \end{pmatrix}$ | $\vec{u} + \vec{v}$ |
| $t\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} tx \\ ty \end{pmatrix}$ | $t\vec{u}$ |
| $\begin{pmatrix} x_N - x_M \\ y_N - y_M \end{pmatrix}$ | $\vec{MN}$ |
| $\left(\dfrac{x_N + x_M}{2}, \dfrac{y_N + y_M}{2}\right)$ | $P$ milieu de $\vec{MN}$ |

<u>**Exemple**</u> Dans le plan muni d'un repère $R = (O, \vec{\imath}, \vec{\jmath})$ on donne :
$$A(0, 5), \quad B(4, 3), \quad C(2, 1)$$

**(a)** Calculer les coordonnées de …
$$\vec{AB}, \quad \vec{AC}, \quad \frac{1}{2}\vec{AC}, \quad \text{milieu de } \vec{AC}$$

**(b)** Coordonnées de $B$ dans $(O, \vec{\imath} + \vec{\jmath}, \vec{\imath})$
$$\vec{OB} = 4\vec{\imath} + 3\vec{\jmath}$$

Appelons les $(x, y)$. On a :
$$\vec{OB} = x(\vec{\imath} + \vec{\jmath}) + y\vec{\imath} = (x + y)\vec{\imath} + x\vec{\jmath}$$
$$x = 3, \quad y = 1$$
$$\vec{OB} = \begin{pmatrix} 3 \\ 1 \end{pmatrix}$$

---

### 3. Produit scalaire

Même notation qu'aux paragraphes 1 et 2

> [!important] <u>Proposition</u>
> $$\underset{x\vec{\imath} + y\vec{\jmath}}{\vec{u}\begin{pmatrix} x \\ y \end{pmatrix}},\quad \underset{x'\vec{\imath} + y'\vec{\jmath}}{\vec{v}\begin{pmatrix} x' \\ y' \end{pmatrix}} \qquad \vec{u} \cdot \vec{v} = xx'{\color{red}\|\vec{\imath}\|^2} + yy'{\color{red}\|\vec{\jmath}\|^2} + (xy' + x'y)\,{\color{red}\vec{\imath} \cdot \vec{\jmath}}$$

En particulier, <span style="color:red">si $R$ orthonormé</span>, on a

| | |
| :-- | :-- |
| $xx' + yy'$ | $\vec{u} \cdot \vec{v} \quad \big) \ \Vert \vec{u}\Vert \,\Vert \vec{v}\Vert  \cos\theta$ |
| $\sqrt{x^2 + y^2}$ | $\Vert \vec{u}\Vert  \quad \big) \ \sqrt{\vec{u} \cdot \vec{u}}$ |
| $\cos\theta = \dfrac{xx' + yy'}{\sqrt{x^2 + y^2}\,\sqrt{x'^2 + y'^2}}$ | $\theta \in [0, \pi]$ angle géométrique entre $\vec{u}$ et $\vec{v}$ |
| $\begin{pmatrix} -y \\ x \end{pmatrix}, \begin{pmatrix} y \\ -x \end{pmatrix}$ | Vecteurs orthogonaux à $\vec{u}$ et de norme $\Vert \vec{u}\Vert $ $\Big)$ <span style="color:orange">« tourner $\vec{u}$ d'un angle droit »</span> |

![[g4-angle.svg]]

![[g4-orthogonal.svg]]

#### <u>Exemples</u>

**(a)** Reprise du paragraphe 2 avec $R$ orthonormé $\qquad \vec{AB}\begin{pmatrix} 4 \\ -2 \end{pmatrix}, \ \vec{AC}\begin{pmatrix} 2 \\ -4 \end{pmatrix}$

| | |
| :-- | :-- |
| $\Vert \vec{AB}\Vert , \Vert \vec{AC}\Vert $ | $\sqrt{20}, \sqrt{20} = 2\sqrt{5}, 2\sqrt{5}$ $\quad$ <span style="color:orange">$ABC$ isocèle en $A$</span> |
| angle au sommet $A$ | $\cos\hat{A} = \dfrac{\vec{AB} \cdot \vec{AC}}{\Vert \vec{AB}\Vert \,\Vert \vec{AC}\Vert } = \dfrac{4}{5} \qquad \hat{A} \simeq 36.9^\circ$ |

**(b)** Supposons que $\|\vec{\imath}\| = \|\vec{\jmath}\| = 1$ et $\theta$ de $\vec{\imath}$ vers $\vec{\jmath} = \dfrac{\pi}{3}$

![[g4-pi-sur-3.svg]]

$$\vec{u}\begin{pmatrix} x \\ y \end{pmatrix}, \quad \vec{v}\begin{pmatrix} x' \\ y' \end{pmatrix}$$
$$\implies \vec{u} \cdot \vec{v} = xx' + yy' + \frac{1}{2}(xy' + x'y) \qquad \left(\vec{\imath} \cdot \vec{\jmath} = \frac{1}{2}\right)$$
$$\|\vec{u}\| = \sqrt{x^2 + y^2 + xy}$$

---

### 4. Aire et orientation

Mêmes notations que ci-dessus. On note aussi <span style="color:red">$\theta \in\, ]-\pi, \pi]$</span> l'<span style="color:red">angle orienté</span> de $\vec{u}$ vers $\vec{v}$

> [!definition] <u>Définition</u>
> On appelle <span style="color:red">aire orientée</span> de $\vec{u}$ et $\vec{v}$ le réel :
> $$\underset{\text{surface}}{\color{red}\sigma(\vec{u}, \vec{v})} = \pm\ \text{aire}\big(\text{parallélogramme construit sur } \vec{u}, \vec{v}\big)$$
> - $+$ si $\vec{u}, \vec{v}$ direct, $-$ sinon
> - $= \|\vec{u}\|\,\|\vec{v}\| \sin\theta$

![[g4-aire-orientee.svg]]

> [!definition] <u>Définition</u>
> On appelle <span style="color:red">déterminant</span> de $\vec{u}$ et $\vec{v}$ dans $R$ le réel :
> $$\det_R(\vec{u}, \vec{v}) = \begin{vmatrix} x & x' \\ y & y' \end{vmatrix} = xy' - x'y$$

> [!important] <u>Proposition</u> <span style="color:red">($R$ orthonormé direct)</span>
> $$\sigma(\vec{u}, \vec{v}) = \det_R(\vec{u}, \vec{v})$$

Si $R$ est orthonormé direct, on a donc

| | |
| :-- | :-- |
| $\dfrac{xy' - x'y}{\sqrt{x^2 + y^2}\,\sqrt{x'^2 + y'^2}}$ | $\sin\theta \quad \Big) \ \dfrac{\sigma(\vec{u}, \vec{v})}{\Vert \vec{u}\Vert \,\Vert \vec{v}\Vert }$ |
| $\operatorname{sgn}(xy' - x'y)$ | orientation de $\vec{u}$ à $\vec{v}$ $\Big)$ signe $\sin\theta$ |
| $\lvert\sigma(\vec{u}, \vec{v})\rvert = \lvert\det_R(\vec{u}, \vec{v})\rvert$ | aire du parallélogramme construit sur $\vec{u}$ et $\vec{v}$ |
| $\begin{pmatrix} y \\ -x \end{pmatrix}$ : $\begin{vmatrix} x & y \\ y & -x \end{vmatrix} = -x^2 - y^2 = -(x^2 + y^2)$ | $\vec{u}$ tourné de $-\dfrac{\pi}{2}$ |
| $\begin{pmatrix} -y \\ x \end{pmatrix}$ : $\begin{vmatrix} x & -y \\ y & x \end{vmatrix} = x^2 + y^2$ | $\vec{u}$ tourné de $\dfrac{\pi}{2}$ |
| $\sigma(\vec{u}, \vec{v}) = \det_R(\vec{u}, \vec{v}) = 0$ | $\vec{u}, \vec{v}$ colinéaires |

<u>**Exemple**</u> : On reprend l'exemple du paragraphe 2
$$A(0, 5), \quad B(4, 3), \quad C(2, 1)$$
$$\vec{AB}\begin{pmatrix} 4 \\ -2 \end{pmatrix}, \quad \vec{AC}\begin{pmatrix} 2 \\ -4 \end{pmatrix}, \quad \vec{BA}\begin{pmatrix} -4 \\ 2 \end{pmatrix}, \quad \vec{BC}\begin{pmatrix} -2 \\ -2 \end{pmatrix}$$

Si $R$ est orthonormé direct :

| | |
| :-- | :-- |
| $\begin{vmatrix} 4 & 2 \\ -2 & -4 \end{vmatrix} = -16 + 4 = -12$ | $\sigma(\vec{AB}, \vec{AC})$ $\quad$ (aire parallélogramme complété de $ABC$) |
| $\dfrac{1}{2} \cdot \lvert -12 \rvert = 6$ | aire triangle |
| $\operatorname{sgn}\big(\sigma(\vec{AB}, \vec{AC})\big) = -1$ | $\vec{AB}, \vec{AC}$ indirect |
| $\operatorname{sgn}\big(\sigma(\vec{BA}, \vec{BC})\big) = 1$ | $BAC$ directement |
