### Relazioni e funzioni
>[!note] Relazioni su insiemi diversi
>Siano $A,B,C$ insiemi, $R,S\subseteq A\times B$ e $T\subseteq B\times C$. Allora: $$\begin{align*}
&M_{R\cup S}=M_{R}\oplus_{1} M_{S}\quad& M_{R\cap S}=M_{R}\otimes M_{S}\\
&M_{R^{C}}=\ominus_{1} M_{R}\quad &M_{R\cdot T}= M_{R}\cdot M_{T}
\end{align*}$$

>[!note] Proprietà delle relazioni su uno stesso insieme
>Siano $A$ insieme e $R\subseteq A\times A$.
>
>| nome | proprietà | chiusura |
>| - | - | - |
>| Seriale | $\forall a\in A\space\exists b\in A:\space aRb$ | $\nexists$ |
>| riflessiva | $\forall a\in A:\space aRa$ | $M_{R}\oplus I$ |
>| simmetrica | $\forall a,b\in A:\space aRb \Longrightarrow bRa$ | $M_{R}\oplus M_{R}^{T}$ |
>| antisimmetrica | $\forall a,b \in A:\space aRb, bRa\Longrightarrow a=b$ | $\nexists$ |
>| transitiva | $\forall a,b,c\in A:\space aRb,bRc\Longrightarrow aRc$ | $\bigcup\limits_{i<n-1} R^{i}$ |
>
>La chiusura di equivalenza è riflessiva, simmetrica e transitiva e consiste nel collegare tutti i nodi a se stessi e rendere la matrice di adiacenza a blocchi.

>[!note] Classe di equivalenza (definizione)
>Siano $A$ insieme e $R\subseteq A\times A$:
> $$[A]_{R}=\set{b\in A:\space aRb}$$

>[!note] funzioni
>Una relazione $R$ è funzionale se e solo se è seriale.
>Una funzione è iniettiva se ha un $1$ per colonna.
>Una funzione è suriettiva se ha un $1$ per riga.

>[!note] Chiusura d'ordine
>La chiusura d'ordine è riflessiva, transitiva e antisimmetrica. In generale la chiusura antisimmetrica è possibile se la relazione da chiudere è già antisimmetrica e non è ciclica.

### Logica proposizionale
>[!note] Modelli
>I modelli sono le righe vere di una $F$. Se ogni interpretazione è un modello allora è una tautologia. Se i modelli di $F$ $\subseteq$ modelli di $G$, allora $F\models G$. Se $F\models G$ e $G\models F$ allora $F\equiv G$.

>[!note] Parsing tavole di verità
>$$F\equiv (\text{Righe con 0})\land\cdots\equiv (\text{Righe con 1})\lor\cdots\equiv(A\Rightarrow (\cdots))\land (\lnot A\Rightarrow(\cdots))$$

>[!note] Teoria L
>$$\Gamma\vdash_{L} A\iff \Gamma\models A$$

>[!note] Formule su PDF
>Quelle sul pdf + $$P\iff Q\equiv (P\implies Q)\land(Q\implies P)$$

>[!note] Risoluzione
>$\Gamma$ insoddisfacibile se $\Gamma\vdash_{R}\square$.
>$\Gamma\models F$ se e solo se $\Gamma\cup\set{\lnot F}\vdash_{R}\square$.
>
>Forma clausole: $$(\cdots\lor\cdots)\land(\cdots\lor\cdots)$$

### Logica del primo ordine
>[!note] Chiusura universale e forma di Skolem
>Se abbiamo una costante $c$ nella fbf $A(c)$ la chiudiamo universalmente prefissando $\forall c\space A(c)$. In forma di Skolem rimuoviamo i quantificatori esistenziali e sostituiamo le loro occorrenze con lettere funzionali dipendenti dai quantificatori universali precedenti ad esso: $$\forall a\space\exists c\space A(a,c)\Longrightarrow\forall a\space A(a,f(a))$$

>[!note] Formule da imparare
>$$\lnot\forall x B\equiv \exists x\lnot B \text{ o }\lnot\exists xB\equiv \forall x\lnot B$$$$(\forall x B(x)\land\mathcal{E})\equiv\forall y(B[y/x]\land\mathcal{E})\text{ o }(\exists x B(x)\lor\mathcal{E})\equiv\exists y(B[y/x]\lor\mathcal{E})$$$$\forall x B(x)\Rightarrow\mathcal{E}\equiv\exists y( B[y  \mathbin{ / }x] \Rightarrow\mathcal{E})\text{ o }\exists x B(x)\Rightarrow\mathcal{E}\equiv\forall y( B[y  \mathbin{/} x] \Rightarrow\mathcal{E})$$$$\mathcal{E}\Rightarrow\forall x B(x)\equiv \forall y(\mathcal{E}\Rightarrow B[y \mathbin{ / }x])\text{ o } \mathcal{E}\Rightarrow\exists x B(x)\equiv \exists y(\mathcal{E}\Rightarrow B[y \mathbin{/}x])$$
>