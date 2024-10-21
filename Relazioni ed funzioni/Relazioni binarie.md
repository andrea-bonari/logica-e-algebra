>[!note]
>Una relazione binaria è una relazione $R$ tale che: $$R\subseteq A\times A$$

### Proprietà di una relazione binaria
>[!tip] Serialità
>La proprietà formale è: $$\forall a\in A\quad \exists b\in A\qquad(a,b)\in R$$
>Possiamo dire che nella rappresentazione a grafo di adiacenza ogni vertice ha una freccia uscente, mentre nella matrice di adiacenza ogni riga ha almeno un elemento non nullo.

>[!tip] Riflessività
>La proprietà formale è: $$\forall a\in A\qquad (a,a)\in R$$
>Nel grafo ogni elemento avrà una relazione con se stesso, mentre nella matrice di adiacenza avremo solo $1$ sulla diagonale ($I=\set{(a,a):\quad a\in A} \subseteq M_{R}$). 

>[!tip] Simmetria
>La proprietà formale è: $$\forall a,b\in A\qquad (a,b)\in R\Longrightarrow (b,a)\in R$$
>Nel grafo di adiacenza ogni elemento avrà una relazione con se stesso, inoltre ogni nodo uscente da $a$ a $b$ avrà un nodo rientrante da $b$ ad $a$. Nella matrice di adiacenza equivarrà a dire $M_{R}=M_{R}^{T}$.

>[!tip] Antisimmetria
>La proprietà formale è: $$\forall a,b \in A\qquad (a,b)\in R\text{ e } (b,a)\in R\Longrightarrow a=b$$
>Nel grafo di adiacenza ogni elemento avrà una relazione con se stesso. Inoltre ogni nodo uscente da $a$ in $b$ non dovrà avere un nodo rientrante da $b$ ad $a$. Nella matrice di adiacenza equivarrà a dire $R\cap R^{-1}\subseteq I_{A}$.

>[!tip] Transitività
>La proprietà formale è: $$\forall a,b,c\in A\qquad (a,b)\in R\text{ e }(b,c)\in R\Longrightarrow (a,c)\in R$$
>Nella matrice di adiacenza equivarrà a dire $$R^{2}\subseteq R$$

Un paio di osservazioni su queste proprietà:
- $\text{Seriale}\centernot{\Longrightarrow}\text{Riflessiva}$, tuttavia $\text{Riflessiva}\Longrightarrow\text{Seriale}$
- $\text{Antisimmetria}\centernot{\Longrightarrow}\text{Non simmetrica}$
- $\text{Transitiva}+\text{Simmetrica}\centernot{\Longrightarrow}\text{Riflessiva}$
- $\text{Transitiva}+\text{Seriale}+\text{Simmetrica}\Longrightarrow\text{Riflessiva}$

>[!tip] Comportamento delle proprietà rispetto a delle operazioni
>$$R,T\subseteq A\times A$$
>
>| $$R,T$$                   | $$R\cap T$$    | $$R\cup T$$    | $$R\times T$$  | $$R^{-1}$$     |
>| ------------------------- | -------------- | -------------- | -------------- | -------------- |
>| $$\text{Seriale}$$        | $$\bigtimes$$  | $$\checkmark$$ | $$\checkmark$$ | $$\bigtimes$$  |
>| $$\text{Riflessiva}$$     | $$\checkmark$$ | $$\checkmark$$ | $$\checkmark$$ | $$\checkmark$$ |
>| $$\text{Simmetrica}$$     | $$\checkmark$$ | $$\checkmark$$ | $$\bigtimes$$  | $$\checkmark$$ |
>| $$\text{Antisimmetrica}$$ | $$\checkmark$$ | $$\bigtimes$$  | $$\bigtimes$$  | $$\checkmark$$ |
>| $$\text{Transitiva}$$     | $$\checkmark$$ | $$\bigtimes$$  | $$\bigtimes$$  | $$\checkmark$$ |

