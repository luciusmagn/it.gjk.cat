nazev = "Složitosti algoritmu"
tagy = ["unix", "algoritmy"]

+++
# Složitosti algoritmu

Algoritmus je popis nějakého postupu.

- délka kódu
- počet provedených instrukcí
- doba běhu programu
- počet cyklů

| funkce      | $N = 10$ | $N = 100$ | $N = 1000$ | $N = 10000$ |
|-------------|----------|-----------|------------|-------------|
| $log_2 N$   | 1        | 2         | 3          | 4           |
| $N$         | 10       | 100       | 1000       | 10000       |
| $L log_2 N$ | 10       | 200       | 3000       | 40000       |
| $N^2$       | 100      | 10000     | $10^6$     | $10^8$      |
| $2^n$       | 1024     | $10^31$   | $10^310$   | $10^3100$   |

---

```c
for(i = 0; i < n; i++){
	printf("*");
}
```

slozitost je $3n+1$, tj. $O(n)$.

- 1 prirazeni
- n porovnani
- n souctu
- n print

---

```c
for(i = 0; i < n; i++){
	for(j = 0; h < n; j++>){
		printf("*");
	}
}
```

slozitost je $n*(3n+1)+1+n = 3n^2+3n+1$, tj. $n^2$.

- 1 prirazeni
- n i++
- n prirazeni
- n^2 j++

---

```c
for(i = 0; i < n; i++){
	for(j = 0; j < i; j++){
		printf("*");
	}
}
```

$0+1+2+3+...+n = \frac{(n^2+n)}{2} = \frac{1}{2}n^2 + \frac{1}{2}n^2 = O(n)^2$

---

```c
while(n >= 1){
	printf("*");
	n = n/2;
}
```

---

Bubble sort ma slozitorst $O(n^2)$
