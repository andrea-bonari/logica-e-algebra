>[!note]
>Date due strutture algebriche $(A_{1},\Omega_{1})$ e $(A_{2},\Omega_{2})$ e una funzione $f:A_{1}\to A_{2}$ diciamo che $f$ preserva le operazioni $+\in\Omega_{1}$ e $\oplus\in\Omega_{2}$ (della stessa arità) se:
>- $+,\oplus$ binarie: $\forall a,b\in A_{1}\quad f(a+b)=f(a)\oplus f(b)$
>- $^{-1},-$ unaria: $\forall a \in A_{1}\quad f(a^{-1})=-f(a)$
>- $e\in A_{1},\space s\in A_{2}$ $0$-arie: $f(e)=s$
>
>Se $f$ preserva tutte le operazioni tra $\Omega_{1}$ e $\Omega_{2}$ allora $f$ si chiama un omomorfismo tra le due strutture algebriche.
>
>Se $f$ è $\begin{cases}\text{iniettiva}\to\text{Monomorfismo} \\\text{suriettiva}\to\text{Epimorfismo} \\\text{Biunivoca}\to\text{Isomorfismo}\end{cases}$.

Se $f:A\to B$ e $g:B\to C$ sono omomorfismo, allora $f\circ g: A\to C$ è un omomorfismo.
Se $f:A\to B$ è un isomorfismo, allora $f^{-1}:B\to A$ è un isomorfismo.

>[!tip] Criterio per gruppi
>Se $f: (G,*)\to (H,\bullet)$ è di gruppi, $f$ è un omomorfismo se e solo se: $$\forall g_{1},g_{2}\in G\quad f(g_{1}*g_{2})=f(g_{1})*f(g_{2})$$

>[!tip] Criterio per anelli
>Con $(A,+,\cdot)$ e $(B,\oplus,\odot)$ anelli, $f:A\to B$ è un omomorfismo di anelli se e solo se: $$\begin{align*}
&\forall a,b\in A\quad f(a+b)=f(a)\oplus f(b)\\
&\forall a,b\in A\quad f(a\cdot b)=f(a)\odot f(b)
\end{align*}$$

### Epimorfismo canonico
>[!note]
>Siano $(A,\Omega)$ una struttura algebrica e $\rho$ una congruenza su tale struttura, esiste un importante epimorfismo: $$\pi_{\rho}:A\to A\mathbin{ / }\rho\qquad \pi_{\rho}(a)=[a]_{\rho}\quad\forall a\in A$$
>Viceversa dato un omomorfismo $f:(A,\Omega)\to(B,\Omega')$ tra due strutture, possiamo definire: $$\ker f=\set{(a_{1},a_{2})\in A\times A:\quad f(a_{1})=f(a_{2})}$$
>Una congruenza di $(A,\Omega)$.

### Teorema di fattorizzazione
>[!note]
>Sia $f:(A,\Omega)\to(B,\Omega')$ un omomorfismo, se $\rho=\ker f$ e se con $\pi_{\rho}:A\to A\mathbin{ / }\rho$ indico l'epimorfismo canonico, allora esiste unico il monomorfismo $g:A\mathbin{ / }\rho\to B$ tale che: $$f=\pi_{\rho}\cdot g$$
>Inoltre se $f$ è epimorfismo, allora $g$ è isomorfismo.