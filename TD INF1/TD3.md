# INF1 - TD3
### Exercice 1: Carre

1. Ecrire une fonction Java `lireEnier()` qui renvois un entier saisi par l utilisateur. Cette fonction ne dois rien afficher.
```Java
import java.util.Scanner;

public static int lireEntier() {
	Scanner sc = new Scanner(System.in);
	return sc.nextInt();
}
```

2. Ecrire une fonction Java `carre()` qui prends en entree un entier `a` et qui renvois `a²`.
```Java
public static int lireEntier(int a) {
	return a*a;
}
```

3. Ecrire un programme Java qui demande a l'utilisateur de saisir un entier au clavier et qui qffiche le carre de ce nombre Ce programme doit appeller les fonctions   `lireEnier()` et  `carre()` .
```Java
import java.util.Scanner;

public class Main {
	public static int lireEntier() {
		Scanner sc = new Scanner(System.in);
		System.out.println("Rentrez un nombre a elever au carre")
		return sc.nextInt();
	}

	public static int lireEntier(int a) {
		return a*a;
	}

	public static void main(String[] args) {
		int nombre = lireEntier();
		System.ourt.println(carr(nombre));
	}
}
```

### Exercice 2: Pyramide de nombres

Nous souhaitons pouvoir afficher une pyramide de nombres, de hauteur n  strictemment positive. Voici ce a quoi doit ressembeler la pyramide:

pour n= 4:
```

1
12
123
1234
```
pour n = 5
```

1
12
123
1234
12345
```

En programation, il est souvent pertinent d'introduire des fonctions intermediaires qui permettent de decomposer le probleme en sous-problemes. Un sous-probleme pertinent a isoler dans une fonction intermediaire est l affichage d une seule ligne de la pyramide, la i-eme ligne.

1. Ecrire une fonction  `afficheLigne` qui prend i un entier posit
```Java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args){  
        Scanner sc = new Scanner(System.in);  
        int h = sc.nextInt();  
        StringBuilder sb = new StringBuilder();  
        for (int i = 1; i <= h; i++){  
            sb.append(i+" ");  
           
        } 

         System.out.println(sb);  
    }  
}
```

## 3 Date du lendemain

```Java
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args){  
        Scanner sc = new Scanner(System.in);  
        int year = sc.nextInt();  

		
    }  
    public static boolean isLeapYear(int year) {  
	   return year%4 == 0 && year % 100 != 0 || year % 400 == 0;  
	}
}
```