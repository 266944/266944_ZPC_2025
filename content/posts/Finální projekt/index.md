---
Title: "Finální projekt - Filament recykler"
layout: "simple"
---

Cílem tohoto projektu je návrh a realizace zařízení pro drcení podpěr a odpadního materiálu vznikajícího při 3D tisku. Výsledný produkt (granulát) je určen k opětovnému zpracování, ať už formou extruze nového filamentu, nebo pro využití při vstřikování plastů. 

Vývoj zařízení probíhal v několika fázích: 

## 1. Iterace

V první iteraci byla vyvinuta samotná drticí jednotka. Jako funkční prvky byly využity vyřazené frézy z CNC strojů, které rotují proti sobě a vtahují materiál ze zásobníku. Rozdrcený plast dopadá na separační síto – částice požadované frakce propadají do sběrné nádoby, zatímco nadměrné kusy jsou pomocí bubnu vyneseny zpět mezi břity k opětovnému drcení. 
<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2297.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 270px; height: 480px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2301.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 270px; height: 480px;
              border-radius: 20px; object-fit: cover;">
</div>

<img 
    src="/266944_ZPC_2025/images/f/IMG_2304.jpeg" 
    style="transform: rotate(0deg); transform-origin: center center;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
</img>

## 2. Iterace

Druhá iterace se zaměřila na optimalizaci konstrukce a odstranění nedostatků prvního prototypu. Došlo ke korekci směru otáčení fréz, eliminaci tření neřezných ploch a zpevnění uchycení jednotky k nosným profilům. Součástí úprav byla také konstrukce svodu odpadu, horní násypky a modifikace ložiskových domků. 
<div style="max-width: 1000px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2327.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 480px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2329.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 480px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>
Po těchto úpravách proběhlo úspěšné funkční testování. 

### Videa testování
 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <video autoplay loop muted playsinline
    style="transform: rotate(0deg); transform-origin: center center;
           width: 270px; height: 480px;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
    <source src="/266944_ZPC_2025/videos/f/IMG_2351.mp4" type="video/mp4">
  </video>

  <video autoplay loop muted playsinline
    style="transform: rotate(0deg); transform-origin: center center;
           width: 270px; height: 480px;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
    <source src="/266944_ZPC_2025/videos/f/IMG_2366.mp4" type="video/mp4">
  </video>
</div>

### Model 2. iterace

<iframe 
    src="https://gmail5614076.autodesk360.com/g/shares/SH90d2dQT28d5b60281173346ff951c31eeb?mode=embed" 
    width="1000" 
    height="480" 
    allowfullscreen="true" 
    webkitallowfullscreen="true" 
    mozallowfullscreen="true"  
    frameborder="0"
    style="border-radius: 20px; overflow: hidden; object-fit: cover;">
</iframe>

## 3. Iterace / O pár iterací později

Finální fáze zahrnovala automatizaci a kompletaci systému. Zařízení je vybaveno horní násypkou pro vstupní materiál a spodním zásobníkem pro hotový granulát. Hladina v obou zásobnících je monitorována ultrazvukovými senzory, které zajišťují automatické vypnutí stroje v případě vyprázdnění násypky nebo přeplnění sběrné nádoby. Rovněž byl i přidán magnetický kryt ložiska, jehož účelem je zajistit uník granulátu bočním výstupem a rotační buben byl vyroben z materiálu PA11 CF (směsi polyamidu a uhlíkových vláken) pomocí metody SLS pro zlepšení mechanických vlastností bubnu. 

<video autoplay loop muted playsinline
    src="/266944_ZPC_2025/videos/f/IMG_2413.mp4" 
    style="transform: rotate(0deg); transform-origin: center center;
           border-radius: 20px; overflow: hidden; object-fit: cover;">
</video>

Bezpečnost a plynulý chod zajišťuje řídicí systém: 

Bezpečnostní prvky: Dvojice koncových spínačů funguje jako pojistka, která znemožňuje spuštění stroje při otevřené konstrukci nebo během údržby. 

Ochrana pohonu: Rotační enkodér monitoruje otáčky hřídele. V případě detekce zaseknutí systém spustí automatickou uvolňovací sekvenci (reverzní chod). Pokud překážka přetrvává, proces se bezpečně ukončí. 

Rozhraní: K ovládání a sledování stavu zařízení slouží OLED displej na čelním panelu. 

Spoje: Na stroji se nachází i několik bistabilních mechanismů, které zajišťují spojení dílů. 
<div style="max-width: 1000px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/f/bozi.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 480px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2550.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 480px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>

### Model finální iterace

<iframe 
    src="https://gmail5614076.autodesk360.com/g/shares/SH90d2dQT28d5b602811703e7b2bfaaefd2d?mode=embed" 
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

### Fotky finální iterace

<div style="max-width: 1000px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2570.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 480px; height: 270px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/f/IMG_2571.jpeg"
       style="transform: rotate(0deg); transform-origin: center center;
              width: 480px; height: 270px;
              border-radius: 20px; object-fit: cover;">
</div>
Will be there soon. 