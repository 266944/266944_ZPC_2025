---
title: "2D grafika a řezání"
layout: "simple"
---

## Miniprojekt-Nálepka

Obě zařízení – jak **řezačka fólií**, tak i **laser určený pro řezání materiálů** – mají společnou vlastnost, a to tu, že využívají soubory ve formátu **SVG nebo DXF**. 

První věc, kterou jsme se na hodině naučili, bylo jak tyto **formáty exportovat** a jak s nimi následně pracovat, především v programu **Inkscape**. 

 

Při tvorbě nálepky jsme využili vlastní obrázek, který jsme do programu Inkscape nahráli a následně převedli do vektorové podoby pomocí funkce **„převést na bitmapu“**. Po převedení jsme vektory dále upravovali a dolaďovali. Jakmile jsme byli s výsledkem spokojeni, mohli jsme si samotný návrh nechat vyřezat na řezačce, se kterou jsme byli na hodině seznámeni, včetně jejích základních pravidel a zásad používání. 

 

Jedním z těchto pravidel je například to, že u nálepek by se **nemělo používat příliš mnoho ostrých rohů**, protože nůž řezačky má potíže takové obrysy přesně vyřezat. Z tohoto důvodu je vhodnější používat **zaoblení (rádiusy)**. 

Já jsem si jako motiv své nálepky zvolil logo našeho **sportovního klubu Mlékárna Olešnice Svitávka**. U tohoto obrázku jsem upravil všechny ostré rohy právě pomocí rádiusů. 

 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/2/KOLOVA1.jpg"
       style="transform:  transform-origin: center center;
              width: 360px; height: 480px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/2/IMG_2090.jpg"
       style="transform:  transform-origin: center center;
              width: 360px; height: 480px;
              border-radius: 20px; object-fit: cover;">
</div>

Po dokončení návrhu řezačka nálepku vyřezala. Následně bylo potřeba provést několik drobnějších úprav – například **odstranit přebytečnou fólii a přilepit průhlednou přenosovou fólii**. Ta slouží k tomu, aby bylo možné nálepku přesně přenést na cílový povrch. Průhledná fólie umožňuje přenést všechny části nálepky současně a poté ji jednoduše odstranit, protože její lepidlo je slabší než lepidlo samotné nálepky. 

 
 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/2/IMG_2092.jpg"
       style="transform:  transform-origin: center center;
              width: 360px; height: 480px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/2/IMG_2096.jpg"
       style="transform:  transform-origin: center center;
              width: 360px; height: 480px;
              border-radius: 20px; object-fit: cover;">
</div>

V mém případě však přenosová fólie nefungovala správně – nevím, zda jsem ji špatně nalepil, nebo zda se nálepka časem poškodila při delším nošení na batohu. Nakonec jsem musel jednotlivé části nálepky lepit ručně po jednom. V mém případě to nebyl zásadní problém, ale dokážu si představit, že u složitější nálepky s větším počtem dílů by to mohlo být velmi **nepříjemné a časově náročné**. 

 

## Miniprojekt-2D řezání 

Druhým úkolem v tomto projektu bylo vyřezání a realizace našeho návrhu na **laserové řezačce**. 

K realizaci jsme obdrželi dvě **kartonové desky o rozměrech 1200 × 800 mm**. Z těchto desek jsme mohli vytvořit jakýkoliv výrobek dle vlastního návrhu. Jedinou podmínkou bylo, že nesmíme použít žádný jiný materiál než karton – tedy **žádné lepidlo, špejle ani lepicí pásku**. Spoje bylo možné vytvářet pouze pomocí **zámků z kartonu**. 

 

Zvažoval jsem, co z kartonu vyrobit, až jsem narazil na video o **Cayan Tower**, což je výškový mrakodrap postavený v Dubaji. Tento objekt mě zaujal natolik, že jsem se rozhodl vytvořit **vlastní model inspirovaný touto stavbou**. 

<img 
    src="/images/2/cayan.jpg" 
    style="transform: rotate(0deg); transform-origin: center center;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
</img>


Začal jsem jednodušším návrhem, protože budova má tvar hranolu se zkroucenou horní podstavou. Model jsem nejprve vymodeloval a následně „prořezal“ pomocí funkce vysunutí, abych viděl, jak by konstrukce vypadala z kartonu. Původně jsem plánoval pouze pět vrstev (řezů), ale brzy jsem zjistil, že by tím model ztratil na detailech. Ve finální verzi jsem se proto rozhodl pro devět vrstev, což s sebou přineslo i několik komplikací, se kterými jsem však dopředu počítal – například **úzké stěny, deformace kartonu a problémy s přesností**. 

 

Zpočátku jsem modeloval v programu **Autodesk Inventor**, který mi je prostředím bližší, později jsem však přešel do **SolidWorksu**, protože nabízí kvalitnější **generování DXF křivek**. Po jejich vytvoření jsem využil program **Inkscape** k rozložení křivek na pracovní plochu, odkud se následně přenesly do programu pro řezání. 

 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/2/Carboar-x.jpg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/2/carboard-z_1.jpg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 390px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>


Řezání jsem prováděl v programu **LightBurn**, kde jsem si – kvůli velikosti pracovní plochy – vytvořil tzv. **aretační čtverce**. Ty jsem umístil do rohů pracovní plochy a nechal je gravírovat, jelikož samotný laser nemá diodu, která by ukazovala jeho aktuální polohu. Tato volba se ukázala jako velmi praktická, protože při řezání druhé desky jsem musel **pracovní plochu kalibrovat přibližně pětkrát**. 

 

V programu LightBurn jsem si nastavil **rychlost řezu, intenzitu laseru a kompenzaci** podle doporučených hodnot, které jsme obdrželi při školení na práci s laserem. 

Před samotným řezáním bylo nutné upevnit kartonové desky k pracovní mřížce pomocí **lepicí pásky**, protože karton neměl dokonale rovný povrch. Poté proběhla **kalibrace výšky laseru**, aby se jeho hlava nacházelo **4 mm nad nejvyšším bodem kartonu**, a následně se spustila samotná řezací operace. 

 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <video autoplay loop muted playsinline
    style="transform: rotate(90deg); transform-origin: center center;
           width: 270px; height: 480px;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
    <source src="/videos/2/IMG_2153.mp4" type="video/mp4">
  </video>

  <video autoplay loop muted playsinline
    style="transform: rotate(90deg); transform-origin: center center;
           width: 270px; height: 480px;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
    <source src="/videos/2/IMG_2155.mp4" type="video/mp4">
  </video>
</div>

Po vyřezání jsem jednotlivé díly vyndal z desky, což zpětně hodnotím jako chybu, protože jsem si **nezkontroloval**, zda byly všechny **křivky dostatečně proříznuty**. Tím jsem přišel o možnost spustit druhý průchod laseru.

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/2/IMG_2157.jpeg"
       style="transform: rotate(90deg); transform-origin: center center;
              width: 270px; height: 480px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/2/IMG_2162.jpeg"
       style="transform: rotate(90deg); transform-origin: center center;
              width: 270px; height: 480px;
              border-radius: 20px; object-fit: cover;">
</div>




První deska byla vyřezaná správně a odstranění dílů nebyl problém. U druhé desky jsem však musel použít **zalamovací nůž k dořezání** některých míst, což bylo **časově náročné**. 

 

Nakonec následovala poslední fáze – **složení samotného modelu**. 

Zpočátku to působilo komplikovaně kvůli **velkému množství dílů**, avšak po krátkém zorientování šlo vše poměrně hladce. Díky tomu, že jsem zvolil **uložení s přesahem 0,5 mm**, jednotlivé části do sebe přesně **zapadly a pevně drží**. 


<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/images/2/IMG_2181.jpeg"
       style="transform:  transform-origin: center center;
              width: 360px; height: 480px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/images/2/IMG_2183.jpeg"
       style="transform:  transform-origin: center center;
              width: 360px; height: 480px;
              border-radius: 20px; object-fit: cover;">
</div>