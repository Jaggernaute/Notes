# Qu'est-ce que la calculabilite ?

## 1. Qu'est-ce que qu'une fonction calculable ?


```ad-abstract 
title: Fonctions calculables :
Une fonction est calculable si elle possede un algorithme. Si elle peu etre programme dans un langage suffisament expressif (de preference Turing complete) et execute sur un ordinateur sufisament puissant
```

Cette definition peu etre demontre empiriquement :
- Les progres technologiques permettent d executer plus rapidement les programmes 
- Les differentss paradigmes de calculs (quantiques ou biologiques) 
- Les nouveaux systemes d exploitation / langages / compilateurs / interpreteurs

Touts ces facteurs ne permettent pas d'augmenter la classe des fonctions calculables.

_Un probleme subsiste :_
	Quelle est la garntie que le progres ne vas pas un jour depasser cette definition,  qu'un nouveau paradigme de calcul ou une nouvelle maniere de raisoner permettant de consifderer comme calculables une plus large classe de fonctions n'emergera pas ?
	C'est le sujet de la these de Church-Turing en 1936.

**Cette definition reste pour l'instant tres informelle.**

Au regard de cette définition, la plupart (si ce n'est la totalité) des fonctions usuelles sont calculables. Comme l'addition / la multiplication / la fonction $(n,m)\mapsto n^m$ / la fonction qui a $n$assossie le $n$-eme nombre premier ou encore  celle qui calcule le plus grand diviseur commun de deux entiers. On peux aussi citer des exemples moins triviaux: la fonctionqui prends un programme ecrit en C++ et determine si le programme est syntaxiquement correct (c'est ce que fait entre autre un compilateur pour C++), ou encore celle qui renvois la $n$-eme decimale de $\pi$, $\sqrt{2}$ou du nombre d'or (chaqun de ces nombres est la somme d'une suite calculable de rationels de convergence suffisament rapide) ou pour finir celle qui q $n$ associe le nombre de partie possibles que l'on peu faire sur un plateau au jeu de Go, (appelé aussi *goban*) de taille $n\times n$. Ce dernier illustre bien le fait qu'en calculabilite on ne s'occupe pas du temps que prends le calcul. Seule l'existence d'un algorithme nous importe.

Dans le cas du jeu de go  le principe de base est plutot simple, il "suffit" de lister toutes les partie possibles et de les compter,cependant le temps d'execution d un tel alogorithme est telement grand que cela le rends impossible a utiliser en pratique pour $n>2$. Pour $n=19$ (qui est la taille d'un goban standard) ce nombre est compris entre $10^{10^{48}}$ et $10^{10^{171}}$, meme avec touts les ordinateurs du monde pendant un milliard d années ca fait clairement trop de parties a simuler.

Meme si la multiplication par 2 nous estbien plus accessible que la fonction qui calcule les partie de jeu de go, 

## 2. Quelles sont les fonctions incalculables ?

The halting problem (Church / Turing thesis).