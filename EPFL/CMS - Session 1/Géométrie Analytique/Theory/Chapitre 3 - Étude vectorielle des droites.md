---
cours: Géométrie Analytique
chapitre: 3
source: "Chapitre 3 - Géométrie Analytique.pdf"
tags: [geometrie-analytique, chapitre-3]
---

# Chapitre 3. Étude vectorielle des droites

### 1. Équations vectorielles

Soit $O$ un point, $\vec{u}$ et $\vec{v}$ <span style="color:red">$\neq \vec{0}$</span> deux vecteurs

$$
d:\ \underset{\text{point mobile}}{\vec{OM}} = \underbrace{\vec{u}}_{\text{constante}} + \underset{\text{« paramètre »}}{t}\,\underbrace{\vec{v}}_{\text{constante}}, \quad t \in \mathbb{R}
\qquad \Big)\ \text{équation vectorielle de } \underline{d}
$$

![[g3-equation-vectorielle.svg]]

Le couple
$$R = (\underset{\text{point de } d}{A},\ \underset{\substack{\text{vecteur directeur} \\ \text{non nul de } d}}{\vec{v}})$$
est appelé un <span style="color:red">repère</span> de $d$ et le paramètre $t$ l'<span style="color:red">abscisse</span> de $M$ dans $R$.

> [!important]
> $${\color{orange}\text{« } \frac{\vec{AM}}{\vec{v}} \text{ »}} \quad t = \pm \frac{\|\vec{AM}\|}{\|\vec{v}\|}$$
> ($+$ si $\vec{AM}$ et $\vec{v}$ de même sens, $-$ sinon)

#### <u>Exemples</u>

**(a)** On donne le triangle

![[g3-triangle.svg]]

Tracer sur le dessin :
$$d:\ \vec{BM} = \vec{BA} + t\vec{AC}, \quad t \in \mathbb{R}$$
$$g:\ \vec{BM} = \vec{CB} + t\vec{AB}, \quad t \in \mathbb{R}$$
$$h:\ \vec{AM} = \frac{1}{2}\vec{AB} + t\vec{BC}, \quad t \in \mathbb{R}$$

![[g3-ex-a-d.svg]]

![[g3-ex-a-gh.svg]]

▶ Localiser l'intersection $I$ de $g$ et $h$

$$\color{gray} g:\ \vec{BM} = \vec{CB} + t\vec{AB} \qquad h:\ \vec{AM} = \frac{1}{2}\vec{AB} + t\vec{BC}$$

<u>Solution.</u> On commence par observer $g$ et $h$ depuis le même point (par exemple $B$)

$$
\begin{cases}
g:\ \vec{BM} = \vec{CB} + t\vec{AB} \\[2mm]
h:\ \underbrace{\vec{BM}}_{\vec{BA} + \vec{AM}} = \dfrac{1}{2}\vec{BA} + t\vec{BC}
\end{cases}
$$

Pour $M = I$, on en déduit
$$\vec{BI} = \underbrace{\vec{CB} + t\vec{AB}}_{-t\vec{BA} - \vec{BC}} = \frac{1}{2}\vec{BA} + s\vec{BC}, \quad s \in \mathbb{R}$$

> Les temps de passages en $I$ peuvent être différents.

Comme $\vec{BA}$ et $\vec{BC}$ ne sont pas colinéaires, la décomposition de $\vec{BI}$ est unique.

$$
\begin{cases}
-t = 1/2 \\
-1 = s
\end{cases}
=
\begin{cases}
t = -0.5 \\
s = -1
\end{cases}
$$

**(b)** On donne

![[g3-mediane.svg]]

Écrire des équations vectorielles de $m$
$$m:\ \vec{CM} = \vec{CA} + t\vec{AI}, \quad t \in \mathbb{R}$$

> - $A$ : abscisse $0$
> - $I$ : abscisse $1$
> - milieu de $\|\vec{AI}\| = 0.5$

Les trois médianes du triangle $ABC$ s'intersectent au <span style="color:red">centre de gravité</span> $G$ de $ABC$. Il vérifie :
$$\vec{AG} = \frac{2}{3}\vec{AI} \quad \text{et aussi} \quad \vec{AG} + \vec{BG} + \vec{CG} = \vec{0}$$

**(c)** On donne :

![[g3-bissectrice.svg]]

Écrire des équations vectorielles pour $d$

<u>Solution</u> Les vecteurs directeurs de $d$ sont ceux du type :
$$\vec{v} = \lambda\vec{AB} + \mu\vec{AC} \quad \text{avec} \quad \|\lambda\vec{AB}\| = \|\mu\vec{AC}\|$$

> <span style="color:orange">On rééquilibre $\vec{AB}$ et $\vec{AC}$ pour créer un losange</span>

Voici quelques exemples d'équations :
$$d:\ \vec{AM} = t\Big(\underbrace{\frac{1}{c}\vec{AB}}_{\text{normé}} + \underbrace{\frac{1}{b}\vec{AC}}_{\text{normé}}\Big), \quad t \in \mathbb{R}$$

Les trois bissectrices s'intersectent en un point [Série 3 Ex 6.] appelé <span style="color:red">centre du cercle inscrit</span> à $ABC$.

---

### 2. Équations normales (2D)

Soit $O$ un point, $\vec{n} \neq \vec{0}$ un vecteur et $\alpha$ un réel.

$$d:\ \underset{\color{red}\substack{\text{Variable} \\ \text{« point mobile »}}}{\vec{OM}} \cdot \vec{n} = \alpha \quad : \text{ équation normale de } d \text{ depuis } O$$

$$\vec{OM} \cdot \vec{n} = 0 \implies \vec{OM} \perp \vec{n}$$
$$\vec{OM} \cdot \vec{n} = \alpha \iff P_{\vec{n}}(\vec{OM}) = \frac{\alpha}{\|\vec{n}\|^2}\vec{n}$$

![[g3-equation-normale.svg]]

La distance $O \to A$ vaut
$$\delta = \frac{|\alpha|}{\|\vec{n}\|}$$
$$\|\vec{OA}\| = \left\|\frac{\alpha}{\|\vec{n}\|^2} \cdot \vec{n}\right\|$$

#### <u>Exemples</u>

**a)** Cas particulier : $\vec{n}$ unitaire, $\|\vec{n}\| = 1$
$$\vec{OM} \cdot \vec{n} = \alpha \iff P_{\vec{n}}(\vec{OM}) = \alpha\vec{n}$$
$$\delta = |\alpha|$$

![[g3-normales-paralleles.svg]]

**b)** On donne

![[g3-rectangle-b.svg]]

<u>Tracer sur le dessin les droites suivantes</u>

| $\vec{AM} \cdot \vec{AB} = 0$ | $\vec{CM} \cdot \vec{AB} = 0$ | $\vec{AM} \cdot \overset{\color{cyan}\vec{n}}{\vec{AB}} = \overset{\color{cyan}\alpha}{2}$ |
| :-- | :-- | :-- |
| 1) passe par $A$ | 2) passe par $C$ | $\iff P_{\vec{AB}}(\vec{AM}) = \dfrac{2}{2^2}\vec{AB} = \dfrac{1}{2}\vec{AB}$ |
| $\vec{AM} \perp \vec{AB}$ | $\vec{CM} \perp \vec{AB}$ | |

Observons ② depuis $A$ :
$$\vec{AM} \cdot \vec{AB} = (\vec{AC} + \vec{CM}) \cdot \vec{AB} = \vec{AC} \cdot \vec{AB} + \vec{CM} \cdot \vec{AB}$$
$$= \underbrace{(\vec{AB} + \vec{BC}) \cdot \vec{AB}}_{\text{décalage d'observateur}}$$

Écrire des équations normales pour $d$ :

![[g3-rectangle-d.svg]]

$$d:\ \vec{CM} \cdot \vec{BD} = 0$$

Observateur en $A$ :
$$d:\ \vec{AM} \cdot \vec{BD} = \text{constante}$$
$$M = C \to\ = \vec{AC} \cdot \vec{BD}$$

On a donc
$$
\begin{aligned}
\vec{AC} \cdot \vec{BD} &= (\vec{AB} + \vec{AD}) \cdot (\vec{AD} - \vec{AB}) \\
&= \|\vec{AD}\|^2 - \|\vec{AB}\|^2 = 1^2 - 2^2 = -3
\end{aligned}
$$

Localiser $I$, intersection de $d$ et $(AB)$
$$\vec{AM} \cdot \vec{BD} = -3$$
$$\vec{AM} = t\vec{AB}, \quad t \in \mathbb{R}$$

$$
\begin{cases}
\vec{AI} = t\vec{AB} \\
\vec{AI} \cdot \vec{BD} = -3
\end{cases}
\implies (t\vec{AB}) \cdot \vec{BD} = -3
$$
$$t\vec{AB} \cdot \vec{BD} = -4t$$

Or
$$
\begin{aligned}
\vec{AB} \cdot \vec{BD} &= \vec{AB} \cdot (\vec{BA} + \vec{AD}) \\
&= -\|\vec{AB}\|^2 + \vec{AB} \cdot \vec{AD}
\end{aligned}
$$

donc $t = \dfrac{3}{4}$ et $\vec{AI} = \dfrac{3}{4}\vec{AB}$

**c)** On donne :

![[g3-mediatrice.svg]]

Équation droite $(d) \to$ médiatrice $AB$

$$d:\ \vec{AM} \cdot \vec{AB} = \underset{M = I}{\vec{AI} \cdot \vec{AB}} = \frac{1}{2}\|\vec{AB}\|^2$$

> [!important]
> Les trois médiatrices s'intersectent en $O$, <span style="color:red">centre du cercle circonscrit</span> au triangle [S4, Ex 5]

**d)** On donne :

![[g3-hauteur.svg]]

$$\underset{\text{vue depuis } A}{h:\ \vec{AM} \cdot \vec{BC} = 0} \qquad\qquad \underset{\text{vue depuis } B}{h:\ \vec{BM} \cdot \vec{BC}} = \text{constante} = \underset{M = A}{\vec{BA} \cdot \vec{BC}}$$

Les hauteurs s'intersectent en $M$ appelé <span style="color:red">orthocentre</span>.
