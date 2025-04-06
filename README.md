📖 OpenBook – E-Book Reader Open-Source
OpenBook este un e-book reader open-source, low-cost, dezvoltat în cadrul proiectului TSC. Dispozitivul este construit pe baza microcontrolerului ESP32-C6 și integrează funcționalități avansate de afișare, comunicare și consum redus de energie, fiind pregătit pentru producție în masă.

🧩 Diagrama Bloc

Diagrama bloc care ilustrează conexiunile dintre toate componentele se află în Images/diagrama.png.


📦 BOM – Bill of Materials

Cod Componentă	Descriere	Datasheet / Link	Achiziție
ESP32-C6-WROOM-1-N8	MCU WiFi 6, BLE, Zigbee	Link	Mouser
W25Q512JVEIQ	Flash SPI 512Mb	Link	Mouser
MAX17048G+T10	Fuel Gauge IC	Link	Mouser
MCP73831T	Li-Ion Charge Controller	Link	Mouser
DS3231SN#	Real-Time Clock	Link	Mouser
BME680	Senzor aer, umiditate, temperatură	Link	Mouser
USB4110-GF-A	USB Type-C Conector	Link	Mouser
CPH3225A	Supercapacitor	Link	-
📁 BOM complet detaliat se află în Manufacturing/BOM.csv.

Link:
https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k
https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO
https://a360.co/4iZy6AA
https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda
https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k
https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda
https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D
https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda
https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda
https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda
https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D
https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda
https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor
https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY)
https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO
https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k
https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home
https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda
https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda
https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda

📌 Pinout ESP32-C6
Componentă	Interfață	Pini ESP32-C6	Motiv
E-Paper Display	SPI	MOSI, SCK, CS, DC, RST, BUSY	viteză ridicată, dedicat grafică
BME680	I2C	SDA, SCL	partajat cu RTC
RTC DS3231	I2C	SDA, SCL	consum redus în sleep
FLASH SPI	SPI	separat de display	acces paralel în multitasking
USB-C	GPIO + UART	Rx, Tx, VBUS, GND	debug și alimentare
Baterie	ADC	GPIO pentru citire nivel	monitorizare încărcare
Fuel Gauge	I2C	comun cu RTC & BME680	eficiență rutare

🛠️ Proces de Proiectare

✅ Etape parcurse:
Schema importată și ajustată după modelul oficial pe OCW

switch to pbc tot ajustata dupa modelul pe ocw

Plan de masă realizat pe ambele straturi pe pbc (TOP/BOTTOM)

Netclass-uri pentru trasee de alimentare (0.3mm) și date (0.15mm)

Autorouting selectiv pe TOP si pe BOTTOM pentru alimentare (cu AUTO 3V3 EPD_3V3 EPD_3V3_C VBUS VUSB ...)

rezolvarea errori de airwire, overlap, copper clearness

am pus piesele 3d pe pleaca , am luat carcasa pe ocw 

am implementat displayul si bateria de pe ocw si le am pus in carcasa 
 
am facut animatia -exploded  view 

🧩 Probleme întâlnite și soluții:
Footprint bobină L1 avea pad-uri sincronizate – am editat din bibliotecă și am înlocuit cu versiune custom (35x190mil).

Silkscreen suprapus – am folosit Copy Format pentru scalare uniformă.

Import și asocieri modele 3D:
Pentru componente unice: .step importat manual în Add New 3D Design

Pentru componente repetitive: am folosit Edit Component → Create New 3D Model, apoi Replace Package pentru a le atașa corect în bibliotecă

După ce modelele au fost salvate, s-a făcut Update from Library în PCB

Am testat exportul .step final și poziționarea corectă a componentelor în pbc

Overlap de paduri (în special la bobina L1) rezolvat prin modificarea dimensiunii pad-urilor(in edit footprint) si dupa am dat update pe biblioteca 



📸 Randări & Documentație
✅ Randări 3D în folderul Images/

✅ Model 3D complet în folderul Mechanical/

✅ Fișiere de producție în Manufacturing/

✅ Schemă și PCB în Hardware/

📚 Licență
Acest proiect este licențiat sub licența Apache 2.0 – îl puteți folosi, modifica și distribui în scopuri educaționale și comerciale.

