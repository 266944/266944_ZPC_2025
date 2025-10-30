---
title: "3D tisk"
layout: "simple"
---

Cílem mini projektu zaměřeného na aditivní technologie bylo vytvořit **mechanizmus pomocí 3D tisku**. Limitací projektu bylo, že bylo možné použít maximálně **100 g filamentu**. 

 

Jelikož jsem již delší dobu uvažoval o výrobě **rotačního ventilu**, přišel mi tento projekt jako ideální příležitost. Ventil má jeden vstup a více výstupů, a pomocí elektroniky a krokového motoru lze ovládat, který z výstupů je právě aktivní. Tento koncept jsem se rozhodl realizovat mechanickými díly vytištěnými na 3D tiskárně. 

<div style="max-width: 800px; margin: 0 auto; border-radius: 20px; overflow: hidden; position: relative; padding-top: 56.25%;">
  <iframe
    src="https://www.youtube.com/embed/XFg6k97tLfE?autoplay=1&mute=1&loop=1&playlist=XFg6k97tLfE"
    title="YouTube video"
    frameborder="0"
    allow="autoplay; encrypted-media; fullscreen"
    allowfullscreen
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;">
  </iframe>
</div>


Pro zvýšení přesnosti a snížení zátěže na krokový motor jsem do sestavy přidal **planetární převodovku**. Ta umožňuje přesnější nastavení polohy motoru a zároveň prodlužuje jeho životnost tím, že snižuje mechanické zatížení. 

 

Pro modelování jednotlivých dílů jsem použil **Autodesk Fusion 360**. Práce s tímto softwarem probíhala překvapivě dobře, protože je velmi podobný programu Autodesk Inventor. Hlavní rozdíl je, že Fusion 360 je omezenější v pokročilých funkcích, na druhou stranu je pro nekomerční účely zdarma. 

<iframe 
    src="https://gmail5614076.autodesk360.com/shares/public/SH90d2dQT28d5b602811b7a8b95caf39959d?mode=embed" 
    width="1000" 
    height="480" 
    allowfullscreen="true" 
    webkitallowfullscreen="true" 
    mozallowfullscreen="true"  
    frameborder="0"
    style="transform: rotate(0deg); transform-origin: center center;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
    ">
</iframe>


Modely jsem si dale vyexportoval ve **formátu STL.**, který je pro zpracování dat vhodný. K vygenerování **G-codu**, tedy codu který používá tiskárna, jsem využil **Prusaslicer**. V programu jsem využil nemálo funkcí například funkci **brim**, která udělá vrstvu příléhající na desku záměrně větší, aby se zvýšila stabilita dílu a byly nižší tendence k jeho odtrhnutí od desky, což by mělo za následek kolaps tisku. Nebo funkci **CUT**, díky které jsem jeden z dílů rozpůlil, aby se lépe tisknul a nebylo nutné využítívat podpěry.  

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/3/prusaslicer.png"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/3/gearbox.png"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>


Po vymodelování jednotlivých součástí následoval 3D tisk. Jelikož jsem tisk dělal již dříve, probíhal hladce. Sestavu jsem rozdělil na dva díly – planetární převodovku a samotný rotační ventil. Celková doba tisku se po sečtení pohybovala kolem **10 hodin**.

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/3/IMG_2220.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/3/IMG_2195.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>

Po vytištění jednotlivých součástí následovalo jejich **sestavení**. Při montáži jsem využil jak **3D tiskem vyrobené konektory**, tak také **adhezivní pojiva a šrouby** M3 o délkách 8, 12 a 45 mm. S tisknutými konektory jsem pracoval poprvé, proto výsledné díly neodpovídaly zcela původním představám. V budoucí iteraci bych věnoval **větší pozornost jejich rozměrům**, aby do sebe jednotlivé části lépe zapadaly.

V rámci projektu jsem sice spojení jednotlivých dílů úspěšně realizoval, avšak použití konektorů **nebylo zcela optimální** a při montáži jsem měl **obavy z možného poškození** výtisku. Adhezivní spoj byl aplikován především na rozříznuté části konstrukce, a to zejména z důvodu zajištění její **vodotěsnosti**.

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/3/IMG_2232.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/3/IMG_2233.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>