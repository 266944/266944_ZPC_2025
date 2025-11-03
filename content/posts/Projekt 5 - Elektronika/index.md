---
title: "Elektronika"
layout: "simple"
---

Cílem pátého mini projektu bylo vytvořit funkční **elektrický obvod**. Pro realizaci jsem si zvolila zařízení, které sleduje aktuální **cenu bitcoinu** v intervalu 15 minut a zobrazuje její vývoj v čase na **OLED displeji**. 

 

## Použité knihovny 

 

V projektu byly využity následující knihovny: 

**WiFi.h** – poskytuje rozhraní pro připojení mikrokontroléru ESP32 k Wi-Fi síti (např. funkce WiFi.begin(), WiFi.status() apod.). 

**WiFiClientSecure.h** – umožňuje zabezpečené HTTPS připojení pomocí SSL/TLS protokolu. 

**HTTPClient.h** – poskytuje jednoduché HTTP/HTTPS API pro odesílání požadavků typu GET nebo POST; spolupracuje s knihovnou WiFiClientSecure. 

**ArduinoJson.h** – slouží k parsování (dekódování) JSON odpovědí ze serveru do struktury DynamicJsonDocument. 

**Adafruit_GFX.h** – základní grafická knihovna pro práci s textem, fonty a tvary. 

**Adafruit_SH110X.h** – ovladač pro OLED displeje s řadičem SH1106/SH1107 (v projektu byla použita verze SH1106 se SPI rozhraním). 

```html
#include <WiFi.h> 

#include <WiFiClientSecure.h> 

#include <HTTPClient.h> 

#include <ArduinoJson.h> 

#include <Adafruit_GFX.h> 

#include <Adafruit_SH110X.h> 
``` 
 

## Konfigurace a nastavení 

 

V úvodu programu byly definovány konfigurační konstanty, jako například: 

**název a heslo Wi-Fi** sítě, 

**interval aktualizace** ceny bitcoinu (15 minut), 

**adresa** webové stránky, ze které se získávají data o aktuální ceně. 

 ```cpp 
// ===== Wi-Fi údaje ===== 
const char* ssid = "Název"; // název Wi-Fi 
const char* password = "Heslo"; // heslo Wi-Fi 
// ===== CoinGecko API ===== 
const char* api_url = "https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd"; 
// ===== Interval aktualizace ===== 
const unsigned long waiting_time = 900000; // 15 minut 
``` 

Dále bylo nutné specifikovat zapojení jednotlivých pinů displeje k mikrokontroléru ESP32. 

 ```C
// ===== SPI piny pro OLED ===== 
#define OLED_MOSI 23 
#define OLED_CLK 18 
#define OLED_DC 2 
#define OLED_CS 5 
#define OLED_RESET 4 

// Inicializace OLED (128x64, SPI) 
Adafruit_SH1106G display(128, 64, OLED_MOSI, OLED_CLK, OLED_DC, OLED_RESET, OLED_CS); 
``` 

<div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/5/IMG_0378.jpg"
       style="transform: rotate(270deg); transform-origin: center center;
              width: 270px; height: 390px;
              border-radius: 20px; object-fit: contain; 
              background-color: #eaeaea;">
              
  <img 
       src="/266944_ZPC_2025/images/5/IMG_2246 (1).jpeg"
       style="transform: rotate(270deg); transform-origin: center center;
              width: 270px; height: 390px;
              border-radius: 20px; object-fit: contain; 
              background-color: #eaeaea;">
</div>


## Funkční popis programu 

 

Po inicializaci displeje probíhá proces **připojení zařízení k Wi-Fi** síti. Po úspěšném připojení program v hlavní **smyčce (loop)** čeká stanovených 15 minut, poté odešle HTTP požadavek na získání aktuální ceny bitcoinu, zpracuje přijatou JSON odpověď a aktualizuje zobrazenou **hodnotu na OLED displeji**. 

 

```C 
void loop() { 
delay(waiting_time); 
updateBitcoinPrice(); 
} 
``` 
 
 <div style="max-width: 800px; margin: 0 auto; display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; align-items: center;">
  <img 
       src="/266944_ZPC_2025/images/5/IMG_2254 (1).jpeg"
       style="transform: rotate(270deg); transform-origin: center center;
              width: 270px; height: 390px;
              border-radius: 20px; object-fit: cover;">
              
  <img 
       src="/266944_ZPC_2025/images/5/IMG_2257 (1).jpeg"
       style="transform: rotate(270deg); transform-origin: center center;
              width: 270px; height: 390px;
              border-radius: 20px; object-fit: cover;">
</div>

## Celý kód 
```C 
#include <WiFi.h> 
#include <WiFiClientSecure.h> 
#include <HTTPClient.h> 
#include <ArduinoJson.h> 
#include <Adafruit_GFX.h> 
#include <Adafruit_SH110X.h> 
// ===== Wi-Fi údaje ===== 
const char* ssid = "název"; // název Wi-Fi 
const char* password = "heslo"; // heslo Wi-Fi 

// ===== CoinGecko API ===== 
const char* api_url = "https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd"; 

// ===== Interval aktualizace ===== 
const unsigned long waiting_time = 900000; // 15 minut 

// ===== SPI piny pro OLED ===== 
#define OLED_MOSI 23 
#define OLED_CLK 18 
#define OLED_DC 2 
#define OLED_CS 5 
#define OLED_RESET 4 

// Inicializace OLED (128x64, SPI) 
Adafruit_SH1106G display(128, 64, OLED_MOSI, OLED_CLK, OLED_DC, OLED_RESET, OLED_CS); 

// Proměnná pro poslední cenu (šipka ↑/↓) 
double lastPrice = 0; 

void setup() { 
Serial.begin(115200); 
delay(1000); 

// Inicializace OLED 
display.begin(0, true); 
display.clearDisplay(); 
display.setTextColor(SH110X_WHITE); 
display.setTextSize(1); 
display.setCursor(0, 10); 
display.println("Connecting WiFi..."); 
display.display(); 

// Připojení k Wi-Fi 
WiFi.begin(ssid, password); 
Serial.print("Connecting to Wi-Fi"); 
while (WiFi.status() != WL_CONNECTED) { 
delay(500); 
Serial.print("."); 
} 
Serial.println("\nWi-Fi connected!"); 
display.clearDisplay(); 
display.setCursor(0, 10); 
display.println("WiFi connected!"); 
display.display(); 
delay(500); 
updateBitcoinPrice(); 
} 
void loop() { 
delay(waiting_time); 
updateBitcoinPrice(); 
} 
void updateBitcoinPrice() { 
if (WiFi.status() != WL_CONNECTED) return; 
WiFiClientSecure client; 
``` 
## Videoukázka hotového projektu
<div style="display: flex; justify-content: center; align-items: center; min-height: 100vh;">
  <video autoplay loop muted playsinline
      style="transform: rotate(270deg); transform-origin: center center;
             width: 100%; max-width: 540px; height: auto;
             border-radius: 20px; object-fit: contain;">
    <source src="/266944_ZPC_2025/videos/5/IMG_2251.mp4" type="video/mp4">
  </video>
</div>

