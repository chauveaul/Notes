1. Ordonner les fonctions suivantes par ordre de croissance 
$$
 n + 50, n \sqrt{n}, 2n, 100, 10n^{0.1}, n^2, n^3 + n^2, n^3, n^{1.1}, |sin(n)| + 1, n^{10}.
$$
$$
|sin(n)|+1, 100, 10n^{0.1}, n+50, 2n, n^{1.1}, n\sqrt{n}, n^{2}, n^{3}, n^{3}+n^{2}, n^{10}
$$
2. Pour n ∈ N, prouvez les affirmations en exhibant une constante C (ou des constantes C1 et C2) et un rang N appropriés :
	1. 
		$2n+100 = \Theta(n)$ : pour tout $n \geq 1$,$$1\cdot n \;\leq\; 2n+100 \;\leq\; 102\,n$$donc $C_1 = 1$, $C_2 = 102$, $N = 1$.
	2. 
		$an + b = \Theta(n)$: avec a, b > 0 pour tout $n \geq 1$, on a $b \leq b\,n$, donc $$a\,n \;\leq\; an+b \;\leq\; (a+b)\,n$$
		donc $C_1 = a$, $C_2 = a+b$, $N = 1$
	3. 
		$100n\sqrt{n} = \mathcal{O}(n^2)$ : pour tout $n \geq 1$, $\sqrt{n} \leq n$, Donc $$100\,n\sqrt{n} \;\leq\; 100\,n^2$$
		Donc, $C = 100$, $N=1$

3. On donne ci-dessous l’algorithme `carre` (sous forme d’un code Python), qui prend un entier positif n en entrée et affiche un carré d’astérisques de côté n.
```python
def carre(n):
	for i in range(1, n+1):
		for j in range (1, n+1):
			print("*", end = " ")
		print()
```
1. Combien d'astérisques l'algorithme affiche-t-il pour l'entrée $n$?
	$n^2$
2. Donnez, en notation $\Theta(\cdot)$, l'ordre de croissance du temps de parcours de cet algorithme en fonction de $n$.
	$$\Theta(n^2)$$
3. Mêmes questions pour l'algorithme `triangle` qui prend un entier positif $n$ en entrée et affiche un triangle de côté $n$:
```python
def triangle(n):
	for i in range(1, n+1):
		for j in range(1, i+1):
			print("*", end=" ")
		print()
```
	
 a) $\frac{n(n+1)}{2}$
 b) $\frac{n(n+1)}{2} = \frac{n^2+n}{2} = \frac{1}{2}n^2 + \frac{1}{2}n$, le terme dominant est toujours $n^2$ $\implies \Theta (n^2)$

 4. On reproduit ci-dessous l'algorithme `max_somme` vu au cours, qui calcule la somme maximale de deux éléments d'une liste `L` de nombres:
	```python
	def max_somme_lin(L):
		if len(L) < 2:
			return
		max_1, max_2 = 0,0
		if L[0] > L[1]:
			max_1 = L[0]
			max_2 = L[1]
		else:
			max_1 = L[1]
			max_2 = L[0]
		for i in range(2, len(L)):
			if L[i] > max_2:
				max_2 = L[i]
			if max_2 > max_1:
				max_1, max_2 = max_2, max_1
		return max_1 + max_2	
	```

	L'algorithme regarde `n = len(L)` éléments ce qui lui donne une compléxité de n. $\iff \Omega{n}, \mathcal{O}(n) \iff \Theta(n)$

5. 
	Max:
	- $\mathcal{O}(n), \Omega(n) \implies \Theta(n)$
	