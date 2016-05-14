## Datové vstupy
Výsledný dataset je pospojován z několika zdrojů, jde o:

- [Přehled projektů od MMR](http://www.strukturalni-fondy.cz/cs/Informace-o-cerpani/Seznamy-prijemcu) - ony datové soubory nejsou pro jednotlivé roky, každý odkaz obsahuje všechna data, starší než datum vydání, takže berte ty aktuální. V Seznamu příjemců je celkem nečistá tabulka, v Přehledu projektů jsou lepší informace, takže ten dataset jsem použil já.
- [Seznam vládních institucí](http://www.mfcr.cz/cs/verejny-sektor/rozpoctove-ramce-statisticke-informace/verejny-sektor/sektor-vladnich-instituci/2016/seznam-vladnich-instituci-v-cr-2016-24749) a [Seznam veřejných společností](http://www.mfcr.cz/cs/verejny-sektor/rozpoctove-ramce-statisticke-informace/verejny-sektor/verejne-spolecnosti/2016/seznam-verejnych-spolecnosti-v-cr-2016-24752) od MFČR. Použil jsem tyto dva seznamy, abych mohl napárovat evropské dotace na veřejné instituce.
- [ARES MFČR](http://wwwinfo.mfcr.cz/ares/ares.html.cz) je systém pro dohledání informací o firmách a veřejných institucích. Až data pořádně zapracuji, nahradí výše zmíněné seznamy MFČR, protože je to kompletnější databáze. Na základě ARES je pak vyplněn soubor `rucni-iso.csv`, kde jsem dohledával konkrétní IČO pro napárování nekompletních dat MMR.

### Dva MMR zdroje

Problém je, že MMR nabízí dva zdroje k přehledu projektů. Menší Seznam příjemců a větší Přehled projektů. Je těžké vybrat lepší zdroj, protože každý má své výhody. Oba mají shodný počet *realizovaných* projektů, ale jiné informace k nim.

- Seznam příjemců má mírně více detailu k žadatelům (např. Úřady práce jsou rozděleny podle krajských organizací, Přehled projektů má vše pod ÚP ČR)
- **Seznam příjemců obsahuje i zrušené projekty (cca 3000 za 5 miliard)**
- Přehled projektů obsahuje více indikátorů k prostředkům (vč. celkové hodnoty projektu, z čehož jde dopočítat úroveň kofinancování)
- Přehled projektů obsahuje kategorizaci podle právní formy (redundantní, pokud máte data z ARES)
- **Přehled projektů má detaily projektů, ne jen názvy**
- Přehled projektů má krom operačních programů i prioritní osy, číslo projektu atd.
- Přehled projektů má mezery v seznamu IČO, ty už jsem ale dočistil

V kostce tak při použití Přehledu projektů přijdeme o pár tisíc zrušených projektů a musíme je trochu očistit, ale získáme pár věcí navíc.