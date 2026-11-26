---
cours: Physique
chapitre: 4
source: "Chapitre 4 - Physique.pdf"
tags: [physique, chapitre-4]
---

# 4. Énergie

### 4.1 Exemple de conservation d'énergie

<u>ex :</u> pendule simple

![[p4-pendule.svg]]

Objet : bille
$$h \propto \frac{1}{v}$$

Loi de conservation (expérience ou par calcul)
$$\frac{1}{2}mv^2 + mgh = \text{constante}$$

On montrera cela comme conséquence de Newton.

Dans un système considéré, on peut calculer une grandeur abstraite, un nombre appelé <u>énergie</u>, noté $E$. Si le système est isolé (sans échange avec son environnement), l'énergie est conservée.

- **Système isolé**

  ![[p4-systeme-isole.svg]]

  Entre deux instants $t_1$ et $t_2$ $(t_1 < t_2)$, la variation de l'énergie est nulle
  $$\Delta E = E(t_2) - E(t_1) = 0$$

- **Système non isolé**

  ![[p4-systeme-non-isole.svg]]

  $$\Delta E = E(t_2) - E(t_1) \neq 0$$

<u>Convention :</u>
- $\Delta E > 0$, alors le système a reçu de l'énergie
- $\Delta E < 0$, alors le système a perdu de l'énergie

<u>Formes d'énergies :</u>
- énergie cinétique (associée au mouvement)
- énergie potentielle de gravitation
- énergie potentielle électrique
- énergie potentielle élastique
- énergie nucléaire
- énergie électromagnétique (ex. lumière)
- énergie chimique
- énergie thermique.

<u>**Exemple :**</u> bille sur rail

![[p4-bille-rail.svg]]

Bille : $m\vec{g} + \vec{S} = m\vec{a}$

En particulier pour $A$ et $B$
$$\frac{1}{2}mv_A^2 + mgh_A = \frac{1}{2}mv_B^2 + mgh_B \implies \frac{1}{2}mv_B^2 = mgh_A$$

<u>Remarque :</u> $v_B^2$ est indépendant de la forme de la trajectoire !

<u>ex :</u> choc élastique, inélastique, mou

Juste avant le choc d'une balle sur le sol

![[p4-choc-balle.svg]]

| | |
| :-- | :-- |
| avant | $E_{cin} = \dfrac{1}{2}mv^2$ |
| après | $E'_{cin} = \dfrac{1}{2}mv'^2$ |

En général, de l'énergie est perdue pendant le choc : $E'_{cin} \leq E_{cin}$
- $E'_{cin} = E_{cin}$ : choc élastique
- $0 < E'_{cin} < E_{cin}$ : choc inélastique
- $E'_{cin} = 0$ : choc mou

---

### 4.2 Énergie cinétique et travail

#### 4.2.1 Théorème de l'énergie cinétique

Considérons un objet en mouvement

![[p4-objet-mouvement.svg]]

L'évolution du centre de masse est donnée par $m\vec{a}_{cm} = \vec{F}_{ext}$

Effectuons le produit scalaire avec $\vec{v}_{cm}(t)$
$$m\vec{v}_{cm} \cdot \vec{a}_{cm} = \vec{F}_{ext} \cdot \vec{v}_{cm}$$

<u>Remarque (importante) :</u> toute description selon $\vec{e}_n$ disparaît !

En effet :
$$\vec{v} \cdot \vec{a} = \vec{v} \cdot (\vec{a}_t + \vec{a}_n) = \vec{v} \cdot \vec{a}_t + \underbrace{\vec{v} \cdot \vec{a}_n}_{0} = \vec{v} \cdot \vec{a}_t$$
$$\vec{v} \cdot \vec{F} = \vec{v} \cdot (\vec{F}_t + \vec{F}_n) = \vec{v} \cdot \vec{F}_t$$

C'est une projection selon $\vec{e}_t$

Avec l'égalité (cf. intermède)
$$\frac{d}{dt}v^2 = \frac{d}{dt}(\vec{v} \cdot \vec{v}) = 2\vec{v} \cdot \dot{\vec{v}} = 2\vec{v} \cdot \vec{a}$$

pour avoir
$$\frac{d}{dt}\left(\frac{1}{2}mv_{cm}^2\right) = \vec{F}_{ext} \cdot \vec{v}_{cm}$$

> [!definition] Énergie cinétique du CM
> $$E_{cin,cm} = \frac{1}{2}mv_{cm}^2$$
> Unité : $\dfrac{\mathrm{kg\,m^2}}{\mathrm{s^2}} = \mathrm{J} = \mathrm{N\,m}$ « joule »

Donc $\dfrac{d}{dt}E_{cin,cm} = \vec{F} \cdot \vec{v}_{cm}$, la variation par rapport au temps de l'énergie cinétique du CM est donnée par $\vec{F}_{ext} \cdot \vec{v}_{cm}$

Signe de $\vec{F}_{ext} \cdot \vec{v}_{cm}$ pour une force donnée

- ![[p4-force-avant.svg]]

  $\vec{F}$ est plutôt en avant : $\vec{F} \cdot \vec{v} > 0$
  $\implies \Vert\vec{v}_{cm}\Vert$ tend à augmenter
  $\implies E_{cin,cm}$ tend à augmenter

- ![[p4-force-arriere.svg]]

  $\vec{F}$ est plutôt en arrière : $\vec{F} \cdot \vec{v} < 0$
  $\implies E_{cin,cm}$ tend à diminuer

- ![[p4-force-perpendiculaire.svg]]

  $\vec{F}$ est $\perp \vec{v}_{cm}$ : $\vec{F} \cdot \vec{v}_{cm} = 0$
  $\implies \vec{F}$ ne contribue pas à modifier $E_{cin,cm}$

Dans le membre de droite $\vec{F}_{ext} \cdot \vec{v}_{cm}$, $\ \vec{v}_{cm} = \dfrac{d\vec{r}_{cm}}{dt}$ est le changement de position du CM par rapport au temps.
Pendant une petite durée $dt$, le CM se déplace de $d\vec{r}_{cm}$

![[p4-deplacement-dt.svg]]

$$d(E_{cin,cm}) = \vec{F}_{ext} \cdot d\vec{r}_{cm}$$

Le changement d'énergie cinétique du CM entre les instants $t$ et $t + dt$ est $dE_{cin,cm}$ et est donné par le travail ⭐ des forces extérieures.

> [!definition] Travail
> $$dW_{ext} = \vec{F}_{ext} \cdot d\vec{r}_{cm}$$

Donc pendant $dt$ $\qquad dE_{cin,cm} = dW_{ext}$

Pour le mouvement entre les instants $t_1$ (position 1) et $t_2$ (position 2), en additionnant les travaux (sommes)

![[p4-travail-trajet.svg]]

Travail des forces extérieures de 1 à 2 :
$$\boxed{W_{ext\,1 \to 2} = \int_1^2 dW_{ext} \underset{\color{cyan}\text{« somme »}}{=} \int_1^2 \vec{F}_{ext} \cdot d\vec{r}_{cm}}$$

Par conséquent, la variation de l'énergie cinétique du CM entre $t_1$ et $t_2$ est directement

> [!important] Théorème de l'énergie cinétique du CM
> $$E_{cin,cm}(2) - E_{cin,cm}(1) = W^{ext}_{1 \to 2}$$

> <span style="color:cyan">« $W$ est la contribution à changer l'énergie cinétique »</span>

<u>Ex :</u> bloc sur une descente

![[p4-bloc-descente.svg]]

Objet : bloc
Forces : poids, soutien, frottement

Théorème de l'énergie cinétique :
$$\frac{1}{2}mv_2^2 - \frac{1}{2}mv_1^2 = W_{1 \to 2}(m\vec{g}) + W_{1 \to 2}(\vec{S}) + W_{1 \to 2}(\vec{F})$$

- $$W_{1 \to 2}(\vec{S}) = \int_1^2 \underbrace{\vec{S} \cdot d\vec{r}}_{0 \text{ car } \vec{S} \perp \vec{v}} = 0 \qquad : \vec{S} \text{ ne travaille pas}$$
- $$W_{1 \to 2}(\vec{F}) = \int_1^2 \vec{F} \cdot d\vec{r} = \int_1^2 -F\,ds$$
  si $F = F_0$ = constante, $\quad W_{1 \to 2}(\vec{F}) = -F_0\underbrace{\int_1^2 ds}_{\text{longueur du trajet}} = -F_0\,l$
- $$W_{1 \to 2}(m\vec{g}) = \int_1^2 m\vec{g} \cdot d\vec{r} \underset{m\vec{g} \text{ constante}}{=} m\vec{g} \cdot \underbrace{\int_1^2 d\vec{r}}_{\substack{\text{déplacement} \\ \text{total (vecteur)}}} = m\vec{g} \cdot \Delta\vec{r}$$

<u>Remarque :</u> le travail du poids est indépendant de la forme de la trajectoire.

![[p4-travail-poids.svg]]

- prouver $W_{1 \to 2} = mgh_1 - mgh_2$

<u>**Cas particuliers**</u>

1) $\vec{F} \perp \vec{v} \ \forall t$ (force normale) : $W_{1 \to 2}(\vec{F}) = 0$
2) $\vec{F} = F_0\,\vec{e}_t$ avec $F$ constant $\forall t$ (force tangentielle de norme constante) : $W_{1 \to 2}(\vec{F}) = F_0\,l$ $\quad$ ($l$ : longueur du parcours)
3) $\vec{F} = m\vec{g}$ = constante : $W_{1 \to 2}(m\vec{g}) = mgh_1 - mgh_2$

<u>Remarque :</u> En général le travail d'une force dépend du trajet ! Parfois il ne dépend que des extrémités du trajet

#### 4.2.2 Forces conservatives

> [!definition]
> Une force est dite <u>conservative</u> si son travail de ① vers ② ne dépend pas du chemin de ① à ②

<u>**Exemple :**</u> le poids

![[p4-poids-conservatif.svg]]

Objet : $m$

Travail du poids $m\vec{g}$
$$W_{1 \to 2}(m\vec{g}) = \int_1^2 m\vec{g} \cdot d\vec{r}_{cm} \underset{m\vec{g} \,:\, \text{const}}{=} m\vec{g} \cdot \underbrace{\int_1^2 d\vec{r}_{cm}}_{\color{orange}{\Delta\vec{r} \,:\, \text{déplacement total}}} = m\vec{g} \cdot \Delta\vec{r} = m\vec{g} \cdot (\vec{r}_2 - \vec{r}_1)$$
$$= (-m\vec{g} \cdot \vec{r}_1) - (-m\vec{g} \cdot \vec{r}_2) \qquad \color{orange}{\text{indépendant du trajet !}}$$

<u>Remarque :</u>

![[p4-g-dot-r.svg]]

$$\vec{g} \cdot \vec{r} = -gh$$

Donc
$$\boxed{W_{1 \to 2}(m\vec{g}) = mgh_1 - mgh_2}$$

On peut donc écrire ce travail comme une différence de 2 termes similaires, associés aux extrémités du trajet.
On peut associer une énergie dite potentielle à tout point $\vec{r}$ !

> [!important] Énergie potentielle de gravitation
> $$E_{pot}(\vec{r}) = -m\vec{g} \cdot \vec{r} = mgh$$

C'est l'énergie associée au poids : définie en tout point à une constante arbitraire près (choix de l'origine).
Cette constante tombe dans la différence

![[p4-energie-pot-points.svg]]

$$
\begin{aligned}
E_{pot}(P) &= -m\vec{g} \cdot \vec{r}_P + \text{const} = mgh_P + \text{const} \\
E_{pot}(Q) &= mgh_Q + \text{const} \\
E_{pot}(R) &= mgh_R + \text{const}
\end{aligned}
$$

Alors, par exemple, le travail entre $Q$ et $R$ est directement
$$W_{1 \to 2} = E_{pot}(Q) - E_{pot}(R)$$

<u>**Ex.**</u> gravitation (cas général)

![[p4-gravitation-general.svg]]

Objet : $m$
$$\vec{F} = -G\,\frac{Mm}{r^2}\,\vec{e}_r$$

On peut calculer
$$W_{1 \to 2}(\vec{F}) = \int_1^2 \vec{F} \cdot d\vec{r}_{cm} = \dots = E_{pot}(1) - E_{pot}(2)$$

avec
$$\boxed{E_{pot}(\vec{r}) = -\frac{GMm}{r} + \text{const}}$$

<u>Remarque :</u> on a bien que $E_{pot}$ augmente si on s'éloigne de $M$
- cas $m\vec{g}$ : $E_{pot} = mgh + \text{const}$ et $E_{pot} \nearrow$ si $h \nearrow$
- cas général : pour const $= 0$

![[p4-epot-graphe.svg]]

<u>**Ex :**</u> force élastique

![[p4-ressort.svg]]

Objet : $m$
$$W_{1 \to 2}(\vec{F}) = \dots = \frac{1}{2}kd_1^2 - \frac{1}{2}kd_2^2$$
d'où
$$\boxed{E_{pot}(\vec{r}) = \frac{1}{2}kd^2 + \text{const}}$$

Le travail d'une force conservative s'écrit donc comme différence d'énergie potentielle.

> [!important]
> $$W_{1 \to 2}(\vec{F}^{\,cons}) = E_{pot}(1) - E_{pot}(2) \qquad \color{red}{⚠️ \text{ordre}}$$

Si toutes les forces sont conservatives (ou ne travaillent pas), on a
$$E_{cin,cm}(2) - E_{cin,cm}(1) = W_{1 \to 2}(\vec{F}^{\,cons}) = E_{pot}(1) - E_{pot}(2)$$
$$\iff \underbrace{E_{cin,cm}(2) + E_{pot}(2)}_{\color{orange}{E_{mec}(2)}} = \underbrace{E_{cin,cm}(1) + E_{pot}(1)}_{\color{orange}{E_{mec}(1)}}$$

D'où
$$\boxed{E_{mec} = E_{cin} + E_{pot}}$$
l'énergie mécanique est l'énergie associée au mouvement et à la position.

> [!important]
> Donc si toutes les forces sont conservatives ou ne travaillent pas,
> $$E_{mec} = \text{const} \quad \forall t$$

<u>Remarque :</u> d'où le terme de force conservative.

<u>**Ex :**</u> pendule simple

![[p4-pendule-energie.svg]]

Objet : $m$
Forces : $\left.\begin{aligned} &\text{poids (conservatif)} \\ &\text{tension (ne travaille pas)} \end{aligned}\right\} E_{mec} = \text{const}$
Newton : $m\vec{g} + \vec{T} = m\vec{a}$

Énergie mécanique conservée : $\dfrac{1}{2}mv^2 + mgh = \text{const} \ \forall t$

<u>**Ex.**</u> Vitesse de libération d'un astre : vitesse initiale pour qu'un objet ne retombe pas

![[p4-liberation.svg]]

Objet : $m$
Force : gravitation (conservative)

<u>Remarque :</u> $E_{mec} = \text{const} \ \forall t$ $\qquad$ cas limite : $\vec{v}_2 = \vec{0}$ à l'$\infty$ $\qquad$ choix const $= 0$

$$
\begin{aligned}
E_{mec}(1) &= \frac{1}{2}mv_1^2 + \left(-G\frac{Mm}{R}\right) \\
E_{mec}(2) &= 0 + 0 \\
\implies \frac{1}{2}mv_1^2 - G\frac{Mm}{R} &= 0 \implies v_1 = \sqrt{\frac{2GM}{R}}
\end{aligned}
$$

ex. pour la terre, $v_1 \cong 11 \ \mathrm{km/s}$
