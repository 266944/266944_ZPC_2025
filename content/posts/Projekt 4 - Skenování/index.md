---
title: "Skenování"
layout: "simple"
---
Úkolem čtvrtého miniprojektu bylo naskenování předem určeného dílu. Já i můj kolega Jan Ludva jsme dostali přidělený stejný díl a to díl ve tvaru vázy, který byl vyroben aditivní technologií. Jelikož ani jeden z nás neměl se skenováním zkušenosti, rozhodli jsme jít skenovat společněa vzájemně si vypomoct.

## Skenování dílu

Pomocí výukové prezentace jsme dokázali zprovoznit skener SimScan i příslušnou aplikaci určenou ke skenování. Prezentace neobsahovala pouze popis **zapojení skeneru**, ale také postup jeho **kalibrace** a **propojení s aplikací**. 

 

Prvním krokem samotného skenování bylo **načtení kalibračních bodů**, které se nacházely jak na podložce, tak i na samotném dílu – tyto individuální body bylo nutné předem nalepit na povrch vázy. Pomocí těchto bodů jsme následně v aplikaci **vytvořili rovinu** podložky. 

 

Poté bylo nutné nastavit skenovací parametry, konkrétně **Resolution (rozlišení) a Exposure (expozici)**. 

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/4/IMG_2164.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/4/IMG_2169.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>

Následovalo samotné **naskenování dílu**. Protože váza nebyla příliš rozměrná a její povrch byl pro skenování vhodný, celý proces proběhl poměrně rychle a bez komplikací. Po dokončení bylo nutné díl vyexportovat ve formátech **STL a p5j**. 

 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/4/IMG_2167.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/4/IMG_2171.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>

Kolega Jan následně celý postup provedl samostatně na svém dílu. Po dokončení následoval **úklid pracoviště, uložení skeneru a odstranění kalibračních bodů** z vázy. 

 

## Úprava dat v aplikaci GOM Inspect 

 

Druhou částí úkolu byla úprava naskenovaných dat v aplikaci GOM Inspect. 

Do této aplikace byl nejprve naimportován **soubor STL**, po čemž následovaly jednotlivé korekce modelu – konkrétně **zalepení děr** po skenování a **odstranění vzniklých fragmentů**. Program pro tyto účely nabízí automatické funkce, které fungují velmi spolehlivě. 

 

Následovalo **vyhlazení povrchu a úprava polygonové sítě**. Původní sken obsahoval přibližně **400 000 bodů**, po zjemnění sítě se jejich počet zvýšil na **1 250 000 bodů**. 

 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/4/1.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/4/2.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>

Dalším krokem bylo změření **plochy dílu**, k čemuž má aplikace vlastní funkci. Výsledek měření je možné vidět na přiloženém obrázku (**102034.99**). 

Následně bylo potřeba určit maximální rozměr dílu. Bohužel jsem v aplikaci nenašel žádnou funkci, která by tento výpočet prováděla automaticky, a proto jsem zvolil vlastní postup. 

Pomocí vytvoření pomocných kružnic jsem určil krajní body, mezi nimiž jsem poté změřil vzdálenosti. Největší z naměřených hodnot jsem označil jako **maximální rozměr** dílu (**205.34**). 

Posledním krokem bylo změření jednoho z dílčích rozměrů. Rozhodl jsem se změřit **poloměr dolní podstavy**, jak je vidět na obrázku níže (**41.00**). 

<img 
    src="/266944_ZPC_2025/images/4/3.jpeg" 
    style="transform: rotate(0deg); transform-origin: center center;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
</img>
