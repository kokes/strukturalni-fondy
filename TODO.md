## TODO

- **Vzít seznam firem z RES a napojit na ně celkový dotace, tj. ne projekty, ale sumu za každou firmu.**
- vyřešit pořadí projektů - jsou ty skrytý řádky důležitý?
- rozkouskovat na stages - příprava, realizace, zaplacení, certifikace
 - pokud pouzijem ten mensi zdroj, je tam moznost groupovani podle ongoing, finalised, cancelled
- všechny tabulky dělat pro všechny peněžní metriky
- kofinance + histogram kofinančních poměrů
- dotace per capita (dotace pro veřejnost i soukromníky)
- Agrofert, jako minule, ze závěrky (+ ARES); + pivovary, škoda, soukromý sš/vš, učiliště, ...; scio; křetinský, penta, ppf atd., soláry
- doprava - SŽDC, ŘSD atd.
- CzechTrade, Czech Tourism atd.; Odbory
- podnikatelský subjekty rozkouskovat podle Čísla prioritní osy (a/nebo Čísla oblasti podpory) - 3.2.2 je CZC nebo Zoner

- group by pravni forma (ESA z RES) a NACE (RES)
- vyřešit IČO 53141260/53141337 (neni to český ičo, ale plete se to)

- pridat ares.py - uklidit a odokumentovat
- porovnat hodnoty z prehledu xlsx s tim puvodnim spreadsheetem od MMR - ktera metrika jsou proplaceny penize?
- pridat exportovanej seznam dotaci (s cistyma jmenama subjektu - smazat moje prepisy subjektu)
- rozdelit ipynb na cisteni a analyzy
- zacit zapracovavat veci z emailu
- **zacit parsovat OR**
- OR půjde napojit na registr změn - získat tam seznam všech IČO! (tedy nejen tyhle firmy)

- len(ico) != 8 - nejsou to nahodou fyzicky osoby? asi spis CR-Polsko. + isdigit()
- dc.js - asi mam moc dat (jde tam AJAXovat?); [SO k ajaxování dc.js](http://stackoverflow.com/questions/24184986/using-dc-js-on-the-clientside-with-crossfilter-on-the-server)
- elastic/solr/lunr pro RES/OR data
- **napojit data na RES dataset!! zrušit všechny mapování od MMR**
- při napojení RES dat kontrolovat NUTS4 že sedí
- kolik peněz šlo firmám pod zahraniční kontrolou?
- zaniklý firmy často (pre 4/2013) nemaj ESA kód, je jich ale hrstka
- propojit hotely a golfy s NACE

### Hotovo

- <strike>kontroluj erár (po implementaci Ostatní) vůči MFČR seznamu (v dubnu novej)</strike>
- <strike>**dopravní podnik prahy je vedenej jako podnikatelskej subjekt**</strike>
 - <strike>45274649 28196678 26827719 00005886 25508881 61974757 - tohle jsou příklady IČA eráru, který jsou podnikatelé v datasetu</strike>
 - <strike>[jinej mfcr seznam](http://www.mfcr.cz/cs/verejny-sektor/rozpoctove-ramce-statisticke-informace/verejny-sektor/verejne-spolecnosti/2016/seznam-verejnych-spolecnosti-v-cr-2016-24752) - nezapomeň lpadnout nulama (třeba DPP je bez nul)</strike>
- <strike>roztřídit Ostatní mezi soukromý a veřejný (je tam toho pár)</strike>

- <strike>Česko-Polsko vyřešit (je to ale jen cca 1 mld)</strike>
- <strike>uložit názvy sloupců do proměnných</strike>
- <strike>len(ico) != 8 vyhodit, spocitat jejich miliardy</strike>
- <strike>přidat dummy sloupec - veřejné či ne</strike>
- <strike>rozdělení na operační programy</strike>
- <strike>rozlišit v rámci neziskovek na církve, ops, ...</strike>
- uklidit
 - <strike>např. obecně prospěšný společnosti (viz výše)</strike>
 - <strike>VŠ a VŠ (státní) jsou zvlášť, ale ve skutečnosti jsou jedno (soukromý VŠ jsou v podnikatelích)</strike>
 - <strike>Ostatní -> ústav zařadit mezi neziskovky (je to forma ops)</strike>
- <strike>najít firmy s významným podílem státu (ČD, Ruzyň, ČEZ)</strike>
- <strike>IČO a názvů žadatelů jsou různý počty - unifikuj</strike>
- <strike>pridat README do vsech slozek - hlavne do rootu</strike>
- <strike>**Rozřešit, kterej ze dvou MMR zdrojů použít**</strike>