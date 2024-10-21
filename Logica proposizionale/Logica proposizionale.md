>[!note]
>La logica proposizionale è un linguaggio composto da un alfabeto di:
>1) Lettere enunciative (ente atomico) al più numerabile
>2) Connettivi: $\lnot,\land,\lor,\Rightarrow,\Leftrightarrow$
>3) Ausiliari: $),($
>
>Tra tutte le stringhe generabili su questo alfabeto, individuo le Formule Ben Formate (FBF):
>- Ogni lettera enunciativa è una FBF.
>- Se $A,B$ sono FBF, allora $(A\Rightarrow B)$, $(A\Leftrightarrow B)$, $(A\land B)$, $(A\lor B)$, $(A\lnot B)$ sono FBF.
>- Nient'altro è una FBF.

>[!tip] Sottoformule
>Le sottoformule di una FBF $F$ sono sottostringhe di $F$, che sono FBF. Dato $F$ si può costruire l'albero delle sue sottoformule.

>[!tip] Priorità degli operatori
>Introduco una priorità sugli operatori, come in aritmetica:
>$$\lnot>\land>\lor>\Rightarrow>\Leftrightarrow $$
>E connettivi uguali si associano a sinistra.

### Semantica
>[!note]
>Un interpretazione è una funzione: $$\nu:\set{F: F\text{ è una FBF}}\to\set{0,1}$$
>Che soddisfa:
>- $\nu(\lnot A)=1-\nu( A)$
>- $\nu(A\land B)=\min(\set{\nu(A),\nu(B)})$
>- $\nu(A\lor B)=\max(\set{\nu(A),\nu(B)})$
>- $\nu(A\Rightarrow B)=\max(\set{1-\nu(A),\nu(B)})$
>- $\nu(A\Leftrightarrow B)=\min({\max({1-\nu(A),\nu(B)}),\max({\nu(A),1-\nu(B)})})$
>
>Queste sono rappresentabili come tabelle di verità:
>$$\begin{array}{|c c|c|c|c|c|}
>\nu(A) & \nu(B) & \nu(A \land B) & \nu(A\lor B) & \nu(A\Rightarrow B) & \nu(A\Leftrightarrow B)\\
>\hline
>0 & 0 & 0 & 0 & 1 & 1\\ 0 & 1 & 0 & 1 & 1 & 0\\ 1 & 0 & 0 & 1 & 0 & 0\\ 1 & 1 & 1 & 1 & 1 &1 \\ \end{array}$$
>Un interpretazione è un assegnamento alle lettere enunciative (variabili) e la verità ($1$) o meno ($0$) di una formula dipende da questo assegnamento e dalle tabelle di verità.

### Soddisfacibilità
>[!note]
>Una FBF $A$ si dice soddisfacibile se esiste un interpretazione $\nu$ tale che $\nu(A)=1$. In questo caso $\nu$ è chiamato un modello di $A$ e scriviamo $\nu\models A$. In caso contrario $A$ si dice insoddisfacibile.

I modelli di una formula sono le righe che rendono vera $A$.

Una FBF $A$ con $\nu(A)=1$ per ogni interpretazione si dice una tautologia, e la scriviamo $\models A$.

### Conseguenza semantica
>[!note]
>Una FBF $A$ si dice essere conseguenza semantica di un insieme $\Gamma$ di FBF ($\Gamma\models A$) se ogni modello di $\Gamma$ è anche modello di $A$.
>
>Inoltre, per il teorema della deduzione semantica: $$\Gamma\cup\set{B}\models A\Leftrightarrow \Gamma\models(B\Rightarrow A)$$
>Per il teorema del legame tra insoddisfacibilità e conseguenza semantica: $$\Gamma\models A\text{ se e solo se }\Gamma\cup\set{\lnot A} \text{ è insoddisfacibile}$$

Per verificare che $\Gamma\models A$:
- Calcolo i modelli di $\Gamma$
- Verifico che questi siano anche modelli di $A$

>[!example] Dimostrazione
>Sia $\nu$ un interpretazione:
>- Se $\nu$ non è modello di $\Gamma$, allora non è modello di $\Gamma\cup\set{\lnot A}$
>- Se $\nu$ è modello di $\Gamma$, allora dall'ipotesi $\Gamma\models A$ allora $\nu$ è modello di $A$: $\nu(A)=1\Rightarrow\nu(\lnot A)=0$, cioè $\nu$ non è modello di $\Gamma\cup\set{\lnot A}$

### Equivalenza semantica
>[!note]
>Due FBF $A$ e $B$ si dicono semanticamente equivalenti ($A\equiv B$) se $A$ e $B$ hanno gli stessi modelli: $$A\models B\text{ e }B\models A$$
>Cioè hanno la stessa tabella di verità.

>[!tip]
>$$A\equiv B\text{ se e solo se }\models A\Leftrightarrow B$$

Data una tavola di verità, è possibile costruire il suo rappresentante $[A]_{\equiv}$ nei seguenti metodi:

>[!tip] Forma normale congiuntiva
>Guardiamo nella tabella di verità le righe con $0$: $$F\equiv (\text{prima riga con }0)\land(\text{seconda riga con }0)\land\cdots\land(n-\text{esima riga con }0)$$

>[!tip] Forma normale disgiuntiva
>Guardiamo nella tabella di verità le righe con $1$:
>$$F\equiv (\text{prima riga con }1)\lor(\text{seconda riga con }1)\lor\cdots\lor(n-\text{esima riga con }1)$$

È sempre possibile trasformare una FBF in un'equivalente che contiene solo i connettivi: $$\set{\lnot,\land}\quad\set{\lnot,\lor}\quad\set{\lnot, \Rightarrow}$$
Detti connettivi completi adeguati. L'equivalenza non è unica.