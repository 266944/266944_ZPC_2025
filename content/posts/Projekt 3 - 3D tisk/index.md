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

<script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>

<div style="width: 600px; height: 400px; margin: 0 auto;">
  <model-viewer 
      src="/models/miniprojekt-ZPC.glb" 
      alt="3D model" 
      auto-rotate 
      camera-controls 
      style="width: 100%; height: 100%; background-color: #f0f0f0;">
  </model-viewer>
</div>


Modely jsem si dale vyexportoval ve **formátu STL.**, který je pro zpracování dat vhodný. K vygenerování **G-codu**, tedy codu který používá tiskárna, jsem využil **Prusaslicer**. V programu jsem využil nemálo funkcí například funkci **brim**, která udělá vrstvu příléhající na desku záměrně větší, aby se zvýšila stabilita dílu a byly nižší tendence k jeho odtrhnutí od desky, což by mělo za následek kolaps tisku. Nebo funkci **CUT**, díky které jsem jeden z dílů rozpůlil, aby se lépe tisknul a nebylo nutné využítívat podpěry.  

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/3/prusaslicer.png"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/3/gearbox.png"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>


Po vymodelování jednotlivých součástí následoval 3D tisk. Jelikož jsem tisk dělal již dříve, probíhal hladce. Sestavu jsem rozdělil na dva díly – planetární převodovku a samotný rotační ventil. Celková doba tisku se po sečtení pohybovala kolem **10 hodin**.

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/3/IMG_2195.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/3/IMG_2195.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>