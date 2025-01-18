>[!note]
>Sia $(A,\Omega)$ una struttura algebrica e $H\subseteq A$. Allora $(H,\Omega)$ è una sottostruttura algebrica se tutte le operazioni di $\Omega$ si restringono ad $H$. Cioè se $*\in\Omega$ allora $\forall h_{1},h_{2}\in H\quad h_{1}*h_{2}\in H$.

- $(H,\bullet)$ è sottosemigruppo di un semigruppo $(S,\bullet)$ con $H\subseteq S$ se e solo se $\forall a,b\in H\quad a\bullet b\in H$.
- $(H,\bullet,e)$ è un sottomonoide del monoide $(M,\bullet,e)$ con $H\subseteq M$ se e solo se $(H,\bullet)$ è sottosemigruppo di $(M,\bullet)$ e $e\in H$.
- $(H,\bullet,e,^{-1})$ è un sottogruppo del gruppo $(G,\bullet,e,^{-1})$ se e solo se $\forall a,b\in H\quad a\cdot b\in H$ e $\forall a\in H\quad a^{-1}\in H$. Più comodamente lo è se e solo se $\forall a,b\in H\quad a\bullet b^{-1}\in H$.
- $(H,\oplus,\odot)$ è un sottoanello dell'anello $(A,\oplus,\odot)$ se:
	- $(H,\oplus)$ è un sottogruppo di $(A,\oplus)$
	- $(H,\odot)$ è un sottosemigruppo di $(A,\odot)$
- $(H,\oplus,\odot)$ è un sottocampo/sottocorpo di $(A,\oplus,\odot)$ se è sottoanello di $(A,\oplus,\odot)$ e $(H\smallsetminus\set{0},\odot)$ è un sottogruppo di $(A\smallsetminus\set{0},\odot)$.

>[!tip]
>A volte invece di verificare se $(G,\odot)$ ha una certa struttura algebrica usando la definizione, è più conveniente trovare una struttura algebrica $(A,\odot)$ tale che $G\subseteq A$ che abbia quella struttura algebrica e poi usare i criteri di sottostrutture.

