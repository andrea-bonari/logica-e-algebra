>[!note]
>Sia $P$ un insieme di proprietà. La $P$-chiusura di $R\subseteq A\times A$ è una relazione $T\subseteq A\times A$ tale che:
>- $R\subseteq T$
>- $T$ soddisfa $P$
>- $\forall s\subseteq A\times A$ che soddisfa $P$ $\Longrightarrow T\subseteq S$ (Chiusura la più piccola possibile)

>[!tip]
>Se $T$ esiste allora è unica. Questo perché soddisfacendo le condizioni precedenti, dalla terza proprietà abbiamo $$S=T_{1}\Longrightarrow T_{2}\subseteq T_{1}\text{ e per simmetria }T_{1}\subseteq T_{2}\Longrightarrow T_{1}=T_{2}$$

>[!tip]
>Se $R$ soddisfa $P$ allora la $P$ chiusura di $R$ è $R$ stessa.

Affinché $R\subseteq A\times A$ abbia una $P$-chiusura è necessario che:
- $\exists H\subseteq A\times A$ con le proprietà $P$ tale che $R\subseteq H$
- L'insieme $P$ di proprietà è chiuso rispetto all'intersezione

>[!tip]
>Se $P\subseteq\set{\text{Riflessiva},\text{Transitiva},\text{Simmetrica}}$ allora ogni $R\subseteq A\times A$ possiede la $P$-chiusura

### Tipologie di chiusure
>[!tip] Chiusura riflessiva
>Data una relazione $R\subseteq A\times A$ una chiusura riflessiva è tale che: 
>$$\overline{R}^{\text{Riflessiva}}=R\cup I_{A}$$
>La sua matrice di adiacenza sarà: $$M_{R^{\text{Riflessiva}}}=M_{R}\oplus I$$

>[!tip] Chiusura simmetrica
>Data una relazione $R\subseteq A\times A$ una chiusura simmetrica è tale che: 
>$$\overline{R}^{\text{Simmetrica}}=R\cup R^{-1}$$
>La sua matrice di adiacenza sarà: $$M_{R^{\text{Simmetrica}}}=M_{R}\oplus M_{R}^{T}$$

>[!tip] Chiusura transitiva
>Data una relazione $R\subseteq A\times A$ una chiusura transitiva è tale che: $$\overline{R}^{\text{Transitiva}}=R\cup R^{2}\cup R^{3}\cup \cdots=\bigcup_{n\geq 1}R^{n}$$
>La sua matrice di adiacenza sarà: $$M_{R^{\text{Transitiva}}}=M_{R}\oplus M_{R^{2}}\oplus\cdots$$

>[!tip] Chiusura riflessiva e simmetrica
>Data una relazione $R\subseteq A\times A$ una chiusura riflessiva e simmetrica è tale che: $$\overline{R}^{\text{Riflessiva+Simmetrica}}=R \cup R^{-1}\cup I_{a}$$
>La sua matrice di adiacenza sarà: $$M_{R^{\text{Riflessiva+Simmetrica}}}=M_{R}\oplus M_{R}^{T}\oplus I_{A}$$

>[!tip] Chiusura riflessiva e transitiva
>Data una relazione $R\subseteq A\times A$ una chiusura riflessiva transitiva è tale che: $$\overline{R}^{\text{Riflessiva+Transitiva}}=\bigcup_{i\geq 0} R^{i}=\bigcup_{i\geq 1}R^{i}+I_{A}$$

>[!tip] Chiusura simmetrica e transitiva
>Data una relazione $R\subseteq A\times A$ una chiusura simmetrica e transitiva è tale che: $$\overline{R}^{\text{Simmetrica+Transitiva}}=\bigcup_{i\geq 1} (R\cup R^{-1})^{i}$$

>[!tip] Chiusura riflessiva, simmetrica e transitiva
>Data una relazione $R\subseteq A\times A$ una chiusura riflessiva, simmetrica e transitiva è tale che: $$\overline{R}^{\text{Riflessiva+Simmetrica+Transitiva}}=\bigcup_{i\geq 1} (R\cup R^{-1})^{i}\cup I_{A}$$

In generale la chiusura antisimmetrica non esiste, a meno che $R\subseteq A\times A$ non sia già antisimmetrica. Questa è detta chiusura d'ordine. Questa equivale alla chiusura transitiva e riflessiva se sia lei che la relazione $R$ sono antisimmetriche.

