>[!note]
>Una relazione $R\subseteq A\times A$ si dice d'ordine se è riflessiva, transitiva e antisimmetrica. Solitamente si utilizzano il simbolo $\leq$ al posto di $R$, e scriviamo $a\leq b$ o $(a,b)\in\leq$ al posto di $aRb$.

Se una relazione d'ordine $\leq\subseteq A\times A$ soddisfa $\forall a,b\in A\qquad a\leq b\text{ o } b\leq a$ (cioè $a$ e $b$) sono confrontabili, allora $\leq$ si dice totale. Se per certi elementi non vale tale relazione allora si dicono non confrontabili. In quel caso si dice poset (Partially Ordered Set). 

### Diagramma di Hasse di un poset
>[!note]
>Il diagramma di Hasse è un modo per rappresentare graficamente un poset. Si costruisce in questo modo:
>1) Nel grafo di adiacenza del poset $\leq$ considero solo gli archi con $a\leq b$ (di copertura)
>2) Oriento gli archi inserendo $b$ sopra, $a$ sotto, e rimuovendo la freccia.
>
>![[Pasted image 20241009151156.png]]

>[!tip]
>Dati $b,a\in A$, si dice che $b$ copre $a$ se $a\leq b$ e $\nexists c\in A\smallsetminus\set{a,b}:\quad a\leq c\leq c$.

>[!tip]
>Dato un diagramma di Hasse è possibile ricostruire la relazione d'origine che lo genera.

### Massimi e minimi
>[!note]
>Sia $(A,\leq)$ un poset. Un elemento $a\in A$ può essere definito come:
>
| $$\text{Massimo}$$               | $$\text{Minimo}$$               | $$\text{Minimale}$$                                | $$\text{Massimale}$$                               |
| -------------------------------- | ------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| $$\forall x \in A\quad a\leq x$$ | $$\forall x\in A\quad x\leq a$$ | $$\forall x\in A\quad x\leq a\Longrightarrow x=a$$ | $$\forall x\in A\quad a\leq x\Longrightarrow x=a$$ |
>

Il minimo (o massimo) è rispettivamente minimale (o massimale), e se esiste è unico. Se esiste il minimo (o massimo) non esistono altri minimali (o massimali). Infine se $A$ è finito, e ha un solo minimale (o massimale) allora è minimo (o massimo).

### Minoranti e Maggioranti
>[!note]
>Sia $(A,\leq)$ e sia $B\subseteq A$. Un elemento $m\in A$ si dice maggiorante o minorante di $B$ se:
>
>| $$\text{Maggiorante}$$ | $$\text{Minorante}$$ |
>| - | - |
>| $$\forall x\in B\quad x\leq m$$ | $$\forall x\in B\quad m\leq x$$ |
>
>Inoltre definiamo $M(B)$ e $m(B)$: $$\begin{align*}
M(B)&= \set{ m\in A:\quad m\text{ maggiorante di }B}\\
m(B)&= \set{m\in A:\quad m\text{ minorante di }B}
\end{align*}$$
>
>Infine definiamo l'estremo inferiore e superiore di $B$: $$\begin{align*}
\sup(B)&= \min(M(B))\\
\min(B)&= \max(m(B))
\end{align*}$$

Date queste definizioni possiamo definire un reticolo come un poset $(A,\leq)$ in cui: $$\forall a,b\quad \exists \inf(\set{a,b})\qquad\exists\set{a,b}$$

