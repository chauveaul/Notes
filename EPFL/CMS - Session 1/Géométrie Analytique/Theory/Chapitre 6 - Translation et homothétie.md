---
cours: Géométrie Analytique
chapitre: 6
source: "Chapitre 6 - Géométrie Analytique.pdf"
tags: [geometrie-analytique, chapitre-6]
---

# Chapitre 6. Translation et homothétie

### 1. Translation

Soit $\vec{u}$ un vecteur du plan

![[g6-translation.svg]]

$$\begin{pmatrix} x' - x \\ y' - y \end{pmatrix} = \begin{pmatrix} \lambda \\ \mu \end{pmatrix}$$

| <span style="color:lime">transformation géométrique</span> | <span style="color:cyan">expression analytique</span> |
| :-- | :-- |
| $t_{\vec{u}} : M \to M'$ où $\vec{MM'} = \vec{u}$ | $\begin{cases} x' = x + \lambda \\ y' = y + \mu \end{cases}$ |
| translation de vecteur $\vec{u}$ | |

<u>**Exemple**</u>

**a)** Trouver la nature et les éléments caractéristiques de la transformation
$$\begin{cases} x' = x + 3 \\ y' = y + 4 \end{cases}$$

Il s'agit de la translation $t_{\vec{u}}$ avec $\vec{u} = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$

![[g6-exemple-translation.svg]]

**b)** Si $\vec{u} = \vec{0}$ alors $\underset{\substack{x' = x \\ y' = y}}{t_{\vec{u}} : M \to M}$ est la transformation identité

---

### 2. Homothétie

Soit $\Omega$ un point et $\alpha \in \mathbb{R}$ avec $\alpha \neq 0$ et $\alpha \neq 1$

![[g6-homothetie.svg]]

$$
\begin{aligned}
\begin{pmatrix} x' - x_\Omega \\ y' - y_\Omega \end{pmatrix} &= \alpha\begin{pmatrix} x - x_\Omega \\ y - y_\Omega \end{pmatrix} \\
&= \begin{pmatrix} \alpha x - \alpha x_\Omega \\ \alpha y - \alpha y_\Omega \end{pmatrix} \\
\iff \begin{pmatrix} x' \\ y' \end{pmatrix} &= \begin{pmatrix} \alpha x + (1 - \alpha)x_\Omega \\ \alpha y + (1 - \alpha)y_\Omega \end{pmatrix}
\end{aligned}
$$

| | |
| :-- | :-- |
| $\underbrace{h_{\Omega,\alpha} : M \to M' \text{ avec } \vec{\Omega M'} = \alpha\vec{\Omega M}}_{\text{homothétie de centre } \Omega \text{ et de rapport } \alpha}$ | $\begin{cases} x' = \alpha x + \lambda \\ y' = \alpha y + \mu \end{cases}$ $\qquad \lambda = (1 - \alpha)x_\Omega, \ \mu = (1 - \alpha)y_\Omega$ |
| $h_{\Omega,\alpha}(O)$ : image de l'origine par la transformation | $(\lambda, \mu) = \big((1 - \alpha)x_\Omega, (1 - \alpha)y_\Omega\big)$ |
| $\underset{M' = M}{\text{point fixe}}$ : $\Omega$ (unique) | $(x_\Omega, y_\Omega) = \left(\dfrac{\lambda}{1 - \alpha}, \dfrac{\mu}{1 - \alpha}\right)$ ou $\begin{cases} x_\Omega = \alpha x_\Omega + \lambda \\ y_\Omega = \alpha y_\Omega + \mu \end{cases}$ |

<u>**Exemple**</u>

**a)** Trouver la nature et les éléments caractéristiques de
$$\begin{cases} x' = 3x - 6 \\ y' = 3y + 2 \end{cases} \qquad \alpha = 3, \ \lambda = -6, \ \mu = 2$$

Il s'agit de l'homothétie $h_{\Omega,3}$ où $\Omega$ est l'unique point fixe
$$
\begin{cases} x' = x \\ y' = y \end{cases}
\qquad
\begin{cases} 3x - 6 = x \\ 3y + 2 = y \end{cases}
\iff
\begin{cases} 2x = 6 \\ 2y = -2 \end{cases}
\qquad
\begin{aligned} x &= 3 \\ y &= -1 \end{aligned}
\qquad \Omega(3, -1)
$$

**b)** Déterminer l'expression analytique de $h_{\Omega,-2}$ où $\Omega(4, 5)$

$$
\begin{aligned}
M' = h_{\Omega,-2}(M) &\iff \vec{\Omega M'} = -2\,\vec{\Omega M} \\
&\iff \begin{pmatrix} x' - 4 \\ y' - 5 \end{pmatrix} = -2\begin{pmatrix} x - 4 \\ y - 5 \end{pmatrix}
\end{aligned}
$$

$$\begin{cases} x' - 4 = -2x + 8 \\ y' - 5 = -2y + 10 \end{cases}$$

$$\begin{cases} x' = -2x + \boxed{12} \\ y' = -2y + \boxed{15} \end{cases} \qquad \color{red}\text{ne sont pas les coordonnées de } \Omega$$

**c)** Image d'une droite $d$ par $h_{\Omega,\alpha}$

![[g6-image-droite.svg]]

> <span style="color:magenta">vrai point $B$, $d'$ est en vrai $/\!/$ à $d$</span>

$$\vec{A'B'} = \alpha\,\vec{AB} \qquad \Big) \quad \begin{aligned} \vec{\Omega A'} &= \alpha\,\vec{\Omega A} \\ \vec{\Omega B'} &= \alpha\,\vec{\Omega B} \end{aligned}$$
$$
\begin{aligned}
\vec{A'B'} &= \vec{\Omega B'} - \vec{\Omega A'} \\
&= \alpha\big(\vec{\Omega B} - \vec{\Omega A}\big)
\end{aligned}
$$

$h_{\Omega,\alpha}(d)$ est une droite $/\!/$ à $d$

**d)** Caractérisation par le rapport $\alpha$ et un couple point image

![[g6-placer-omega.svg]]

<span style="color:red">⭐ $\Omega = t_{\frac{1}{3}\vec{BA}}(A)$</span>

Placer $\Omega$ sachant que $h_{\Omega,4}(A) = B$

<u>Solution :</u> on a
$$h_{\Omega,4}(A) = B \qquad \underbrace{\vec{\Omega B}}_{\vec{\Omega A} + \vec{AB}} = 4\,\vec{\Omega A} \iff 3\,\vec{\Omega A} = \vec{AB}$$
$$\iff \vec{A\Omega} = \frac{1}{3}\vec{BA}$$

---

### 3. Composition ⭐

Les homothéties et les translations se composent entre elles selon le tableau suivant :

| | |
| :-- | :-- |
| $\begin{cases} x' = (x + \lambda) + \rho \\ y' = (y + \mu) + \sigma \end{cases}$ | $\begin{cases} x' = \alpha x + \lambda + \rho \\ y' = (\alpha y + \mu) + \sigma \end{cases}$ |
| $\underline{t_{\vec{v}} \circ t_{\vec{u}} = t_{\vec{u} + \vec{v}}}$ | $t_{\vec{v}} \circ h_{\Omega,\alpha} = h_{?,\alpha}$ |
| $h_{\Delta,\beta} \circ t_{\vec{u}} = h_{?,\beta}$ | $h_{\Delta,\beta} \circ h_{\Omega,\alpha} = \begin{cases} t & \text{si } \alpha\beta = 1 \\ h_{?,\alpha\beta} & \text{si } \alpha\beta \neq 1 \end{cases}$ |
| $\begin{cases} x' = \beta(x + \lambda) + \rho \\ y' = \beta(y + \mu) + \sigma \end{cases}$ | $\begin{cases} x' = \beta(\alpha x + \lambda) + \rho \\ y' = \beta(\alpha y + \mu) + \sigma \end{cases}$ |

<u>**Exemple**</u> On donne : $A$, $B$

Déterminer la nature et les éléments caractéristiques de la composée
$$h_{B,\frac{1}{3}} \circ h_{A,3}$$

<u>Solution</u>, c'est une translation $t_{\vec{u}}$ car $3 \cdot \dfrac{1}{3} = 1$

Pour tout point $M$, on a donc :
$$\vec{u} = \vec{MM'} \quad \text{où} \quad M' = h_{B,\frac{1}{3}}\big(h_{A,3}(M)\big)$$

![[g6-composition-A.svg]]

Par exemple si $M = A$, on obtient $\vec{AA'} = \underbrace{\boxed{\frac{2}{3}\vec{AB}}}_{\vec{u}}$

car $A' = h_{B,\frac{1}{3}}(A) \quad \Big) \ \vec{BA'} = \dfrac{1}{3}\vec{BA}$

<u>Conclusion</u>
$$h_{B,\frac{1}{3}} \circ h_{A,3} = t_{\frac{2}{3}\vec{AB}}$$

![[g6-composition-M.svg]]
