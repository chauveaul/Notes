---
cours: Analyse II
chapitre: 1
source: "Chapitre 1 - Analyse II.pdf"
tags: [analyse-II, chapitre-1]
---

# Chapitre 1 : test

### 1.1 Cercle et angles trigo.

Dans un repère orthonormé $\circlearrowleft$, $x, y$, on appelle <u>cercle trigonométrique</u> le cercle de rayon $1$ centré en $O = (0, 0)$

![[an2-1-cercle-trigo.svg]]

Le cercle trigo est séparé en 4 quadrants $\mathrm{I}, \mathrm{II}, \mathrm{III}, \mathrm{IV}$

Un point $P$ sur le cercle se
- représente à l'aide d'un couple $(x, y)$
- représente à l'aide d'un angle trigonométrique $\alpha$

Un angle $\alpha$ a
1) une orientation $\begin{cases} \text{positive (ou trigonométrique)} & \underline{\text{CCW}} \\ \text{négative dans le sens} & \underline{\text{CW}} \end{cases}$
2) une mesure $\begin{cases} \text{en radians} \\ \text{en degrés} \end{cases}$

Le point $P$ est noté $P(\alpha)$ est appelé le <u>point associé à $\alpha$</u>

L'angle mesuré en radians représente la longueur, avec un signe, de l'arc de cercle reliant $\vec{i}\,(1, 0)$ à $P(\alpha) = (x, y)$

![[an2-1-longueur-arc.svg]]

Le radian donne un lien entre la droite $\mathbb{R}$ et le cercle

![[an2-1-droite-cercle.svg]]

<u>**Quelques exemples**</u>

| | | |
| :-- | :-: | :-- |
| ① tour complet | ![[an2-1-tour-complet.svg\|200]] | <span style="color:magenta">$2\pi = 360°$</span><br><span style="color:cyan">$-2\pi = -360°$</span> |
| ② Demi tour | ![[an2-1-demi-tour.svg\|200]] | <span style="color:magenta">$\pi = 180°$</span><br><span style="color:cyan">$-\pi = -180°$</span> |
| ③ Quart de tour | ![[an2-1-quart-tour.svg\|200]] | <span style="color:magenta">$\frac{\pi}{2} = 90°$</span><br><span style="color:cyan">$-\frac{\pi}{2} = -90°$</span> |
| ④ 8<sup>ème</sup> de tour | ![[an2-1-huitieme-tour.svg\|200]] | <span style="color:magenta">$\pi/4 = 45°$</span><br><span style="color:cyan">$-\pi/4 = -45°$</span> |

On observe qu'un point $P$ sur le cercle peut se représenter avec une infinité d'angles différents

![[an2-1-infinite-angles.svg]]

$$P = P(\alpha) = \color{magenta}{P(\alpha + 2\pi)} = \color{cyan}{P(-2\pi + \alpha)}$$

On observe que $\forall k \in \mathbb{Z}$, $P(\alpha + k2\pi) = P(\alpha)$

autrement dit,

> [!important]
> $$P(\alpha) = P(\beta) \iff \alpha = \beta + k2\pi \iff \alpha - \beta = k2\pi$$

<u>**exemple ①**</u>

Soit $\alpha = \dfrac{9\pi}{4}$. Vérifions $P(\alpha) = P\left(\dfrac{\pi}{4}\right)$

![[an2-1-9pi-4.svg]]

$$P\left(\frac{\pi}{4}\right) = P\left(\frac{9\pi}{4}\right) = P\left(2\pi + \frac{\pi}{4}\right)$$

en effet, $\dfrac{9\pi}{4} = \dfrac{8\pi}{4} + \dfrac{\pi}{4} = \underline{2\pi} + \dfrac{\pi}{4}$

<u>**Terminologie**</u>

On dit que $\dfrac{\pi}{4}$ et $\dfrac{9\pi}{4}$ sont deux <u>déterminations</u> du même point $P$

$$\left.\begin{aligned} \frac{\pi}{4} &\in [0, 2\pi] \\ \frac{9\pi}{4} &\in [2\pi, 4\pi] \end{aligned}\right\} \ \underline{\text{déterminations}}$$

<u>Question :</u> Comment représenter $P\left(\frac{\pi}{4}\right)$ avec un angle $\alpha \in [-2\pi, 0]$
$$\alpha = -\frac{7\pi}{4}$$

<u>**Symétrie du cercle**</u>

① placer $P(-\alpha)$ à partir de $P(\alpha)$

![[an2-1-sym-horizontale.svg]]

$\left.\begin{aligned} P(\alpha) &= (x, y) \\ \color{magenta}{P(-\alpha)} &\color{magenta}{= (x, -y)} \end{aligned}\right\}$ Symétrie horizontale

② placer $P(\pi - \alpha)$ par rapport à $P(\alpha)$

![[an2-1-sym-verticale.svg]]

$\left.\begin{aligned} \color{magenta}{P(\pi - \alpha)} &\color{magenta}{= (-x, y)} \\ P(\alpha) &= (x, y) \end{aligned}\right\}$ Symétrie verticale

③ Placer $P(\alpha + \pi)$ à partir de $P(\alpha)$

![[an2-1-sym-centrale.svg]]

$\left.\begin{aligned} P(\alpha) &= (x, y) \\ \color{magenta}{P(\alpha + \pi)} &\color{magenta}{= (-x, -y)} \end{aligned}\right\}$ Symétrie centrale

<u>**exemple ②**</u> : à partir de $P\left(\frac{\pi}{4}\right)$ plaçons <span style="color:magenta">$P\left(-\frac{\pi}{4}\right)$</span>, <span style="color:cyan">$P\left(\frac{3\pi}{4}\right)$</span>, <span style="color:orange">$P\left(\frac{5\pi}{4}\right)$</span>

![[an2-1-exemple-pi-4.svg]]

<u>**exemple ③**</u> plaçons $P\left(\frac{\pi}{3}\right)$ et <span style="color:magenta">$P\left(\frac{\pi}{6}\right)$</span> et tous les points correspondants dans $\mathrm{II}, \mathrm{III}, \mathrm{IV}$

![[an2-1-exemple-pi-3-pi-6.svg]]

<u>**exemple ④**</u> On considère $P\left(-\frac{\pi}{6}\right)$

Donner $\alpha \in [0, 2\pi]$ tel que $P\left(-\frac{\pi}{6}\right) = P(\alpha)$

![[an2-1-exemple-11pi-6.svg]]

$$\color{magenta}{\alpha = \frac{11\pi}{6}}$$

<u>**exemple ⑤**</u> On considère $P\left(\frac{5\pi}{6}\right)$

donner $\alpha \in [-2\pi, 0]$ tel que $P(\alpha) = P\left(\frac{5\pi}{6}\right)$
et donner $\beta \in [2\pi, 4\pi]$ tel que $P(\beta) = P\left(\frac{5\pi}{6}\right)$

![[an2-1-exemple-5pi-6.svg]]

$$\alpha = -\frac{7\pi}{6} \qquad \beta = \frac{17\pi}{6}$$

<u>**exemple ⑥**</u> Soit la famille d'angles $\alpha = \dfrac{\pi}{3} + k\pi$, $k \in \mathbb{Z}$

dessiner les points associés à $P(\alpha)$ pour $\forall \alpha$

![[an2-1-exemple-famille.svg]]

<u>**Un peu de géométrie dans des cercles de rayon $R$ quelconque.**</u>

① Longueur d'arc

$$\color{magenta}{L = \alpha \cdot R \ \text{(radians)}}$$

![[an2-1-arc-R.svg]]

② Calculer l'aire d'un secteur

$$
\begin{aligned}
A &= 2\pi \longleftrightarrow \pi R^2 \\
A &= \alpha \longleftrightarrow \frac{\alpha}{2}R^2
\end{aligned}
$$

![[an2-1-secteur-R.svg]]

---

### 1.2 Fonctions trigo

> [!definition] Déf (cosinus et sinus)
> Soit un angle $\alpha \in \mathbb{R}$ et on considère $P(\alpha)$ son point associé
>
> On appelle <u>cosinus</u> de $\alpha$, noté $\cos(\alpha)$, l'abscisse de $P(\alpha)$ $\quad (\cos\alpha = x)$
>
> On appelle <u>sinus</u> de $\alpha$, noté $\sin(\alpha)$, l'ordonnée de $P(\alpha)$ $\quad \sin\alpha = y$

On a ainsi défini 2 fonctions :
$$\cos : \mathbb{R} \to [-1, 1] \quad \text{et} \quad \sin : \mathbb{R} \to [-1, 1]$$

<u>**Propriétés :**</u>

① 
- $P(\alpha) \in \mathrm{I}$, $\cos\alpha \geq 0$ et $\sin\alpha \geq 0$
- $P(\alpha) \in \mathrm{II}$, $\cos\alpha \leq 0$ et $\sin\alpha \geq 0$
- $P(\alpha) \in \mathrm{III}$, $\cos\alpha \leq 0$ et $\sin\alpha \leq 0$
- $P(\alpha) \in \mathrm{IV}$, $\cos\alpha \geq 0$ et $\sin\alpha \leq 0$

② Quelques valeurs

![[an2-1-valeurs-remarquables.svg]]

> $$
> \begin{aligned}
> \cos 0 &= \cos 2\pi = 1 & \sin 0 &= \sin 2\pi = 0 \\
> \cos\frac{\pi}{2} &= \cos\frac{3\pi}{2} = 0 \\
> \sin\frac{\pi}{2} &= 1 & \sin\frac{3\pi}{2} &= -1 \\
> \cos\pi &= -1 & \sin\pi &= 0
> \end{aligned}
> $$

③ <u>Périodicité</u>

> [!important]
> $\forall \alpha \in \mathbb{R}, \ \forall k \in \mathbb{Z}$
> $$\cos(\alpha + k2\pi) = \cos(\alpha) \qquad \sin(\alpha + k2\pi) = \sin(\alpha)$$

On dit que $\cos$ et $\sin$ sont <span style="color:red">périodiques</span> de période $2\pi$

④ <u>Symétries</u>

- **angles opposés**

  ![[an2-1-angles-opposes.svg]]

  > [!important]
  > $$\cos(-\alpha) = \cos\alpha \qquad \sin(-\alpha) = -\sin\alpha$$

  $P(\alpha) = (\cos\alpha, \sin\alpha)$
  $P(-\alpha) = \big(\cos(-\alpha), \sin(-\alpha)\big) = \big(\cos(\alpha), -\sin(\alpha)\big)$

- **angles supplémentaires**

  ![[an2-1-angles-supplementaires.svg]]

  > [!important]
  > $$\cos(\pi - \alpha) = -\cos(\alpha) \qquad \sin(\pi - \alpha) = \sin(\alpha)$$

- **angles diamétralement opposés**

  ![[an2-1-angles-diametralement-opposes.svg]]

  > [!important]
  > $$\cos(\alpha + \pi) = -\cos\alpha \qquad \sin(\alpha + \pi) = -\sin\alpha$$

- **angles complémentaires**

  ![[an2-1-angles-complementaires.svg]]

  > [!important]
  > $$\cos\left(\frac{\pi}{2} - \alpha\right) = \sin\alpha \qquad \sin\left(\frac{\pi}{2} - \alpha\right) = \cos\alpha$$

⑤ Par Pythagore

![[an2-1-pythagore.svg]]

> [!important]
> $$\color{red}{\cos^2\alpha} + \color{cyan}{\sin^2\alpha} = 1$$

> [!definition] Déf : tangente et cotangente
> On considère la droite <span style="color:cyan">$i$</span> tangente au cercle et qui passe par $I$ et la droite <span style="color:red">$j$</span> tangente qui passe par $J$

![[an2-1-tangente-cotangente.svg]]

On considère l'intersection du rayon avec <span style="color:cyan">$i$</span> et <span style="color:red">$j$</span> et on obtient <span style="color:cyan">$T(\alpha)$</span> et <span style="color:red">$T'(\alpha)$</span>

On considère tangente, noté $\tan(\alpha)$, l'ordonnée de <span style="color:cyan">$T(\alpha)$</span> et cotangente, noté $\cot(\alpha)$, l'abscisse de <span style="color:red">$T'(\alpha)$</span>

<u>**Propriétés**</u>

① Domaine de définition
$$D_{\tan} = \mathbb{R} \setminus \left\{\frac{\pi}{2} + k\pi, \ k \in \mathbb{Z}\right\} \qquad \tan : D_{\tan} \to \mathbb{R}$$
$$D_{\cot} = \mathbb{R} \setminus \{k\pi, \ k \in \mathbb{Z}\} \qquad \cot : D_{\cot} \to \mathbb{R}$$

②
- $P(\alpha) \in \mathrm{I}$, $\tan(\alpha) \geq 0 \quad \cot(\alpha) \geq 0$
- $P(\alpha) \in \mathrm{II}$, $\tan(\alpha) \leq 0 \quad \cot(\alpha) \leq 0$
- $P(\alpha) \in \mathrm{III}$, $\tan(\alpha) \geq 0 \quad \cot(\alpha) \geq 0$
- $P(\alpha) \in \mathrm{IV}$, $\tan(\alpha) \leq 0 \quad \cot(\alpha) \leq 0$

③ Périodicité

$\forall \alpha \in \mathbb{R}, \ \forall k \in \mathbb{Z}$

> [!important]
> $$\tan(\alpha + k\pi) = \tan(\alpha) \qquad \cot(\alpha + k\pi) = \cot(\alpha)$$
> $\pi$-périodicité

![[an2-1-tan-cot-points.svg]]

<u>**Quelques conséquences de Thalès**</u>

![[an2-1-thales-tan.svg]]

$(\alpha \neq \frac{\pi}{2} + k\pi)$

> [!important] Par Thalès
> $$\tan\alpha = \frac{\tan\alpha}{1} = \frac{\sin\alpha}{\cos\alpha}$$
> $$\cot\alpha = \frac{\cos\alpha}{\sin\alpha} \quad (\alpha \neq k\pi)$$

Une autre conséquence : calcul du cosinus et du sinus

![[an2-1-triangle-ABC.svg]]

$$
\begin{aligned}
\cos\alpha &= \frac{\cos\alpha}{1} = \frac{AB}{AC} = \frac{\text{adjacent}}{\text{hypothénuse}} \\
\sin\alpha &= \frac{\sin\alpha}{1} = \frac{BC}{AC} = \frac{\text{opposé}}{\text{hypothénuse}} \\
\tan\alpha &= \frac{\sin\alpha}{\cos\alpha} = \frac{BC}{AB} = \frac{\text{opposé}}{\text{adjacent}}
\end{aligned}
$$

<u>**Calculons des valeurs remarquables**</u>

① le $\cos$, $\sin$ et $\tan$ de $\frac{\pi}{4}$

![[an2-1-carre-pi-4.svg]]

$$\cos\frac{\pi}{4} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2} \qquad \sin\frac{\pi}{4} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2} \qquad \tan\frac{\pi}{4} = 1 = \cot\frac{\pi}{4}$$

② les angles $\frac{\pi}{3}$, $\frac{\pi}{6}$

![[an2-1-triangle-pi-3.svg]]

$$\cos\frac{\pi}{3} = \frac{1}{2} \qquad \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2} \qquad \cos\frac{\pi}{6} = \frac{\sqrt{3}}{2} \qquad \sin\frac{\pi}{6} = \frac{1}{2}$$

<u>**Tableau**</u>

> [!important]
> | | $0$ | $\frac{\pi}{6}$ | $\frac{\pi}{4}$ | $\frac{\pi}{3}$ | $\frac{\pi}{2}$ |
> | :-: | :-: | :-: | :-: | :-: | :-: |
> | $\cos$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |
> | $\sin$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
> | $\tan$ | $0$ | $\frac{1}{\sqrt{3}}$ | $1$ | $\sqrt{3}$ | $/\!/\!/$ |
> | $\cot$ | $/\!/\!/$ | $\sqrt{3}$ | $1$ | $\frac{1}{\sqrt{3}}$ | $0$ |

![[an2-1-quart-cercle-valeurs.svg]]

<u>**exemple (exo 1.a)**</u>

Calculer
$$\cos\left(\frac{47\pi}{3}\right) = \cos\left(\frac{48\pi}{3} - \frac{\pi}{3}\right) = \cos\Big(\underbrace{16\pi}_{8 \cdot 2\pi} - \frac{\pi}{3}\Big)$$
$$\cos(-\pi/3) = \cos(\pi/3) = \frac{1}{2}$$

<u>**exemple (exo 2)**</u>

Donner la valeur de $\sin(x)$ sachant que $\cos x = \frac{5}{13}$ et $\frac{15\pi}{2} \leq x \leq 8\pi$

<u>étape 1</u> : localisation avec dessin

![[an2-1-exo2-localisation.svg]]

$$P(x) \in (\mathrm{IV}) \implies \begin{aligned} \cos x &\geq 0 \\ \cos x &= 5/13 \end{aligned} \qquad \implies \sin x \leq 0$$

<u>étape 2</u> : Pythagore
$$
\begin{aligned}
\sin^2 x + \cos^2 x &= 1 \\
\sin^2 x &= 1 - \cos^2 x \\
\sin x &= \pm\sqrt{1 - \cos^2 x} \\
\sin x &= \pm\sqrt{1 - \frac{25}{169}} \\
\sin x &= \pm\sqrt{\frac{144}{169}} = \pm\frac{12}{13} \underset{\sin x \leq 0}{=} -\frac{12}{13}
\end{aligned}
$$

<u>**exemple ③ (exo 2)**</u>

Calculer $\cos x$, $\sin x$ et $\tan x$ sachant que $\tan x = \pm\frac{5}{12}$ et $-\frac{7\pi}{2} \leq x \leq -3\pi$

<u>étape 1</u> localiser

![[an2-1-exo2-ex3-localisation.svg]]

$$P(x) \in \mathrm{II} \qquad \tan x = -\frac{5}{12}$$

<u>étape 2</u> par Thalès

![[an2-1-triangle-5-12-13.svg]]

$$\implies \cos x = \pm\frac{12}{13} \qquad \sin x = \pm\frac{5}{13}$$

$$\underbrace{P(x) \in \mathrm{II}} \qquad \cos x = -\frac{12}{13} \qquad \sin x = +\frac{5}{13}$$

---

### 1.3 Équations élémentaires

<u>Résoudre $\cos x = a$</u>
- $D_{déf} = \mathbb{R}$
- l'équation n'a de solutions que si $a \in [-1, 1]$

<u>Méthode</u>
1) On choisit $\alpha \in \mathbb{R}$ tel que $\cos\alpha = a$ (par exemple parmi les valeurs remarquables)
2) On résout l'égalité $\cos x = \cos\alpha$ avec l'équivalence

> [!important]
> $$\cos x = \cos\alpha \iff \begin{cases} x = \alpha + k2\pi \\ \text{ou} \\ x = -\alpha + k2\pi \end{cases} \qquad k \in \mathbb{Z}$$

![[an2-1-equation-cos.svg]]

<u>**exemple ①**</u> résoudre $\cos x = \frac{1}{2}$

<u>étape 1</u> on choisit $\alpha = \frac{\pi}{3}$

<u>étape 2</u> on résout $\cos x = \cos\frac{\pi}{3} \iff \begin{cases} \pi/3 + k2\pi \\ -\pi/3 + k2\pi \end{cases} \quad k \in \mathbb{Z}$
$$\iff S = \left\{\pm\frac{\pi}{3} + k2\pi, \ k \in \mathbb{Z}\right\}$$

<u>**exemple ②**</u> résoudre $\cos(2x) = \frac{1}{2}$

<u>étape 1</u> on choisit $\alpha =$ tel que $\cos\alpha = \frac{1}{2}$

<u>étape 2</u> On résout $\cos 2x = \cos\frac{\pi}{3}$
- on pose $y = 2x$ <span style="color:magenta">→ Changement de variable</span>
  et on résout $\cos(y) = \cos\pi/3$
  $$\iff y = \pm\frac{\pi}{3} + k2\pi$$
- on rechange $y$ par $2x$, on a
  $$2x = \pm\frac{\pi}{3} + k2\pi \iff x = \pm\frac{\pi}{6} + k\pi$$

$$S = \left\{\pm\frac{\pi}{6} + k\pi, \ k \in \mathbb{Z}\right\}$$

![[an2-1-cos2x.svg]]

<u>**exemple ③**</u> résoudre $\cos\left(3x + \frac{\pi}{4}\right) = \frac{\sqrt{2}}{2}$

<u>étape 1</u> On choisit $\alpha$ tel que $\cos\alpha = \frac{\sqrt{2}}{2}$, par ex. $\alpha = \frac{\pi}{4}$

<u>étape 2</u> on pose $y = 3x + \frac{\pi}{4}$
$$\cos y = \cos\left(\frac{\pi}{4}\right) \iff \begin{cases} y = \frac{\pi}{4} + k2\pi \\ y = -\frac{\pi}{4} + k2\pi \end{cases}$$

Donc on a
$$3x + \frac{\pi}{4} = \frac{\pi}{4} + k2\pi \quad \text{ou} \quad 3x + \frac{\pi}{4} = -\frac{\pi}{4} + k2\pi$$
$$\iff 3x = k2\pi \quad \text{ou} \quad 3x = -\frac{\pi}{2} + k2\pi$$
$$\iff x = k\frac{2\pi}{3} \quad \text{ou} \quad x = -\frac{\pi}{6} + k\frac{2\pi}{3} \qquad (k \in \mathbb{Z})$$

![[an2-1-cos3x.svg]]

<u>Résoudre $\sin x = a$</u>
- $D_{déf} = \mathbb{R}$
- l'équation n'a de solutions que si $a \in [-1, 1]$

<u>Méthode</u>
1) On cherche $\alpha$ tel que $\sin\alpha = a$
2) On résout l'égalité en $\sin$

> [!important]
> $$\sin x = \sin\alpha \iff \begin{cases} x = \alpha + k2\pi \\ x = \pi - \alpha + k2\pi \end{cases}$$

![[an2-1-equation-sin.svg]]

<u>**Exemple ④**</u> Résoudre $\sin(2x) = \frac{\sqrt{3}}{2}$

1) On choisit $\alpha$ tel que $\sin\alpha = \frac{\sqrt{3}}{2}$, $\ \alpha = \frac{\pi}{3}$
2) $y = 2x$
$$\sin y = \sin\pi/3 \iff \begin{cases} y = \pi/3 + k2\pi \\ \text{ou} \\ y = \pi - \pi/3 + k2\pi = 2\pi/3 + k2\pi \end{cases}$$
$$2x = \frac{\pi}{3} + k2\pi \quad \text{ou} \quad 2x = \frac{2\pi}{3} + k2\pi$$
$$\underline{x = +\frac{\pi}{6} + k\pi} \quad \text{ou} \quad x = \frac{\pi}{3} + k\pi$$
$$S = \left\{\frac{\pi}{6} + k\pi, \ \frac{\pi}{3} + k\pi, \ k \in \mathbb{Z}\right\}$$

<u>**exemple ⑤**</u> Résoudre $\sin\left(2x - \frac{\pi}{4}\right) = 1$ et $\underbrace{x \in [\pi, 2\pi]}_{\text{localisation}}$

1) Résout sans localisation
$$\sin\left(2x - \frac{\pi}{4}\right) = 1 \iff \sin\left(2x - \frac{\pi}{4}\right) = \sin\left(\frac{\pi}{2}\right)$$
$$\iff 2x - \frac{\pi}{4} = \frac{\pi}{2} + k2\pi \quad \text{ou} \quad 2x - \frac{\pi}{4} = \pi - \frac{\pi}{2} + k2\pi$$
$$\iff 2x - \frac{\pi}{4} = \frac{\pi}{2} + k2\pi$$
$$x = \frac{3\pi}{8} + k\pi$$

2) on localise avec dessin

![[an2-1-ex5-localisation.svg]]

1. On place les points solutions avec des angles standards
2. on identifie la zone correspondant à $[\pi, 2\pi]$
3. On garde les points dans la zone
4. On exprime les angles des points conservés à 3) avec des valeurs entre $\pi$ et $2\pi$

<u>Conclusion :</u> il y a une seule solution
$$x = \frac{11\pi}{8}$$

<u>**exemple ⑥**</u> Résoudre $\sin\left(2x - \frac{\pi}{4}\right) = 1$ et $x \in [-\pi, 0]$

<u>étape 1</u> on a $x = \frac{3\pi}{8} + k\pi$, $k \in \mathbb{Z}$

<u>étape 2</u> on localise

![[an2-1-ex6-localisation.svg]]

$$\frac{11\pi}{8} \in [\pi, 2\pi] \qquad -\frac{5\pi}{8} \in [-\pi, 0]$$

<u>Conclusion :</u> $x = -\dfrac{5\pi}{8}$

<u>**exemple ⑦**</u> résoudre $\sin(2x) \geq \frac{1}{2}$ et $x \in [2\pi, 3\pi]$

<u>étape 1</u> Sans localisation, avec un dessin

![[an2-1-ex7-etape1.svg]]

On pose $y = 2x$ et on résout $\sin(y) \geq \frac{1}{2}$
$$k2\pi + \frac{\pi}{6} \leq y \leq \frac{5\pi}{6} + k2\pi$$
$$\iff \frac{\pi}{12} + k\pi \leq y \leq \frac{5\pi}{12} + k\pi, \quad k \in \mathbb{Z}$$

<u>étape 2</u> on localise avec un dessin

![[an2-1-ex7-etape2.svg]]

$$S = \underline{x \in \left[\frac{25\pi}{12}, \frac{29\pi}{12}\right]}$$

<u>Résoudre $\tan x = a$ / $\cot x = a$</u>

| $\tan x = a$ | $\cot x = a$ |
| :-- | :-- |
| $D_{déf} = \mathbb{R} \setminus \left\{\frac{\pi}{2} + k\pi, \ k \in \mathbb{Z}\right\}$, $\ a \in \mathbb{R}$ | $D_{déf} = \mathbb{R} \setminus \{k\pi, \ k \in \mathbb{Z}\}$, $\ a \in \mathbb{R}$ |
| 1) Choisir $\alpha$ tel que $\tan\alpha = a$ | 1) Choisir $\alpha$ tel que $\cot\alpha = a$ |
| 2) $\boxed{\tan x = \tan\alpha \iff x = \alpha + k\pi}$ | 2) $\boxed{\cot x = \cot\alpha \iff x = \alpha + k\pi}$ |

![[an2-1-equation-tan-cot.svg]]

<u>**exemple ⑧**</u> résoudre $\tan x \geq -\frac{\sqrt{3}}{3}$ et $x \in [0, 2\pi]$

<u>étape 1</u> avec un dessin sans localisation

$$-\frac{\pi}{6} + k\pi \leq x < \frac{\pi}{2} + k\pi$$

![[an2-1-ex8-etape1.svg]]

<u>étape 2</u> on localise avec un dessin

<u>Stratégie :</u> on tourne de $0$ à $2\pi$ et on exprime chaque morceau capturé ainsi avec des angles entre $0$ et $2\pi$

![[an2-1-ex8-etape2.svg]]

$$S = \left[0, \frac{\pi}{2}\right[ \ \cup \ \left[\frac{5\pi}{6}, \frac{3\pi}{2}\right[ \ \cup \ \left[\frac{11\pi}{6}, 2\pi\right]$$

---

### 1.4 Formules trigonométriques

<u>But :</u> obtenir des formules pour $\cos(\alpha + \beta)$, $\sin(\alpha + \beta)$, $\cos(\alpha) + \cos(\beta)$, $\cos(\alpha) + \sin(\beta)$

① <u>Formules d'addition</u> $\big(\cos(\alpha + \beta), \sin(\alpha + \beta), \tan(\alpha + \beta)\big)$

![[an2-1-formule-addition.svg]]

$$
\begin{aligned}
P &= \big(\cos(\alpha), \sin(\alpha)\big) \\
P' &= \big(\cos(\alpha + \beta), \sin(\alpha + \beta)\big) \\
\vec{OP} &= \cos(\alpha)\,\vec{OI} + \sin(\alpha)\,\vec{OJ} \\
\vec{OP'} &= \cos(\alpha + \beta)\,\vec{OI} + \sin(\alpha + \beta)\,\vec{OJ}
\end{aligned}
$$

$$
\begin{aligned}
\vec{OP'} &= \cos(\alpha)\,\vec{OI'} + \sin(\alpha)\,\vec{OJ'} \\
\vec{OI'} &= \cos\beta\,\vec{OI} + \sin\beta\,\vec{OJ} \\
\vec{OJ'} &= \cos\left(\frac{\pi}{2} + \beta\right)\vec{OI} + \sin\left(\frac{\pi}{2} + \beta\right)\vec{OJ} \\
&= -\sin(\beta)\,\vec{OI} + \cos(\beta)\,\vec{OJ} \\
\vec{OP'} &= \cos(\alpha)\big(\cos\beta\,\vec{OI} + \sin\beta\,\vec{OJ}\big) + \sin\alpha\big(-\sin\beta\,\vec{OI} + \cos\beta\,\vec{OJ}\big) \\
\vec{OP'} &= [\cos\alpha\cos\beta - \sin\alpha\sin\beta]\,\vec{OI} + [\cos\alpha\sin\beta + \sin\alpha\cos\beta]\,\vec{OJ}
\end{aligned}
$$

Donc forcément on doit avoir

> [!important]
> $$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$
> $$\sin(\alpha + \beta) = \cos\alpha\sin\beta + \sin\alpha\cos\beta$$

② <u>Formule de soustraction</u>

Si on remplace $\beta$ par $-\beta$ et qu'on utilise le fait que $\alpha - \beta = \alpha + (-\beta)$, on a

> [!important]
> $$
> \begin{aligned}
> \cos(\alpha - \beta) &= \cos\big(\alpha + (-\beta)\big) = \cos\alpha\cos(-\beta) - \sin\alpha\sin(-\beta) \\
> &= \cos\alpha\cos\beta + \sin\alpha\sin\beta \\
> \sin(\alpha - \beta) &= \sin\big(\alpha + (-\beta)\big) = \cos\alpha\sin(-\beta) + \sin\alpha\cos(-\beta) \\
> &= -\cos\alpha\sin\beta + \sin\alpha\cos\beta
> \end{aligned}
> $$

<u>Pour la tangente</u> (là où c'est fini)
$$\tan(\alpha + \beta) = \frac{\sin(\alpha + \beta)}{\cos(\alpha + \beta)} = \frac{\sin\alpha\cos\beta + \cos\alpha\sin\beta}{\cos\alpha\cos\beta - \sin\alpha\sin\beta}$$
$$= \frac{\dfrac{\sin\alpha\cos\beta + \cos\alpha\sin\beta}{\cos\alpha\cos\beta}}{\dfrac{\cos\alpha\cos\beta - \sin\alpha\sin\beta}{\cos\alpha\cos\beta}} = \frac{\tan\alpha + \tan\beta}{1 - \tan\alpha\tan\beta}$$

$$\tan(\alpha - \beta) = \frac{\tan\alpha - \tan\beta}{1 + \tan\alpha\tan\beta}$$

<u>**exemple (exo 1)**</u>

Calculer $\cos\left(\frac{7\pi}{12}\right)$
$$
\begin{aligned}
\cos\left(\frac{7\pi}{12}\right) = \cos\left(\frac{\pi}{4} + \frac{\pi}{3}\right) &= \cos\frac{\pi}{4}\cos\frac{\pi}{3} - \sin\frac{\pi}{4}\sin\frac{\pi}{3} \\
&= \frac{\sqrt{2}}{2} \cdot \frac{1}{2} - \frac{\sqrt{2}}{2}\frac{\sqrt{3}}{2} \\
&= \frac{\sqrt{2}}{4}\big(1 - \sqrt{3}\big)
\end{aligned}
$$

③ <u>Formules de duplication</u>

On pose $\alpha = \beta$ dans les formules d'addition,

> [!important] on trouve :
> $$
> \begin{aligned}
> \cos(2\alpha) &= \cos(\alpha + \alpha) = \cos^2(\alpha) - \sin^2(\alpha) \\
> &= 1 - 2\sin^2\alpha = 2\cos^2\alpha - 1 \\
> \sin(2\alpha) &= \sin(\alpha + \alpha) = \sin\alpha\cos\alpha + \sin\alpha\cos\alpha \\
> &= 2\sin\alpha\cos\alpha \\
> \tan(2\alpha) &= \frac{2\tan(\alpha)}{1 - \tan^2(\alpha)}
> \end{aligned}
> $$

④ <u>Formule de bissection</u>

On a $\forall \beta \quad \cos(2\beta) = 1 - 2\sin^2(\beta) = 2\cos^2(\beta) - 1$

posons $\beta = \frac{\alpha}{2}$

$$\cos\alpha = 1 - 2\sin^2\frac{\alpha}{2} \implies \boxed{\sin\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \cos\alpha}{2}}}$$
$$\cos\alpha = 2\cos^2\frac{\alpha}{2} - 1 \implies \boxed{\cos\frac{\alpha}{2} = \pm\sqrt{\frac{1 + \cos\alpha}{2}}}$$

$$\boxed{\tan\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \cos\alpha}{1 + \cos\alpha}}}$$

<u>**exemple (exo 3)**</u>

Calculer $\cos\frac{\alpha}{2}$ et $\sin\frac{\alpha}{2}$ sachant $\sin\alpha = \frac{-2\sqrt{2}}{3}$ et $\alpha \in \left[\frac{\pi}{2}, \frac{3\pi}{2}\right]$

<u>1<sup>ère</sup> étape</u> on calcule $\cos\alpha$
$$\cos\alpha = \pm\sqrt{1 - \sin^2\alpha} = \pm\sqrt{1 - 8/9} = \pm 1/3$$

de plus $\alpha \in \left[\frac{\pi}{2}, \frac{3\pi}{2}\right]$, $P(\alpha) \in \mathrm{II} \cup \mathrm{III}$
$$\implies \cos\alpha < 0 \implies \cos\alpha = -\frac{1}{3}$$

<u>2<sup>e</sup> étape</u>
$$\cos\frac{\alpha}{2} = \pm\sqrt{\frac{1 - \frac{1}{3}}{2}} = \pm\sqrt{\frac{1}{3}} \qquad \sin\frac{\alpha}{2} = \pm\sqrt{\frac{1 + \frac{1}{3}}{2}} = \pm\sqrt{\frac{2}{3}}$$

On localise $P\left(\frac{\alpha}{2}\right)$

<u>1<sup>er</sup> essai</u>
$$\alpha \in \left[\frac{\pi}{2}, \frac{3\pi}{2}\right] \implies \frac{\alpha}{2} \in \left[\frac{\pi}{4}, \frac{3\pi}{4}\right]$$
$$\implies \sin\frac{\alpha}{2} \geq 0 \quad \text{car } P(\alpha) \in \mathrm{I}, \mathrm{II}$$
$$\sin\frac{\alpha}{2} = +\frac{\sqrt{2}}{2}$$

<u>2<sup>e</sup> essai</u> $\quad \alpha \in \left[\frac{\pi}{2}, \frac{3\pi}{2}\right]$ et $\sin\alpha \leq 0$
$$\implies \alpha \in \left[\pi, \frac{3\pi}{2}\right]$$
donc $\frac{\alpha}{2} \in \left[\frac{\pi}{2}, \frac{3\pi}{4}\right] \implies P\left(\frac{\alpha}{2}\right) \in \mathrm{II}$

donc $\cos\frac{\alpha}{2} \leq 0$ et donc $\cos\frac{\alpha}{2} = -\frac{1}{\sqrt{3}}$

⑤ <u>Transformations sommes-produits</u>

> [!important]
> $$\cos(\alpha + \beta) + \cos(\alpha - \beta) = 2\cos\alpha\cos\beta$$
> $$\cos(\alpha + \beta) - \cos(\alpha - \beta) = -2\sin\alpha\sin\beta$$

$$
\begin{aligned}
\sin(\alpha + \beta) &= \sin\alpha\cos\beta + \cos\alpha\sin\beta \\
\sin(\alpha - \beta) &= \sin\alpha\cos\beta - \cos\alpha\sin\beta
\end{aligned}
$$

> [!important]
> $$\sin(\alpha + \beta) + \sin(\alpha - \beta) = 2\sin\alpha\cos\beta$$
> $$\sin(\alpha + \beta) - \sin(\alpha - \beta) = 2\cos\alpha\sin\beta$$

Si on pose $\alpha = \dfrac{p + q}{2} \qquad \beta = \dfrac{p - q}{2}$

> [!important]
> $$
> \begin{aligned}
> \cos p + \cos q &= 2\cos\left(\frac{p + q}{2}\right)\cos\left(\frac{p - q}{2}\right) \\
> \cos p - \cos q &= -2\sin\left(\frac{p + q}{2}\right)\sin\left(\frac{p - q}{2}\right) \\
> \sin p + \sin q &= 2\sin\left(\frac{p + q}{2}\right)\cos\left(\frac{p - q}{2}\right) \\
> \sin p - \sin q &= 2\cos\left(\frac{p + q}{2}\right)\sin\left(\frac{p - q}{2}\right)
> \end{aligned}
> $$

<u>**exemple exo 7**</u>

résoudre $\cos x + \cos\left(\frac{\pi}{3} - x\right) = \sin\frac{\pi}{3}$

On applique les transformations sommes-produits
$$\cos x + \cos\left(\frac{\pi}{3} - x\right) = 2\cos\left(\frac{x + \frac{\pi}{3} - x}{2}\right)\cos\left(\frac{x - \frac{\pi}{3} + x}{2}\right)$$

$$2\cos\left(\frac{\pi}{6}\right)\cos\left(x - \frac{\pi}{6}\right) = \sin(\pi/3)$$

$$
\begin{aligned}
&\iff 2\cos\left(x - \frac{\pi}{6}\right) = 1 \qquad \left(\sin\frac{\pi}{3} = \cos\frac{\pi}{6} = \frac{\sqrt{3}}{2}\right) \\
&\iff \cos\left(x - \frac{\pi}{6}\right) = \frac{1}{2} \\
&\iff \cos\left(x - \frac{\pi}{6}\right) = \cos\frac{\pi}{3} \\
&\implies \begin{cases} x - \frac{\pi}{6} = \frac{\pi}{3} + k2\pi \\ x - \frac{\pi}{6} = -\frac{\pi}{3} + k2\pi \end{cases} \\
&\iff x = \frac{\pi}{2} + k2\pi \quad \text{ou} \quad x = -\frac{\pi}{6} + k2\pi, \quad k \in \mathbb{Z}
\end{aligned}
$$

<u>**exemple**</u> résoudre
$$\cos^2\left(\frac{3x}{2}\right) - \frac{1}{2} \geq \frac{\sqrt{3}}{4} \qquad x \in [-2\pi, -\pi]$$

<u>1<sup>ère</sup> étape</u> On résout sans la localisation
$$
\begin{aligned}
&\cos^2\left(\frac{3x}{2}\right) - \frac{1}{2} \geq \frac{\sqrt{3}}{4} \\
&\iff 2\cos^2\left(\frac{3x}{2}\right) - 1 \geq \frac{\sqrt{3}}{2} && \cos(2\alpha) = 2\cos^2(\alpha) - 1, \ \alpha = \frac{3x}{2} \\
&\iff \cos(3x) \geq \frac{\sqrt{3}}{2}
\end{aligned}
$$

![[an2-1-cos3x-inequation.svg]]

$$-\frac{\pi}{6} + k2\pi \leq 3x \leq \frac{\pi}{6} + k2\pi \qquad k \in \mathbb{Z}$$
$$-\frac{\pi}{18} + k\frac{2\pi}{3} \leq x \leq \frac{\pi}{18} + k\frac{2\pi}{3}$$

<u>2<sup>ème</sup> étape</u> on localise

![[an2-1-cos3x-localisation.svg]]

$$\left[-2\pi, -\frac{35\pi}{18}\right] \qquad \left[-\frac{25\pi}{18}, -\frac{23\pi}{18}\right]$$

$$S = \left[-2\pi, -\frac{35\pi}{18}\right] \cup \left[-\frac{25\pi}{18}, -\frac{23\pi}{18}\right]$$

---

### 1.5 Équations trigonométriques

#### 1.5.1 Équations linéaires

<u>But :</u> résoudre
$$a\cos(x) + b\sin(x) = c \qquad (a, b, c \in \mathbb{R})$$

<u>Illustration :</u>

![[an2-1-droite-cercle-lineaire.svg]]

<u>**Exemples de démarrage**</u>

① $\frac{1}{2}\cos x + \frac{\sqrt{3}}{2}\sin x = 1$
$$
\begin{aligned}
&\iff \cos\frac{\pi}{3}\cos x + \sin\frac{\pi}{3}\sin x = 1 \\
&\iff \cos\left(\frac{\pi}{3} - x\right) = 1 \\
&\iff \cos\left(\frac{\pi}{3} - x\right) = \cos(0) \\
&\iff \begin{cases} \frac{\pi}{3} - x = 0 + k2\pi \\ \text{ou} \\ \frac{\pi}{3} - x = -0 + k2\pi \end{cases} \\
&\iff \frac{\pi}{3} - x = k2\pi, \ k \in \mathbb{Z} \\
&\iff x = \frac{\pi}{3} + k2\pi, \ k \in \mathbb{Z}
\end{aligned}
$$

② $\frac{1}{2}\cos x + \frac{\sqrt{3}}{2}\sin x = 1$
$$
\begin{aligned}
&\iff \sin\frac{\pi}{6}\cos x + \cos\frac{\pi}{6}\sin x = 1 \\
&\iff \sin\left(\frac{\pi}{6} + x\right) = 1 \\
&\iff \sin\left(\frac{\pi}{6} + x\right) = \sin\left(\frac{\pi}{2}\right) \\
&\iff \begin{cases} \frac{\pi}{6} + x = \frac{\pi}{2} + k2\pi \\ \text{ou} \\ \frac{\pi}{6} + x = \pi - \frac{\pi}{2} + k2\pi \end{cases} \\
&\iff \frac{\pi}{6} + x = \frac{\pi}{2} + k2\pi \iff x = \frac{\pi}{3} + k2\pi
\end{aligned}
$$

③ $\cos x + \sqrt{3}\sin x = 1$
$$
\begin{aligned}
&\iff \frac{1}{2}\cos x + \frac{\sqrt{3}}{2}\sin x = \frac{1}{2} && \text{normalisation} \to \vec{OP}(x) = \frac{\vec{OP}}{\Vert\vec{OP}\Vert} \\
&\iff \cos\left(\frac{\pi}{3} - x\right) = \frac{1}{2} \\
&\iff \cos\left(\frac{\pi}{3} - x\right) = \cos\left(\frac{\pi}{3}\right) \\
&\iff \begin{cases} \frac{\pi}{3} - x = \frac{\pi}{3} + k2\pi \\ \text{ou} \\ \frac{\pi}{3} - x = -\frac{\pi}{3} + k2\pi \end{cases} \\
&\iff \begin{cases} x = k2\pi \\ \text{ou} \\ x = \frac{2\pi}{3} + k2\pi \end{cases} \qquad k \in \mathbb{Z}
\end{aligned}
$$

<u>**Méthode générale pour résoudre des équations du type**</u>
$$a\cos x + b\sin x = c \qquad (a, b, c \in \mathbb{R})$$

<u>Étape 1</u> : on calcule la « norme » $\sqrt{a^2 + b^2}$

<u>Étape 2</u> : on normalise si norme $\neq 1$
$$a\cos x + b\sin x = c \iff \frac{a}{\sqrt{a^2 + b^2}}\cos x + \frac{b}{\sqrt{a^2 + b^2}}\sin x = \frac{c}{\sqrt{a^2 + b^2}}$$

<u>Étape 3</u> : on vérifie si $\dfrac{c}{\sqrt{a^2 + b^2}} \in [-1, 1]$

Si $\dfrac{c}{\sqrt{a^2 + b^2}} \notin [-1, 1] \qquad S = \varnothing$

<u>Étape 4</u> : (variante cosinus)

on cherche $\alpha$ tel que $\cos\alpha = \dfrac{a}{\sqrt{a^2 + b^2}}$ et $\sin\alpha = \dfrac{b}{\sqrt{a^2 + b^2}}$

on a alors
$$
\begin{aligned}
&a\cos x + b\sin x = c \\
&\iff \cos\alpha\cos x + \sin\alpha\sin x = \frac{c}{\sqrt{a^2 + b^2}} \\
&\iff \cos(\alpha - x) = \cos(\beta) \quad \text{avec } \beta \text{ un angle tel que } \cos\beta = \frac{c}{\sqrt{a^2 + b^2}} \\
&\iff \begin{cases} \alpha - x = \beta + k2\pi \\ \text{ou} \\ \alpha - x = -\beta + k2\pi \end{cases} \\
&\iff \begin{cases} x = \alpha - \beta + k2\pi \\ \text{ou} \\ x = \alpha + \beta + k2\pi \end{cases} \qquad k \in \mathbb{Z}
\end{aligned}
$$

<u>Étape 4</u> : (variante sinus) on cherche $\alpha$ tel que
$$\sin\alpha = \frac{a}{\sqrt{a^2 + b^2}} \quad \text{et} \quad \cos\alpha = \frac{b}{\sqrt{a^2 + b^2}}$$

Donc
$$
\begin{aligned}
&a\cos x + b\sin x = c \\
&\iff \sin\alpha\cos x + \cos\alpha\sin x = \frac{c}{\sqrt{a^2 + b^2}} \\
&\iff \sin(\alpha + x) = \sin(\beta) \quad \text{avec } \beta \text{ un angle tel que } \sin(\beta) = \frac{c}{\sqrt{a^2 + b^2}} \\
&\iff \begin{cases} \alpha + x = \beta + k2\pi \\ \text{ou} \\ \alpha + x = \pi - \beta + k2\pi \end{cases} \\
&\iff \begin{cases} x = \beta - \alpha + k2\pi \\ \text{ou} \\ x = \pi - \beta - \alpha + k2\pi \end{cases} \qquad k \in \mathbb{Z}
\end{aligned}
$$

<u>**Exemple ①**</u> (variante cos)
$$\sqrt{3}\cos x - \sin x = \sqrt{2}$$
$$\iff \frac{\sqrt{3}}{2}\cos x - \frac{1}{2}\sin x = \frac{\sqrt{2}}{2}$$
$$
\begin{aligned}
&\iff \cos\left(\frac{\pi}{6}\right)\cos x - \sin\left(\frac{\pi}{6}\right)\sin x = \frac{\sqrt{2}}{2} \\
&\iff \cos\left(\frac{\pi}{6} + x\right) = \cos\left(\frac{\pi}{4}\right) \\
&\iff \begin{cases} \frac{\pi}{6} + x = \frac{\pi}{4} + k2\pi \\ \text{ou} \\ \frac{\pi}{6} + x = -\frac{\pi}{4} + k2\pi \end{cases} \\
&\iff \begin{cases} x = \frac{\pi}{12} + k2\pi \\ \text{ou} \\ x = -\frac{5\pi}{12} + k2\pi \end{cases} \qquad k \in \mathbb{Z}
\end{aligned}
$$

<u>**Exemple ①**</u> (variante sin)
$$
\begin{aligned}
&\frac{\sqrt{3}}{2}\cos x - \frac{1}{2}\sin x = \frac{\sqrt{2}}{2} \\
&\iff \frac{\sqrt{3}}{2}\cos(-x) + \frac{1}{2}\sin(-x) = \frac{\sqrt{2}}{2} \\
&\iff \sin\left(\frac{\pi}{3}\right)\cos(-x) + \cos\left(\frac{\pi}{3}\right)\sin(-x) = \frac{\sqrt{2}}{2} \\
&\iff \sin\left(\frac{\pi}{3} - x\right) = \frac{\sqrt{2}}{2} \iff \sin\left(\frac{\pi}{3} - x\right) = \sin\left(\frac{\pi}{4}\right) \\
&\iff \begin{cases} \frac{\pi}{3} - x = \frac{\pi}{4} + k2\pi \\ \text{ou} \\ \frac{\pi}{3} - x = \pi - \frac{\pi}{4} + k2\pi \end{cases} \qquad k \in \mathbb{Z} \\
&\iff \begin{cases} x = \frac{\pi}{12} + k2\pi \\ \text{ou} \\ x = -\frac{5\pi}{12} + k2\pi \end{cases}
\end{aligned}
$$

<u>**Exemple ②**</u>
$$
\begin{aligned}
&\cos x + \sin x = \sqrt{3} \\
&\iff \frac{1}{\sqrt{2}}\cos x + \frac{1}{\sqrt{2}}\sin x = \underbrace{\frac{\sqrt{3}}{\sqrt{2}}}_{\frac{\sqrt{3}}{\sqrt{2}} > 1 \ \to \ S = \varnothing}
\end{aligned}
$$

<u>**Exemple ③**</u>

résoudre $2\cos\left(\frac{x}{2}\right) + \sqrt{12}\sin\left(\frac{x}{2}\right) = 2$ et $x \in [3\pi, 5\pi]$
$$
\begin{aligned}
&\iff \frac{1}{2}\cos\left(\frac{x}{2}\right) + \frac{\sqrt{12}}{4}\sin\left(\frac{x}{2}\right) = \frac{1}{2} \\
&\iff \frac{1}{2}\cos\left(\frac{x}{2}\right) + \frac{\sqrt{3}}{2}\sin\left(\frac{x}{2}\right) = \frac{1}{2} \\
&\iff \sin\left(\frac{\pi}{6}\right)\cos\left(\frac{x}{2}\right) + \cos\left(\frac{\pi}{6}\right)\sin\left(\frac{x}{2}\right) = \frac{1}{2} \\
&\iff \sin\left(\frac{\pi}{6} + \frac{x}{2}\right) = \frac{1}{2} \\
&\iff \sin\left(\frac{\pi}{6} + \frac{x}{2}\right) = \sin\left(\frac{\pi}{6}\right) \\
&\iff \begin{cases} \frac{\pi}{6} + \frac{x}{2} = \frac{\pi}{6} + k2\pi \\ \text{ou} \\ \frac{\pi}{6} + \frac{x}{2} = \pi - \frac{\pi}{6} + k2\pi \end{cases} \qquad k \in \mathbb{Z} \\
&\iff \begin{cases} \frac{x}{2} = k2\pi \\ \frac{x}{2} = \frac{2\pi}{3} + k2\pi \end{cases} \iff \begin{cases} x = k4\pi \\ \text{ou} \\ x = \frac{4\pi}{3} + k4\pi \end{cases}
\end{aligned}
$$

$$S = \{4\pi\}$$

<u>**exemple ④**</u>

résoudre $\sin(2x) + \cos(2x) \geq 1$ et $x \in [-2\pi, \pi]$

<u>Étape 1</u> sans localisation
$$
\begin{aligned}
&\sin(2x) + \cos(2x) \geq 1 \\
&\iff \frac{1}{\sqrt{2}}\sin(2x) + \frac{1}{\sqrt{2}}\cos(2x) \geq \frac{1}{\sqrt{2}} \\
&\iff \frac{\sqrt{2}}{2}\sin(2x) + \frac{\sqrt{2}}{2}\cos(2x) \geq \frac{\sqrt{2}}{2} \\
&\phantom{\iff} \sin\frac{\pi}{4}\sin 2x + \cos\frac{\pi}{4}\cos 2x \geq \frac{\sqrt{2}}{2} \\
&\iff \cos\left(\frac{\pi}{4} - 2x\right) \geq \frac{\sqrt{2}}{2} \\
&\iff \cos\left(2x - \frac{\pi}{4}\right) \geq \sqrt{2}/2
\end{aligned}
$$

![[an2-1-ex4-lineaire-etape1.svg]]

$$\iff -\frac{\pi}{4} + k2\pi \leq 2x - \frac{\pi}{4} \leq \frac{\pi}{4} + k2\pi$$
$$x \geq k\pi \quad \text{et} \quad x \leq \frac{\pi}{4} + k\pi$$

<u>Étape 2</u> localise avec un dessin

![[an2-1-ex4-lineaire-etape2.svg]]

$$S = \left[-2\pi, -\frac{7\pi}{4}\right] \cup \left[-\pi, -\frac{3\pi}{4}\right] \cup \left[0, \frac{\pi}{4}\right] \cup \{\pi\}$$

#### 1.5.2 Cas général

<u>exemple introductif :</u>

résoudre $\sin^2(x) + 2\cos(x) - 2 = 0$

<u>Choix 1</u> : on écrit $\cos(x) = \pm\sqrt{1 - \sin^2(x)}$

On résout $\sin^2(x) \pm 2\sqrt{1 - \sin^2(x)} - 2 = 0$

on pose $z = \sin x$ et on résout
$$z^2 \pm 2\sqrt{1 - z^2} - 2 = 0$$

<u>Choix 2</u> : On écrit $\sin^2(x) = 1 - \cos^2(x)$ et on résout
$$
\begin{aligned}
&1 - \cos^2(x) + 2\cos(x) - 2 = 0 \\
&\iff -\cos^2(x) + 2\cos(x) - 1 = 0 \\
&\iff \cos^2(x) - 2\cos(x) + 1 = 0
\end{aligned}
$$

On pose $z = \cos(x)$ et on résout
$$z^2 - 2z + 1 = 0 \iff (z - 1)^2 = 0 \iff z = 1 \iff \cos(x) = 1 \iff x = 2k\pi, \ k \in \mathbb{Z}$$

**A) changement de variable $z = \cos(x)$** (Test de Bioche $x \to -x$)

> Si l'équation ne change pas quand on remplace $x$ par $-x$ on pose $z = \cos(x)$ et on exprime les autres fonctions de $z$
> $$\sin(x) = \sqrt{1 - z^2}, \qquad \tan(x) = \frac{\sqrt{1 - z^2}}{z} \quad (z \neq 0)$$

Résoudre :
$$3\tan^2(x) + 5 = \frac{7}{\cos x}$$

<u>Étape 1</u> : établir le $D_{déf}$ de $f$
$$D_{déf} = \mathbb{R} \setminus \left\{\frac{\pi}{2} + k\pi, \ k \in \mathbb{Z}\right\}$$

<u>Étape 2</u> : On teste un des tests de Bioche
$$
\begin{aligned}
&3\tan^2(-x) + 5 = \frac{7}{\cos(-x)} \\
&\iff 3(-\tan(x))^2 + 5 = \frac{7}{\cos x} \\
&\iff 3\tan^2 x + 5 = \frac{7}{\cos x}
\end{aligned}
$$

<u>Étape 3</u> : Comme l'équation est invariante, quand on remplace $x$ par $-x$, on pose $z = \cos x$ et on réécrit l'équation en termes de $z$
$$
\begin{aligned}
&3\tan^2(x) + 5 = \frac{7}{\cos x} \ \text{ et } x \in D_{déf} \\
&\iff 3\left(\frac{\sqrt{1 - z^2}}{z}\right)^2 + 5 = \frac{7}{z} \ \text{ et } z \neq 0 \\
&\iff 3\,\frac{1 - z^2}{z^2} + 5 = \frac{7}{z} \ \text{ et } z \neq 0 \\
&\iff 3(1 - z^2) + 5z^2 = 7z \ \text{ et } z \neq 0 \\
&\iff 2z^2 - 7z + 3 = 0 \ \text{ et } z \neq 0 \\
&\iff 2\left(z^2 - \frac{7}{2}z + \frac{3}{2}\right) = 0 \ \text{ et } z \neq 0 \\
&\phantom{\iff} 2(z - 3)\left(z - \frac{1}{2}\right) = 0 \ \text{ et } z \neq 0 \\
&\iff z = 3 \ \text{ ou } \ z = 1/2 \\
&\iff \cancel{\cos x = 3} \ \text{ ou } \ \cos x = \frac{1}{2} \\
&\iff \cos x = \frac{1}{2} \\
&\iff x = \pm\frac{\pi}{3} + k2\pi, \ k \in \mathbb{Z}
\end{aligned}
$$

<u>Remarque :</u> en posant $\sin x = \sqrt{1 - z^2} \geq 0$ on cherche les solutions dans les quadrants $\mathrm{I} \cup \mathrm{II}$ et on récupère toutes les solutions qui sont dans $\mathrm{III} \cup \mathrm{IV}$ en résolvant $\cos x = z$

**B) changement $z = \sin(x)$** (test $x \to \pi - x$)

> Si l'équation ne change pas quand on remplace $x$ par $\pi - x$, on pose $z = \sin(x)$ et on écrit
> $$\cos(x) = \sqrt{1 - z^2}, \qquad \tan(x) = \frac{z}{\sqrt{1 - z^2}}$$

<u>Remarque :</u> en posant $\cos(x) = \sqrt{1 - z^2} \geq 0$, on cherche les solutions dans $\mathrm{I} \cup \mathrm{IV}$ et on récupère celles dans $\mathrm{II} \cup \mathrm{III}$ en résolvant $z = \sin x$.

<u>**exemple :**</u> résoudre $\sin(2x) + \cos(x) - 3\tan(x) = 0$

<u>Étape 1</u> : $D_{déf} = \mathbb{R} \setminus \left\{\frac{\pi}{2} + k\pi, \ k \in \mathbb{Z}\right\}$

<u>Étape 2</u> : Bioche : Remplace $x$ par $\pi - x$
$$
\begin{aligned}
&\sin(2(\pi - x)) + \cos(\pi - x) - 3\tan(\pi - x) = 0 \\
&\iff \sin(2\pi - 2x) - \cos(x) + 3\tan(x) = 0 \\
&\iff \sin(-2x) - \cos(x) + 3\tan(x) = 0 \\
&\iff -\sin(2x) - \cos(x) + 3\tan(x) = 0 \\
&\iff \sin(2x) + \cos(x) - 3\tan(x) = 0
\end{aligned}
$$

<u>Étape 3</u> : puisque l'équation est invariante si on remplace $x$ par $\pi - x$, on pose $z = \sin(x)$
$$
\begin{aligned}
&\sin(2x) + \cos(x) - 3\tan(x) = 0 \\
&\iff 2\sin(x)\cos(x) + \cos x - 3\tan x = 0 \ \text{ et } x \in D_{déf} \\
&\iff 2z\sqrt{1 - z^2} + \sqrt{1 - z^2} - 3\frac{z}{\sqrt{1 - z^2}} = 0 \ \text{ et } z \neq \pm 1 \\
&\iff 2z(1 - z^2) + (1 - z^2) - 3z = 0 \ \text{ et } z \neq \pm 1 \\
&\iff -2z^3 - z^2 - z + 1 = 0 \ \text{ et } z \neq \pm 1 \\
&\iff 2z^3 + z^2 + z - 1 = 0 \ \text{ et } z \neq \pm 1 \\
&\iff \left(z - \frac{1}{2}\right)(2z^2 + 2z + 2) = 0 \ \text{ et } z \neq \pm 1
\end{aligned}
$$

$$\Delta = 4 - 4 \cdot 2 \cdot 2 < 0 \to \text{pas de solutions}$$

$$
\begin{aligned}
&\iff z = \frac{1}{2} \iff \sin x = \frac{1}{2} \\
&\iff x = \frac{\pi}{6} + k2\pi \quad \text{ou} \quad x = \frac{5\pi}{6} + k2\pi \qquad k \in \mathbb{Z}
\end{aligned}
$$

> [!tip] Coin astuce
> $$
> \begin{aligned}
> 2z^3 + z^2 + z - 1 &= \left(z - \frac{1}{2}\right)(az^2 + bz + c) \\
> &= az^3 + \left(b - \frac{1}{2}a\right)z^2 + \left(c - \frac{1}{2}b\right)z - \frac{c}{2}
> \end{aligned}
> $$
> $$\iff \begin{cases} 2 = a \\ 1 = b - \frac{1}{2}a \\ 1 = c - \frac{1}{2}b \\ -1 = -\frac{c}{2} \end{cases} \iff \begin{cases} a = 2 \\ b = 2 \\ c = 2 \end{cases}$$

**C) Changement $z = \tan x$** (test $x \to x + \pi$)

> Si l'équation ne change pas quand on remplace $x$ par $x + \pi$, on pose $z = \tan(x)$ et
> $$\sin(x) = \frac{z}{\sqrt{1 + z^2}} \qquad \cos(x) = \frac{1}{\sqrt{1 + z^2}}$$

![[an2-1-triangle-tan.svg]]

⚠️ $z = \tan x$ est défini si $x \neq \frac{\pi}{2} + k\pi$, $k \in \mathbb{Z}$

On doit vérifier à part si $\frac{\pi}{2} + k\pi$ est solution ou non

<u>**exemple :**</u> résoudre $\cot x + 2\sin^2 x - 2 = 0$

<u>Étape 1</u> : $D_{déf} = \mathbb{R} \setminus \{k\pi, \ k \in \mathbb{Z}\}$

<u>Étape 2</u> : Bioche : $x \to \pi + x$
$$
\begin{aligned}
&\cot(x + \pi) + 2\sin^2(x + \pi) - 2 = 0 \\
&\iff \cot(x) + 2(-\sin(x))^2 - 2 = 0 \\
&\iff \cot(x) + 2\sin^2 x - 2 = 0
\end{aligned}
$$

<u>Étape 3</u> : on teste les valeurs $\frac{\pi}{2} + k\pi$, $k \in \mathbb{Z}$
$$\cot\left(\frac{\pi}{2} + k\pi\right) + 2\sin^2\left(\frac{\pi}{2} + k\pi\right) - 2 = 0 + 2 \cdot 1 - 2 = 0$$
donc $\frac{\pi}{2} + k\pi$, $k \in \mathbb{Z}$ est solution

<u>Étape 4</u> : pour $x \neq \frac{\pi}{2} + k\pi$, on pose $z = \tan(x)$
$$
\begin{aligned}
&\cot(x) + 2\sin^2(x) - 2 = 0 \\
&\iff \frac{1}{z} + 2\,\frac{z^2}{1 + z^2} - 2 = 0 \ \text{ et } z \neq 0 \\
&\iff 1 + z^2 + 2z^3 - 2z(1 + z^2) = 0 \ \text{ et } z \neq 0 \\
&\iff z^2 - 2z + 1 = 0 \ \text{ et } z \neq 0 \\
&\iff (z - 1)^2 = 0 \ \text{ et } z \neq 0 \\
&\iff z = 1 \iff \tan x = 1 \\
&\iff x = \frac{\pi}{4} + k\pi, \ k \in \mathbb{Z}
\end{aligned}
$$

donc les solutions sont
$$\underbrace{x = \frac{\pi}{4} + k\pi}_{\text{Étape 4}} \quad \text{ou} \quad \underbrace{x = \frac{\pi}{2} + k\pi}_{\text{Étape 3}}$$

**D) Changement en $\tan\left(\frac{x}{2}\right)$**

> Si aucun test de Bioche ne fonctionne.
>
> On pose $z = \tan\frac{x}{2}$ et on pose
> $$\cos x = \frac{1 - z^2}{1 + z^2}, \qquad \sin x = \frac{2z}{1 + z^2}, \qquad \tan x = \frac{2z}{1 - z^2} \quad (z \neq \pm 1)$$

⚠️ le changement de variable $z = \tan\left(\frac{x}{2}\right)$ n'est défini que pour $x \neq \pi + k2\pi$, $k \in \mathbb{Z}$, donc on doit tester à part les valeurs $\pi + k2\pi$

<u>**Exemple :**</u> résoudre $5\cos x - 6\tan x = 5$

<u>Étape 1</u> : $D_{déf} = \mathbb{R} \setminus \left\{\frac{\pi}{2} + k\pi\right\}$

<u>Étape 2</u> : On teste Bioche et on observe qu'il n'est pas concluant. On pose $z = \tan\left(\frac{x}{2}\right)$

<u>Étape 3</u> : on teste les valeurs $\pi + k2\pi$
$$5\cos(\pi + k2\pi) - 6\tan(\pi + k2\pi) = -5 - 6 \cdot 0 = -5 \neq 5$$
$\pi + k2\pi$ n'est pas une solution

<u>Étape 4</u> : on applique $z = \tan\left(\frac{x}{2}\right)$
$$
\begin{aligned}
&5\cos(x) - 6\tan(x) = 5 \ \text{ et } x \in D_{déf} \\
&\iff 5\left(\frac{1 - z^2}{1 + z^2}\right) - 6\left(\frac{2z}{1 - z^2}\right) = 5 \ \text{ et } z \neq \pm 1 \\
&\iff 5(1 - z^2)^2 - 6 \cdot 2z(1 + z^2) = 5(1 - z^2)(1 + z^2) \ \text{ et } z \neq \pm 1 \\
&\iff 5(1 - 2z^2 + z^4) - 12z - 12z^3 = 5 - 5z^4 \ \text{ et } z \neq \pm 1 \\
&\iff 10z^4 - 12z^3 - 10z^2 - 12z = 0 \ \text{ et } z \neq \pm 1 \\
&\iff 2z(5z^3 - 6z^2 - 5z - 6) = 0 \ \text{ et } z \neq \pm 1 \\
&\iff 2z(z - 2)(5z^2 + 4z + 3) = 0 \ \text{ et } z \neq \pm 1 \qquad \Delta = 16 - 4 \cdot 3 \cdot 5 < 0 \\
&\iff z = 0, \ z = 2 \\
&\iff \tan\frac{x}{2} = 0 \ \text{ ou } \ \tan\frac{x}{2} = 2 \\
&\iff \frac{x}{2} = k\pi \ \text{ ou } \ \frac{x}{2} = \alpha + k\pi \ \text{ où } \tan(\alpha) = 2 \\
&\iff x = 2k\pi \ \text{ ou } \ x = 2\alpha + 2k\pi, \ k \in \mathbb{Z} \text{ et } \tan(\alpha) = 2
\end{aligned}
$$

Les solutions sont donc $2k\pi$ ou $2\alpha + 2k\pi$, $k \in \mathbb{Z}$

---

### 1.6 Résolutions de triangles

#### A. Théorème des cosinus

Dans le plan on considère un triangle $ABC$ orienté positivement

![[an2-1-triangle-cosinus.svg]]

On a
$$a^2 = h^2 + (c - k)^2 \qquad \text{où } \begin{aligned} h &= b\sin\alpha \\ k &= b\cos\alpha \end{aligned}$$
$$
\begin{aligned}
a^2 &= b^2\sin^2\alpha + c^2 - 2ck + k^2 \\
&= b^2\sin^2\alpha + c^2 - 2cb\cos\alpha + b^2\cos^2\alpha \\
&= b^2 + c^2 - 2bc\cos\alpha
\end{aligned}
$$

> [!important] On appelle théorème du cosinus les relations
> $$
> \begin{aligned}
> a^2 &= b^2 + c^2 - 2bc\cos\alpha \\
> b^2 &= a^2 + c^2 - 2ac\cos\beta \\
> c^2 &= a^2 + b^2 - 2ab\cos\gamma
> \end{aligned}
> $$

#### B. Théorème des sinus

Dans la figure précédente on a $h = b\sin\alpha$ et $h = a\sin\beta$
$$b\sin\alpha = a\sin\beta \iff \frac{\sin\alpha}{a} = \frac{\sin\beta}{b}$$

> [!important] On appelle théorème du sinus les relations
> $$\frac{\sin\alpha}{a} = \frac{\sin\beta}{b} = \frac{\sin\gamma}{c}$$

<u>**exemple :**</u> (résoudre le triangle)

Soit un triangle $ABC$ de côté $a = 91$, $b = 65$, $c = 39$

![[an2-1-triangle-exemple.svg]]

Par le théorème du cosinus, on a
$$\cos\alpha = \frac{a^2 - b^2 - c^2}{-2bc} = -\frac{1}{2} \quad \text{et } \alpha \in [0, \pi]$$
$$\alpha = \frac{2\pi}{3}$$

Par le théorème du sinus
$$\sin\beta = \frac{b}{a}\sin\alpha \cong 0.62$$

$\beta$ est un angle aigu car $\alpha > \frac{\pi}{2}$
$$\implies \beta = \sin^{-1}(0.62) \cong 38.2°$$
$$\alpha = \frac{2\pi}{3} = 120° \qquad \gamma = 180 - 120 - 38.2 \cong 21.8°$$

#### C. Formule de Héron

<u>But :</u> calculer l'aire d'un triangle $ABC$ en fonction des longueurs $a, b, c$, plus précisément en fonction du demi périmètre
$$p = \frac{a + b + c}{2}$$

![[an2-1-triangle-heron.svg]]

$$
\begin{aligned}
\mathcal{A} = \frac{1}{2}h \cdot c &= \frac{1}{2}bc\sin\alpha \qquad (\sin\alpha \geq 0) \\
&= \frac{1}{2}bc\sqrt{1 - \cos^2\alpha} \\
&= \frac{1}{2}bc\sqrt{(1 - \cos\alpha)(1 + \cos\alpha)}
\end{aligned}
$$

or par le théorème du cosinus on a
$$\cos\alpha = \frac{b^2 + c^2 - a^2}{2bc}$$

$$
\begin{aligned}
\text{donc } \mathcal{A} &= \frac{1}{2}bc\sqrt{\left(1 - \frac{b^2 + c^2 - a^2}{2bc}\right)\left(1 + \frac{b^2 + c^2 - a^2}{2bc}\right)} \\
&= \frac{1}{2}bc\sqrt{\left(\frac{2bc - b^2 - c^2 + a^2}{2bc}\right)\left(\frac{2bc + b^2 + c^2 - a^2}{2bc}\right)} \\
&= \frac{1}{2}bc\sqrt{\frac{1}{4b^2c^2}\big(2bc - b^2 - c^2 + a^2\big)\big(2bc + b^2 + c^2 - a^2\big)} \\
&= \frac{1}{4}\sqrt{\big(a^2 - (b - c)^2\big)\big((b + c)^2 - a^2\big)} \\
&= \frac{1}{4}\sqrt{\big(a - (b - c)\big)\big(a + (b - c)\big)(b + c - a)(b + c + a)} \\
&= \frac{1}{4}\sqrt{(a - b + c)(a + b - c)(b + c - a)(a + b + c)} \\
&= \frac{1}{4}\sqrt{(a + b + c - 2b)(a + b + c - 2c)(b + c + a - 2a)(a + b + c)} \\
&= \frac{1}{4}\sqrt{(2p - 2b)(2p - 2c)(2p - 2a) \cdot 2p} \\
&= \sqrt{(p - b)(p - c)(p - a)\,p}
\end{aligned}
$$

> [!important] Formule de Héron
> $$S = \sqrt{p(p - a)(p - b)(p - c)}$$
> aire du triangle en fonction de $p = \dfrac{a + b + c}{2}$

#### D. Rayon du cercle circonscrit

<u>But :</u> pour un triangle $ABC$ trouver le rayon $R$ du cercle circonscrit en fonction de $a, b, c$.

Le cercle circonscrit est le cercle passant par les 3 sommets. Le centre du cercle est l'intersection des 3 médiatrices.

![[an2-1-cercle-circonscrit.svg]]

On a $\sin(\alpha) = \dfrac{a/2}{R} \implies R = \dfrac{a}{2\sin\alpha}$

<u>premier résultat</u> par le théorème du sinus
$$R = \frac{a}{2\sin\alpha} = \frac{b}{2\sin\beta} = \frac{c}{2\sin\gamma}$$

<u>deuxième résultat</u>

on a que $\mathcal{A}$ = aire du triangle $= \frac{1}{2}bc\sin\alpha$
$$\implies \sin\alpha = \frac{2\mathcal{A}}{bc} \implies R = \frac{abc}{4\mathcal{A}}$$

donc par la formule de Héron
$$R = \frac{abc}{4} \cdot \frac{1}{\sqrt{p(p - a)(p - b)(p - c)}}$$

#### E. Rayon du cercle inscrit

Le cercle inscrit est le cercle contenu dans le triangle et tangent à chaque côté. Son centre est l'intersection des trois bissectrices

![[an2-1-cercle-inscrit.svg]]

on a
$$
\begin{aligned}
\mathcal{A} &= \text{aire } ABC \\
&= \text{aire } ABO + BCO + CAO \\
&= \frac{1}{2}rc + \frac{1}{2}ra + \frac{1}{2}rb \\
&= r\left(\frac{a + b + c}{2}\right)
\end{aligned}
$$

$$\implies r = \frac{S}{p} = \frac{\sqrt{p(p - a)(p - b)(p - c)}}{p} = \sqrt{\frac{(p - a)(p - b)(p - c)}{p}}$$

---

### 1.7 Fonctions réciproques

#### 1) Fonction réciproque du sinus

La fonction sinus est bijective sur tout intervalle du type $\left[-\frac{\pi}{2} + k\pi, \frac{\pi}{2} + k\pi\right]$

On appelle ces intervalles <u>les déterminations du sinus</u>.

![[an2-1-determinations-sinus.svg]]

On appelle <u>détermination principale</u> l'intervalle $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$

> [!definition]
> On définit la fonction réciproque $\arcsin$.
> $$[-1, 1] \to \left[-\frac{\pi}{2}, \frac{\pi}{2}\right] \qquad x \mapsto y = \arcsin(x)$$
> où $y$ est l'unique angle entre $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ tel que $\sin(y) = x$

<u>**Propriétés**</u>

① $\forall x \in [-1, 1] : \sin(\arcsin(x)) = x$

② $\arcsin(\sin(x)) = x \iff x \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$

<u>ex :</u> $\arcsin\left(\sin\left(\frac{5\pi}{6}\right)\right) = \arcsin\left(\frac{1}{2}\right) = \frac{\pi}{6} \neq \frac{5\pi}{6}$

![[an2-1-arcsin-5pi-6.svg]]

③ $\forall a \in [-1, 1]$
$$\sin(x) = a \iff \begin{cases} x = \arcsin(a) + k2\pi & \color{red}{\to \mathrm{I} \cup \mathrm{IV}} \\ \text{ou} \\ x = \pi - \arcsin(a) + k2\pi & \color{red}{\to \mathrm{II} \cup \mathrm{III}} \end{cases}$$

<u>**exemple :**</u> résoudre $\sin(x) = \frac{3}{4}$ et $x \in [2\pi, 3\pi]$

<u>étape 1</u> : on résout sans localisation
$$\sin(x) = \frac{3}{4} \iff x = \arcsin\left(\frac{3}{4}\right) + k2\pi \quad \text{ou} \quad x = \pi - \arcsin\left(\frac{3}{4}\right) + k2\pi$$

![[an2-1-arcsin-3-4.svg]]

$$A = P\left(\arcsin\left(\tfrac{3}{4}\right)\right) \qquad A' = P\left(\pi - \arcsin\left(\tfrac{3}{4}\right)\right)$$

<u>étape 2</u> : localisation <span style="color:red">avec un dessin</span>

$$\arcsin\left(\frac{3}{4}\right) \in \left[0, \frac{\pi}{2}\right] \subset [0, \pi] \ \longrightarrow \ \color{magenta}{\arcsin(3/4) + 2\pi \in [2\pi, 3\pi]}$$
$$\pi - \arcsin\left(\frac{3}{4}\right) \in \left[\frac{\pi}{2}, \pi\right] \subset [0, \pi] \ \longrightarrow \ \color{magenta}{3\pi - \arcsin\left(\tfrac{3}{4}\right) \in [2\pi, 3\pi]}$$

④ $\cos(\arcsin(x)) = \sqrt{1 - x^2} \quad \forall x \in [-1, 1]$

<u>preuve :</u>
$$
\begin{aligned}
\cos(\arcsin(x)) &= +\sqrt{1 - \sin^2(\arcsin(x))} \qquad \left(\arcsin \in \left[-\tfrac{\pi}{2}, \tfrac{\pi}{2}\right]\right) \\
&= \sqrt{1 - \sin(\arcsin(x)) \cdot \sin(\arcsin(x))} \\
&= \sqrt{1 - x^2}
\end{aligned}
$$

⑤ $\tan(\arcsin(x)) = \dfrac{x}{\sqrt{1 - x^2}} \quad \forall x \in\ ]-1, 1[$

⑥ $\forall x \in [-1, 1]$, $\arcsin(-x) = -\arcsin(x)$

<u>preuve :</u>
$$\sin(\arcsin(-x)) = -x = -\sin(\arcsin(x))$$

En résumé $\forall x \in [-1, 1]$ on a
$$\sin(\arcsin(-x)) = \sin(-\arcsin(x))$$

or on a $\arcsin(-x) \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$, $\ -\arcsin(x) \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$

#### 2) Fonction réciproque du cosinus

Les déterminations du cosinus sont les intervalles $[k\pi, (k + 1)\pi]$. Le cosinus y est bijectif

![[an2-1-determinations-cosinus.svg]]

La détermination principale est $[0, \pi]$

> [!definition]
> $\arccos$ la fonction réciproque définie par
> $$\arccos : [-1, 1] \to [0, \pi] \qquad x \mapsto y = \arccos(x)$$
> où $y$ est l'unique angle dans $[0, \pi]$ tel que $\cos(y) = x$

<u>**Propriétés**</u>

① $\forall x \in [-1, 1] \quad \cos(\arccos(x)) = x$

② $\arccos(\cos(x)) = x \iff x \in [0, \pi]$

③ $\forall a \in [-1, 1]$
$$\cos(x) = a \iff \begin{cases} x = \arccos(a) + k2\pi & \color{red}{\to \mathrm{I} \cup \mathrm{II}} \\ \text{ou} \\ x = -\arccos(a) + k2\pi & \color{red}{\to \mathrm{III} \cup \mathrm{IV}} \end{cases}$$

<u>**exemple :**</u> résoudre $\cos(x) \geq -\frac{3}{4}$ et $x \in \left[-\frac{3\pi}{2}, -\frac{\pi}{2}\right]$

<u>Étape 1</u> : par le dessin et sans localisation

![[an2-1-arccos-inequation.svg]]

$$A = P\left(\arccos\left(-\tfrac{3}{4}\right)\right) \qquad B = P\left(-\arccos\left(-\tfrac{3}{4}\right)\right)$$
$$-\arccos\left(-\frac{3}{4}\right) + k2\pi \leq x \leq \arccos\left(-\frac{3}{4}\right) + k2\pi \qquad k \in \mathbb{Z}$$

<u>Étape 2</u> : on localise
$$\arccos\left(-\frac{3}{4}\right) \in \left[\frac{\pi}{2}, \pi\right] \subset \left[\frac{\pi}{2}, \frac{3\pi}{2}\right] \ \xrightarrow{-2\pi} \ \color{magenta}{\arccos\left(-\tfrac{3}{4}\right) - 2\pi \in \left[-\tfrac{3\pi}{2}, -\tfrac{\pi}{2}\right]}$$
$$-\arccos\left(-\frac{3}{4}\right) \in \left[-\pi, -\frac{\pi}{2}\right] \subset \left[-\frac{3\pi}{2}, -\frac{\pi}{2}\right]$$

$$S = \left[-\frac{3\pi}{2}, \arccos\left(-\tfrac{3}{4}\right) - 2\pi\right] \cup \left[-\arccos\left(-\tfrac{3}{4}\right), -\frac{\pi}{2}\right]$$

④ $\forall x \in [-1, 1] \quad \sin(\arccos(x)) = \sqrt{1 - x^2}$

⑤ $\forall x \neq 0$, $\tan(\arccos(x)) = \dfrac{\sqrt{1 - x^2}}{x}$

⑥ $\forall x \in [-1, 1] \quad \arccos(-x) = \pi - \arccos(x)$

<u>Preuve :</u>
$$\cos\Big(\underbrace{\arccos(-x)}_{\color{magenta}{\in [0, \pi]}}\Big) = -x = -\cos(\arccos(x)) = \cos\Big(\underbrace{\pi - \arccos(x)}_{\color{magenta}{\in [0, \pi]}}\Big)$$

$\implies$ par injectivité du $\cos$, on a $\arccos(-x) = \pi - \arccos(x)$

#### 3) Fonctions réciproques de tan et cotan

On définit sur $\left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$ qui est la détermination principale de la tangente, la fonction réciproque :

> [!definition]
> $$\arctan : \mathbb{R} \to \left]-\frac{\pi}{2}, \frac{\pi}{2}\right[ \qquad x \mapsto y = \arctan(x)$$
> où $y$ est l'unique angle dans $\left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$ tel que $\tan(y) = x$

Sur $]0, \pi[$ qui est la détermination principale de la cot, on définit

> [!definition]
> $$\mathrm{arccot} : \mathbb{R} \to\ ]0, \pi[ \qquad x \mapsto y = \mathrm{arccot}(x)$$
> où $y$ est l'unique angle dans $]0, \pi[$ tel que $\cot(y) = x$

① $\forall x \in \mathbb{R}$, $\tan(\arctan(x)) = x$

② $\forall x \in \left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$, $\arctan(\tan(x)) = x$

③ $\tan(x) = a \iff x = \arctan(a) + k\pi$
$\quad \big(\cot(x) = a \iff x = \mathrm{arccot}(a) + k\pi\big)$

④ $\sin(\arctan(x)) = \dfrac{x}{\sqrt{1 + x^2}}$

![[an2-1-triangle-arctan.svg]]

⑤ $\cos(\arctan(x)) = \dfrac{1}{\sqrt{1 + x^2}}$

⑥ $\forall x \in \mathbb{R}$, $\arctan(-x) = -\arctan(x)$
$\quad \big(\forall x \in \mathbb{R}$, $\mathrm{arccot}(-x) = \pi - \mathrm{arccot}(x)\big)$

<u>**exemple :**</u> Soit $\alpha = \arctan(2) + \arctan(3)$. Calculer $\alpha$

On commence par calculer
$$\tan(\alpha) = \tan(\beta + \gamma) = \frac{\tan(\beta) + \tan(\gamma)}{1 - \tan(\beta)\tan(\gamma)} = \frac{2 + 3}{1 - 2 \cdot 3} = -1$$

$\implies \tan(\alpha) = -1 \iff \alpha = -\frac{\pi}{4} + k\pi$, $\mathbb{Z}$ — reste à déterminer $k$

or $\arctan(2) \in \left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$, $\arctan(3) \in \left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$

donc $\alpha = \beta + \gamma \in\ ]-\pi, \pi[$

![[an2-1-arctan-somme.svg]]

On fait un peu mieux
$$\left.\begin{aligned} \beta &= \arctan(2) \in \left]0, \tfrac{\pi}{2}\right[ \\ \gamma &= \arctan(3) \in \left]0, \tfrac{\pi}{2}\right[ \end{aligned}\right\} \ \alpha \in\ ]0, \pi[$$

$$\implies \alpha = -\frac{\pi}{4} + \pi = \frac{3\pi}{4}$$

<u>**exemple ①**</u> $\forall x \in [-1, 1]$ montrons que
$$\boxed{\arcsin(x) + \arccos(x) = \frac{\pi}{2}}$$

<u>Illustration</u>

![[an2-1-arcsin-arccos.svg]]

<u>étape 1</u> on prend le sinus
$$
\begin{aligned}
&\sin(\arcsin(x) + \arccos(x)) \\
&= \sin(\arcsin(x)) \cdot \cos(\arccos(x)) + \cos(\arcsin(x))\sin(\arccos(x)) \\
&= x \cdot x + \sqrt{1 - x^2} \cdot \sqrt{1 - x^2} \\
&= x^2 + 1 - x^2 = 1
\end{aligned}
$$

Notons $\alpha = \arcsin(x) + \arccos(x)$, alors on a trouvé que $\alpha$ satisfait $\sin(\alpha) = 1$

<u>étape 2</u> localisation

on a $\left.\begin{aligned} \arcsin(x) &\in \left[-\tfrac{\pi}{2}, \tfrac{\pi}{2}\right] \\ \arccos(x) &\in [0, \pi] \end{aligned}\right\} \implies \alpha \in \left[-\frac{\pi}{2}, \frac{3\pi}{2}\right]$

en résumé $\alpha$ doit satisfaire
$$\sin(\alpha) = 1 \ \text{ et } \ \alpha \in \left[-\frac{\pi}{2}, \frac{3\pi}{2}\right] \iff \alpha = \frac{\pi}{2} \iff \arccos(x) + \arcsin(x) = \frac{\pi}{2}$$

<u>**exemple ②**</u> Déterminer $A$ et $B$ tels que pour
$$f(x) = 2\sin\left(\frac{\pi}{3} - x\right) + 2\sin(x)$$
on a $f : A \to B$ est bijective avec $B = \mathrm{Im}\,f$. Donner l'expression de $f^{-1}$

<u>étape 1</u> on réduit l'expression de $f$
$$f(x) = 2\left[\sin\left(\frac{\pi}{3} - x\right) + \sin(x)\right] = 2 \cdot 2\sin\left(\frac{\pi}{6}\right)\cos\left(\frac{\pi}{6} - x\right) = 2\cos\left(\frac{\pi}{6} - x\right)$$

<u>étape 2</u> : on calcule l'image

pour $x \in \mathbb{R}$, $\cos\left(\frac{\pi}{6} - x\right) \in [-1, 1]$

donc $f(x) \in [-2, 2]$ et on peut poser $B = \mathrm{Im}(f) = [-2, 2]$

<u>étape 3</u> : on cherche $A$ pour que $f : A \to B$ soit bijectif.

on peut par exemple, imposer $\frac{\pi}{6} - x \in [0, \pi]$
$$\iff 0 \leq \frac{\pi}{6} - x \leq \pi \iff -\frac{\pi}{6} \leq -x \leq \frac{5\pi}{6} \iff -\frac{5\pi}{6} \leq x \leq \frac{\pi}{6}$$

Donc on pose $A = \left[-\frac{5\pi}{6}, \frac{\pi}{6}\right]$ et on a bien
$$f : \left[-\frac{5\pi}{6}, \frac{\pi}{6}\right] \to [-2, 2] \ \text{ bijectif}$$

<u>étape 4</u> : on calcule $f^{-1}$ : pour $x \in \left[-\frac{5\pi}{6}, \frac{\pi}{6}\right]$ et $y \in [-2, 2]$, on résout $f(x) = y$
$$
\begin{aligned}
&\iff 2\cos\left(\frac{\pi}{6} - x\right) = y \\
&\iff \cos\left(\frac{\pi}{6} - x\right) = \frac{y}{2} && \color{magenta}{\cos \text{ bijectif}, \ \tfrac{\pi}{6} - x \in [0, \pi]} \\
&\iff \frac{\pi}{6} - x = \arccos\left(\frac{y}{2}\right) \\
&\iff x = \frac{\pi}{6} - \arccos\left(\frac{y}{2}\right) = f^{-1}(y)
\end{aligned}
$$

<u>**exemple ③**</u> Résoudre par rapport à $x \in \mathbb{R}$ l'équation
$$\arcsin\left(x - \frac{1}{2}\right) + \arcsin(\sqrt{2}x) = -\frac{\pi}{4}$$

<u>Étape 1</u> :
$$
\begin{aligned}
D_{déf} &= \left\{x \in \mathbb{R} \ \middle|\ x - \tfrac{1}{2} \in [-1, 1] \text{ et } \sqrt{2}x \in [-1, 1]\right\} \\
&= \left[-\frac{1}{2}, \frac{3}{2}\right] \cap \left[-\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}\right] \\
&= \left[-\frac{1}{2}, \frac{3}{2}\right] \cap \left[-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right]
\end{aligned}
$$

Donc $D_{déf} = \left[-\frac{1}{2}, \frac{\sqrt{2}}{2}\right]$

<u>étape 2</u> (pas nécessaire) localisation

On pose $\alpha = \arcsin\left(x - \frac{1}{2}\right)$ et $\beta = \arcsin(\sqrt{2}x)$

On a $\alpha, \beta \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right] \implies \alpha + \beta \in [-\pi, \pi]$

or $-\frac{\pi}{4} \in [-\pi, \pi]$, donc il y a une chance de résoudre.

<u>étape 3</u> On prend les sinus ⚠️

<u>1<sup>ère</sup> méthode</u> (☹)
$$
\begin{aligned}
&\alpha + \beta = -\frac{\pi}{4} \\
&\underset{\color{red}{\not\Leftarrow}}{\implies} \sin(\alpha + \beta) = \sin\left(-\frac{\pi}{4}\right) \\
&\iff \sin(\alpha)\cos(\beta) + \cos(\alpha)\sin(\beta) = -\frac{\sqrt{2}}{2} \\
&\iff \left[x - \frac{1}{2}\right] \cdot \sqrt{1 - 2x^2} + \sqrt{1 - \left(x - \tfrac{1}{2}\right)^2} \cdot \sqrt{2}x = -\frac{\sqrt{2}}{2} \quad \text{☹}
\end{aligned}
$$

<u>2<sup>ème</sup> méthode</u> ☺

on écrit
$$
\begin{aligned}
&\alpha + \beta = -\frac{\pi}{4} \ \text{ et } x \in D_{déf} \\
&\iff \alpha = -\frac{\pi}{4} - \beta \ \text{ et } x \in D_{déf} \\
&\implies \sin(\alpha) = \sin\left(-\frac{\pi}{4} - \beta\right) \ \text{ et } x \in D_{déf} \\
&\iff x - \frac{1}{2} = -\left(\sin\left(\frac{\pi}{4} + \beta\right)\right) \ \text{ et } x \in D_{déf} \\
&\iff x - \frac{1}{2} = -\sin\frac{\pi}{4}\cos(\beta) - \cos\left(\frac{\pi}{4}\right)\sin(\beta) \ \text{ et } x \in D_{déf} \\
&\iff x - \frac{1}{2} = -\frac{\sqrt{2}}{2}\sqrt{1 - 2x^2} - \frac{\sqrt{2}}{2}\sqrt{2}x \ \text{ et } x \in D_{déf} \\
&\iff x - \frac{1}{2} = -\frac{\sqrt{2}}{2}\sqrt{1 - 2x^2} - x \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{\sqrt{2}}{2}\right] \\
&\iff 2x - \frac{1}{2} = -\frac{\sqrt{2}}{2}\sqrt{1 - 2x^2} \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{\sqrt{2}}{2}\right] \\
&\iff \frac{1}{2} - 2x = \frac{\sqrt{2}}{2}\sqrt{1 - 2x^2} \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{\sqrt{2}}{2}\right] \\
&\iff \left(\frac{1}{2} - 2x\right)^2 = \frac{1}{2}\left[1 - 2x^2\right] \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{\sqrt{2}}{2}\right] \text{ et } \left(\tfrac{1}{2} - 2x \geq 0\right) \\
&\iff \left(\frac{1}{2} - 2x\right)^2 = \frac{1}{2}\left[1 - 2x^2\right] \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{1}{4}\right] \\
&\iff \frac{1}{4} - 2x + 4x^2 = \frac{1}{2} - x^2 \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{1}{4}\right] \\
&\iff 5x^2 - 2x - \frac{1}{4} = 0 \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{1}{4}\right] \\
&\iff 5\left(x^2 - \frac{2}{5}x - \frac{1}{20}\right) = 0 \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{1}{4}\right] \\
&\iff 5\left(x - \frac{1}{2}\right)\left(x + \frac{1}{10}\right) = 0 \ \text{ et } x \in \left[-\tfrac{1}{2}, \tfrac{1}{4}\right] \\
&\iff x = -\frac{1}{10}
\end{aligned}
$$

<u>étape 4</u> $x = -\frac{1}{10}$ est un candidat. On teste s'il satisfait l'équation ou non :

on a
$$\arcsin\left(-\frac{1}{10} - \frac{1}{2}\right) + \arcsin\left(-\frac{\sqrt{2}}{10}\right) = \arcsin\left(-\frac{3}{5}\right) + \arcsin\left(-\frac{\sqrt{2}}{10}\right) = \ ?$$

pour vérifier si $x = -\frac{1}{10}$ est une solution, on passe par la localisation

Posons $\gamma = \arcsin\left(-\frac{3}{5}\right)$ et $\delta = \arcsin\left(-\frac{\sqrt{2}}{10}\right)$

on sait que $\gamma$ et $\delta$ satisfont $\sin(\gamma) = \sin\left(-\frac{\pi}{4} - \delta\right)$

de plus $\gamma \in \left[-\frac{\pi}{2}, 0\right] \subset \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$, $\ \delta \in \left[-\frac{\pi}{4}, 0\right]$
$$\implies -\frac{\pi}{4} - \delta \in \left[-\frac{\pi}{4}, 0\right] \subset \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$$

par injectivité du sinus, on a $\gamma = -\frac{\pi}{4} - \delta \iff \gamma + \delta = -\frac{\pi}{4}$

donc $x = -\frac{1}{10}$ est solution.

<u>**exemple ④**</u> résoudre par rapport à $x$
$$2\arctan(x) + \arctan(\sqrt{3}x) = -\frac{5\pi}{6}$$

<u>étape 1</u> $D_{déf} = \mathbb{R}$

<u>étape 2</u> notons $\alpha = \arctan(x) \in \left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$, $\ \beta = \arctan(\sqrt{3}x) \in \left]-\frac{\pi}{2}, \frac{\pi}{2}\right[$

donc $2\alpha + \beta \in \left]-\frac{3\pi}{2}, \frac{3\pi}{2}\right[$ et $-\frac{5\pi}{6} \in \left]-\frac{3\pi}{2}, \frac{3\pi}{2}\right[$

donc il y a une chance de résoudre.

<u>étape 3</u>. On prend la tangente
$$2\alpha + \beta = -\frac{5\pi}{6} \implies \tan(2\alpha + \beta) = \tan\left(-\frac{5\pi}{6}\right) \quad \text{☹}$$

<u>mieux</u> ☺
$$
\begin{aligned}
&2\alpha + \beta = -\frac{5\pi}{6} \\
&\iff 2\alpha = -\frac{5\pi}{6} - \beta \\
&\implies \tan(2\alpha) = \tan\left(-\frac{5\pi}{6} - \beta\right) \ \text{ et } 2\alpha \neq \frac{\pi}{2} + k\pi \ \text{ et } -\frac{5\pi}{6} - \beta \neq \frac{\pi}{2} + k\pi \\
&\iff \frac{2\tan(\alpha)}{1 - \tan^2(\alpha)} = -\frac{\tan\left(\frac{5\pi}{6}\right) + \tan(\beta)}{1 - \tan(\beta)\tan\left(\frac{5\pi}{6}\right)} \\
&\iff \frac{2x}{1 - x^2} = \frac{\frac{\sqrt{3}}{3} - \sqrt{3}x}{1 + x} \ \text{ et } x \neq \pm 1
\end{aligned}
$$

<u>étape 4</u> test des valeurs interdites
$$2\arctan(-1) + \arctan(-\sqrt{3}) = -\frac{\pi}{2} - \frac{\pi}{3} = -\frac{5\pi}{6} \ \color{lime}{\checkmark}$$
$$2\arctan(1) + \arctan(\sqrt{3}) = \frac{5\pi}{6} \neq -\frac{5\pi}{6}$$

donc $x = -1$ est solution ☺

<u>étape 5</u> on résout l'équation pour $x \neq \pm 1$

on a
$$
\begin{aligned}
&2x(1 + x) = \left(\frac{\sqrt{3}}{3} - \sqrt{3}x\right)(1 - x^2) \\
&\iff 2x(1 + x) = \left(\frac{\sqrt{3}}{3} - \sqrt{3}x\right)(1 - x)(1 + x) \\
&\iff 2x = \frac{\sqrt{3}}{3} - \sqrt{3}x - \frac{\sqrt{3}}{3}x + \sqrt{3}x^2 \\
&\iff \sqrt{3}x^2 - \left[\sqrt{3} + \frac{\sqrt{3}}{3} + 2\right]x + \frac{\sqrt{3}}{3} = 0
\end{aligned}
$$

- on peut calculer $\Delta > 0$ : il existe $x_1$ et $x_2$ $(x_1 \neq x_2)$ 2 racines

De plus, par Viète on a $x_1x_2 = \frac{c}{a} > 0$ et $x_1 + x_2 = -\frac{b}{a} > 0$
$$\implies x_1 > 0 \ \text{ et } \ x_2 > 0$$

donc $2\arctan(x_1) + \arctan(\sqrt{3}x_1) > 0$ et $2\arctan(x_2) + \arctan(\sqrt{3}x_2) > 0$

et donc ni $x_1$ ni $x_2$ n'est solution

<u>étape 6</u> Conclusion : la seule solution $x = -1$
