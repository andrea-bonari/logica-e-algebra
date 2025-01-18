>[!note]
>La finalità di un sistema deduttivo, o un metodo formale, è di avere un metodo automatico per verificare che $\Gamma\models A$.
>Quindi partendo dall'insieme $\Gamma$ e da un insieme di assiomi $\text{Ax}$, con delle regole di riscrittura, dette di inferenza, cerchiamo di generare una sequenza di FBF tale che: $$\Gamma\cup\text{Ax}\vdash D_{0}\qquad \Gamma\cup\text{Ax}\cup\set{D_{0}}\vdash D_{1}\quad\cdots\Gamma\cup\text{Ax}\cup\set{D_{0},\cdots, D_{n-1}}\vdash A$$
>I sistemi formali possono essere:
>- Corretti: $\Gamma\vdash A\Rightarrow\Gamma\models A$
>- Completi: $\Gamma\models A\Rightarrow\Gamma\vdash A$

### Teoria L
>[!note]
>Ha come sintassi una FBF contenenti solo $\lnot$ e $\Rightarrow$. Gli assiomi sono: $$\text{Ax}:\begin{cases}
>A_{1}:&A\Rightarrow(B\Rightarrow A) \\
>A_{2}:&(A\Rightarrow(B\Rightarrow C))\Rightarrow((A\Rightarrow B)\Rightarrow (A\Rightarrow C)) \\
>A_{3}:& (\lnot A\Rightarrow\lnot B)\Rightarrow((\lnot A\Rightarrow B)\Rightarrow A)
>\end{cases}$$
>Questi in realtà sono schemi di assiomi poiché $A,B,C$ sono FBF. Inoltre consideriamo come regola d'inferenza la "modus ponens": $$A,A\Rightarrow B\vdash_{L} B$$

Quindi se da un insieme di formula $\Gamma$, usando gli assiomi $\text{Ax}$ e il modus ponens ottengo una sequenza di FBF $D_{1},\cdots, D_{n}$ tale che: $$\Gamma\cup\text{Ax}\vdash_{L} D_{0}\qquad \Gamma\cup\text{Ax}\cup\set{D_{0}}\vdash_{L} D_{1}\quad\cdots\Gamma\cup\text{Ax}\cup\set{D_{0},\cdots, D_{n-1}}\vdash_{L} D_{n}$$
Allora si dice che $D_{n}$ è un teorema della teoria L che ha $x$ premesse $\Gamma$ e $D_{1},\cdots,D_{n}$ è una dimostrazione di $D_{n}$, e scriviamo $\Gamma\vdash_{L} D_{n}$

>[!tip] Teorema di correttezza e completezza forte
>La teoria L è:
>- Corretta: $\Gamma\vdash_{L} A\Rightarrow\Gamma\models A$
>- Completa: $\Gamma\models A\Rightarrow\Gamma\vdash_{L} A$
>  
>Nel caso $\Gamma=\emptyset$, il teorema si riduce a $\vdash_{L} A\Leftrightarrow\models A$, cioè $A$ è una tautologia.

### Risoluzione
>[!note]
>A differenza della teoria L, non ha assiomi propri e funziona per refutazione. La risoluzione verifica se un insieme $\Lambda$ di formule è insoddisfacibile. Quindi: $$\Lambda\text{ è insoddisfacibile se }\Lambda^{C}\vdash_{R}\square$$
>Definiamo:
>- Letterale: una lettera enunciativa o una sua negata ($A$ o $\lnot A$)
>- Clausola: È un insieme di letterali, anche dette stringhe privilegiate. La clausola vuota è indicata come $\square$, mentre l'insieme di clausole di $\Lambda$ è $\Lambda^{C}$
>- Regola d'inferenza: diciamo che la clausola $R$ è una risolvente delle clausole $C_{1},C_{2}$ e scriviamo $C_{1},C_{2}\vdash_{R}R$ se: $$A\in C_{1}\quad \lnot A\in C_{2}\qquad R=(C_{1}\smallsetminus\set{A})\cup(C_{2}\smallsetminus\set{\lnot A})$$

>[!warning]
>La regola di inferenza si applica per un letterale e il suo negato alla volta.

Sia $\Lambda^{C}$ l'insieme di clausole, una derivazione per risoluzione della clausola $C$ da $\Lambda^{C}$ è una sequenza di clausole $D_{1},\cdots,D_{n}$ tale che $D_{n}=C$ e: $$\Lambda^{C}\vdash_{R}D_{1}\quad\Lambda^{C}\cup\set{D_{1}}\vdash_{R}D_{2}\quad\cdots\quad \Lambda^{C}\cup\set{D_{1},\cdots,D_{n-1}}\vdash_{R}=D_{n}$$
>[!tip]
>Le clausole, in generale, si possono utilizzare più di una volta.

