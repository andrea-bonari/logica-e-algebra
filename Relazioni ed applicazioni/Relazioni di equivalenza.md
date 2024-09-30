>[!note]
>Una relazione binaria $R\subseteq A\times A$ si dice d'equivalenza se è riflessiva, simmetrica e transitiva.

>[!tip]
>Esiste sempre la chiusura riflessiva, simmetrica e transitiva. Questa viene detta chiusura di equivalenza:
>$$\overline{R}^{\text{EQ}}=\bigcup_{i\geq0}^\infty(R\cup R^{-1})^{i}$$
>Nel grafo di adiacenza basta completare le componenti connesse fino a renderle cliques (componenti in cui tutto è connesso con tutto).
>![[Pasted image 20240926091812.png]]

>[!tip]
>Se $S,T$ sono d'equivalenza la loro unione non è d'equivalenza, ma l'intersezione si.

### Classi d'equivalenza
>[!note]
>Sia $\rho\subseteq A\times A$ d'equivalenza $\forall a\in A$, la classe d'equivalenza con rappresentante $a$ è definita come: $$[a]_{\rho}:=\set{b\in A:\quad (a,b)\in\rho}$$ Il rappresentante non è unico in generale, infatti: $$b\rho a\Longrightarrow [a]_{\rho}=[b]_{\rho}$$
>

Data $\rho\subseteq A\times A$ d'equivalenza, allora $A / \rho$ forma una partizione di $A$, cioè: $\set{A_{i}}_{i\in I}\quad A_{i}\subseteq A$ collezione di sottoinsiemi di $A$ tale che $\bigcup_{i\in I} A_{i}=A$ e $A_{i}\cap A_{j}\quad i\neq j$.
