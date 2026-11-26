---
cours: Géométrie Analytique
chapitre: 2
source: "Chapitre 2 - Géométrie Analytique.pdf"
tags: [geometrie-analytique, chapitre-2]
---

# Chapitre 2. Vecteurs : produit scalaire

### 1. Définition

Soient $\vec{u}$ et $\vec{v}$ deux vecteurs formant un angle géométrique <span style="color:red">$\theta \in [0, \pi]$</span> (non orienté)

![[g2-angle.svg]]

Le produit scalaire de $\vec{u}$ et $\vec{v}$ est le réel :

> [!important]
> $$\vec{u} \cdot \vec{v} = \|\vec{u}\|\,\|\vec{v}\| \cos\theta$$
> <span style="color:red">« $\vec{u}$ scalaire $\vec{v}$ »</span>

> [!important] <u>Proposition</u>
> On a :
> $$-\|\vec{u}\|\,\|\vec{v}\| \leq \vec{u} \cdot \vec{v} \leq \|\vec{u}\|\,\|\vec{v}\|$$
>
> | Égalité à gauche | Égalité à droite |
> | :-- | :-- |
> | égalité lorsque $\theta = \pi$ | égalité lorsque $\theta = 0$ |
> | $\vec{u}, \vec{v}$ colinéaires de sens opposé | $\vec{u}, \vec{v}$ colinéaires de même sens |
> | | Par ex : $\vec{u} \cdot \vec{u} = \Vert \vec{u}\Vert ^2$ |

> [!important] <u>Proposition</u>
> Si $\vec{u}$ et $\vec{v}$ sont non nuls, on a :
> $$
> \vec{u} \cdot \vec{v} \text{ est } \begin{cases}
> {>}\, 0 \iff 0 \leq \theta < \pi/2 & \color{orange}\setminus\ \theta \text{ « aigu »} \\
> = 0 \iff \theta = \pi/2 & \color{orange}\setminus\ \theta \text{ « droit »} \\
> < 0 \iff \dfrac{\pi}{2} < \theta \leq \pi & \color{orange}\setminus\ \theta \text{ « obtus »}
> \end{cases}
> $$

---

### 2. Projection orthogonale

Soit $\vec{u} \neq \vec{0}$. Pour tout vecteur $\vec{v}$, on note <span style="color:red">$P_{\vec{u}}(\vec{v})$</span> la projeté orthogonal de $\vec{v}$ sur $\vec{u}$

![[g2-projection.svg]]

C'est un vecteur colinéaire à $\vec{u}$ :
$$P_{\vec{u}}(\vec{v}) = \boxed{\alpha}\,\vec{u} \qquad \color{orange}\text{« } \frac{P_{\vec{u}}(\vec{v})}{\vec{u}} \text{ »}$$

où :
$$\alpha = \pm \underbrace{\frac{\|P_{\vec{u}}(\vec{v})\|}{\|\vec{u}\|}}_{\text{rapport des normes}}$$

$$
\alpha = \begin{cases}
+\dfrac{\|\vec{v}\| \cos\theta}{\|\vec{u}\|} & \text{si } \theta \text{ aigu} \\[4mm]
-\dfrac{\|\vec{v}\| \underbrace{\cos(\pi - \theta)}_{\color{orange}-\cos\theta}}{\|\vec{u}\|} & \text{si } \theta \text{ obtus}
\end{cases}
$$

$$\alpha = \frac{\|\vec{v}\| \cos\theta}{\|\vec{u}\|} = \frac{\overbrace{\|\vec{u}\|\,\|\vec{v}\| \cos\theta}^{\color{orange}\vec{u} \cdot \vec{v}}}{\|\vec{u}\|^2}$$

> [!important] <u>Proposition</u>
> $$P_{\vec{u}}({\color{red}\vec{v}}) = \underbrace{\left(\frac{\color{red}\vec{u} \cdot \vec{v}}{\|\vec{u}\|^2}\right)}_{\alpha \in \mathbb{R}} \vec{u}$$

#### <u>Exemples</u>

**(a)** Si $\|\vec{u}\| = 1$ $\quad$ ($\vec{u}$ <span style="color:red">unitaire</span>)

![[g2-unitaire.svg]]

$$P_{\vec{u}}(\vec{v}) = (\vec{u} \cdot \vec{v})\,\vec{u}$$

**(b)** $\quad$ carré de côté $1$

![[g2-carre.svg]]

Représenter les vecteurs $\vec{v}$ tel que $\vec{u} \cdot \vec{v} = 0$
$$\theta = \frac{\pi}{2}$$

**(c)** Pareil qu'au b) mais avec $\vec{u} \cdot \vec{v} = 1$

On a :
$$\vec{u} \cdot \vec{v} = 1 \iff P_{\vec{u}}(\vec{v}) = \frac{\vec{u} \cdot \vec{v}}{\|\vec{u}\|^2} \cdot \vec{u}$$
$$P_{\vec{u}}(\vec{v}) = \frac{1}{2} \cdot \vec{u}$$

![[g2-uv-egal-1.svg]]

---

### 3. Propriétés algébriques

> [!important] <u>Proposition</u>
> Soient $\vec{u}, \vec{v}, \vec{w}$ des vecteurs et $\alpha, \beta \in \mathbb{R}$. On a alors :
> - **(a)** $\vec{u} \cdot \vec{v} = \vec{v} \cdot \vec{u}$ $\quad$ (symétrie)
> - **(b)** $(\alpha\vec{u} + \beta\vec{v}) \cdot \vec{w} = \alpha\,\vec{u} \cdot \vec{w} + \beta\,\vec{v} \cdot \vec{w}$
> - **(c)** $\vec{w} \cdot (\alpha\vec{u} + \beta\vec{v}) = \alpha\,\vec{w} \cdot \vec{u} + \beta\,\vec{w} \cdot \vec{v}$
>
> $\Big\}$ (distributivité)

<u>Preuve</u> (a) est clair par définition. (b) $\iff$ (c) d'après (a). Pour (c) :

|                                                                                                                                      |                                                                                                                                                                                     |
| :----------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $P_{\vec{u}}(\alpha\vec{v}) = \alpha P_{\vec{u}}(\vec{v})$                                                                           | $P_{\vec{u}}(\vec{v} + \vec{w}) = P_{\vec{u}}(\vec{v}) + P_{\vec{u}}(\vec{w})$                                                                                                      |
| $\downarrow$ <span style="color:gray">formule de projection</span>                                                                   |                                                                                                                                                                                     |
| $\dfrac{(\alpha\vec{v}) \cdot \vec{u}}{\Vert \vec{u}\Vert ^2} \cdot \vec{u} = \dfrac{\alpha(\vec{v} \cdot \vec{u})}{\Vert \vec{u}\Vert ^2}\,\vec{u}$ | $\dfrac{\vec{u} \cdot (\vec{v} + \vec{w})}{\Vert \vec{u}\Vert ^2}\,\vec{u} = \dfrac{\vec{u} \cdot \vec{v}}{\Vert \vec{u}\Vert ^2}\,\vec{u} + \dfrac{\vec{u} \cdot \vec{w}}{\Vert \vec{u}\Vert ^2}\,\vec{u}$ |
| $\underline{\vec{u} \cdot (\alpha\vec{v}) = \alpha\,\vec{u} \cdot \vec{v}}$                                                          | $\underline{\vec{u} \cdot (\vec{v} + \vec{w}) = \vec{u} \cdot \vec{v} + \vec{u} \cdot \vec{w}}$                                                                                     |

#### <u>Exemples</u>

**(a)**

![[g2-exemple-45.svg]]

$45^\circ \to \pi/4$

$$\vec{u} \cdot \vec{u} = \|\vec{u}\|^2 = \underline{4} \qquad\qquad \vec{u} \cdot \vec{v} = \|\vec{u}\|\,\|\vec{v}\| \cdot \cos\left(\frac{\pi}{4}\right)$$
$$\vec{v} \cdot \vec{v} = \|\vec{v}\|^2 = \underline{9} \qquad\qquad \vec{u} \cdot \vec{v} = 6 \cdot \frac{\sqrt{2}}{2} = \underline{3\sqrt{2}}$$

$$
\begin{aligned}
\|2\vec{u} - \vec{v}\| \implies \|2\vec{u} - \vec{v}\|^2 &= (2\vec{u} - \vec{v}) \cdot (2\vec{u} - \vec{v}) \\
&= 4\,\vec{u} \cdot \vec{u} - 2\,\vec{u} \cdot \vec{v} - 2\,\vec{v} \cdot \vec{u} + \vec{v} \cdot \vec{v} \\
&= 4(4) - 2(3\sqrt{2}) - 2(3\sqrt{2}) + 9 \\
&= 25 - 12\sqrt{2}
\end{aligned}
$$

**(b)** $\quad$ Calculer $\theta$

![[g2-prisme.svg]]

<u>Calculons :</u>
$$\vec{AE} \cdot \vec{AF} = \|\vec{AE}\|\,\|\vec{AF}\| \cdot \cos\theta$$

$$(\vec{AB} + \vec{BE}) \cdot (\vec{AC} + \vec{CF}) = \underbrace{\vec{AB} \cdot \vec{AC}}_{1/2} + \underbrace{\vec{AB} \cdot \vec{CF}}_{0} + \underbrace{\vec{BE} \cdot \vec{AC}}_{0} + \underbrace{\vec{BE} \cdot \vec{CF}}_{25}$$
$$= \frac{51}{2}$$

$$\underbrace{\|\vec{AE}\|}_{\sqrt{26}}\ \underbrace{\|\vec{AF}\|}_{\sqrt{26}} \cdot \cos\theta = \frac{51}{2} \implies \underline{\cos\theta = \frac{51}{52}}$$
