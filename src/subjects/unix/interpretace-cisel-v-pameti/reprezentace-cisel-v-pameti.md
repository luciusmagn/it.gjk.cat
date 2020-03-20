nazev = "Reprezentace čísel v paměti"
tagy = ["unix", "typy", "pamet"]

+++
# Reprezentace čísel v paměti

## Binární soustava

Počítače vidí rozumí jen binárním stavům, které reprezentujeme jako `1` a `0`.

## Hexadecimální soustava

894 -> 37E

894 /16 | 55.875 | r14
55 /16  | 3.4375 | ...

37E =
  E * 16^0
 +7 * 16^1
 +3 * 16^2

 14 * 1
+7  * 16
+3  * 256
    = 894

479 -> 1DF

## Integer

### Unsigned int

- scitani mocnin dvou
- 8 bitu (char) -> 256 hodnot

### Signed int

Číslo se znaménkem. Reprezentuje se tak, že první bit definuje znaménko, kde `1` je mínus a `0` je plus. Efektivní rozsah je `-128` až `127`.

Záporné číslo je znározněné doplňkovým kódem. Znamená to, že přičítáme směrem k nule od `-128`. Máme-li binární signed int `10000001`, nejde o číslo `-1`, ale o `-127`. Přičetli jsme totiž jedničku (`0000001`) k `-128`.

Doplňkový kód lze vypočítat jednoduše. Chceme-li získat záporné číslo `-25`, stačí nám `25` zkonvertovat do dvojkové soustavy (7 bitů) - což je `0011001` - a invertujeme všechny bity na `1100110`. Poté přidáme jako první bit znaménko, tj. `1` a dostaneme číslo `-25`.

`-13` je `11110011`, `13` je `0001101`. Dopocitava se k nule, tj. `1001101` je `-128 + 13 = -115`. muzem invertovat bity a vyjde to.

## Float



V desétkové soustavě zapisujeme desetinné číslo ve formátu `1000 100 10 1 . 1/10 1/100 1/1000`.

Číslo, které není rekurzivní v jedné soustavě, může být rekurzivní v jiné soustavě. Zlomek $\frac{1}{3}$ zapíšeme v desítkové soustavě jako $0.\overline{3333333}$. Stejně tak číslo $0.1$ zapíšeme v binární soustavě jako $0.0001100\overline{1100110011}$. Počítače nerozumí rekurzi, což znamená, že při práci s destinými čísli přicházíme o přesnost.

$0.1 + 0.2 = 0.300000...000001$

$\frac{1}{3} + \frac{1}{3} + \frac{1}{3} = 0.3\overlive{333333} + 0.3\overline{333333} + 0.3\overline{333333} = 1$

u vypoctu zbytku (z floatu na binarni) nasobime zakladem (2).

```
7/10 | 1
4/10 | 0
8/10 | 1
6/10 | 1
2/10 | 0
4/10 | 0 |
8/10 | 1 |
6/10 | 1 |
...
```

- v pameti jsou cisla s plovouci nebo pevnou desetinno ucarkou
- u starych jsou s pevnou, tj. presne dany pocet cifer pred a za carkou
	- omezeny rozsah cisel
- s plovouci carkou je znazornene, kde se carka nachazi
- maji kladnou i zapornou nulu lol
- dane u IEEE-754
- neperiodicke cislo v jedne soustave muze byt periodicke v druhe
	- `0.1 + 0.2 = 0.30000000000004`

