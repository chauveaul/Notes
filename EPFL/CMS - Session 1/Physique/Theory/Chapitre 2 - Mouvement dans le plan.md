---
cours: Physique
chapitre: 2
source: "Chapitre 2 - Physique.pdf"
tags: [physique, chapitre-2]
---

# 2. Mouvement dans le plan

### 2.1 Objet, masse et volume

- <u>Objet</u> : morceau de matière
- <u>Masse</u> : quantité de matière
  - Symboles : $M, m$ $\qquad$ Unité : $\mathrm{kg}$
- <u>Volume</u> : portion de l'espace qui est occupée par l'objet
  - Symbole : $V$ $\qquad$ Unité : $\mathrm{m^3}$ $\qquad (1 \ \mathrm{L} = 10^{-3} \ \mathrm{m^3})$, $\ 1 \ \mathrm{dm^3} = 1 \ \mathrm{L}$

<u>Masse volumique</u> (moyenne)

> [!important]
> $$\underset{\text{« rho »}}{\rho} = \frac{m}{V} \qquad \text{Unité : } \frac{\mathrm{kg}}{\mathrm{m^3}}$$

C'est une propriété d'un matériel.

<u>ex.</u>
- eau liquide $\quad \rho = 10^3 \ \mathrm{kg/m^3}$
- solide $\quad \rho \doteq 0.9 \cdot 10^3 \ \mathrm{kg/m^3}$

<u>Densité</u> : comparaison entre deux masses volumiques

> [!important]
> $$d = \frac{\rho}{\rho_{\text{eau liquide}}} \qquad \text{Unité : N/A}$$

- Cercle : $\quad C = 2\pi R \qquad S = \pi R^2$
- Sphère : $\quad S = 4\pi R^2 \qquad V = \dfrac{4}{3}\pi R^3$

---

### 2.2 Référentiel, origine, repère fixe

Le mouvement d'un objet ne peut être donné que par rapport à un objet de référence (« fixe ») : le <u>référentiel</u>

<u>ex.</u> une personne marchant dans un train

![[p2-train.svg]]

- Référentiel 1 : le train
- Référentiel 2 : le sol

$\Big\}$ Selon le référentiel, la vitesse de la personne est différente

<u>Origine</u> : point fixe du référentiel, noté $O$

<u>Repère</u> : pour faire des calculs, on munit le référentiel d'un repère $(\vec{e}_x, \vec{e}_y)$, orthonormé : $\|\vec{e}_x\| = \|\vec{e}_y\| = 1$, $\ \vec{e}_x \perp \vec{e}_y$

![[p2-reperes.svg]]

---

### 2.3 Vecteur-position

La position d'un objet, dans le référentiel et par rapport à l'origine choisie, est donnée par le vecteur-position. <u>Notation</u> : $\vec{r}$ $\quad$ <u>unité</u> : $\mathrm{m}$

![[p2-vecteur-position.svg]]

<u>Rappel</u> : tout vecteur est caractérisé par
- sa direction
- sens
- sa norme

![[p2-caracteristiques.svg]]

Pour les calculs, décomposons le vecteur position dans le repère choisi :

![[p2-decomposition.svg]]

$x \cdot \vec{e}_x$ : multiple de $\vec{e}_x$ (unit vector)

$$\vec{r} = x \cdot \vec{e}_x + y \cdot \vec{e}_y \qquad x, y \in \mathbb{R} : \text{composantes, } \underline{\text{unité}} : \mathrm{m}$$

$$\vec{r} = \begin{pmatrix} x \\ y \end{pmatrix} \quad \text{si } (\vec{e}_x, \vec{e}_y) \text{ est orthonormé}$$

<u>Trigo</u> :
$$x = r\cos(\alpha) \qquad y = r\sin(\alpha) \qquad r = \|\vec{r}\| = \sqrt{x^2 + y^2}$$

L'objet peut bouger dans le référentiel ; sa position change avec le temps

<u>Temps</u> : comparaison de durée
- <u>symboles</u> : $t, T$ $\qquad$ <u>unité</u> : $\mathrm{s}$

On cherche à connaître la réponse aux questions <u>« où ? »</u> et <u>« quand ? »</u>

La position est donc une <u>fonction du temps</u>

> [!important]
> $\vec{r}(t)$ : « position à l'instant $\underline{t}$ »

![[p2-positions-t1-t2.svg]]

$$\vec{r}_1 = \vec{r}(t_1) \qquad \vec{r}_2 = \vec{r}(t_2)$$

<u>Trajectoire</u> : « trace laissée par l'objet »

![[p2-trajectoire.svg]]

$$\Gamma = \left\{ P \mid \exists t, \ \vec{OP} = \vec{r}(t) \right\}$$

<u>Déplacement</u> : changement de position (différence de vecteurs)

![[p2-deplacement.svg]]

$$\vec{r}_1 = \vec{r}(t_1) \qquad \vec{r}_2 = \vec{r}(t_2)$$
$${\color{magenta}\Delta\vec{r} = \vec{r}_2 - \vec{r}_1}$$

<u>Remarque</u> : $\Delta t = t_2 - t_1$ : durée du déplacement

<u>Rencontre entre deux objets</u> : $A$ et $B$ au même endroit et même instant.

![[p2-rencontre.svg]]

$$\exists t_r, \quad \vec{r}_A(t_r) = \vec{r}_B(t_r)$$

#### Cas particuliers

**1.** Objet immobile en un point $A$

![[p2-immobile.svg]]

$$\vec{r}(t) = \vec{OA} = \vec{r}_0 \quad \forall t$$

Le vecteur position est inchangé

**2.** Objet avançant régulièrement sur une droite et passant par $A$ à un certain instant $t_0$

![[p2-regulier.svg]]

<u>Régulier</u> : $\Delta\vec{r} \propto \Delta t$
$$\underline{\Delta\vec{r} = \vec{v}_0\,\Delta t}$$

Alors,
$$\vec{r}(t) - \vec{r}_0 = \vec{v}_0 \cdot (t - t_0)$$

> [!important]
> $$\vec{r}(t) = \vec{v}_0\,(t - t_0) + \vec{r}_0$$

C'est le MRU (mouvement rectiligne uniforme)

---

### 2.4 Vitesse

Un objet se déplace. Considérons sa position aux instants $t_1$ et $t_2$ $(t_1 < t_2)$

![[p2-vitesse-moyenne.svg]]

| | |
| :-- | :-- |
| $\vec{r}_1 = \vec{r}(t_1)$ | ancienne position |
| $\vec{r}_2 = \vec{r}(t_2)$ | nouvelle position |
| <span style="color:orange">$\Delta\vec{r}$</span> $= \vec{r}_2 - \vec{r}_1$ | déplacement |
| $\Delta t = t_2 - t_1$ | durée du ″ |

Comparer déplacement et durée par un quotient qui s'appelle la <span style="color:red">vitesse moyenne</span> durant le déplacement

> [!important]
> $$\vec{v}_{\text{moy}} = \frac{\Delta\vec{r}}{\Delta t} \qquad \text{unité : } \frac{\mathrm{m}}{\mathrm{s}}$$

<u>Remarque</u> : on n'a pas d'infos sur les temps intermédiaires

On va donc augmenter la précision !

Si l'intervalle de temps $\Delta t$ est très petit, les positions $\vec{r}_1$ et $\vec{r}_2$ sont très proches et le déplacement donne la direction et le sens du mouvement à l'instant $t_1$

![[p2-tangente.svg]]

<span style="color:orange">$\Delta\vec{r}$</span> devient vecteur directeur de la tangente à $\Gamma$ au point atteint à l'instant $t$

Lorsque $\Delta t$ devient « infiniment petit » (on note $\Delta t \to 0$), on définit la vitesse (« instantanée ») à l'instant $t$ par

> [!important]
> $$\vec{v}(t) = \lim_{\Delta t \to 0} \frac{\Delta\vec{r}}{\Delta t} = \lim_{\Delta t \to 0} \frac{\vec{r}(t + \Delta t) - \vec{r}(t)}{\Delta t} = \frac{d\vec{r}}{dt} = \dot{\vec{r}}(t)$$
> « vitesse à l'instant $t$ »

La vitesse est ainsi,
- le taux de variation de la position par rapport au temps
- un vecteur (direction, sens et norme)
- tangente à la trajectoire, dans le sens du mouvement
- de norme $\|\vec{v}\|$ donnant la distance parcourue par unité de temps

La vitesse peut changer au cours du temps donc c'est une fonction du temps.

<u>Cas particulier</u> : vitesse constante signifie
- direction constante $\implies \Gamma \implies$ droite
- sens constant $\implies$ pas de demi-tour
- norme constante

Pour les calculs, on décompose le vecteur vitesse selon le repère choisi $(\vec{e}_x, \vec{e}_y)$

![[p2-composantes-vitesse.svg]]

$${\color{green}\vec{v}(t) = v_x(t)\,\vec{e}_x + v_y(t)\,\vec{e}_y}$$

${\color{green}v_x, v_y}$ : composantes

<u>rem</u> : $v_x = \dot{x}$, $\ v_y = \dot{y}$

<u>**Ex : pendule simple**</u>

![[p2-pendule.svg]]

<u>**Ex : lancer de balle**</u>

![[p2-lancer-balle.svg]]

$${\color{green}v_{1x} = v_{2x}} \qquad {\color{green}v_{1y} \neq v_{2y}}$$

La vitesse horizontale est constante et $\vec{v}_2$ est tangente

#### <u>Cas particuliers</u>

**1.** Objet immobile en $A$

![[p2-immobile.svg]]

$$
\begin{aligned}
\text{immobile} &\iff \vec{v}(t) = \vec{0} \quad \forall t \\
&\iff \text{la position ne change pas} \\
&\iff \vec{r}(t) = \vec{r}_0 = \vec{OA} \quad \forall t
\end{aligned}
$$

En effet :
$$\vec{v}(t) = \lim_{\Delta t \to 0} \frac{\vec{r}(t + \Delta t) - \vec{r}(t)}{\Delta t}$$
$$\vec{v}(t) = \lim_{\Delta t \to 0} \frac{\vec{r}_0 - \vec{r}_0}{\Delta t} = \lim_{\Delta t \to 0} \frac{\vec{0}}{\Delta t} = \vec{0}$$

**2.** Objet avance à une vitesse constante $\vec{v}_0$ et passant par $A$ à l'instant $t_0$ : $\vec{r}(t_0) = \vec{r}_0 = \vec{OA}$

![[p2-mru.svg]]

$$\vec{v}(t) = \vec{v}_0 \quad \forall t$$

Elle est donc égale à la vitesse moyenne
$$\vec{v}_{\text{moy}} = \frac{\Delta\vec{r}}{\Delta t}$$

$$\implies \vec{v}_0 = \frac{\Delta\vec{r}}{\Delta t} \implies \underline{\vec{r}(t) = \vec{v}_0 \cdot (t - t_0) + \vec{r}_0}$$

C'est le MRU

**3.** Objet passant par $A$ à l'instant $t_0$ $(\vec{r}(t_0) = \vec{r}_0 = \vec{OA})$ avec une vitesse $\vec{v}_0$ $(\vec{v}(t_0) = \vec{v}_0)$ et la vitesse change régulièrement : le changement de vitesse est proportionnel à la durée

Il existe un facteur $\vec{a}_0$ tel que $\Delta\vec{v} = \vec{a}_0 \cdot \Delta t$
$$\iff \vec{v}(t) = \vec{a}_0 \cdot (t - t_0) + \vec{v}_0$$

![[p2-mua.svg]]

On dit que c'est un MUA : mouvement uniformément accéléré

Alors,
$$\vec{r}(t) = \frac{1}{2}\vec{a}_0 \cdot (t - t_0)^2 + \vec{v}_0 \cdot (t - t_0) + \vec{r}_0$$

À vérifier : $\dot{\vec{r}}(t) = \vec{v}(t) \dots$

<u>**Exemple : tir oblique**</u>

![[p2-tir-oblique.svg]]

<u>Critère</u> $\quad \exists t_r, \ \vec{r}_p(t_r) = \vec{r}_c(t_r)$
- projectile : $\vec{r}_p(t)$
- cible : $\vec{r}_c(t)$
- etc…

---

### 2.5 Accélération

Considérons un objet aux instants $t_1$ et $t_2$ (p.ex. $t_1 < t_2$) et comparons les vitesses

![[p2-acceleration-t1-t2.svg]]

| | |
| :-- | :-- |
| ${\color{green}\vec{v}_1} = \vec{v}(t_1)$ | ancienne vitesse |
| ${\color{green}\vec{v}_2} = \vec{v}(t_2)$ | nouvelle vitesse |
| $\Delta\vec{v} = \vec{v}_2 - \vec{v}_1$ | changement de vitesse |
| $\Delta t = t_2 - t_1$ | durée du changement |

<u>Odographe</u> : <span style="color:orange">$\Delta\vec{v}$ — même origine</span>

![[p2-odographe.svg]]

Comme pour la vitesse, on considère $\Delta t$ tout petit

![[p2-acceleration-dt.svg]]

Comparons (quotient) le changement de vitesse et la durée :
$$\vec{a}_{\text{moy}} = \frac{\Delta\vec{v}}{\Delta t}$$

Pour $\Delta t$ « infiniment » petit, on définit l'accélération par

> [!important] Unité : $\mathrm{m/s^2}$
> $$\vec{a} = \lim_{\Delta t \to 0} \frac{\Delta\vec{v}}{\Delta t} = \lim_{\Delta t \to 0} \frac{\vec{v}(t + \Delta t) - \vec{v}(t)}{\Delta t} = \frac{d\vec{v}}{dt} = \dot{\vec{v}}(t) = \ddot{\vec{r}}(t)$$

L'accélération est ainsi :
- le taux de variation de la vitesse par rapport au temps
- un vecteur (direction, sens et norme)
- toujours dirigé vers l'intérieur du virage

![[p2-acceleration-decomposition.svg]]

On peut décomposer l'accélération
$$\vec{a} = \underset{/\!/ \text{ tangente}}{\vec{a}_t} + \underset{/\!/ \text{ normale}}{\vec{a}_n}$$

- Selon la tangente : changement de la norme de $\vec{v}$ (+ ou − vite)
- Selon la normale : changement de la direction (virage)

L'accélération est une fonction du temps :
$$\vec{a}(t) \ \text{« accélération à l'instant } t \text{ »}$$

<u>**Exemple**</u> : prendre un pendule simple

![[p2-pendule-acceleration.svg]]

<u>**Exemple : objet lancé**</u>

![[p2-objet-lance.svg]]

- $v_x =$ constante
- $v_y \neq v_y'$ : la vitesse change verticalement !
- $\vec{a} = \vec{g}$

---

<u>**QCM 2**</u> $\quad$ MRU

![[p2-qcm2.svg]]

$$\vec{r}(t) = \vec{v}_0\,t + \vec{r}_0$$
$$1 : \ \vec{v}_0 \ /\!/ \ \vec{r}_0$$

---

#### <u>Cas particuliers</u>

**1. MRU** : objet avançant à vitesse constante $\vec{v}_0$ et passant par un point $A$ à l'instant $t_0$ : $\vec{r}(t_0) = \vec{OA} = \vec{r}_0$

![[p2-mru-2.svg]]

$$
\left.
\begin{aligned}
\vec{a}(t) &= \vec{0} \\
\vec{v}(t) &= \vec{v}_0 \\
\vec{r}(t) &= \vec{v}_0 \cdot (t - t_0) + \vec{r}_0
\end{aligned}
\right\} \quad \forall t
$$

**2. MUA** (mouvement uniformément accéléré) : On considère un objet qui passe par $A$ à l'instant $t_0$ $(\vec{r}(t_0) = \vec{OA} = \vec{r}_0)$ avec la vitesse $\vec{v}_0$ $(\vec{v}(t_0) = \vec{v}_0)$ et dont l'accélération est constante $(\vec{a}(t) = \vec{a}_0 \ \forall t)$ ; la vitesse change régulièrement

<u>Remarque</u> : le trajet est une parabole d'axe de symétrie parallèle à $\vec{a}_0$

![[p2-mua-parabole.svg]]

$$\vec{a}(t) = \vec{a}_0$$
$$\vec{v}(t) = \vec{a}_0\,(t - t_0) + \vec{v}_0$$
$$\vec{r}(t) = \frac{1}{2}\vec{a}_0 \cdot (t - t_0)^2 + \vec{v}_0 \cdot (t - t_0) + \vec{r}_0$$

À vérifier :
$$\dot{\vec{r}}(t) = \lim_{\Delta t \to 0} \frac{\vec{r}(t + \Delta t) - \vec{r}(t)}{\Delta t} = \vec{v}(t)$$

Accélération constante :

> [!important]
> $$\vec{a}(t) = \vec{a}_0$$
> $$\vec{v}(t) = \vec{a}_0\,\Delta t + \vec{v}_0$$
> $$\vec{r}(t) = \frac{1}{2}\vec{a}_0\,\Delta t^2 + \vec{v}_0\,\Delta t + \vec{r}_0$$
