# INF1 - TD2

### Exercice 1: Les `if` imbriques

On considere la suite d'instruction suivante, ou a et b sont deux variables de type entier :
```Java
if (a > b){
	if (a > 10) System.out.println("1");
	else if (b < 10) System.out.println("2");
} else {
	if (a == b) System.out.println("3");
	else System.out.println("4");
}
```

1. Pour quelles valeurs de a et b ce programme affiche-t-il respectivement 1,2,3,4 ?
> 1 -> `a > 10` && `b < 10`
>2 -> `a < 10` && `b < 10`
>3 -> `a == b`
>4 -> `a < b`

2. Existe-t-il des valeurs de a et b pour lesquelles ce programme n affiche rien ?
Non car tout les `if` possedent un `else` donc touts les cas sont traites

 3. Peut-on simplifier le code , et si oui comment ?
 4. 