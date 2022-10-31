# INF1 - TD1

### Exercice 1:  Programme mystere

On considere la suite d'instruction suivante :
```java
int a;
a = 3;
a = 42;
a = 7 - 6;

a = a + 1;
int b = 5;
b = a + b;
a = b - a;
b = b - a;
```

1. Decrivez apres chaques instructions la valeur des differentes variables
```java
int a;       // a = 0
a = 3;       // a = 3
a = 42;      // a = 42
a = 7 - 6;   // a = 1

a = a + 1;   // a = 2
int b = 5;   // b = 5
b = a + b;   // b = 7
a = b - a;   // a = 5
b = b - a;   // b = 2
```

2. Que realise globalement la suite d instruction aux lignes `7,8 et 9` ?
```tikz
\begin{document}
\begin{tikzpicture}[thick,scale=3, every node/.style={scale=3}]
	\usetikzlibrary {arrows.meta,positioning}
	\node [draw] (a) {a};
	\node [draw] (b) [right=of a] {b};
	\draw [->] (a) to [bend left=45] (b);
	\draw [<- ] (a) to [bend right=45] (b);
\end{tikzpicture}
\end{document}
```

3. Proposez une simplification de la suite d'instructions complete excluant toute operation arithmetiques.
```java
int a = 2;
int b = 5;
int temp;

temp = a;
a = b;
b = temp;
```

```tikz
\begin{document}
\begin{tikzpicture}[thick,scale=3, every node/.style={scale=3}]
	\usetikzlibrary {arrows.meta,positioning}
	\node [draw] (a) at (0,0) {a};
	\node [draw] (b) at (2, 0) {b};
	\node [draw] (temp) at (1,-1) {temp};	
	\draw [<-] (a) to [bend left=45] (b);
	\draw [-> ] (temp) to [bend right=45] (b);
	\draw [-> ] (a) to [bend right=45] (temp);
\end{tikzpicture}
\end{document} 
```
---
### Exercice 2: XOR

On definit l'operateur $op1$ par:
$$
\begin{equation}
	\Large
	op_{1}(a,b)=(a\land\lnot b)\lor(\lnot a\land b)
\end{equation}
$$

1. Determinez la priorite des operations.
$$
\begin{equation}
	\Large
	op_{1}(a,b)=\colorbox{lime}{$(a\land\lnot b)$}\colorbox{pink}{$\lor$}\colorbox{lime}{$(\lnot a\land b)$}
\end{equation}
$$

$\colorbox{lime}{(x+y)}:$ Les blocs entre parentheses sont prioritaires sur le reste,
A l'interieur des parentheses l'operateur $\lnot$ est prioritaire sur les autres.
$\colorbox{pink}{(x+y)}:$  Ce qui se trouve en dehors des parentheses n est pas prioritaire

L'ordre des operations est simillaire a celui que l'on retrouve en algebre. A la difference de l'operateur $\lnot$ qui prends la priorite sur les parentheses.


2. Ecrivez la table de verite de cet operateur

| a   | b   | a $\oplus$ b |  
| --- | --- | ------------ |
| 0   | 0   | 0            |
| 1   | 0   | 1            |
| 0   | 1   | 1            |
| 1   | 1   | 0            |

```tikz
\begin{document}
\Large
\usetikzlibrary {circuits.logic.US}
\begin{tikzpicture}[circuit logic US,thick,scale=3, every node/.style={scale=1}]
  \node[xor gate,inputs={nn}, point right]  (or1)  at (-3,0) {$\oplus$};
  \draw [black,very thick] (or1.input 1) -- ++(left:1) node [above]{a};
  \draw [black,very thick] (or1.input 2) -- ++(left:1) node [above]{b};
  \draw [black,very thick] (or1.output) -- ++(right:1) node [above]{$a\oplus b$};
\end{tikzpicture}
\end{document}
```

3. Montrez que $op_{1}(a,b)$ est aussi egale a $(a\lor b)\land(\lnot a\land\lnot b)$. Cet operateur est le "OU exclusif" aussi appelle "XOR".
4. 
| a   | b   | a $\oplus$ b  | $(a\lor b)\land(\lnot a\land\lnot b)$    |
| --- | --- | ------------ | ------------------------------------- |
| 0   | 0   | 0            | 0                                     |
| 1   | 0   | 1            | 1                                     |
| 0   | 1   | 1            | 1                                     |
| 1   | 1   | 0            | 0                                     |

```tikz
\begin{document}
\usetikzlibrary {circuits.logic.US}
\begin{tikzpicture}[circuit logic US,thick,scale=3, every node/.style={scale=1}]
  \node[not gate,inputs={n}, point right]  (not1)  at (-2.5,0.5) {$\lnot$};
  \draw [black,very thick] (not1.input) -- ++(left:0.5) node [above]{a};
  \draw [black,very thick] (-1.95,0.5) -- ++(down:0.4);

  \node[not gate,inputs={n}, point right]  (not2)  at (-2.5,-0.5) {$\lnot$};
  \draw [black,very thick] (not2.input) -- ++(left:0.5) node [above]{b};
  \draw [black,very thick] (-1.95,-0.1) -- ++(down:0.4);

  \node[or gate,inputs={nn}, point right]  (or1)  at (-2.5,1.5) {$\lor$};
  \draw [black,very thick] (or1.input 1) -- ++(left:0.5) node [above]{a};
  \draw [black,very thick] (or1.input 2) -- ++(left:0.5) node [above]{b};
  \draw [black,very thick] (or1.output) -- ++(right:1.7) node [above]{};
  
  \draw [black,very thick] (-0.3,1.5) -- ++(down:0.9);

  \node[and gate,inputs={nn}, point right]  (or2)  at (-1,0) {$\lor$};
  \draw [black,very thick] (or2.input 1) -- ++(left:0.58) node [above]{};
  \draw [black,very thick] (or2.input 2) -- ++(left:0.58) node [above]{};
  \draw [black,very thick] (or2.output) -- ++(right:0.3);
  
  \draw [black,very thick] (-0.29,0) -- ++(up:0.4);
    
  \node[and gate,inputs={nn}, point right]  (and)  at (0.5,0.5) {$\land$};
  \draw [black,very thick] (and.input 1) -- ++(left:0.42) node [above]{};
  \draw [black,very thick] (and.input 2) -- ++(left:0.42) node [above]{};
  \draw [black,very thick] (and.output) -- ++(right:0.48) node [above]{$a\oplus b$};
\end{tikzpicture}
\end{document}
```

4. En Java, declarez deux variables booleennes a et b en initialisant a a false et b a true. Ecrivez l expression Java qui stocke le resultat du "OU exclusif" entre a et b dans une variable c

```java
boolean a = false;
boolean b = true;

boolean c = a^b;

c = ((a || b) && (!a && !b))
```
