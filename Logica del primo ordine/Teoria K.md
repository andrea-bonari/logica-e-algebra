>[!note]
>Ha come sintassi delle FBF con solo $\lnot,\Rightarrow$. Utilizza gli stessi assiomi della teoria L assieme a: $$\text{Ax}:\begin{cases}
>(\forall x\space A(x))\Rightarrow A[t\mathbin{/}x]\qquad\text{dove }t\text{ è un termine libero per }x \\
>\forall x\space (A\Rightarrow B)\Rightarrow (A\Rightarrow \forall x\space B)
>\end{cases}$$
>Inoltre ha come regole di inferenza:
>1. Modus ponens $A,A\Rightarrow B\vdash_{K}B$
>2. Generalizzazione: $A(x)\vdash_{K}\forall x\space A(x)$
>
>Diciamo $\Gamma\vdash_{K} A$ se esiste $A_{1},\cdots,A_{m}$ tale che: $$\Gamma\vdash_{K}A_{1},\quad\Gamma\cup\set{A_{1}}\vdash_{K}A_{2},\quad\cdots,\Gamma\cup\set{A_{1},\cdots,A_{m-1}}\vdash_{K}A_{m}$$
>Dove ciascuna $A_{i}$ è assioma appartenente a $\Gamma\cup\set{A_{1},\cdots,A_{i-1}}$ oppure è ottenuta mediante una regola di inferenza da $\Gamma\cup\set{A_{1},\cdots, A_{i-1}}$.
>
>Per il teorema di correttezza a completezza forte la teoria K è:
>- Corretta: $\Gamma\vdash A\Rightarrow\Gamma\models A$
>- Completa: $\Gamma\models A\Rightarrow\Gamma\vdash A$

>[!tip]
>La teoria K è indecidibile.

Se $\Gamma\neq\emptyset$, pensiamo a $\Gamma$ come degli assiomi di una teoria.

### Teoria K con assiomi propri
>[!note] Teoria con identità (uguaglianza)
>Abbiamo bisogno di una lettera predicativa $E(x,y)$ che catturi la relazione di uguaglianza: $$\Gamma=\begin{cases}
>\forall x\space E(x,x) \\
>\forall x\space\forall y\space \left(E(x,y)\Rightarrow (A(x\space|\space x)\Rightarrow A(x\space|\space y\mathbin{/}x)\right)
>\end{cases}$$
>In una teoria simile possiamo definire il concetto di esistenza unica: $$\exists! x\space A(x)\equiv \exists x\space(A(x)\land\forall y( A(y)\Rightarrow E(x,y)))$$

>[!note] Teoria con identità dei numeri naturali
>Prima formulazione assiomi di Peano:
>1. $0$ è un numero naturale
>2. Se $x$ è un numero naturale, allora ne esiste un altro $S(x)$ detto successivo di $x$
>3. $0\neq S(x)\quad\forall x$
>4. Se $S(x)=S(y)\Longrightarrow x=y$
>5. Principio di induzione: se $Q$ è una proprietà su $\mathbb{N}$ che soddisfa:
>	- $0$ soddisfa $Q$
>	- se ogni volta che $x$ soddisfa $Q$, anche $S(x)$ soddisfa $Q$
>Allora tutti i naturali soddisfano $Q$.

>[!tip] Assiomi teoria dei numeri naturali
>Abbiamo come lettere funzionali $f(x)=x+1,\quad S(x,y)=x+y,\quad P(x,y)=x\cdot y$ e come costante $0$:
>$$\begin{align*}
&\forall x\space(\lnot E(0,f(x)))&0\neq S(x)\quad\forall x&\\
&\forall x\space\forall y\space(E(f(x),f(y))\Rightarrow E(x,y))&S(x)=S(y)\Longrightarrow x=y&\\
&\forall x\space(E(S(x,0),x))&x+0=x\\
&\forall x\space\forall y\space(E(S(f(x),y),f((S(x,y)))))& (x+1)+y=(x+y)+1\\
&\forall x\space E(P(x,0),0)&x\cdot 0=0\\
&\forall x\space\forall y\space(E(P(x,f(y)),S(P(x,y),x)))& x\cdot (y+1)=x\cdot y+x\\
&( A(0)\land \forall x\space(A(x)\Rightarrow A(f(x))))\Longrightarrow\forall x\space A(x)&\text{Principio di induzione per }A
\end{align*}$$

### Primo teorema di incompletezza di Gödel
>[!note]
>Se $S$ è una teoria del primo ordine che contiene l'aritmetica ($S_{1},\cdots,S_{n}\in S$) e che sia consistente (cioè non produca sia $\varphi$ che $\lnot\varphi$), allora esiste una FBF $\psi$ tale che né $\psi$ né $\lnot\psi$ sono dimostrabili: $S\not\vdash_{K}\psi$ e $S\not\vdash_{K}\lnot\psi$. Inoltre $\psi$ è un affermazione che è vera nella teoria dei numeri naturali.

