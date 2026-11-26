---
cours: Physique
chapitre: 3
source: "Chapitre 3 - Physique.pdf"
tags: [physique, chapitre-3]
---

# 3. Dynamique ⭐ Chapitre

### 3.1 Principe d'inertie

<u>Idée :</u> si on ne fait rien, rien ne change et réciproquement (si rien ne change → on n'a rien fait)

Considérons un objet <span style="color:orange">(IMPORTANT À PRÉCISER LEQUEL)</span>

Principe d'inertie :

> [!important]
> Un objet en mouvement ne subit aucune action
> **si et seulement si**
> son mouvement est rectiligne et uniforme $(\vec{a} = \vec{0})$

<u>Ex :</u> un puck sur une patinoire (entre deux chocs)

![[p3-puck.svg]]

> [!definition] <u>Référentiel d'inertie</u>
> référentiel dans lequel le principe d'inertie est valable.

- <u>ex :</u> la patinoire est un référentiel d'inertie
- <u>ex :</u> un camion qui démarre (avec glace et puck) n'est pas un référentiel d'inertie.

![[p3-camion.svg]]

Initialement tout est au repos. Le camion démarre
- par rapport au sol le puck est immobile
- par rapport au camion le puck recule.

---

### 3.2 Deuxième loi de Newton

Contraposée du principe d'inertie $\qquad (P \Rightarrow Q) \iff (\neg Q \Rightarrow \neg P)$

> [!important]
> Un objet en mouvement subit une action si et seulement si sa vitesse est modifiée. $(\vec{a} \neq \vec{0})$

Considérons un objet (important !) La loi s'écrit

$$\boxed{\vec{F} = m\vec{a}}$$

- $m$ = masse de l'objet considéré
- $\vec{a}$ = accélération
- $\vec{F}$ : somme des actions que subit cet objet (force)

<u>Force :</u> action qui modifie la vitesse de l'objet

Symboles : $\vec{F}, \vec{S}, \vec{N}, \vec{T} \qquad$ Unité : $\dfrac{\mathrm{kg \cdot m}}{\mathrm{s^2}} : \mathrm{N}$

<u>Remarque :</u>
- la force est la cause.
- l'accélération est la conséquence
- $\vec{a}$ et $\vec{F}$ sont colinéaires et de même sens
- plus la masse est importante, plus il est difficile de modifier la vitesse (inertie) $\left(m \propto \dfrac{1}{a}\right)$

<u>**Exemple :**</u> une balle roulant sur le sol, vue de dessus

![[p3-balle-vent.svg]]

L'air appuie sur la balle (force) $\implies$ déviation

<u>Cas particulier :</u> sans aucune action $(\vec{F} = \vec{0})$, il n'y a pas d'accélération $(\vec{a} = \vec{0})$ : MRU

<u>Statique :</u> l'objet est au repos $\implies \vec{v} = \vec{0} \ \forall t \implies \vec{a} = \vec{0} \implies \vec{F} = \vec{0}$

<u>Ex :</u> chariot sur rail à air

![[p3-chariot-rail.svg]]

<u>Liaisons :</u>
- Fil parfait : $T = T'$
- si pendant $\Delta t$ le contrepoids avance de $\Delta y$ selon $\vec{e}_y$, le chariot avance de $\Delta x = \Delta y$ selon $-\vec{e}_x$

$$\implies \frac{\Delta x}{\Delta t} = \frac{\Delta y}{\Delta t} \implies v_{M,x} = v_{m,y}$$
$$\implies a_{M,x} = a_{m,y}$$

À résoudre :
$$
\begin{aligned}
mg - T &= ma \\
T &= Ma \\
mg &= (m + M)a \implies a = \frac{m}{m + M}\, g
\end{aligned}
$$

---

### 3.3 Forces particulières

#### 3.3.1 Forces à distance

Sans lien matériel avec l'objet

**1) Gravitation** <span style="color:red">« les masses s'attirent »</span>

![[p3-gravitation.svg]]

Objet : $m$ — $m$ est attiré par $M$

$$\Vert\vec{F}\Vert = G\,\frac{M \cdot m}{r^2}$$
où $G \cong 6.67 \cdot 10^{-11} \ \mathrm{N\,m^2/kg^2}$ (constante de la gravitation universelle)

<u>ex :</u> la lune est attirée par la terre

![[p3-terre-lune.svg]]

<u>Cas particulier :</u> près de la surface de la terre, un objet $m$ subit le poids : $m\vec{g}$

Si le poids est la seule force exercée sur un objet,
$$\text{Newton : } \vec{F} = m\vec{a}$$
$$\cancel{m}\vec{g} = \cancel{m}\vec{a} \implies \vec{a}(t) = \vec{g} \ : \text{ c'est un MUA}$$

**2) Force électrique**

**3) Force magnétique**

#### 3.3.2 Forces de contact

Par lien matériel : traction (ex : tension dans un fil), poussée (ex : soutien), cisaillement (force tangentielle, ex : frottement).

<u>ex :</u> pendule simple

![[p3-pendule.svg]]

Objet : $m$
Forces : poids, tension
Newton : $\vec{T} + m\vec{g} = m\vec{a}$

<u>Remarque :</u> au point le plus bas : $\Vert\vec{T}\Vert > \Vert m\vec{g}\Vert$ car il y a un virage donc $\vec{a} \neq \vec{0}$

![[p3-pendule-bas.svg]]

<u>Ex :</u> bloc au repos sur un plan incliné

![[p3-plan-incline-repos.svg]]

Objet : $M$
Forces : poids, force de contact

$$M\vec{g} + \vec{C} = \vec{0} \ \text{(repos)}$$

<u>Remarque :</u> on peut décomposer $\vec{C}$ en force normale $\vec{S}$ (soutien) et tangentielle $\vec{F}$ (frottement) $\qquad \vec{C} = \vec{S} + \vec{F}$

![[p3-plan-incline-decomposition.svg]]

<u>Remarque :</u> si je fais non repos

$$\text{Newton : } M\vec{g} + \vec{S} + \vec{F} = M\vec{a}$$

$$
\begin{aligned}
&\text{Selon } \vec{e}_x : && +Mg\sin\alpha - F = Ma_x \\
&\text{Selon } \vec{e}_y : && -Mg\cos\alpha + S = Ma_y = 0 \ \text{(pas de mouvement)}
\end{aligned}
$$

Si $F$ est constant $(F = F_0)$, $\quad Mg\sin\alpha - F_0 = Ma_x$
$$\implies a_x = \text{constante} \qquad \underline{\text{MUA !}}$$

Si $F_0 = 0$ (pas de frottement) $\implies a_x = g\sin\alpha$

<u>Ex :</u> bloc sur un plan incliné et tiré par un fil

![[p3-plan-incline-fil.svg]]

Objet : bloc, masse : $M$
Forces : poids, tension, force de contact ($\vec{S}$ et $\vec{F}$)

$$
\begin{aligned}
&\text{Newton :} && M\vec{g} + \vec{F} + \vec{T} + \vec{S} = M\vec{a} && \text{(vecteurs)} \\
&\text{Selon } \vec{e}_x : && -F + T\cos\beta - Mg\sin\alpha = Ma_x && \text{(scalaires)} \\
&\text{Selon } \vec{e}_y : && -Mg\cos\alpha + S + T\sin\beta = Ma_y &&
\end{aligned}
$$

<u>Remarque :</u> si $\vec{F} = \vec{F}_0$ = constant
$$\iff a = \frac{1}{M}\big(-Mg\sin\alpha + T\cos\beta - F_0\big) = \text{constant}$$
MUA → équations horaires

<u>Ex :</u> chariot sur rail + fil + contrepoids

![[p3-chariot-contrepoids.svg]]

La gravitation fait descendre $m$ et tend le fil, tirant le bloc.
Cherchons les accélérations de $M$ et $m$.

**Objet $m$ :**
- Forces : poids, tension
- Newton : $m\vec{g} + \vec{T} = m\vec{a}_m \qquad$ (vecteur)
  - selon $\vec{e}_y$ : $mg - T = ma_m \qquad$ (scalaire)

**Objet $M$ :**
- Forces : poids, tension, support, (frottement négligeable)
- Newton : $\vec{0} + \vec{T}' + \vec{0} = M\vec{a}_M$
  - selon $\vec{e}_x$ : $0 + T' + 0 = Ma_M$

<u>Ex :</u> force de rappel, bloc suspendu à un ressort

![[p3-ressort.svg]]

Ressort à vide, $l_0$ : longueur naturelle

Objet : bloc
Forces : poids, rappel
Newton : $m\vec{g} + \vec{T} = \vec{0}$
$$m\vec{g} + (-k\vec{d}) = \vec{0}$$

Selon $\vec{e}_y$ : **variante 1** $\big(d = \Vert\vec{d}\Vert\big)$
$$mg - kd = 0 \implies d = \frac{mg}{k} > 0 \quad \text{ok.}$$

<u>Remarque :</u> on sait que $\vec{d}$ est vers le bas

**Variante 2** $\big(\vec{d} = d\,\vec{e}_y\big) \qquad d \in \mathbb{R}$ (on ne sait pas le sens de la déformation)
$$
\begin{aligned}
mg\,\vec{e}_y - kd\,\vec{e}_y &= \vec{0} \\
mg - kd &= 0 \\
d &= \frac{mg}{k} > 0
\end{aligned}
$$

<u>Rem :</u> le calcul dit que notre hypothèse est vraie ($\vec{d}$ vers le bas)

---

### 3.4 Quantité de mouvement

<u>Question :</u> dans $\vec{F} = m\vec{a}$, $\vec{a}$ est l'accélération d'un point matériel (objet réduit à un point).
Comment faire mieux :
objet = ensemble de points matériels

<u>Remarque :</u>
$$\vec{F} = m\vec{a} = m\,\frac{d\vec{v}}{dt} = \frac{d}{dt}(m\vec{v})$$

Quantité de mouvement de l'objet choisi :

$$\boxed{\vec{p} = m\vec{v}} \qquad \text{unité : } \frac{\mathrm{kg \cdot m}}{\mathrm{s}}$$

C'est une « mise en commun » de la masse et de la vitesse

<u>ex :</u> 2 chariots

![[p3-deux-chariots.svg]]

Exerçons la même force de freinage : la même loi d'évolution.
$$\vec{F} = \frac{d}{dt}\vec{p}$$

En particulier, le temps jusqu'à l'arrêt est le même

<u>Remarque :</u> $\vec{a}_1 \neq \vec{a}_2$

Pour un objet formé de plusieurs points matériels :

![[p3-points-materiels.svg]]

> [!important] Quantité de mouvement
> $$\vec{p} = \vec{p}_1 + \vec{p}_2 + \vec{p}_3 + \dots + \vec{p}_n = m_1\vec{v}_1 + m_2\vec{v}_2 + \dots + m_n\vec{v}_n$$

Individuellement :
$$
\begin{aligned}
\vec{F}_1 &= m_1\vec{a}_1 = \dot{\vec{p}}_1 \\
\vec{F}_2 &= m_2\vec{a}_2 = \dot{\vec{p}}_2 \\
&\ \ \vdots \\
\vec{F}_n &= m_n\vec{a}_n = \dot{\vec{p}}_n
\end{aligned}
$$

Somme :
$$
\begin{aligned}
\vec{F} &= \vec{F}_1 + \dots + \vec{F}_n \\
\vec{F} &= \dot{\vec{p}}_1 + \dots + \dot{\vec{p}}_n = \dot{\vec{p}}
\end{aligned}
$$

soit
$$\boxed{\vec{F} = \dot{\vec{p}}}$$

> <span style="color:orange">« La somme de toutes les forces exercées sur toutes les parties de l'objet donne l'évolution de la quantité de mouvement de l'objet »</span>

---

### 3.5 3<sup>e</sup> loi de Newton (« action-réaction »)

On observe que la force qu'une partie 1 d'un objet exerce sur une partie 2 $(\vec{F}_{1 \to 2})$ et la force que 2 exerce sur 1 $(\vec{F}_{2 \to 1})$ sont
- de même support
- opposées
- de même norme

$$\iff \vec{F}_{1 \to 2} + \vec{F}_{2 \to 1} = \vec{0}$$

![[p3-action-reaction.svg]]

Ainsi, dans la somme de toutes les forces, les forces exercées entre les parties de l'objet considéré (forces internes) s'annulent deux à deux. Ne restent que les forces extérieures.

Newton :
$$\boxed{\vec{F}_{ext} = \dot{\vec{p}}}$$

<u>Ex :</u> choc sur rail à air

Objet : les 2 chariots
Forces (ext) : poids, soutien

- avant le choc :

  ![[p3-choc-avant.svg]]

- pendant le choc :

  ![[p3-choc-pendant.svg]]

  <u>Remarque :</u> les forces entre $m_1$ et $m_2$ s'annulent

- après le choc

  ![[p3-choc-apres.svg]]

À chaque instant (avant, pendant et après le choc) :
$$\vec{F}^{ext} = \vec{0}$$

Newton :
$$\vec{F}^{ext} = \dot{\vec{p}} = \vec{0} \implies \vec{p} = \text{constante}$$
(la quantité de mouvement est conservée)

En particulier : $\vec{p}(\text{avant}) = \vec{p}(\text{après})$
$$\iff m_1\vec{v}_1 + m_2\vec{v}_2 = m_1\vec{v}_1\,' + m_2\vec{v}_2\,'$$

par exemple : $m_1 = m_2 = m$ et $\vec{v}_2 = \vec{0}$ et ils restent collés
$$m\vec{v} + \vec{0} = (m + m)\vec{v}\,' \implies \vec{v}\,' = \frac{1}{2}\vec{v}$$

---

### 3.6 Centre de masse

Dans $\vec{F} = m\vec{a}$, $\vec{a}$ est l'accélération de l'objet

Précisons l'idée pour un vrai objet.

<u>Remarque :</u> la quantité de mouvement est
$$
\begin{aligned}
\vec{p} &= m_1\vec{v}_1 + \dots + m_n\vec{v}_n \\
&= m_1\dot{\vec{r}}_1 + \dots + m_n\dot{\vec{r}}_n \\
&= \frac{d}{dt}\Big(\underbrace{m_1\vec{r}_1 + \dots + m_n\vec{r}_n}_{\color{red} m\,\vec{r}_{cm}}\Big)
\end{aligned}
$$

> [!definition] Centre de masse
> $$\vec{r}_{cm} = \frac{m_1\vec{r}_1 + \dots + m_n\vec{r}_n}{m}$$
> $m = m_1 + \dots + m_n$ ← masse de l'objet

C'est la position moyenne pondérée par les masses.

<u>ex :</u> haltère symétrique

![[p3-haltere-symetrique.svg]]

Objet : $m$ et $m$
$$\vec{r}_{cm} = \frac{m\vec{r}_1 + m\vec{r}_2}{2m} = \frac{1}{2}\big(\vec{r}_1 + \vec{r}_2\big)$$

<u>ex :</u> haltère asymétrique

![[p3-haltere-asymetrique.svg]]

Objet : $m_1$ et $m_2$
$$\vec{r}_{cm} = \frac{m\vec{r}_1 + 2m\vec{r}_2}{3m} = \frac{1}{3}\vec{r}_1 + \frac{2}{3}\vec{r}_2$$

<u>ex :</u> plaque homogène rectangulaire

![[p3-plaque-rectangle.svg]]

Objet : plaque
CM : centre géométrique (intersection des diagonales)

<u>ex :</u> plaque homogène triangulaire

![[p3-plaque-triangle.svg]]

Objet : triangle
CM : intersection des médianes

<u>Remarque :</u> pour un objet compliqué, on peut chercher le CM des parties et ensuite le CM des CMs trouvés.

<u>ex :</u> plaque + boule.

![[p3-plaque-boule.svg]]

Plaque $m$, boule $m$

Ensuite

![[p3-plaque-boule-cm.svg]]

↳ La deuxième loi de Newton devient, avec :
$$\vec{p} = \frac{d}{dt}\big(m \cdot \vec{r}_{cm}\big) = m \cdot \vec{v}_{cm}$$
$$\vec{F}_{ext} = \dot{\vec{p}} = m\vec{a}_{cm}$$

<u>ex :</u> haltère symétrique lancé

![[p3-haltere-lance.svg]]

Objet : haltère
Forces : poids
Newton : $m\vec{g} + m\vec{g} = 2m\,\vec{a}_{cm}$
$\quad$ ↳ $\vec{a}_{cm} = \vec{g}$ (le cm est en chute libre)

Pas de mouvement du centre de masse = pas d'accélération de l'objet !
Quantité de mouvement = 0 globalement.

---

### 3.7 Pression

Considérons une face de taille $S$ d'un objet et une force $\vec{F}$ exercée sur $S$

![[p3-pression-decomposition.svg]]

($\vec{k}$ : vecteur unitaire indiquant la direction)

Décomposons $\vec{F}$
- $\vec{F} = \vec{F}_n + \vec{F}_t$
- $\vec{F}_n$ : force normale (de compression)
- $\vec{F}_t$ : force tangentielle (cisaillement)

La répartition moyenne de $\vec{F}_n$ sur $S$ est la pression moyenne.

> [!important]
> $$p_{moy} = \frac{\Vert\vec{F}_n\Vert}{S} \qquad \text{Unité : } \mathrm{N/m^2} = \mathrm{Pa} \ \text{« Pascal »}$$

<u>**Exemple :**</u> Une personne de $m = 64 \ \mathrm{kg}$ se tient sur un talon de surface $S = 16 \ \mathrm{cm^2}$. Quelle est la pression sur le talon ?

![[p3-talon.svg]]

Objet : personne
Forces : poids, soutien

$$p_{moy} = \frac{\Vert\vec{N}\Vert}{S} = \frac{\Vert m\vec{g}\Vert}{S} = \frac{64 \ \mathrm{kg} \cdot 10 \ \mathrm{m/s^2}}{16 \cdot 10^{-4} \ \mathrm{m^2}} = 4 \cdot 10^5 \ \mathrm{Pa}$$

<u>Remarque :</u> en remplaçant le talon par $S' = 1 \ \mathrm{cm^2}$, la nouvelle pression (poids reste le même) vaut
$$p'_{moy} = \frac{640 \ \mathrm{N}}{10^{-4} \ \mathrm{m^2}} = 64 \cdot 10^5 \ \mathrm{Pa}$$

<u>**Exemple :**</u> La pression de l'air est de l'ordre de
$$0.95 \cdot 10^5 \ \mathrm{Pa} < p_{air} < 1.05 \cdot 10^5 \ \mathrm{Pa}$$

<u>Remarque :</u> autres unités
$$
\begin{aligned}
1 \ \mathrm{atm} &= 1.013 \cdot 10^5 \ \mathrm{Pa} \\
1 \ \mathrm{bar} &= 10^5 \ \mathrm{Pa} \\
760 \ \mathrm{mmHg} &= 1 \ \mathrm{atm}
\end{aligned}
$$

<u>**Exemple :**</u> boîte + piston + air + gaz enfermé

![[p3-piston.svg]]

Que vaut $p_{gaz}$ ?

<u>Remarque :</u> il faut choisir un objet subissant la force de pression du gaz

Objet : piston

![[p3-piston-forces.svg]]

<span style="color:cyan">$\vec{F}_{gaz}$</span> compense <span style="color:red">$\vec{F}_{air}$ et $m\vec{g}$</span>

Forces : poids, forces de pression (air et gaz)
Newton : $m\vec{g} + \vec{F}_{air} + \vec{F}_{gaz} = \vec{0}$

$$
\begin{aligned}
\text{Selon } \vec{e}_y : \quad -mg - F_{air} + F_{gaz} = 0 &\iff -mg - p_{air}S + p_{gaz}S = 0 \\
\text{avec } F_{air} = p_{air} \cdot S \qquad &\iff p_{gaz} = p_{air} + \frac{mg}{S} > p_{air}
\end{aligned}
$$

Localement, la force de pression n'est pas nécessairement répartie uniformément sur la surface.

![[p3-pression-locale.svg]]

Divisons $S$ en petits morceaux $\Delta S$ subissant une partie $\Delta\vec{F}_n$ de la force de pression $\vec{F}_n$

Pression (locale) à la position $\vec{r}$
$$p(\vec{r}) = \lim_{\Delta S \to 0} \frac{\Vert\Delta\vec{F}_n\Vert}{\Delta S} \qquad \text{« pression à la position } \vec{r} \text{ »}$$

<u>Remarque :</u> clairement,
$$\vec{F}_n = \Delta\vec{F}_{n,\vec{r}_1} + \Delta\vec{F}_{n,\vec{r}_2}$$
$$S = \Delta S_1 + \Delta S_2$$

<u>Remarque :</u> si la pression est partout la même, alors $p(\vec{r}) = p = p_{moy}$ et
$$\boxed{\Vert\vec{F}_n\Vert = pS}$$

<u>**Exemple :**</u> estimation de la vitesse de la balle de ping-pong dans le canon à vide

![[p3-canon-vide.svg]]

Objet : balle
Forces : poids, soutien, force de l'air
Newton : $m\vec{g} + \vec{S} + \vec{F}_{air} = m\vec{a}$
Selon $\vec{e}_x$ : $F_{air} = m \cdot a \ \big| \ p_a S = ma$
$$\hookrightarrow a = \frac{p_a \pi r^2}{m}$$

<u>Remarque :</u> les forces de pression se compensent verticalement et « avant-arrière »

Selon $\vec{e}_x$ : projections $\implies S$ = section de table

<u>Application numérique :</u>
$$a = \frac{10^5 \ \mathrm{Pa} \cdot \pi \cdot (2 \cdot 10^{-2} \ \mathrm{m})^2}{2.8 \cdot 10^{-3}} \cong \dots = \text{constante.}$$
$$\implies v(t) = at \qquad x(t) = \frac{1}{2}at^2$$

Temps de vol : $t_v$, $\ x(t_v) = L \implies t_v$
$$\implies v_{sortie} = v(t_v) = \dots$$

<u>**Exemple :**</u> le chariot + boulet

![[p3-chariot-boulet.svg]]

Objet : chariot + boulet
Forces : poids, soutien du sol
Newton : $(m + M)\vec{g} + \vec{S} = \dot{\vec{p}} = (m + M)\vec{a}_{cm}$

Selon $\vec{e}_x$ : $0 = \dot{p}_x = (m + M)a_{cm,x}$
$$\implies p_x(t) = \text{constante} = 0 = \underset{\color{red} p_{b,x}}{mv_m} + \underset{\color{red} p_{c,x}}{Mv_M}$$
$$\implies m \cdot v_m = -Mv_M \quad \text{(vitesses opposées)}$$

ou
$$\implies a_{cm,x} = 0 \implies v_{cm,x} = \text{constante} = 0$$
$$\implies x_{cm} = \text{constante} \quad \big(\text{le CM est au repos selon } \vec{e}_x\big)$$

Selon $\vec{e}_y$ : $(m + M)g - S = (m + M)a_{cm,y}$

rappel :
$$y_{cm,y} = \frac{my_m + My_M}{m + M} \qquad v_{cm,y} = \frac{mv_m + Mv_M}{m + M}$$
$$a = \frac{ma_{m,y} + Ma_{M,y}}{m + M} \neq 0 \quad \text{car le boulet descend}$$
$$\implies (m + M)g > S$$

**Objet : boulet**

![[p3-boulet-forces.svg]]

- Forces : poids, soutien du chariot
- Newton : $m\vec{g} + \vec{N} = m\vec{a}_m$
- <u>Remarque :</u> $\vec{a}_m$ est à gauche et vers le bas

**Objet : chariot**

![[p3-chariot-forces.svg]]

- Forces : poids, soutien du sol, soutien du boulet
- Newton : $M\vec{g} + \vec{S} + (-\vec{N}) = M\vec{a}_M$
- <u>Remarque :</u> $\vec{a}_M$ est vers la droite

<u>Remarque :</u> addition
$$m\vec{g} + \vec{N} + M\vec{g} + \vec{S} + (-\vec{N}) = m \cdot \vec{a}_m + M\vec{a}_M$$
$$\iff (m + M)\vec{g} + \vec{S} = (m + M)\vec{a}_{cm} \qquad \color{red}\text{Déf. du centre de masse}$$

---

### 3.8 Hydrostatique

#### 3.8.1 Définition d'un fluide

![[p3-fluide-deformation.svg]]

- <u>Solide :</u> si on relâche la contrainte, la déformation disparaît (élasticité)
- <u>Fluide :</u> il s'adapte à la contrainte et se déforme de manière permanente. La contrainte n'est plus nécessaire pour cette déformation.

<u>Remarque :</u> si la contrainte est maintenue, le fluide continue à se déformer.

#### 3.8.2 Forces dans un fluide au repos

Comme le fluide est au repos, il ne peut pas y avoir de forces tangentielles !

![[p3-fluide-forces.svg]]

Il n'y a donc que des forces normales : force de pression

Impossible ! Sinon la force $-\vec{F}_t$ déformerait le fluide.

> [!important] <u>Loi de Pascal</u>
> la norme de la force normale exercée sur une surface $S$ est indépendante de l'orientation

![[p3-pascal.svg]]

$$\text{avec } \Vert\vec{F}_n\Vert = \Vert\vec{F}_n\,'\Vert = \Vert\vec{F}_n\,''\Vert$$

On peut donc définir la pression en tout point d'un fluide :
$$p = \frac{\Vert\vec{F}_n\Vert}{S} \qquad (\text{pour } S \to 0)$$

#### 3.8.3 Loi de l'hydrostatique

Dans un fluide au repos, soumis à la gravitation, considérons un morceau du fluide

![[p3-hydrostatique.svg]]

Objet : morceau du fluide, de base $S$ entre les niveaux $h_1$ et $h_2$
Forces : poids, forces de pression

$$\text{Newton : } m_{fl}\,\vec{g} + \underbrace{\cancel{\vec{F}_{latérales}}}_{\vec{0} \text{ (par symétrie)}} + \vec{F}_{sous} + \vec{F}_{sur} = \vec{0}$$

Selon $\vec{e}_h$ :
$$-m_{fl}\,g + F_{sous} - F_{sur} = 0$$
$$-\underset{\substack{\uparrow \\ \text{masse volumique du fluide}}}{\rho_{fl}} \cdot \cancel{S} \cdot (h_2 - h_1)\,g + \underset{\substack{\uparrow \\ \text{pression au niveau } h_1}}{p(h_1)} \cdot \cancel{S} - p(h_2) \cdot \cancel{S} = 0$$

$$\implies \boxed{p(h_1) - p(h_2) = \rho_{fl} \cdot g \cdot (h_2 - h_1)} \qquad \text{si } \rho_{fl} \text{ est constante.}$$

La différence de pression entre les niveaux $h_1$ et $h_2$ est due au poids du fluide (par unité de surface) entre ces niveaux.

![[p3-recipient-isobares.svg]]

$$p(A) = p(E) < p(B) < p(C) = p(D)$$

En particulier dans un même fluide, la pression est la même à une même hauteur

> [!definition] <u>Isobare</u>
> surface où la pression est la même partout.

<u>Ex :</u> 2 fluides (air + eau)

![[p3-deux-fluides.svg]]

Interface : $\underline{p(\text{air}) = p(\text{eau})}$ (équilibre)

$$
\begin{aligned}
\text{air :} \quad p(0) - p(h_A) &= \rho_{air}\,g\,(h_A - 0) \\
\text{eau :} \quad p(h_B) - p(0) &= \rho_{eau}\,g\,(0 - h_B)
\end{aligned}
$$

#### 3.8.4 Poussée d'Archimède

La pression augmente avec la profondeur $\implies$ un objet immergé subit une résultante de force de pression vers le haut : poussée d'Archimède.

![[p3-archimede-equivalence.svg]]

On peut donner une expression de la poussée d'Archimède

![[p3-archimede-fluide.svg]]

Objet : morceau du fluide au repos
Forces : poids, Archimède.
Newton : $m_{fl}\,\vec{g} + \vec{F}_A = \vec{0}$

Par conséquent,
$$\implies \vec{F}_A = -\underset{\substack{\text{masse} \\ \text{volumique}}}{\rho_{fl}}\,V_{obj}\,\vec{g}$$

Si on remplace le morceau de fluide par un autre objet de même volume (l'objet est donc immergé), la poussée d'Archimède reste la même !

> [!important]
> $$\implies \vec{F}_A = -\rho_{fl}\,V_{immergé}\,\vec{g}$$

<u>ex :</u> ballon de foire

![[p3-ballon.svg]]

Objet : ballon (gaz + membrane)
Forces : poids, Archimède, tension
Newton : $m_{ballon}\,\vec{g} + \vec{F}_A + \vec{T} = \vec{0}$

Selon $\vec{e}_y$ : $-m_{ballon}\,g + \rho_{air} \cdot V_{ballon} \cdot g - T = 0$
$$\implies T = \rho_{air} \cdot V_{ballon}\,g - m_{ballon} \cdot g$$

Si la masse de la membrane est négligeable $\quad m_{ballon} = \rho_{gaz}\,V_{ballon}$
$$\implies T = (\rho_{air} - \rho_{gaz})\,V_{ballon}\,g$$

Pour $T > 0$, il faut $\rho_{gaz} < \rho_{air}$ (+ léger que l'air)

![[p3-volume-immerge.svg]]

---

### 3.9 Deux intermèdes (check moodle 11 novembre)

---

### 3.10 Repère lié à la trajectoire

#### 3.10.1 Abscisse curviligne

Généralisation à une courbe $\Gamma$.

![[p3-abscisse-curviligne.svg]]

Pour repérer la position d'un point $P$ sur $\Gamma$, il faut choisir
- une origine $O \in \Gamma$
- un sens positif

La position est donnée par l'abscisse curviligne

$s \in \mathbb{R}$ : distance algébrique (avec signe) à l'origine $O$
- $s > 0$ : part en avant de $O$ par rapport à $\Gamma$
- $s < 0$ : part en arrière de $O$ par rapport à $\Gamma$

Au point $P$, on définit le repère $(\vec{e}_t, \vec{e}_n)$ tel que
- $\vec{e}_t$ est vers la direction de la trajectoire indiquant le sens $\oplus$

#### 3.10.2 Vitesse scalaire

En tout point, la vitesse est tangente à $\Gamma$ : on peut écrire
$$\vec{v} = v\,\vec{e}_t \qquad \text{car } \vec{v} \,/\!/\, \vec{e}_t$$

Donc $v \in \mathbb{R}$ est la vitesse le long de $\Gamma$, selon $\vec{e}_t$.
C'est la <u>vitesse scalaire</u>, la variation de l'abscisse curviligne par rapport au temps

> [!important]
> $$v = \lim_{\Delta t \to 0} \frac{\Delta s}{\Delta t} = \dot{s}$$

![[p3-vitesse-scalaire.svg]]

<u>Rem :</u> $\Vert\vec{v}\Vert = |v|$

<u>ex :</u> pendule simple

![[p3-pendule-trois-cas.svg]]

| à droite, en montée | à droite, en descente | à gauche, en descente |
| :-: | :-: | :-: |
| $s > 0$, $v > 0$ | $s > 0$, $v < 0$ | $s < 0$, $v > 0$ |

<u>ex :</u> trajet Lausanne – Evian

![[p3-lausanne-evian.svg]]

Durée $= \Delta t = 1.5 \ \mathrm{h}$

- vitesse moyenne
  $$\vec{v}_{moy} = \frac{\Delta\vec{r}}{\Delta t} \qquad \text{et} \qquad \Vert\vec{v}_{moy}\Vert = \frac{\Vert\Delta\vec{r}\Vert}{\Delta t} = \frac{15 \ \mathrm{km}}{1.5 \ \mathrm{h}} = 10 \ \mathrm{km/h}$$
- vitesse scalaire moyenne
  $$v_{scal\,moy} = \frac{\Delta s}{\Delta t} = \frac{120 \ \mathrm{km}}{1.5 \ \mathrm{h}} = 80 \ \mathrm{km/h}$$

#### 3.10.3 Accélération tangentielle et normale

![[p3-acceleration-tn.svg]]

En tout point $P \in \Gamma$, l'accélération se décompose en
$$\boxed{\vec{a} = \vec{a}_t + \vec{a}_n}$$

- $\vec{a}_t \,/\!/\, \vec{e}_t \implies \vec{a}_t = a_t\,\vec{e}_t$

  Accélération selon $\vec{e}_t$ :
  $$\boxed{a_t = \lim_{\Delta t \to 0} \frac{\Delta v}{\Delta t} = \dot{v} = \ddot{s}}$$
  C'est l'accélération tangentielle : variation de la vitesse scalaire par rapport au temps.

  - $a_t > 0$ : $v \nearrow$

    ![[p3-at-positive.svg]]

  - $a_t < 0 \implies v \searrow$

  Donc $a_t$ indique si on va plus vite ou moins vite selon $\vec{e}_t$

- $\vec{a}_n \,/\!/\, \vec{e}_n$ : $\vec{a}_n = a_n\,\vec{e}_n$. $\quad a_n$ est l'accélération selon la normale. C'est <u>l'accélération normale</u>.

<u>Remarque :</u> le vecteur $\vec{a}_n$ est toujours vers l'intérieur du virage. $\vec{e}_n$ pas forcément.

On peut montrer que
$$|a_n| = \frac{v^2}{R}$$
où $v^2 = \vec{v} \cdot \vec{v} = \Vert\vec{v}\Vert^2$ et $R$ est le rayon du cercle osculateur de la trajectoire en $P$ (cercle qui ressemble le plus possible à la trajectoire.)

![[p3-cercle-osculateur.svg]]

<u>Ex :</u> condition de décrochement (perte de contact avec le support)

![[p3-decrochement.svg]]

Objet : $m$
Forces : poids, contact (support)
hyp : pas de frottements

Newton : $m\vec{g} + \vec{S} = m\vec{a}$

Perte de contact lorsque $\vec{S} = \vec{0}$

Comme $\vec{S} \,/\!/\, \vec{e}_n$, on choisit le repère $(\vec{e}_t, \vec{e}_n)$
$$
\begin{aligned}
\vec{e}_t &: \quad +mg\sin\alpha = ma_t \\
\vec{e}_n &: \quad +mg\cos\alpha - S = ma_n
\end{aligned}
$$

Au décrochement $D$ : $S = 0 \qquad mg\cos\alpha_D = m\,\dfrac{v_D^2}{R}$

relation entre position et vitesse au décrochement.

<u>ex :</u> pendule simple

![[p3-pendule-tn.svg]]

$s = L\alpha$ pour $\forall t$

Objet : $m$
Forces : poids, tension
Newton : $m\vec{g} + \vec{T} = m\vec{a}$
$$\vec{e}_t : \quad -mg\sin\alpha = ma_t = m\dot{v} = m\ddot{s} = mL\ddot{\alpha}$$

<u>rem :</u> on cherche la fonction du temps $\alpha(t)$ qui vérifie cette équation. On a aussi le mouvement du pendule. Pas facile…

$$
\begin{aligned}
\vec{e}_n : \quad -mg\cos\alpha + T &= ma_n = m\frac{v^2}{L} \\
\implies T &= mg\cos\alpha + m\frac{v^2}{L}
\end{aligned}
$$

<u>rem :</u> à la verticale $\alpha = 0 \qquad T = mg + m\dfrac{v_0^2}{L} > mg$ !

#### 3.10.4 Mouvement circulaire (fait en séance d'exos)

![[p3-mouvement-circulaire.svg]]

> [!important]
> $$s(t) = R\,\varphi(t) \quad \forall t$$
> relation entre arc (abscisse curviligne) et angle

$$\implies \boxed{v = R\,\omega \quad \forall t}$$
- $v = \dot{s}$ : vitesse scalaire $(\mathrm{m/s})$
- $\omega = \dot{\varphi}$ : vitesse angulaire $(\mathrm{rad/s})$

$$\implies \boxed{a_t = R\,\gamma \quad \forall t}$$
- $a_t = \dot{v} = \ddot{s}$ : accélération tangentielle $(\mathrm{m/s^2})$
- $\gamma = \dot{\omega} = \ddot{\varphi}$ : accélération angulaire $(\mathrm{rad/s^2})$

Objet $m$

$$
\begin{aligned}
&\text{Newton :} && \vec{F} = \vec{F}_t + \vec{F}_n = m\big(\vec{a}_t + \vec{a}_n\big) = m\vec{a} \\
&\text{Selon } \vec{e}_t : && F_t = ma_t = mR\gamma \\
&\text{Selon } \vec{e}_n : && F_n = ma_n = m\frac{v^2}{R} = mR\omega^2
\end{aligned}
$$

<u>ex :</u> un coureur sur piste circulaire, allant de plus en plus vite régulièrement : $F_t = ma_t$ = constante

![[p3-coureur.svg]]

$$
\begin{aligned}
a_t &= R\gamma = \text{constante} \\
\gamma(t) &= \gamma_0 = \text{constante} \\
\implies \omega(t) &= \gamma_0(t - t_0) + \omega_0 \\
\implies \varphi(t) &= \frac{1}{2}\gamma_0(t - t_0)^2 + \omega_0(t - t_0) + \varphi_0
\end{aligned}
$$

pour les conditions initiales $\omega(t_0) = \omega_0$ et $\varphi(t_0) = \varphi_0$

<u>Remarque :</u> si 2 coureurs $A$ et $B$ se rattrapent
$$\varphi_A(t_r) = \varphi_B(t_r) + k\,2\pi \qquad k \in \mathbb{Z}$$

<u>**Exemple**</u> bille sur rail circulaire en rotation.

Vue de côté

![[p3-bille-cote.svg]]

- <u>Remarque :</u> plus $\omega_0$ est important plus $\alpha$ est grand
- <u>Remarque :</u> la bille décrit un cercle horizontal de rayon $r = R\sin\alpha$

Vue du dessus

![[p3-bille-dessus.svg]]

Objet : bille
Forces : poids, soutien
Newton : $m\vec{g} + \vec{S} = m\vec{a}$

$$
\begin{aligned}
&\text{Selon } \vec{e}_t : && -mg + S\cos\alpha = ma_t = 0 \\
& && \implies S\cos\alpha = mg && \textcircled{1} \\
&\text{Selon } \vec{e}_n : && S\sin\alpha = ma_n = mr\,\omega_0^2 = mR\sin\alpha\,\omega_0^2 \\
& && \implies \underbrace{S\sin\alpha}_{} = mR\underbrace{\sin\alpha}_{}\,\omega_0^2 && \textcircled{2}
\end{aligned}
$$

peuvent devenir $0$ → ne pas les multiplier.

Éliminons $S$ par quotient :
$$\frac{\cancel{S}\sin\alpha}{\cancel{S}\cos\alpha} = \frac{\cancel{m}R\sin\alpha\,\omega_0^2}{\cancel{m}g} \iff \sin\alpha\left[\frac{1}{\cos\alpha} - \frac{R\omega_0^2}{g}\right] = 0$$

Solutions :
- $\sin\alpha = 0 \qquad$ <u>Rem :</u> indépendant de $\omega_0$ !
- $\left[\dfrac{1}{\cos\alpha} - \dfrac{R\omega_0^2}{g}\right] = 0 \iff \cos\alpha = \dfrac{g}{R\omega_0^2} \qquad$ solution si $\dfrac{g}{R\omega_0^2} \leq 1 \iff \omega_0^2 \geq \dfrac{g}{R}$

Donc
- 2 solutions si $\omega_0^2 \geq \dfrac{g}{R}$
  - $\cos\alpha = \dfrac{g}{R\omega_0^2} \qquad$ stable
  - $\alpha = 0 \qquad$ instable $\qquad$ <span style="color:orange"><u>Rem !</u> $S = mg$</span>
- 1 solution si $\omega_0^2 < \dfrac{g}{R}$ :
  - $\alpha = 0$

> <span style="color:orange"><u>Rem :</u> $S\cos\alpha = mg \implies S\,\dfrac{g}{R\omega_0^2} = mg \implies S = mR\omega_0^2 > mg$</span>
