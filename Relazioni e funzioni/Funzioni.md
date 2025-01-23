>[!note]
>Una funzione $f:A\to B$ è una relazione binaria $f\subseteq A\times B$: $$\forall a\in A\quad \exists!b\in B\qquad (a,b)\in f$$
>Dato che per ogni $a$, il $b$ associato è unico. $b$ lo si denota anche con il simbolo $f(a)$.

>[!tip]
>La matrice di adiacenza di una funzione $M_{f}$ ha la proprietà che in ogni riga c'è un solo $1$.

### Tipologie di funzioni
>[!tip] Composta (prodotto come relazione)
>Se $f:A\to B$ e $g: B\to C$ sono funzioni, allora il prodotto $f\cdot g: A\to C$ è una funzione: $$g\circ f$$

>[!tip] Inversa
>Sia $f\subseteq A\times B$. La relazione $f^{-1}\subseteq B\times A$ è una funzione se e solo se $f$ è iniettiva e suriettiva (biunivoca). In generale se una funzione è biunivoca sappiamo: $$f\cdot f^{-1}=I_{A}\qquad f^{-1}\cdot f=I_{B}$$

>[!tip] Iniettiva e suriettiva
>Sia $f:A\to B$ una funzione. $f$ è iniettiva se e solo se esiste un inversa $d: B\to A$ tale che: $$f\cdot d=I_{A}$$
>Inoltre $f$ è suriettiva se e solo se esiste un inversa $s:B\to A$ tale che: $$s\cdot f=I_{B}$$
>Se $f$ ha inversa destra $d$ e sinistra $s$ allora $$s=d=f^{-1}$$

### Mappa canonica associata
>[!note]
>Data una relazione d'equivalenza $\rho\subseteq A\times A$, esiste una funzione suriettiva, detta canonica tale che: $$\pi_{\rho}:A\to A \mathbin{/} \rho\qquad \pi_{\rho}(a):=[a]_{\rho}$$

### Nucleo
>[!note]
>Il nucleo di una funzione $f:A\to B$ è la relazione $\ker\cdot f\subseteq A\times A$ tale che $a_{1}\ker a_{2}$ se $f(a_{1})=f(a_{2})$.

Possiamo dire che $a_{1}\ker a_{2}$ se e solo se $a_{1},a_{2}\in f^{-1}(b)$ per qualche $b\in B$. Inoltre $A  \mathbin{/} \ker=\set{f^{-1}(b)\quad b\in B}$

### Teorema di fattorizzazione
>[!note] Teorema di fattorizzazione
>Sia $f:A\to B$ e sia $\rho=\ker f$. Allora se $\pi_{\rho}:A\to A \mathbin{/}\rho$ è la mappa canonica $\pi_{\rho}(a)=[a]_{\rho}$, allora esiste una funzione $g:  A \mathbin{/}\rho\to B$ iniettiva tale che: $$f=\pi_{\rho}\cdot g$$
>Inoltre se $f$ è suriettiva, allora $g$ è biunivoca.

