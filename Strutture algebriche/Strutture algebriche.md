>[!note]
>Un operazione interna $n$-aria (operazione $n$-aria): $$\omega:\underbrace{A\times\cdots\times A}_{n\text{ volte}}\to A$$
>Ci interesseremo ai casi $n=0,1,2$.
>Come notazione si usa $\omega(a,b)$, però nei casi binari si può usare la notazione infissa $a\omega b$.
>Una struttura algebrica è una coppia $(A,\Omega)$ dove $\Omega=\set{\omega_{1},\cdots,\omega_{l}}$ è un insieme di operazioni interne ad $A$.
### Semigruppo
>[!note]
>$$(A,\bullet)\quad \bullet: A\times A\to A$$
>Dove $\bullet$ è un operazione binaria associativa: $$\forall a,b,c\qquad a\bullet (b\bullet c)=(a\bullet b)\bullet c$$
>Se $\forall a,b\quad a\bullet b= b\bullet a$ allora il semigruppo $(A,\bullet)$ si dice commutativo.

>[!tip]
>L'associatività permette di "togliere le parentesi nei prodotti".

In un semigruppo $(S,\bullet)$ è possibile definire la potenza $n$-esima di $a\in S$: $$a^{n}:= a\cdot \underbrace{a\bullet\cdots\bullet a}_{n\text{ volte}}$$
E valgono le usuali regole: $$\begin{cases}
a^{n}\bullet a_{m}=a^{n+m} \\
(a^{n})^{m}=a^{n\bullet m}
\end{cases}\quad\forall n,m>0$$

>[!error]
>$(a\bullet b)^{n}$ **non è** $a^{n}\bullet b^{n}$, a meno che $(S,\bullet)$ non sia commutativo, allora in questo caso $(a\bullet b)^{n}=a^{n}\bullet b^{n}$.

Per i semigruppi commutativi, si usano i simboli $+, \oplus,\cdots$. Inoltre, se in un gruppo commutativo $(S,+)$: $a^{n}=\underbrace{a+\cdots+a}_{n\text{ volte}}$ a volte lo si indica in notazione additiva con $n\cdot a$ invece della notazione $a^{n}$ usata per i semigruppi non commutativi.

>[!tip] Teoria dei semigruppi
>La teoria dei semigruppi è una teoria k con identità/uguaglianza $E(x,y)$ più l'assioma di associatività dell'operazione interna binaria prescritta dalla lettera funzionale $P(x,y)\to x\cdot y$: $$\forall x\space\forall y\space\forall z\quad E(P(x,P(y,z)), P(P(x,y),P(z)))$$

### Monoide
>[!note]
>Una monoide è una struttura algebrica $(M, *, e)$ con $e$ operazione $0$-aria scelta di un elemento di $M$ tale che:
>1. $(M,*)$ è un semigruppo
>2. $e\in M$ è un identità (elemento neutro): $\begin{cases}\forall a\space e* a = a \\\forall a\space a* e = a\end{cases}$

>[!tip]
>Un elemento neutro è unico: se $e_{1},e_{2}$ sono elementi neutri allora $e_{1}=e_{2}$: $$e_{2}=e_{1}* e_{2}=e_{1}$$

>[!tip]
>Se poniamo $\forall a\in M\quad a^{0}:=e$ allora le proprietà delle potenze viste prima possono essere estese $\forall m,n\geq0$.

>[!tip] Teoria dei monoidi
>La teoria dei monoidi è una teoria con identità $E(x,y)$ e $P(x,y)\to x* y$ e una costante e con gli assiomi:
>1. Assioma di associatività
>2. $\forall x\space (E(P(x,e),x)\land E(P(e,x),x))$ 
>
>Se non avessi voluto aggiungere la costante $e$ che mi descrive l'elemento neutro l'assioma diventa: $$\exists x\space \forall y\space(E(P(y,x),y)\land E(P(x,y),y))$$
>Che è la forma di Skolem della precedente.

### Gruppo
>[!note]
>Un gruppo è una struttura algebrica $(G,*,e,^{-1})$ dove:
>1. $(G,*,e)$ è un monoide
>2. Esistenza dell'inverso: $$\forall g\in G\space\exists h\in G\quad\text{t.c.}\quad g* h=h* g=e$$$h$ è detto inverso (sinistro e destro) di $g$.

>[!tip]
>L'inverso è unico: se $h_{1},h_{2}\in G$ sono inversi di $g$ allora: $$h_{1}=h_{1}* e=h_{1}*(g\cdot h_{2})=(h_{1}* g)* h_{2}=e* h_{2}=h_{2}$$
>Quindi, siccome l'inverso di $g$ è unico questo è univocamente determinato da $g$, cioè c'è un un operazione interna unaria $^{-1}:G\to G\quad g\to h$ dove $h$ è l'unico inverso di $g$, da cui si indica $h$ con $g$.

Proprietà dei gruppi $(G,*,e,^{-1})$:
1. $\forall g\in G\space (g^{-1})^{-1}=g$
2. $\forall g,h\in G\space (g* h)^{-1}=h^{-1}* g^{-1}$
3. In un gruppo l'equazione $g*x=h$ ha un unica soluzione $x=g^{-1}h$
4. Valgono le proprietà delle potenze: $$\forall g\in G\quad \begin{cases}
g^{n}*g^{m}=g^{n+m}\\
(g^{n})^{m}=g^{n*m}
\end{cases}\quad\forall n,m\in \mathbb{Z}$$
>[!warning]
>In generale $(g*h)^{-1}\neq g^{1}*h^{-1}$, a meno che $G$ è abeliano.

Sia $\mathbb{Z}_{n}^{*}=\set{[a]_{n}\in\mathbb{Z}_{n}\smallsetminus\set{[0]_{n}}\quad \text{MCD}(a,n)=1}$, allora $(\mathbb{Z}_{n}^{*},\odot,[1]_{n})$ è un gruppo.

>[!tip] Teoria dei gruppi
>La teoria dei gruppi è una teoria k con identità $E(x,y)$, assioma di associatività $*$ interpretato con $P(x,y)$ e con assioma di identità e inversa: $$\exists x\space[\forall (y\space E(P(x,y),y)\land E(P(y,x),y))\land\forall y\space \exists z\space(E(P(y,z),x)\land E(P(z,y),x))]$$Se avessi usato la costante $e$ come elemento neutro, allora avremmo dovuto avere gli assiomi di associatività, di elemento neutro $e$ e: $$\forall y\space \exists z\space(E(P(y,z),e)\land E(P(z,y),e))$$
>
>È possibile semplificare gli assiomi precedenti usando il seguente teorema:
>Se $(G,*,e,^{-1})$ è un gruppo esiste elemento neutro sinistro/inverso e inverso destro/sinistro
>
>Quindi la teoria dei gruppi viene semplificata in: $$\exists x\space(\forall g\space E(P(g,x),g)\land \forall g\space \exists s\space E(P(s,g),x))$$

### Anello
>[!note]
>Un anello è una struttura algebrica $(A,+,\cdot)$ dove:
>1. $(A,+)$ è un gruppo commutativo con elemento neutro indicato con $0$.
>2. $(A,\cdot)$ è un semigruppo (detto moltiplicativo)
>3. Valgono le proprietà distributive: $$\forall a,b,c\in A\quad \begin{align*}
&a\cdot(b+c)=(a\cdot b)+(a\cdot c)\\
&(b+c)\cdot a=(b\cdot a)+(c\cdot a)
\end{align*}$$

>[!tip]
>Se $(A,\cdot,1)$ è un monoide, l'anello è detto con unità. Inoltre se $(A,\cdot)$ è commutativo allora si parla di anello commutativo.

>[!tip] Teoria degli anelli
>La teoria degli anelli è una teoria k con identità $E(x,y)$, $S(x,y)\to x+y$ e $P(x,y)\to x\cdot y$ con:
>- Assiomo di gruppo per $S(x,y)$ e commutatività
>- Assioma di associatività per $P(x,y)$
>- Assioma di distributività: $$\forall x\space \forall y\space\forall z\quad E(P(x,S(y,z)),S(P(x,y),P(x,z)))$$
>
>Gli anelli hanno come proprietà:
>1. L'elemento neutro $0$ del gruppo $(A,+)$ è uno zero del semigruppo $(A,\cdot)$
>2. In un anello $(A,+,\cdot)$ l'elemento neutro $0$ di $+$ è lo zero di $(A,\cdot)$. Inoltre $\forall a,b\in A\quad a\cdot(-b)=-(a\cdot b)$
>3. In un anello $(A,+,\cdot)$ privo di divisori dello zero, detto dominio d'integrità se e solo se valgono le leggi di cancellazione: $$\begin{cases}
b\cdot a=c\cdot a\Longrightarrow b=c \\
a\cdot b=a\cdot c\Longrightarrow b=c
\end{cases}$$

>[!tip] Zero di un semigruppo
>Sia $(A,\cdot)$ un semigruppo, un $z\in A$ tale che: $$\forall a\in A\quad z\cdot a = a\cdot z=z$$
>Si chiama lo zero di $(A,\cdot)$.

>[!tip] Divisori dello zero
>In un anello $(A,+,\cdot)$ due elementi $a,b\neq0$ si dicono divisori dello zero se $a\cdot b=0$

### Corpo
>[!note]
>Un corpo è un anello $(A,+,\cdot)$ in cui $(A\smallsetminus{0},\cdot)$ è un gruppo. Se questo è commutativo allora si chiama campo.

