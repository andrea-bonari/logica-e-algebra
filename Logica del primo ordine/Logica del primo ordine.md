>[!note]
>La logica del primo ordine è un linguaggio composto da un alfabeto di:
>1. Costanti: $a,b,c,\cdots$ (al più numerabile)
>2. Variabili: $x_{1},x_{2},\cdots$ (al più numerabile)
>3. Lettere funzionali: $f_{1}^{n_{1}},f_{2}^{n_{2}},\cdots$ (al più numerabile), dove $n_{i}\in\mathbb{N}_{>0}$ indica la molteplicità delle variabili di ingresso della lettera funzionale
>4. Lettere predicative: $A_{1}^{n_{1}},A_{2}^{n_{2}},\cdots$ (al più numerabile), dove $n_{i}\in\mathbb{N}_{>0}$ indica la molteplicità delle variabili di ingresso della lettera predicativa
>5. Connettivi: $\lnot,\land,\lor,\Rightarrow,\Leftrightarrow$
>6. Quantificatori: $\forall x_{i}$ (quantificativa) e $\exists x_{i}$ (esistenziale)
>7. Simboli ausiliari $),($

>[!tip] Termini
>I termini sono composizioni di lettere funzionali che descrivono composizioni di operazioni.

Ogni variabile e costante sono dei termini. Inoltre se ho $n$ termini $t_{1},t_{2},\cdots,t_{n}$ e se $f^{n}$ è una lettera funzionalità di arità $n$, allora $f^{n}(t_{1},t_{2,},\cdots,t_{n})$ è un termine.

>[!tip] Formule atomiche
>Se $A^{n}$ è una lettera predicativa di arità $n$ e $t_{1},\cdots,t_{n}$ sono termini, allora $A^{n}(t_{1},t_{2},\cdots,t_{n})$ è una forma atomica.

>[!tip] Formule Ben Formate
>1. Ogni formula atomica è una FBF
>2. Se $A$ è una FBF, allora $(\lnot A)$, $(\forall x A)$, $(\exists xA)$ sono FBF
>3. Se $A,B$ sono FBF, allora $(A\land B)$, $(A\lor B)$, $(A\Rightarrow B)$, $(A\Leftrightarrow B)$ sono FBF

>[!tip] Priorità degli operatori
>Introduco una priorità sugli operatori, come in aritmetica:
>- $\lnot$, $\forall$, $\exists$ vengono associati con l'ordine in cui vengono letti.
>- I connettivi uguali sono associati a sinistra.
>- $\lnot,\forall,\exists>\land>\lor>\Rightarrow>\Leftrightarrow$

Le sottoformule e l'albero delle sottoformule si costruiscono in modo analogo al caso proposizionale.

Definiamo il campo di azione di un quantificatore come la sottoformula a cui quel quantificatore si riferisce. Se una variabile $x$ cade nel campo d'azione $\forall x/\exists x$ allora $x$ si dice vincolata, altrimenti si dice libera.

Una FBF si dice chiusa se non ha variabili libere, se invece $f(x_{1},\cdots,x_{n})$ ha $n$ variabili $x_{1},\cdots,x_{n}$ libere possiamo:
- Chiudere universalmente ($\forall x_{1}\space\cdots\space\forall x_{n}\space f(x_{1},\cdots,x_{n})$)
- Chiudere esistenzialmente ($\exists x_{1}\space\cdots\space\exists x_{n}\space f(x_{1},\cdots,x_{n})$)

Una variabile $y$ è libera per la variabile libera $x$, cioè $x$ è libera nel campo di azione di $\forall y$ o $\exists y$.

### Semantica
>[!note]
>L'interpretazione (o struttura) è una coppia $<D,I>$ dove:
>- $D$ è un insieme, detto dominio su cui le variabili prendono valori
>- $I=(I_{1},I_{2},I_{3})$ sono tre funzioni tali che:
>	- $I_{1}: \text{const}=\set{\text{costanti del linguaggio del primo ordine}}\to D\quad a\in\text{const}\quad I(a)\in D$
>	- $I_{2}: \set{\text{Lettere funzionali del linguaggio}}\to\set{\text{operazioni interne }n\text{-arie su }D}$ dove $f^{n}$ è lettera funzionale di arità $n$, allora $I(f^{n}): \underbrace{D\times\cdots\times D}_{n\text{ volte}}\to D$
>	- $I_{3}:\set{\text{Lettere predicative del linguaggio}}\to\set{\text{tutte le relazioni }n\text{-arie su }D}$ dove $\forall A^{k}$ è una lettera predicativa di arità $k$, allora $I_{3}(A^{k})\subseteq \underbrace{D\times\cdots\times D}_{k\text{ volte}}$

La verità di una FBF dipende dagli assegnamenti delle variabili.

>[!tip] Assegnamento
>Dato un linguaggio $L$ del primo ordine, e una interpretazione $<D,I>$, un assegnamento è una funzione: $$s:\underbrace{\text{Var}(L)}_\text{variabili del linguaggio}\to D$$
>Questo assegnamento può essere esteso ai termini di $L$: $$s^{\forall}:\text{Ter}(L)\to D$$
>Nel seguente modo:
>1. $s^{*}(a)=I_{1}(a)\quad\forall a\in\text{Const}(L)$
>2. $s^{*}(x)=s(x)\quad\forall x\in\text{Var}(L)$
>3. Induttivamente $f^{n}$ è una lettera funzionale di $L$ di arità $n$, e $t_{1},\cdots,t_{n}\in\text{Ter}(L)$, allora $s^{*}(f^{n}(t_{1},\cdots,t_{n}))=I_{2}(f^{n})(s^{*}(t_{1}),\cdots,s^{*}(t_{n}))$.

>[!tip] Soddisfacibilità di una FBF
>Sia $<D,I>$ un interpretazione di un linguaggio $L$ del primo ordine e sia: $s:\text{Var}(L)\to D$ un assegnamento, diciamo che la FBF $p$ è soddisfatta da $s$ e scriviamo: $$<D,I>,s\models \rho$$
>Se:
>1. nel caso $\rho=A^{n}(t_{1},\cdots,t_{n})$ è una formula atomica: $$(s^{*}(t_{1}),\cdots,s^{*}(t_{n}))\in I_{3}(A^{n})\subseteq D\times\cdots\times D$$
>2. nel caso $\rho=\lnot\psi$ se $\psi$ non è soddisfatta da $s$: $$<D,I>,s\not\models\psi$$
>3. nel caso $\rho=\psi\land\eta$ (oppure $\rho=\psi\lor\eta$) se: $$<D,I>,s\models \psi\quad\text{ e (o) }\quad<D,I>,s\models\eta$$
>4. nel caso $\rho=\psi\Rightarrow\eta$ (oppure $\rho=\psi\Leftrightarrow\eta$) se: $$\text{se }<D,I>,s\models \psi\text{ allora (oppure se e solo se) }<D,I>,s\models \eta$$
>5. nel caso $\rho=\forall x\psi$ allora $<D,I>,s\models\rho$ se: $$\forall d\in D\qquad <D,I>,s[d \mathbin{/}x]\models\psi$$dove $s[d \mathbin{/}x]$ indica l'assegnazione uguale ad $s$ tranne in un $x$ in cui vale $d$.
>6. nel caso $\rho=\exists x\psi$ se: $$\exists d\in D\text{ tale che } <D,I>,s[d \mathbin{/}x]\models\psi$$

Data un interpretazione $<D,I>$ su un linguaggio $L$ del primo ordine e $\rho$ FBF su L diciamo che $\rho$ è:
- soddisfacibile: se esiste un assegnamento $s:\text{Var}(L)\to D$ che soddisfa $<D,I>,s\models\rho$, in questo caso $<D,I>,s$ è chiamato modello di $\rho$.
- vera: se ogni assegnamento $s:\text{Var}(L)\to D\qquad <D,I>,s\models\rho$, in questo caso scriviamo $<D,I>\models\rho$ 
- falsa: se non esiste nessun assegnamento $s:\text{Var}(L)\to D\qquad <D,I>,s\models\rho$. Quindi $\rho$ è falsa quando non ha modelli.
- logicamente valida: se per ogni interpretazione $<D,I>\quad <D,I>\models\rho$, scriviamo $\models\rho$
- logicamente contraddittoria/insoddisfacibile: se per ogni interpretazione $<D,I>\quad<D,I>\space\not\models\rho$ non ho modelli.

In generale $\rho$ è vera se e solo se la sua chiusura universale è vera. Inoltre $\rho$ è soddisfacibile se e solo se la sua chiusura esistenziale è vera.

### Modello e conseguenza semantica
>[!note]
>Una terna $<D,I,s>$ ($s$ assegnamento) tale che $<D,I>,s\models\varphi$ si dice un modello di $\varphi$.
>Dato un inseme $\Gamma$ di FBF, diciamo che $<D,I,s>$ è un modello di $\Gamma$ se $<D,I,s>$ è modello di ogni $\psi\in\Gamma$. Diciamo che $\varphi$ è conseguenza semantica di $\Gamma$ (scriviamo $\Gamma\models\varphi$) se ogni modello di $\Gamma$ è modello di $\varphi$.

>[!tip]
>Se $\varphi$ non ha modelli, allora è insoddisfacibile o logicamente contraddittoria. Per estensione diciamo che $\Gamma$ è insoddisfacibile se non ha modelli.

Per il teorema di insoddisfacibilità e conseguenza semantica:
$$\Gamma\models\phi\text{ se e solo se }\Gamma\cup\set{\lnot\varphi}\text{ è insoddisfacibile}$$
Inoltre per il teorema di deduzione semantica: $$\Gamma\cup\set{\psi}\models\varphi\text{ se e solo se } \Gamma\models\psi\Rightarrow \psi$$

Due FBF $\psi,\varphi$ si dicono semanticamente equivalenti ($\psi\equiv\varphi$) se $\varphi\models\psi$ e $\psi\models\varphi$ (cioè hanno gli stessi modelli).

>[!tip]
>$$\psi\equiv\varphi\text{ se e solo se } \models\psi\Leftrightarrow\varphi\quad (\psi\Leftrightarrow\varphi\text{ è logicamente valida})$$

### Forma normale prenessa
>[!note]
>Una FBF $A$ si dice in forma normale prenessa se è della forma: $$A=Q_{1}x_{1}\space Q_{2}x_{2}\space\cdots\space Q_{n}x_{n}\space B(x_{1},\cdots,x_{n})\qquad Q_{i}\in\set{\forall,\exists}$$
>Dove $B(x_{1},\cdots,x_{n})$ è una FBF che non contiene quantificatori nelle variabili libere $x_{1},\cdots,x_{n}$ ($B(x_{1},\cdots,x_{n})$ è chiamata la matrice di $A$).
>
>Data una FBF $F$, esiste sempre una FBF $A$ tale che $F\equiv A$ e $A$ è in forma normale prenessa (FNP). Inoltre c'è un algoritmo per portare $F$ in FNP.

Uso le seguenti equivalente semantiche per portare in testa i quantificatori: 
1. $\lnot\forall x B\equiv \exists x\lnot B$ e $\lnot\exists xB\equiv \forall x\lnot B$ con $x$ variabile libera in $B$. $y$ è una variabile che è un termine libero per $x$ se non succede $\forall y(x)$ o $\exists y(x)$. Questo succede se per esempio $y$ non compare in $B(x)$. Con $B[y \mathbin{/}x]$ indico la forma in cui alla variabile libera $x$ sostituisco $y$.
2. $(\forall x B(x)\land\mathcal{E})\equiv\forall y(B[y/x]\land\mathcal{E})$ o $(\exists x B(x)\lor\mathcal{E})\equiv\exists y(B[y/x]\lor\mathcal{E})$ se $y$ non compare in $\mathcal{E}$ e $y$ è libera per $x$ in $B(x)$.
3. $\forall x B(x)\Rightarrow\mathcal{E}\equiv\exists y( B[y  \mathbin{/} x] \Rightarrow\mathcal{E})$ o $\exists x B(x)\Rightarrow\mathcal{E}\equiv\forall y( B[y  \mathbin{/} x] \Rightarrow\mathcal{E})$ se $y$ non compare in $\mathcal{E}$ e $y$ è libera per $x$ in $B(x)$.
4. $\mathcal{E}\Rightarrow\forall x B(x)\equiv \forall y(\mathcal{E}\Rightarrow B[y \mathbin{/}x])$ o $\mathcal{E}\Rightarrow\exists x B(x)\equiv \exists y(\mathcal{E}\Rightarrow B[y \mathbin{/}x])$.

Ricordando che se $\mathcal{E}$ non contiene occorrenze libere di $x$ la sostituzione $y \mathbin{/}x$ è inutile.

### Forma di Skolem
>[!note]
>Partendo da una FBF $A$ in FNP, la forma di Skolem trasforma $A$ in una FBF $A_{\text{SK}}$ che non contiene quantificatori esistenziali.

Uso il seguente algoritmo per portare una FBF $A$ in FNP in forma di Skolem:
1. Chiudiamo universalmente le variabili non quantificate: $$\begin{matrix}Q_{m+1}x_{m+1}\cdots Q_{n}x_{n} \space B(x_{1},\cdots,x_{m},\cdots,x_{n})\\\downarrow\\ \forall x_{1}\space\cdots\forall x_{m}\space Q_{m+1}x_{m+1}\cdots\space Q_{n}x_{n} \space B(x_{1},\cdots,x_{m},\cdots,x_{n})\end{matrix}$$
2. Finché ci sono quantificatori universali nella FBF: $$y=\forall x_{1}\space\cdots\space\forall x_{j-1}\space\underbrace{\exists x_{j}}_\text{primo quantificatore esistenziale} Q_{j+1} x_{j+1}\space\cdots Q_{n} x_{n} \space B(\cdots)$$Costruisci la nuova FBF: $$y'=\forall x_{1}\space\cdots \forall x_{j-1}\space Q_{j+1} x_{j+1}\space\cdots\space Q_{n}x_{n}\space B[f(x_{1},\cdots,x_{j-1})   \mathbin{/}x_{j}]$$Dove $f(x_{1},\cdots,x_{j-1})$ è una nuova lettera funzionale di arità $j-1$, cioè quanti sono i quantificatori universali che ho prima di $\exists x_{j}$.

>[!tip]
>$F_{\text{SK}}$ non è in generale semanticamente equivalente a $F$, ma si dimostra che se $<D,I,s>$ è modello di $F_{\text{SK}}$, allora lo è per $F$: $$<D,I>,s\models F_{\text{SK}}\text{ allora } <D,I>,s\models F$$
>Tuttavia, visto che in $F_{\text{SK}}$ ci sono nuove lettere funzionali, non è vero che un modello di $F$ lo è anche di $F_{\text{SK}}$, ma si dimostra che $<D,I>,s$ si può estendere ad un modello $<D,I',s'>$ di $F$: $$<D,I>,s\models F\text{ allora esiste un modello esteso }<D,I',s'>\text{ tale che }<D,I'>,s'\models F_{\text{SK}}$$

