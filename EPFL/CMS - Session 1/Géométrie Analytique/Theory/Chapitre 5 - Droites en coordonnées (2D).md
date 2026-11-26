---
cours: Géométrie Analytique
chapitre: 5
source: "Chapitre 5 - Géométrie Analytique.pdf"
tags: [geometrie-analytique, chapitre-5]
---

# Chapitre 5 – Droites en coordonnées (2D)

### 1. Droites passant par l'origine

On munit le plan d'un repère $R = (O, \vec{\imath}, \vec{\jmath})$. Soient $a, b \in \mathbb{R}$ avec $(a, b) \neq (0, 0)$. Pour tout $M(x, y)$ on a alors :

$$ax + by = 0 \iff \dots$$

| $R$ quelconque | ==$R$ orthonormé== $*$ |
| :-- | :-- |
| $\begin{vmatrix} x & -b \\ y & a \end{vmatrix} = 0 \iff \vec{OM}, \vec{u}$ colinéaires | $\vec{OM} \cdot \vec{m} = 0$ |
| où $\vec{u}\begin{pmatrix} -b \\ a \end{pmatrix}$ | où $\vec{m}\begin{pmatrix} a \\ b \end{pmatrix}$ |
| $\vec{OM} = t\vec{u}, \ t \in \mathbb{R}$ | |

Géométriquement, cette équation correspond donc à une droite :

![[g5-droite-origine.svg]]

Si $R$ est orthonormé direct, mettre l'équation « sous forme réduite » permet de calculer l'<span style="color:red">angle d'inclinaison</span> $\theta \in \left]-\dfrac{\pi}{2}, \dfrac{\pi}{2}\right]$ que fait $d$ avec l'axe des abscisses. <span style="color:orange">$\big)$ « l'horizontale »</span>

« Forme réduite »
$$d:\ ax + by = 0 \iff \begin{cases} y = -\dfrac{a}{b}x & \text{si } b \neq 0 \\[2mm] x = 0 & \text{si } b = 0 \end{cases}$$

![[g5-pente.svg]]

- $d:\ y = {\color{red}m}x$ (si $b \neq 0$) : $\quad \tan{\color{red}\theta} = {\color{red}m}$ $\quad$ <span style="color:orange">$\big)$ pente de $m$</span>
- $d:\ x = 0$ (si $b = 0$) : $\quad \theta = +\dfrac{\pi}{2}$ $\quad$ <span style="color:orange">$\big)$ pente infinie</span>

---

### 2. Droites quelconques

Mêmes notations qu'au paragraphe 1. On se donne aussi une constante $c \in \mathbb{R}$. On a alors :

$$
ax + by = c \underset{\substack{\color{red}A(x_A, y_A) \\ \color{red}\text{solution} \\ \color{red}\text{particulière}}}{\iff} ax + by = \underbrace{ax_A + by_A}_{c}
$$
$$\iff a(x - x_A) + b(y - y_A) = 0 \iff \dots$$

| $R$ quelconque | ==$R$ orthonormé== |
| :-- | :-- |
| $\vec{AM} = t\vec{u}, \ t \in \mathbb{R}$ | $\vec{AM} \cdot \vec{n} = 0$ |
| $\vec{AM}, \vec{u}$ colinéaires, où $\vec{u}\begin{pmatrix} -b \\ a \end{pmatrix}$ $\Big)$ $\begin{vmatrix} x - x_A & -b \\ y - y_A & a \end{vmatrix} = 0$ | où $\vec{OM} \cdot \vec{n} = c$ |
| | avec $\vec{n}\begin{pmatrix} a \\ b \end{pmatrix}$ |

$$a(x - x_A) + b(y - y_A) = ax + by - c$$

Géométriquement, cette équation décrit donc aussi une droite.

![[g5-droite-quelconque.svg]]

Pour tout vecteur $\vec{v}\begin{pmatrix} \alpha \\ \beta \end{pmatrix}$ directeur de $d$, c'est-à-dire colinéaire à $\vec{u}\begin{pmatrix} -b \\ a \end{pmatrix}$
$$\Big) \begin{vmatrix} \alpha & -b \\ \beta & a \end{vmatrix} = 0$$
$$a\alpha + b\beta = 0$$

On peut aussi décrire $d$ en utilisant $\vec{v}$, via les équations :
$$
d:\ \begin{cases} x = x_A + t\alpha \\ y = y_A + t\beta \end{cases}, \ t \in \mathbb{R}
\qquad \Big) \ \vec{OM} = \vec{OA} + t\vec{v}, \ t \in \mathbb{R}
$$

#### En résumé, <span style="color:red">si $R$ est quelconque</span>

| | |
| :-- | :-- |
| $ax + by = c$ $\quad$ <span style="color:red">$\big)$ équation cartésienne</span> | droite $d$ |
| $(x_A, y_A), \ ax_A + by_A = c$ | <span style="color:magenta">position</span> : point $A \in d$ |
| $\begin{pmatrix} -b \\ a \end{pmatrix}$ | <span style="color:cyan">direction</span> : $\vec{u}$ directeur de $d$ |
| $\begin{pmatrix} \alpha \\ \beta \end{pmatrix}, \ a\alpha + b\beta = 0$ $\quad$ <span style="color:red">$\big)$ équation homogène</span> | <span style="color:cyan">direction</span> : $\vec{v}$ directeur de $d$ |
| $\begin{cases} x = {\color{magenta}x_A} + t{\color{cyan}\alpha} \\ y = {\color{magenta}y_A} + t{\color{cyan}\beta} \end{cases}, \ t \in \mathbb{R}$ $\quad$ <span style="color:red">$\big)$ équations paramétriques</span> | droite $d$ |

#### <span style="color:red">Si $R$ est orthonormé</span>, on a aussi :

| | |
| :-- | :-- |
| $\begin{pmatrix} a \\ b \end{pmatrix}$ | <span style="color:cyan">direction</span> : $\vec{n}$ normal à $d$ |
| $\delta = \dfrac{\lvert ax + by - c \rvert}{\sqrt{a^2 + b^2}}$ | <span style="color:magenta">position</span> : distance $\delta$ de $M(x, y)$ à la droite $d$ |
| $ax + by > c$ $\quad$ <span style="color:gray">$P_{\vec{n}}(\vec{AM})$ et $\vec{n}$ sont de même sens</span> | demi-plan vers lequel $\vec{n}$ pointe |
| $ax + by < c$ $\quad$ <span style="color:gray">$P_{\vec{n}}(\vec{AM})$ et $\vec{n}$ sont de sens opposés</span> | demi-plan vers lequel $-\vec{n}$ pointe |

| $ax + by > c$ | $ax + by < c$ |
| :-: | :-: |
| ![[g5-demi-plan-plus.svg]] | ![[g5-demi-plan-moins.svg]] |

En effet, calculons ($R$ est orthonormé) :
$$
\begin{aligned}
P_{\vec{n}}(\vec{AM}) &= \frac{\vec{AM} \cdot \vec{n}}{\|\vec{n}\|^2} \cdot \vec{n} = \frac{a(x - x_A) + b(y - y_A)}{a^2 + b^2} \cdot \vec{n} \\
&= \frac{ax + by - ax_A - by_A}{a^2 + b^2}\,\vec{n} \\
&\underset{{\color{gray}ax_A + by_A = c}}{=} \frac{ax + by - c}{a^2 + b^2}\,\vec{n} \qquad {\color{gray}\Big) \ \alpha\vec{n}, \quad \|P_{\vec{n}}(\vec{AM})\| = |\alpha|\,\|\vec{n}\|}
\end{aligned}
$$

---

#### <u>Exemples</u>

**a)** Soient $A(2, 0)$ et $B(3, 4)$. Trouver une équation cartésienne de la droite $d = (AB)$.

<u>Solution 1 :</u>
$$4x - y = c \qquad \begin{vmatrix} x & 1 \\ y & 4 \end{vmatrix} = 0$$

![[g5-exemple-a.svg]]

$$d:\ 4x - y = 8$$

Si $R$ est orthonormé direct, ces deux droites sont inclinées de l'angle $\theta$ par rapport à l'horizontale.
$$4x - y = 0 \iff y = 4x$$
$$\underline{\tan\theta = 4} \quad {\color{orange}\Big) \ \theta \simeq 76^\circ}$$

<u>Solution 2</u>
$$M \in d \iff \vec{AM}, \vec{AB} \text{ colinéaires}$$
$$d:\ \begin{vmatrix} x - 2 & 1 \\ y - 0 & 4 \end{vmatrix} = 0 = 4x - 8 - y$$

<u>Solution 3</u>
$$
\underset{\color{gray}\vec{OM} = \vec{OA} + t\vec{AB}, \ t \in \mathbb{R}}{d:\ \begin{cases} x = 2 + t \\ y = 0 + 4t = 4t \end{cases}, \ t \in \mathbb{R}}
\quad \xrightarrow{\color{red}\text{élimination du paramètre}} \quad 4x - y = 8
$$

**b)** La droite $d:\ 3x - 4y = 12$

- … passe par : $(4, 0), (0, -3), (8, 3), \dots$ $\quad \Big)$ solutions de $3x - 4y = 12$
- … est dirigée par $\begin{pmatrix} -4 \\ -3 \end{pmatrix}, \begin{pmatrix} 4 \\ 3 \end{pmatrix}, \begin{pmatrix} 8 \\ 6 \end{pmatrix}, \dots$ $\quad \Big)$ solutions de l'équation homogène de $3x - 4y = 0$

![[g5-exemple-b.svg]]

Si $R$ est orthonormé, alors $\vec{n}\begin{pmatrix} 3 \\ -4 \end{pmatrix}$ est normal à la droite.

L'origine $O(0, 0)$ est située à distance
$$\delta(O, d) = \frac{\lvert 3 \cdot 0 - 4 \cdot 0 - 12 \rvert}{\sqrt{9 + 16}} = \frac{12}{5} = \underline{2.4}$$

dans le demi-plan vers lequel $-\vec{n}$ pointe car
$$0 = 3 \times 0 - 4 \cdot 0 < 12$$
