nazev = "Shell"
tagy = ["unix", "shell"]

+++
Shell je rozhraní pro uživatele umožňující uživatelům spouštět a ovládat programy, tj. *Interpretuje uživatelem zadané příkazy systému*.

Shellů existuje celá řada. Nejběžněji používaným shellem je *Bash*.

## Základní programy

### Práce se soubory a složkami

- ls &mdash; vypsat obsah složky
- cd &mdash; přepnou se do složky
- pwd &mdash; vypsat adresu aktivní složky
- cat &mdash; vypsat obsah souboru/ů
- touch &mdash; vytvořit prázdný soubor
- mkdir &mdash; vytvořit prázdnou složku
- rm &mdash; odstranit soubor/složku
- cp &mdash; zkopírovat soubor/složku
- mv &mdash; přesunout/přejmenovat soubor/složku

### Proudové editory

- grep &mdash; vyhledá všechny řádky obsahující daný obsah
- sed &mdash; najít a nahradit
- awk &mdash; vypisuje dané sloupce

## Proudy

Znak|Funkce
-|-
\||Přesměrování výstupu na vstup jiného programu
>|Přepsat soubor
>>|Připsat na konec souboru

## Aliasy

Alias je uživatelem definovaná zkratka. Pomocí aliasu lze na vybrané klíčové slovo nastavit složitý příkaz, který lze poté vyvolat samotným Klíčovým slovem.

Alias lze nastavit přímo v terminálu: `alias testalias="echo 'i love pizza'"`. Po definování tohoto aliasu a napsáním klíčového slova `testalias` se spustí definovaný příkaz `echo 'i love pizza'`.

```sh
$ alias testalias="echo 'i love pizza'"
$ testalias
i love pizza
```

Příkladem aliasu může být namapování příkazu `cal -m` na klíčové slovo `cal`. To nám umožní automaticky vyvolávat kalendář s prvním dnem nastaveným na pondělí bez toho, aniž bychom museli přepínač `-m` definovat pokaždé manuálně.

### Persistentní aliasy

Po uzavření okna terminálu se nastavené aliasy resetují. Pro jejich uchování je třeba aliasy definovat v konfiguračním souboru shellu, v našem případě tedy v souboru `.basahrc` v našem domovském adresáři.

V konfiguračním souboru stačí na nové řádky aliasy definovat stejně, jako když je definujeme přímo v terminálu.

