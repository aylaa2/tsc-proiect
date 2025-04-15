# OpenBook – Open-Source E-Book Reader

OpenBook este un e-book reader open-source, low-cost, dezvoltat în cadrul proiectului TSC.  
Dispozitivul este construit pe baza microcontrolerului **ESP32-C6** și integrează funcționalități avansate de afișare, comunicație și consum redus de energie, fiind pregătit pentru producție în masă.

---

##  Diagrama Bloc

Diagrama bloc care ilustrează conexiunile dintre toate componentele:

![Diagrama Bloc](Images/diagrama.png)

---

##  BOM – Bill of Materials


# Bill of Materials (BOM)

| Package | Parts | Datasheet |
|:--------|:------|:----------|
| ADAFRUIT_CHIP-LED0603 | CHG_LED | [Datasheet](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603) |
| SJ | SJ1 | [Datasheet](https://www.sameskydevices.com/product/resource/sj1-352xn.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R0402 | R1_PWRUSB, R1, R1_PINH1, R2-PINH, R2-PINH1, R5, R6, R7, R8, R9, R10, R_BOOT, R_CL1, R_RESET, R3, R1_PINH, R4, R_CHANGE, R_CAPACITOR, R2, R1_BAT, R2_BAT, R2_USB, R2_USB1 | [Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-wrover-e_esp32-wrover-ie_datasheet_en.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_C0402 | C1, C2, C4_USB, C6, C8, C9, C10, C_DELAY, EPD_C5, EPD_C1, EPD_C2, EPD_C6, EPD_C7, EPD_C8, EPD_C9, EPD_C10, EPD_C11, EPD_C12, C7, C5, C4, C1_BAT, C1_BAT1, C1_BAT2, C2_BAT, C5_USB | [Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-wrover-e_esp32-wrover-ie_datasheet_en.pdf) |
| RCL_CT3528 | C3 | [Datasheet](https://www.coilcraft.com/en-us/products/emi/power-line-common-mode-choke/high-isolation/cx-up-to-10-a/cg3528/cg3528/) |
| 112ATAARR03ATTEND | J4 | [Datasheet](https://www.digikey.com/en/products/detail/attend-technology/112A-TAAR-R03/17633923) |
| ESP32_WROVER_SPARKFUN-DISCRETESEMI_SOT23-3 | Q1, Q2 | [Datasheet](https://cdn.sparkfun.com/assets/e/b/6/b/0/esp32_datasheet_en-1223853.pdf) |
| IND_4828-WE-TPC_WRE | L1 | [Datasheet](https://media.digikey.com/pdf/Data%20Sheets/Wurth%20Electronics%20PDFs/744043_Kit.pdf) |
| SOT95P280X125-5N | IC1 | [Datasheet](https://www.snapeda.com/parts/BD52E42GTR/Rohm/view-part/) |
| MYBUTTON | BOOT_BUTTON, CHANGE_BUTTON, RESET_BUTTON | [Datasheet](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) |
| CAPCP3225X100N | C10_SUPERCAP | [Datasheet](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=search&t=CPH3225A) |
| SOIC127P1032X265-16N | U3 | [Datasheet](https://www.mouser.com/datasheet/2/472/si864x_datasheet-2507790.pdf) |
| XCVR_ESP32-C6-WROOM-1-N8 | U2 | [Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-c6-wroom-1_wroom-1u_datasheet_en.pdf) |
| ESP32C6_VARISTOR_CT/CN1812 | PFMF.050.1 | [Datasheet](https://www.snapeda.com/parts/PFMF.050.1/Littelfuse/view-part/) |
| ESP32_WROVER_AVX---SD0805S020S1R0_AVX_SD0805S020S1R0_0 | D2, D7 | [Datasheet](https://www.snapeda.com/parts/SD0805S020S1R0/AVX/view-part/) |
| ESP32_WROVER_BME680_PSON80P300X300X100-8N | SENSOR2 | [Datasheet](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds000.pdf) |
| ESP32_WROVER_SPARKFUN-IC-POWER_SOT23-5 | U0 | [Datasheet](https://www.ti.com/lit/ds/symlink/tps61200.pdf) |
| FH34SRJ24S05SH99 | J1 | [Datasheet](https://www.hirose.com/product/en/products/FH34SRJ/) |
| SON50P200X200X80-9N | U4 | [Datasheet](https://www.skyworksinc.com/-/media/Skyworks/SL/documents/public/data-sheets/Si88x2x.pdf) |
| SOD3716X135N | D3, D4, D5 | [Datasheet](https://www.vishay.com/docs/88503/1n4148.pdf) |
| DIOC1608X36N | D6, D8, D9, D10, D11, D12 | [Datasheet](https://www.littelfuse.com/~/media/electronics/datasheets/leds/littelfuse_leds_ltl_1ch_datasheet.pdf.pdf) |
| JST04_1MM_RA | J3 | [Datasheet](https://www.jst-mfg.com/product/pdf/eng/eSH.pdf) |
| SAMACSYS_PARTS_USB4110GFA | J2 | [Datasheet](https://www.snapeda.com/parts/USB4110-GF-A/GCT/view-part/) |
| SOT65P210X110-3N | Q3 | [Datasheet](https://www.onsemi.com/pdf/datasheet/bc817-d.pdf) |
| SOT95P280X145-6N | D1 | [Datasheet](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/) |
| SON127P600X800X80-9N | U1 | [Datasheet](https://www.skyworksinc.com/-/media/Skyworks/SL/documents/public/data-sheets/Si88x2x.pdf) |
| SOT95P280X120-5N | IC4 | [Datasheet](https://www.ti.com
::contentReference[oaicite:0]{index=0}
 


##  Descriere Hardware

OpenBook folosește următoarele module și componente:

- **ESP32-C6-WROOM-1-N8** – Microcontroller principal cu conectivitate WiFi 6, BLE și Zigbee.
- **W25Q512JVEIQ** – Memorie Flash SPI pentru stocarea datelor.
- **MAX17048** – Fuel Gauge pentru monitorizarea nivelului de încărcare a bateriei.
- **MCP73831** – Circuit de încărcare Li-Ion prin USB Type-C.
- **DS3231** – Ceas de timp real cu acuratețe ridicată.
- **BME680** – Senzor ambiental pentru calitatea aerului, temperatură și umiditate.
- **CPH3225A** – Supercapacitor pentru backup RTC.
- **USB4110-GF-A** – Conector USB Type-C pentru alimentare și comunicație.

**Specificații de comunicație și interfețe:**
- **I2C**: DS3231 (RTC), BME680 (senzor ambiental)
- **SPI**: W25Q512JVEIQ (memorie Flash externă)
- **I2C/SPI**: Ecran E-Paper
- **Fuel Gauge (MAX17048)**: comunicație prin I2C
- **USB**: Alimentare și încărcare prin MCP73831 + conector USB-C

**Calcul de consum de energie:**
- Dispozitivul intră în mod Deep Sleep ESP32 pentru a minimiza consumul (~20 µA).
- Fuel Gauge optimizează încărcarea/descărcarea bateriei pentru o autonomie maximă.

---

##  Pini ESP32-C6 folosiți

| Componentă         | Pini ESP32-C6   | Motivare                                   |
|---------------------|-----------------|--------------------------------------------|
| Ecran E-Paper       | SPI (MOSI, MISO, SCLK, CS, DC, RST, BUSY) | Comunicarea eficientă cu ecranul grafic. |
| W25Q512JVEIQ (Flash)| SPI partajat     | Economie de pini, viteze mari de transfer. |
| DS3231 (RTC)        | I2C SDA, SCL     | Comunicare cu precizie orară.             |
| BME680 (Senzor)     | I2C SDA, SCL     | Comunicare senzor ambiental.              |
| MAX17048 (Fuel Gauge)| I2C SDA, SCL    | Monitorizare nivel baterie.               |
| MCP73831 (Charger)  | GPIO pentru statut încărcare | Monitorizare simplă LED statut încărcare.|
| USB4110-GF-A        | USB D+/D-        | Alimentare și comunicare USB.             |

---

##  Alte informații utile

-  **Design Log**: Documentația completă a deciziilor de design se află în `Documentation/DesignLog.md`.
-  **Randări PCB**: Imagini randate cu placa de circuit imprimat în `Images/PCB_Renders/`.
-  **Carcasă**: Așezarea componentelor în carcasă poate fi vizualizată în `Images/Enclosure/`.

---

