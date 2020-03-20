nazev = "Programovací jazyk C"
tagy = ["unix", "c", "promenne", "if", "loop"]

+++
# Základní struktura

```c
int main(void){
	return 0;
}

```

Pro práci se standardním vstupem/výstupem potřebujeme importovat knihovnu `stdio.h`. Chceme-li tedy vypisovat něco na výstup, potřebujeme knihovnu.

```c
#include <stdio.h>

int main(void){
	printf("Hello World!");
	return 0;
}
```

# Proměnné

```c
#include <stdio.h>

int main(void){
	int a = 5;
	int b = 7;
	int c = a + b;

	printf("%d+%d=%d\n",a,b,c);

	return 0;
}
```

# Vstup od uživatele

```c
#include <stdio.h>

int main(void){
	int a, b, c;

	printf("Zadej dve cisla...\n");
	scanf("%d %d", &a, &b);
	c = a + b;
	printf("%d+%d=%d\n",a,b,c);

	return 0;
}
```

# Podmínky

Ověření, zda tři velikosti tvoří pravoúhlý trojúhelník.

```c
#include <stdio.h>

int main(void){
	int a, b, c;

	printf("Zadej tri rozmery sten trojuhelniku...\n")
	scanf("%d %d %d", &a, &b, &c);

// zjistit ktere cislo je nejvetsi

	if(c*c == a*a + b*b){ // Pythagorova veta
		printf("trojuhelnik je pravouhly\n");
	}else{
		printf("trojuhelnik neni pravouhly\n");
	}
	
	printf("%d+%d=%d\n",a,b,c);

	return 0;
}
```

# Cykly

# funkce & procedury

# Pointer
