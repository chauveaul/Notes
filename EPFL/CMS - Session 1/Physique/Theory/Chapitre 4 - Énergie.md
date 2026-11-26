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
