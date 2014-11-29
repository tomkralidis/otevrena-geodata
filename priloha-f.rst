.. index:: 
    single: Čeština
    single: UTF-8

Příloha F: Kódování češtiny
===========================

Pro zapsání české diakritiky do tabulky znaků existuje z historických důvodů
několik možných způsobů. Do dnešní doby přetrvávají na některých systémech
kódování `CP852`, `Windows-1250`, `ISO-8859-2` a další. Neexistoval standardní
způsob, jak systém kódování popsat v databázích či souborech. Proto docházelo (a
někdy stále dochází) k nekoretnímu zápisu a čtení z databází, kdy české znaky
bývají zkomolené. Uživatel se může spolehnout pouze na svůj úsudek či náhodu,
aby se mu znaky zobrazily korektně.

Problémy s nedostatečně velkou tabukou znaků, kdy různé jazyky musely být
ukládány pomocí různých tabulek (např. tzv. "západní jazyky" ISO-8859-1,
"východo evropské" pomocí ISO-8859-2 a podobně) řeší kódování UTF-8, do kterého
lze uložit znaky všech známých jazyků, čímž by se měly problémy s kódováním
vyřešit.

Je proto nezbytné, aby kódování všech data publikovaných jako otevřená data bylo
stejné u všech souborů a to *UTF-8*.
