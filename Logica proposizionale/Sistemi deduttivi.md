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



