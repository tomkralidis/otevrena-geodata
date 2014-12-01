.. index:: 
    single: Čeština
    single: UTF-8

Příloha F: Kódování češtiny
===========================

Pro zapsání české diakritiky do tabulky znaků existuje z historických důvodů
několik možných způsobů. Do dnešní doby přetrvávají na některých systémech
kódování CP852, Windows-1250 či ISO-8859-2. Díky tomu dříve často docházelo (a
někdy stále dochází) k nekoretnímu zápisu a čtení z databází, kdy české znaky
bývají zkomolené. Uživatel se tak může spolehnout pouze na svůj úsudek či náhodu,
aby se mu znaky zobrazily korektně.

Problémy s nedostatečně velkou tabukou znaků řeší kódování UTF-8, do kterého
lze uložit znaky všech známých jazyků, čímž by se měly problémy s kódováním
vyřešit.

Je proto nezbytné, aby kódování znaků dat publikovaných jako otevřená data, bylo
stejné u všech souborů a to *UTF-8*.
