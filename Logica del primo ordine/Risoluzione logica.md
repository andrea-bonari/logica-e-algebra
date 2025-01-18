>[!note]
>Troviamo le clausole di una FBF $F$:
>- Se $F$ non è chiusa, chiuderla universalmente.
>- Portare $F$ in forma di Skolem $F_{\text{SK}}$.
>- Portare la matrice di $F_{\text{SK}}$ in FNC.
>- Rinomino le variabili tar clausole in modo distinto, per avere il massimo grado di libertà per trovare $\square$.
>
>Per risolvere due clausole utilizziamo la sostituzione.

### Sostituzione
>[!note]
>Una sostituzione $\sigma$ è una scrittura: $$\sigma=\set{ t_{1} \mathbin{/}    x_{1},\cdots,t_{n} \mathbin{/}x_{n}}$$
>Dove $x_{1},\cdots,x_{n}$ sono variabili distinte, mentre $t_{1},\cdots,t_{n}$ sono termini. Date delle espressioni del primo ordine $E_{1},\cdots,E_{m}$ e una sostituzione $\sigma$, con $E_{i}\cdot\sigma$ indico l'espressione ottenuta sostituendo alle variabili in $E_{1}$ i termini corrispondenti in $\sigma$. Se $E_{1}\cdot\sigma=E_{2}\cdot\sigma=\cdots=E_{m}\cdot\sigma$ diciamo che $\sigma$ è un unificatore di $E_{1},\cdots,E_{m}$.

Date due sostituzioni: $$\begin{align*}
\sigma&= \set{t_{1}\mathbin{/}x_{1},\cdots,t_{k}\mathbin{/}x_{k},\cdots,t_{n}\mathbin{/}x_{n}}\\
\theta&= \set{v_{1}\mathbin{/}x_{1},\cdots,v_{k}/x_{k},u_{1}/y_{1},\cdots,u_{l}\mathbin{/}y_{l}}
\end{align*}$$
La sostituzione composizione è definita come: $$(\sigma\cdot\theta)=\set{t_{1}\cdot\theta\mathbin{/}x_{1},\cdots,t_{n}\cdot\theta/x_{n},u_{1}/y_{1},\cdots,u_{l}/x_{l}}$$

>[!tip] Unificatore più generale
>L'unificatore più generale delle espressioni $E_{1},\cdots,E_{m}$ è un unificatore $\sigma$ tale che per ogni altro unificatore $\rho$ di $E_{1},\cdots,E_{m}$ esiste una sostituzione $\theta$ tale che: $$\rho=\sigma\cdot\theta$$
>Cioè, $\sigma$ unifica con meno vincoli di $\rho$.

### Risolvente
>[!note]
>Una risolvente tra le due clausole $c_{1},c_{2}$ in cui supponiamo che abbiamo variabili distinte è la clausola $R$ ottenuta nel seguente modo: $$c_{1}=\set{\cdots,L_{1},\cdots,L_{e},\cdots}\qquad c_{2}=\set{\cdots,\lnot S_{1},\cdots,\lnot S_{k},\cdots}$$
>Se $\sigma$ è un unificatore più generale di $L_{1},\cdots,L_{e},S_{1},\cdots,S_{k}$, (sostituendo tutto con $L$)Allora: $$R=c_{1}\cdot\sigma\smallsetminus\set{L}\cup c_{2}\cdot \sigma\smallsetminus\set{\lnot L}$$
>E scriviamo $c_{1},c_{2}\vdash_{R}R$.

### Derivazione
>[!note]
>Sia $\Lambda^{C}$ un insieme di clausole, una derivazione della clausola $C$ da $\Lambda^{C}$ (scritto $\Lambda^{C}\vdash_{R}C$) è una sequenza $C_{1},\cdots,C_{k}=C$ delle clausole tale che:
>$$\Lambda^{C}\vdash_{R}C_{1},\quad \Lambda^{C}\cup\set{C_{1}}\vdash_{R} C_{2},\quad\cdots,\quad \Lambda^{C}\cup\set{C_{1},\cdots,C_{k}}\vdash_{R}C_{k}$$
>Dove $C_{i}$ è una risolvente tra le due clausole $\Lambda^{C}\cup\set{C_{1},\cdots,C_{k-1}}\vdash_{R}C_{k}$.
>
>Per il teorema di correttezza e completezza per refutazione diciamo che: $$\Lambda\text{ è insoddisfacibile se e solo se }\Lambda^{C}\vdash_{R}\square$$
>Inoltre: $$\Gamma\models A\text{ se e solo se }\Lambda=\Gamma\cup\set{\lnot A}\text{ è insoddisfacibile se e solo se} \Lambda^{C}\vdash_{R}\square$$