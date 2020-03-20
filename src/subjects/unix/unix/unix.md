nazev = "Unix"
tagy = ["unix", "os"]

+++
## Základní prvky \*nixového systému (POSIX)

- Vše je soubor
- Program dělá jednu věc a dělá jí dobře
- Výstup jednoho programu může býti vstupem jiného programu
- Programy umí zpracovat textové proudy

### Souborový systém

Souborový systém unixového systému se od systému Windows liší tím, že je vše umístěno pod hlavním tzv. *kořenovým* adresářem `/`. Příklad souborové struktury:

```sh
/
	bin
	dev
	etc
	home
		adam
			documents
			videos
		petr
			music
```

## Absolutní a relativní cesty

Popis cesty v unixovém systému se zapisuje pomocí názvů složek/souborů a znaku `/`. Cesta začínající tímto znakem definuje to, že cesta začíná v kořenovém adresáři a je tedy absolutní, například `/home/user/documents/school`. Relativní popis cesty je kterýkoliv jiný popis.

Relativní cesta může začínat jen názvem složky, nebo jedním ze speciálních znaků:

Znak | Definice
-|-
. | Aktuální složka (working directory)
.. | Rodičovská složka (složka nadřazená aktuálnímu adresáři)
~ | Domovská složka přihlášeného uživatele (*/home/$USER*)

Relativní cestou je například `../documents/school`, nebo `~/documents/school` atd.

