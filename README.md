# Boudis-multiprint
# 📦 BoudiChanger 4 – Vícefilamentový přepínač pro Sovol SV06 Ace

**BoudiChanger 4** je open-source systém pro automatickou výměnu až **4 různých filamentů** pomocí **lineárního selektoru**.  
Navržen pro **levou stranu tiskárny Sovol SV06 Ace**, plně kompatibilní s **Klipperem**.

---

## 🧠 Hlavní funkce

- 4 vstupy pro filament (PTFE 4 mm)  
- 1 výstupní trubice přímo do extruderu  
- Lineární pohyb pomocí krokového motoru (NEMA17)  
- Ovládání přes Klipper (včetně maker)  
- Možnost použití senzoru přítomnosti filamentu  
- Kompatibilní s Orca/Prusa Slicer post-processingem

---

## 🛠️ Obsah repozitáře
---

## 🧩 Požadavky

| Komponenta        | Množství | Poznámka                          |
|------------------|----------|-----------------------------------|
| NEMA17 motor     | 1×       | 1.8°, 200 kroků/rev               |
| PC4-M10 konektor | 5×       | 4 vstupy + 1 výstup               |
| Pi Pico nebo MCU | 1×       | Řízení pohybu + sensor            |
| PTFE trubka 4mm  | 5×       | Spojení se spooly + výstup        |
| Microswitch/IR   | 1×       | Volitelné: detekce přítomnosti    |

---

## 🔧 Instalace

1. Vytiskni STL díly ze složky `/models/STL/`  
2. Sestav mechanickou část podle `/docs/assembly_guide.txt`  
3. Zapoj elektroniku dle `/docs/wiring.txt`  
4. Nahraj makra z `/firmware/klipper_macros.cfg` do `printer.cfg`  
5. Přidej post-processing hook do Orca Sliceru (`/slicer/orca_slicer_macro.txt`)  
6. Spusť testovací přepnutí pomocí: `SELECT_FILAMENT FILAMENT=1` (až 4)

---

## 📌 Poznámka

Tento projekt je ve vývoji. `.STL` a `.STEP` modely budou brzy doplněny.  
Pokud chceš přispět, otevři issue nebo pull request.

---

## 🧑‍💻 Autor

Miroslav Bouda – [@boudis100](https://github.com/boudis100)  
Open-source & community-friendly 🇨🇿
