---
cours: Géométrie Analytique
chapitre: 1
source: "Chapitre 1 - Géométrie Analytique.pdf"
tags: [geometrie-analytique, chapitre-1]
---

# Chapitre 1. Vecteurs : généralités

### 1. Définition

<span style="color:orange">« Un vecteur n'a pas de position »</span>

![[g1-vecteur.svg]]

Un vecteur est une flèche (dessinée dans le plan ou l'espace) qui est « détachée de sa position ».

![[g1-parallelogramme.svg]]

$$\vec{AB} = \vec{CD} \iff ABDC \text{ est un } \underline{\text{parallélogramme}}$$

> <span style="color:magenta">$A \neq C$, $B \neq D$, $[AB] \neq [CD]$</span>

Un vecteur est uniquement caractérisé par :

- sa <span style="color:red">longueur</span> ou <span style="color:red">norme</span> $\in [0, +\infty[$

  ![[g1-norme.svg]]

  Le seul vecteur de norme $0$ est appelé <span style="color:red">vecteur nul</span>, noté <span style="color:red">$\vec{0}$</span>, i.e. $\left\{\vec{AA}\right\}$

- sa <span style="color:red">direction</span>
- son <span style="color:red">sens</span>

  $\Big\}$ si $\vec{u} \neq \vec{0}$

---

### 2. Colinéarité

Deux vecteurs sont dits <span style="color:red">colinéaires</span> s'ils ont la même direction, s'ils sont <span style="color:red">directeurs</span> de la même droite
$\uparrow$ (on peut tracer sur la même droite)

![[g1-colineaires.svg]]

![[g1-alignes.svg]]

$$\vec{AB}, \vec{AC} \text{ colinéaires} \iff A, B, C \text{ alignés}$$

![[g1-paralleles.svg]]

$$\vec{AB}, \vec{CD} \text{ colinéaires} \iff (AB) \text{ parallèle à } (CD)$$

Si $\vec{u} \neq \vec{0}$ les vecteurs colinéaires à $\vec{u}$ sont obtenus par la <span style="color:red">multiplication scalaire</span>

$$\vec{v} = \alpha\vec{u} \qquad \text{où} \qquad \alpha = \underset{\color{magenta}\text{sens}}{\color{magenta}\pm}\ \underset{\color{cyan}|\alpha|}{\color{cyan}\frac{\|\vec{v}\|}{\|\vec{u}\|}}$$

> - <span style="color:magenta">$\pm$ : rapport des sens ($+$ si $\vec{u}$ et $\vec{v}$ même sens)</span>
> - <span style="color:cyan">$\dfrac{\|\vec{v}\|}{\|\vec{u}\|}$ : rapport des normes $|\alpha|$</span>

Si $\vec{u} = \vec{0}$, tout vecteur est colinéaire à $\vec{u}$.

Par contre, on a :
$$\forall \alpha \in \mathbb{R}, \quad \alpha\vec{0} = \vec{0}$$

<u>**Exemple**</u>

![[g1-exemple-droite.svg]]

$$\vec{AC} = {\color{red}3}\,\vec{AB} \qquad \vec{AB} = {\color{red}0.5}\,\vec{BC} \qquad \vec{CA} = {\color{red}-1.5}\,\vec{BC}$$

> [!important] <u>Proposition</u>
> Pour tout vecteur $\vec{u}$ et tous réels $\alpha, \beta$ on a :
> - $1\vec{u} = \vec{u}$
> - $\alpha\vec{u} = \vec{0} \iff \alpha = 0 \text{ ou } \vec{u} = \vec{0}$
> - $\alpha(\beta\vec{u}) = (\alpha\beta)\vec{u}$

---

### 3. Addition et combinaisons linéaires

La <span style="color:red">somme</span> de deux vecteurs $\vec{u}$ et $\vec{v}$ est définie par :

![[g1-somme.svg]]

$$\underset{\color{red}\vec{u}+\vec{v}}{\vec{AC}} = \vec{AB} + \vec{BC} \qquad \color{orange}\text{relation de Chasles}$$

Les <span style="color:red">combinaisons linéaires</span> de $\vec{u}$ et $\vec{v}$ sont les vecteurs de type :
$$\alpha\vec{u} + \beta\vec{v}, \qquad \alpha, \beta \in \mathbb{R}$$

Par ex.
$$0\vec{u} + 0\vec{v} = \vec{0}$$
$$2\vec{u} + 3\vec{v}$$
$$5\vec{u} + 0\vec{v} = 5\vec{u} \ \dots$$

> [!important] <u>Proposition</u>
> Pour tous vecteurs $\vec{u}, \vec{v}, \vec{w}$ et tous $\alpha, \beta \in \mathbb{R}$ on a :
> - $\vec{u} + \vec{0} = \vec{u} = \vec{0} + \vec{u}$
> - $\vec{u} + (-\vec{u}) = \vec{0}$
> - $\vec{u} + \vec{v} = \vec{v} + \vec{u}$
> - $\alpha(\vec{u} + \vec{v}) = \alpha\vec{u} + \alpha\vec{v}$
> - $(\vec{u} + \vec{v}) + \vec{w} = \vec{u} + (\vec{v} + \vec{w})$
> - $(\alpha + \beta)\vec{u} = \alpha\vec{u} + \beta\vec{u}$

---

### 4. Décomposition

> [!important] <u>Théorème (2D)</u>
> Soient $\vec{\imath}$ et $\vec{\jmath}$ deux vecteurs <span style="color:red">non colinéaires</span> du plan. Tout vecteur $\vec{u}$ du plan se <span style="color:red">décompose</span> comme :
> $$\vec{u} = \alpha\vec{\imath} + \beta\vec{\jmath} \qquad (\alpha, \beta \in \mathbb{R})$$
> et ce de manière unique.

<u>Preuve par construction.</u>

![[g1-decomposition.svg]]

> [!important] <u>Théorème (3D)</u>
> Soient $\vec{\imath}, \vec{\jmath}, \vec{k}$ trois vecteurs <span style="color:red">non coplanaires</span> de l'espace. Tout vecteur $\vec{u}$ se décompose de manière unique comme :
> $$\vec{u} = \alpha\vec{\imath} + \beta\vec{\jmath} + \gamma\vec{k} \qquad (\alpha, \beta, \gamma \in \mathbb{R})$$

<u>**Exemple !**</u>

**a)** $\vec{AI}$ en fonction de $\vec{AB}$ et $\vec{BC}$ ?

![[g1-milieu-a.svg]]

$$
\begin{aligned}
\vec{AI} &= \vec{AB} + \vec{BI} \\
&= \vec{AB} + \frac{1}{2}\vec{BC}
\end{aligned}
$$

**b)** $\vec{AI}$ en fonction de <u style="text-decoration-color:orange">$\vec{AB}$</u> et <u style="text-decoration-color:cyan">$\vec{AC}$</u>

![[g1-milieu-b.svg]]

$$
\begin{aligned}
\vec{AI} &= \vec{AB} + \frac{1}{2}\boxed{\vec{BC}} \qquad \left(\vec{BC} = \vec{BA} + \vec{AC}\right) \\
&= \vec{AB} + \frac{1}{2}\left(\vec{BA} + \vec{AC}\right) \\
&= \vec{AB} + \frac{1}{2}\vec{BA} + \frac{1}{2}\vec{AC} \\
&= \vec{AB} - \frac{1}{2}\vec{AB} + \frac{1}{2}\vec{AC} \\
&= \frac{1}{2}\vec{AB} + \frac{1}{2}\vec{AC}
\end{aligned}
$$
