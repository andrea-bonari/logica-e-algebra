>[!note]
>Data una struttura algebrica $(A,\Omega)$, una relazione $\rho\subseteq A\times A$ di equivalenza, si dice compatibile per $*\in\Omega$ se: $$\forall a_{1},a_{2},b_{1},b_{2}\in A\quad a_{1}\space\rho\space b_{1}\text{ e }a_{2}\space\rho\space b_{2}\quad a_{1}*a_{2}\space\rho\space b_{1}*b_{2}$$
>Cioè se $[a_{1}]_{\rho}=[b_{1}]_{rho}$ e $[a_{2}]_{\rho}=[b_{2}]_{\rho}$ allora $[a_{1}*a_{2}]_{\rho}=[b_{1}*b_{2}]_{\rho}$.
>Se $\rho$ è compatibile con tutte le operazioni di $\Omega$ allora si chiama congruenza.

### Struttura quozionente
>[!note]
>Data una struttura algebrica $(A,\Omega)$ e una relazione di congruenza $\rho\subseteq A\times A$, per ogni operazione binaria $*\in\Omega$ possiamo definire una nuova operazione binaria interna su $A\mathbin{/}\rho$: $$*_{\rho}: A\mathbin{/}\rho\times A\mathbin{/}\rho\to A\mathbin{/}\rho$$
>Definita da $[a]_{\rho}*_{\rho}[b]_{\rho}:=[a*b]_{\rho}$.

>[!tip]
>È ben definita, quindi non dipende dai rappresentati delle classi d'equivalenza.

Definiamo quindi la nuova struttura algebrica $(A\mathbin{ / } \rho,\Omega_{\rho})$ dove: $$\Omega_{\rho}:=\set{*_{\rho}:\quad*\in\Omega\text{ definite come in precedenza}}$$
>[!tip]
>Si dimostra che la struttura quoziente $(A\mathbin{ / } \rho,\Omega_{\rho})$ è dello stesso tipo di $(A,\Omega)$.

