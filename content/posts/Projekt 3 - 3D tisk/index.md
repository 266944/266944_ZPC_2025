---
title: "3D tisk"
layout: "simple"
---

Cílem mini projektu zaměřeného na aditivní technologie bylo vytvořit **mechanizmus pomocí 3D tisku**. Limitací projektu bylo, že bylo možné použít maximálně **100 g filamentu**. 

 

Jelikož jsem již delší dobu uvažoval o výrobě **rotačního ventilu**, přišel mi tento projekt jako ideální příležitost. Ventil má jeden vstup a více výstupů, a pomocí elektroniky a krokového motoru lze ovládat, který z výstupů je právě aktivní. Tento koncept jsem se rozhodl realizovat mechanickými díly vytištěnými na 3D tiskárně. 

 

Pro zvýšení přesnosti a snížení zátěže na krokový motor jsem do sestavy přidal **planetární převodovku**. Ta umožňuje přesnější nastavení polohy motoru a zároveň prodlužuje jeho životnost tím, že snižuje mechanické zatížení. 

 

Pro modelování jednotlivých dílů jsem použil **Autodesk Fusion 360**. Práce s tímto softwarem probíhala překvapivě dobře, protože je velmi podobný programu Autodesk Inventor. Hlavní rozdíl je, že Fusion 360 je omezenější v pokročilých funkcích, na druhou stranu je pro nekomerční účely zdarma. 

Modely jsem si dale vyexportoval ve **formátu STL.**, který je pro zpracování dat vhodný. K vygenerování **G-codu**, tedy codu který používá tiskárna, jsem využil **Prusaslicer**. V programu jsem využil nemálo funkcí například funkci **brim**, která udělá vrstvu příléhající na desku záměrně větší, aby se zvýšila stabilita dílu a byly nižší tendence k jeho odtrhnutí od desky, což by mělo za následek kolaps tisku. Nebo funkci **CUT**, díky které jsem jeden z dílů rozpůlil, aby se lépe tisknul a nebylo nutné využítívat podpěry.  

Po vymodelování jednotlivých součástí následoval 3D tisk. Jelikož jsem tisk dělal již dříve, probíhal hladce. Sestavu jsem rozdělil na dva díly – planetární převodovku a samotný rotační ventil. Celková doba tisku se po sečtení pohybovala kolem **10 hodin**.