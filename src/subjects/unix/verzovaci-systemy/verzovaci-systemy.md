nazev = "Verzovací systémy"
tagy = ["unix", "vcs"]

+++
# Verzovací systémy

Verzovací systémy slouží k organizaci sdílené práce na souborech. Tyto systémy se označují jako VCS *(Version Control System)*.

Před nástupem VCS se soubory sdílely různými způsoby, např. přenášením na fyzických médiích, či po síti. Nebylo ovšem spolehlivě zjistitelné, která verze souboru je aktuální/správná.

Pokud se na úpravách jednoho souboru, například programu, chtělo podílet několik uživatelů, mohli mít všichni v jednu chvíli přístup k souboru na serveru. Ovšem pokud soubor upravovovali dva uživatelé ve stejnou chvíli, změny posledního uživatele, který zapsal změny, přepsaly všechny uložené změny předchozího uživatele.

## Centralizované systémy

Tyto systémy se vyznačují tím, že soubory i jejich historie jsou umístěny na jednom zařízení - serveru. Ze serveru si uživatelé stahují vybrané verze souborů a pracují na nich.

### Zamykání souboru

Pokud jeden uživatel otevře soubor pro editaci, ostatním uživatelům je umožněno soubor pouze číst. Tento systém zapříčiní vzniku konfliktu při slučování různých verzí.

Nevýhodou je, že zápis může v jednu chvíli provádět pouze jeden uživatel. To nemusí být v produkci účinné.

### CVS

*Concurrent Version System*, ve zkratce *CVS*, je jedním z prvních rozšířených distribuovaných systémů. Byl vyvíjen jako součást projektu *GNU* a dodnes se v některých projektech používá. Je to ovšem již archaický systém bez dalšího zásadního vývoje.

### Subversion

Subversion, nebo-li *SVN*, je systém, který měl za cíl nahradit *CVS* a opravit jeho nedostatky. Oproti CVS umí lépe řešit konflikty a manipulace se soubory, uchovávat v repozitářích i jiná data kromě textových souborů a větvit repozitář.

Stavy repozitáře se vypočítávají na základe předchozích změn. Výhodou toho je, že se šetří úložiště, ovšem výpočet rozsáhlého projektu může být velmi náročný. Podle zásad nepatří velké binární soubory do repozitáře, čímž se výhoda s využitým místem stává nepodstatnou.

## Distribuované systémy

U distribuovaných systémů jsou zdrojové soubory - včetně celé historie repozitáře - uloženy na zařízeních všech uživatelů, kteří s repozitářem pracují. Změny se poté synchronizují do hlavního repozitáře na serveru.

### Mercurial

Mercurial, často zmiňovaný zkratkou *hg* je distribuovaný verzovací systém. Vznikl přibližně ve stejné době jako git, liší se jednak tím, že je monolitický (jedna binárka) a orientací na přátelskost použití. Několik uživatelů popisuje Mercurial jako *"DropBox pro programátory"*.

Zajímavé je, že že někteří poskytovatelé se Mercurialu zbavují a zachovávají pouze git, například *Bit Bucket*.

### Git

V současnosti nejrozšířenější verzovací systém. který byl napsán Linusem Torvaldsem, autorem kernelu *Linux*. Právě pro vývoj Linuxu byl git napsán. Podobně jako Mercurial se jedná o distribuované VCS, ovšem Git je spousta malých programů, oproti monolitickému Mercurialu.

Git umí velmi dobře procházet a manipulovat s historií repozitáře, je velmi flexibilní a poměrně jednoduše rozšiřitelný přes shellové skripty.

Na rozdíl od SVN uchovává git kopie každé revize, respektive změněných souborů, a nevypočítává jejich stavy na základě změn.
