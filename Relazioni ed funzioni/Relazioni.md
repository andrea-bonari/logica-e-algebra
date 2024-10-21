>[!note]
>Una relazione su $A_{1},\cdots,A_{n}$ è un sottoinsieme $R$: $$R\subseteq A_{1}\times\cdots\times A_{n}$$
>Ed è detta relazione $n$-aria. In una relazione binaria $A_{1}$ si dice dominio e $A_{2}$ si dice codominio: $$R\subseteq\underbrace{A_{1}}_\text{dominio}\times\underbrace{A_{2}}_\text{codominio}$$

>[!tip] Notazione
>La notazione $aRb$ può essere usata per rappresentare $(a,b)\in R$.

Proprietà di due relazioni: $$R\subseteq S\iff \forall(a,b)\in R: \exists(a,b)\in S$$
$$R=S\iff (R\subseteq S )\land(S\subseteq R)$$

### Metodi di rappresentazione di relazioni finite

Prendiamo in considerazione la relazione $R\subseteq A_{1}\times A_{2}$

>[!tip] Elenco di elementi
>È possibile rappresentare gli elementi come elenchi: $$R=\set{(a_{1},b_{1}), \space(a_{2},b_{2}),\cdots}$$

>[!tip] Grafo di adiacenza
>È possibile disegnare un grafo orientato di tutti i vertici in $A_{1}\cup A_{2}$ e disegno una freccia da $a$ a $b$ se $(a,b)\in R$.
>![[Pasted image 20240917165807.png]]

>[!tip] Matrice di adiacenza
>Numerando gli elementi del dominio $(a_{1},\cdots,a_{n})$ e gli elementi del codominio $(a_{1},\cdots,a_{m})$, possiamo definire la matrice $M_{R}\in\mathbb{M}_{m,n}(\set{0,1})$: $$(M_{R})_{ij}=\begin{cases}
1&\text{se } (a_{i},b_{j})\in R \\
0&\text{se } (a_{i},b_{j})\notin R
\end{cases}$$

### Operazioni su relazioni binarie
>[!tip] Unione
>$$R, T\subseteq A_{1}\times A_{2}$$
>$$R\cup T=\set{(a,b): (a,b)\in R\text{ o }(a,b)\in T}$$
>Nel caso della matrice di adiacenza basterà fare un or logico elemento per elemento.

>[!tip] Intersezione
>$$R,T\subseteq A_{1}\times A_{2}$$
>$$R\cap T=\set{(a,b): (a,b)\in R\text{ e }(a,b)\in T}$$

>[!tip] Prodotto di relazioni
>$$R\subseteq A_{1}\times A_{2}\qquad T\subseteq A_{2}\times A_{3}\qquad R\cdot T\subseteq A_{1}\times A_{3}$$
>$$R\cdot T=\set{(a,c)\in A_{1}\times A_{3}\quad |\quad \exists b\in A_{2}\quad |\quad (a,b)\in R, (b,c)\in T}$$
>
>Nella rappresentazione della matrice di adiacenza basta fare il prodotto riga per colonna.
>$$M_{R\cdot T}=M_{R}\cdot M_{T}$$
>La matrice risultante rappresenterà il numero di percorsi che connette $i\to j$, e quindi:
>$$(M_{R\cdot T})_{ij}=\begin{cases}
1&\text{ se } (M_{R}\cdot M_{T})_{ij}\neq0 \\
0&\text{ se } (M_{R}\cdot M_{T})_{ij}=0
\end{cases}$$

>[!tip] Inversa di una relazione
>$$R\subseteq A_{1}\times A_{2}\qquad R^{-1}\subseteq A_{2}\times A_{1}$$
>$$R^{-1}=\set{(b,a)\in A_{2}\times A_{1}\quad |\quad (a,b)\in R}$$

