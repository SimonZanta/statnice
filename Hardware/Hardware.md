# 1. Základní principy počítačů
## elektrické  obvody a jejich výpočty

- napětí U 
- proud I
- odpor R

U = I ⋅ R
- v sérii
	- R = R1 + R2 + ... + Rx
- v paralele
	- 1/R = 1/R1 + 1/R2 + ... 1/Rx
## Číselné soustavy
- počítače v hloubce počítají pouze se dvěma čísly (stavy)
	- 1 a 0
- ty se pak převádí do různých soustav, kde každá soustava má svoje využití
	- Binární 
		- 1 a 0
	- desítková
		- 0 - 9
	- Šestnáctková
		- 0 - 9, A - F
## logické funkce
| Operace | Značka | Výsledek (A=1, B=0) |
| ------- | ------ | ------------------- |
| NOT     | !A     | 0                   |
| AND     | A ∧ B  | 0                   |
| OR      | A ∨ B  | 1                   |
| XOR     | A ⊕ B  | 1                   |
## úprava a minimalizace logických funkcí
- dělá se pro to aby byla struktura zapojení hradel
	- jednodušší
	- levnější
	- potenciálně rychlejší
- usiluje se o
	- minimální počet logických funkcí
	- minimální počet proměnných
- pomocí 
	- Boolovy úpravy
		- A+AB=A (pravidlo absorpce)
	- karnaughova mapa
		- 	seskupení sousedních 1
	- McClusky
		- přístup používaný pro počítače

----------
# 2. Základy mikroprocesorů

  ![[mikroprocesor.jpg]]
## součásti mikroprocesoru
| Komponenta | vlastnost                             |
| ---------- | ------------------------------------- |
| ALU        | provádí matematické a logické výpočty |
| Register   | malá a rychlá paměť                   |
| Řadič      | řídí tok dat                          |
| dekoder    | překládá strojový kód na činnosti CPU |
| sběrnice   | spojuje jednotlivé komponenty         |
## architektura mikroprocesoru
- CISC
	- complex instruction set computer
	- obsahuje víc druhů operací které je možné vykonat na HW úrovni
		- i ty které by bylo možné zjednodušit
	- 
- RISC
	- reduced instruction set computer
	- obsahuje redukovaný počet operací
## Strojové instrukce a jejich zpracování
- MOV
	- přesunout
- JMP
	- skočit 
	- jmpr
		- podmíněné skočení
- ADD
	- sčítání
	- addc
		- sčítání s přenosem
- CMP
	- porovnání
## sběrnice
- spojuje jednotlivé komponenty
- přenáší 
	- data
	- instrukce
	- adresy
- typy
	- datová
	- adresová
	- řídící
## DMA
- direct memory access
- umožňuje přístup periferií k RAM bez CPU
- DMA řadič řídí čtení nebo zápis
- díky tomu má cpu víc času na ostatní věci
## přerušení
- upozornění CPU na nějaký event
- pokud je přerušení nutné CPU zastaví aktuální proces
- obslouží tenhle event
- vrátí se k předchozímu procesu
- příkladem přerušení je třeba event z klávesnice

----------
# 3. Základy architektury počítače
## základní komponenty
- základní deska
	- spojuje všechny komponenty
	- obsahuje 
		- sloty nebo konektory pro všechny komponenty
		- chipset
		- sběrnice
- cpu
- grafická karta
	- integrovaná
	- dedikovaná
- RAM
- paměť
- zdroj
## chipset
- řídí komunikaci mezi CPU, RAM, GPU a IO zařízení
- dříve byla hlavně na MB
	- northbridge 
		- cpu, ram, gpu
	- southbridge
		- cpu a IO
- dneska je většinově v CPU
## mikroprocesor a mikroarchitektura
- elektrický obvod
	- vykonává instrukce
	- vykonává je pomocí hradel
- mikroarchitektura
	- vnitřní návrh mikroprocesoru
- vlastnosti

| Komponenta          | vlastnost                                                        |
| ------------------- | ---------------------------------------------------------------- |
| taktovací frekvence | rychlost (Ghz)                                                   |
| počet jader         | "mikroprocesory v procesoru", které umožňují paralelní procesory |
| cache               | rychle dostupná paměť v CPU                                      |
| tdp                 | doporučená spotřeba (W)                                          |
- komunikace se dělá pomocí sběrnice
## PCI
- slouží ke komunikaci
- standartní rozhraní 

| verze | vlastnost                       |
| ----- | ------------------------------- |
| PCI   | nejstarší, přenos v stovkách mb |
| PCI-x | novější, přenos až GB           |
| PCIe  | aktuální, přenos až 64GB        |
## rozhraní PC
- pro připojení externích komponent či IO 
	- USB
		- USB A
			- standartní USB
		- USB C
			- nový standart
			- rychlejší než USB A
		- jsou schopné
			- přenosu dat
			- přenosu napájení
	- SATA
		- připojení externích disků
	- HDMI, DisplayPort, DVI, VGA...
		- připojení displaye ke grafické kartě
	- Ethernet
		- připojení sítě k síťové kartě
	- Jack
		- různé druhy pro připojení audio vstupů a výstupů

---------------------
# 4. Paměti počítačů
## dělení paměti
| typ          | popis                                                                |
| ------------ | -------------------------------------------------------------------- |
| RAM          | rychlá, dočasná paměť, načítají se do ní soubory spuštěných aplikací |
| trvalá paměť | paměť do které se ukládají soubory                                   |
| cache        | rychlá CPU mezipaměť s RAM                                           |
| rom          | paměť určená jenom ke čtení                                          |
| register     | malá, rychlá paměť v CPU                                             |
## základní parametry
| parametr    | popis                                                    |
| ----------- | -------------------------------------------------------- |
| kapacita    | dostupná velikost paměti                                 |
| rychlost    | jak rychlé je možné číst nebo zapisovat z nebo do paměti |
| propustnost | kolik dat je možné za sekundu projít                     |
| volatilita  | jestli se paměť vymaže při vynutí napájení               |
## hierarchie paměti
- paměti nejblíže cpu jsou nejrychlejší
	- nejdále jsou nejpomalejší
- CPU
	- registery
	- cache
	- ram
	- vnitřní paměť
	- usb ...

## cache
- paměť mezi procesorem a RAM
- L1 (nejrychlejší), L2, L3
## registry
- paměť v CPU
- nejrychlejší paměť
- obsahuje mezivýpočty atp.
## RAM a ROM

| parametr | popis                                                                                                                                    |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| RAM      | volatilní, lze do ní zapisovat i číst                                                                                                    |
| ROM      | nevolatilní, nelze do ní zapisovat - mimo speciální cesty (používá se pokud je potřeba jenom jeden specifický program pro dané zařízení) |
| EPROM    | speciální ROM                                                                                                                            |
## DIMM
- fyzický model RAM stick
- DDR4 a DDR5
## diskové paměti
- fyzické
	- plotny, ssd
	- skládají se ze sektorů atp.
- logické
	- rozdělení disků v OS na oddíly
	- C:, D: ...
	- --
------
 
# 5. principy operačních systémů
## monolitické vs mikrojádro
- monolitické
	- vše běží v jádru
	- to má za výhodu rychlost
	- naopak jsou méně bezpečné
		- jedna chyba může shodit celý OS 
- mikrojádro
	- jádro obsahuje minimum (plánovač paměti, plánovač, IPC)
		- vše ostatní běží jako uživatelské procesy
	- je více bezpečné
	- je nutná vyšší režie mezi procesy
- hybridní
	- aktuálně většina OS
	- berou si jenom "to nejlepší" z obou
## procesy a vlákna
- procesy
	- běžící program s pamětí
		- např. webový prohlížeč
- vlákno
	- lehčí proces
		- sdílí paměť procesu
		- vlastní registr
		- zásobník
		- ....
	- jeden proces může mít více vláken
		- paralelní výpočty - multithreading
- stavy procesu
	- new
		- proces vytvořen
	- ready
		- proces čeká na přidělení
	- running
		- proces běží 
	- waiting
		- čeká na IO nebo jiný procesor
	- terminated
		- procesor ukončen
## CPU scheduling
- kooperativní
	- proces se ukončí po té co se dokončí
- preetemtivní
	- proces má vyhrazený čas po který běží
		- pak jsou ukončení
	- v podstatě v dnešní době jako jediný používaný
		- důvodem pro použití je že není možné zajisti že program se dokončí a jenom se nezasekne
- quantování
	- jak rychle se procesy střídají
		- je nutné to vybalancovat
		- pokud by byly rychlé tak by se nic nestihlo
		- pokud zase moc pomalé tak by se zpracovalo jenom jeden proces
## Správa paměti

- Jeden z hlavních účelů jádra systému
	- Přiřazení dostatku paměti pro jádro i procesy
- Hlavní úkoly
	- Převody mezi různými druhy adres
	- Zpřístupnění paměti mimo adresní prostor
	- Alokace pro různé účely
	- Správa paměti
	- Cache, zápis etc.
	- Řešení nedostatku paměti – swap
## synchronizace procesů
- důležité pro to aby byla data konzistentní
- výrobce x spotřebitel
	- výrobce generuje data do bufferu
		- spotřebitel je čte
	- cíl
		- je nutné nezapisovat do plného bufferu
		- a zároveň je nutné nečíst z prázdného bufferu
--------
# 6. Souborové systémy a logická struktura dat

## principy souborových systémů
- vrstva OS pro logické uspořádání dat
- funkce
	- správa souborů a adresářů
	- ukládání, čtení, editování, mazání
	- oprávnění 
	- optimalizace rychlosti - indexování
- příklady FS
	- windows - FAT32, NTFS ...
	- linux - ext3, ext4 ...
	- flash - fat32, FAT, exFat ...
## atributy souborů
- velikost
- datum vytvoření
- datum změny
- práva
- umístění
- vlastník
- typ
- název
## operace se soubory
- otevření
- zavření
- čtení
- zápis
- mazání
## mapování souborů do virtuálního prostoru
- soubor se namapuje do adresového prostoru OS
	- přístup např pomocí pointerů
	- není nutné používat read(), write() funkce
## vnitřní struktura souborů
- na úrovni os
	- soubor rozdělen na bloky 
		- fs tyhle bloku hlídá a udržuje informaci o tom že jsou z jednoho souboru
- na úrovni aplikce
	- jsou tyhle bloky složené
	- je tedy možné zobrazit obsah souboru
		- text, struktury...
## sekvenční vs přímý přístup
- sekvenční
	- data se čtou nebo zapisují postupně
- přímý
	- data se načtou rovnou
## virtual file system
- v linuxu
- rozhraní mezi os a FS
	- kvůli tomu kolik je různých FS
	- poskytuje tedy jednotný přístup k těmto souborům
## vynucené a nevynucené zamykání souborů
- vynucené
	- OS zabrání ostatním procesům přístup k souboru 
- nevynucené
	- OS nezabraňuje, zabraňují procesy a ty se musí dohodnout
----
# 7. RM ISO/OSI a TCP/IP
## ISO OSI a TCP IP
- ISO OSI model
	- teoretický model
	- má 7 komunikačních vrstev
	
	- **fyzická vrstva
		- specifikuje fyzickou komunikaci, tedy hlavně kabely, huby apod.
	- **linková vrstva
		- uspořádává data z fyzické vrstvy do framů
		- uspořádává tyto framy, nahlašuje chyby
	- **síťová vrstva
		- stará se o směrování a adresování v síti
	- **transportní vrstva
		- přenos dat mezi dvěma koncovými uzly
	- **relační vrstva
		- má za úkol synchronizovat relační vrstvu obou zařízení a zařídit výměnu dat
	- **prezentační vrstva
		- formátuje data do formátu ve které je aplikace očekávají
	- **aplikační vrstva
		- poskytuje aplikaci přístup ke komunikačním vrstvám
- TCP IP model
	- zmenšený ISO OSI model
	- prakticky využívaný
	 
	- **síťová
		- 1-2
	- internetová
		- 3
	- transportní
		- 4
	- aplikační
		- 5-7
## protokoly TCP IP
- transportní vrstva
	- TCP 
		- jsou přesné, nechybí ani prvek, pomalejší - webové stránky
	- UDP 
		- mohou mít díry, rychlejší - streamy, telefonáty
- Internetová vrstva
	- IP
	- ICMP
		- diagnostika sítě
	- ARP
		- překlad IP do mac
- aplikační vrstva
	- HTTPS
		- webové stránky
	- FTP, SMTP
		- přenos souborů
	- SMTP, POP3, IMAP
		- emailové služby
	- DNS
		- překlad doménových adres na IP
## RFC dokumenty
- request for comments
- dokument se všemi internetovými protokoly formálně popsány
## PDU
- protocol data unit - jednotky používané na každé z vrstev

| Vrstva      | PDU                            |
| ----------- | ------------------------------ |
| Aplikační   | Data                           |
| Transportní | Segment (TCP) / Datagram (UDP) |
| Síťová (IP) | Paket                          |
| Linková     | frame                          |
| Fyzická     | Bit                            |
# 8. směrování a přepínání
## základy
- přepínání
	- proces vybírání správné cesty pro pakety v síti
	- k tomu slouží i fyzické zařízení switch
		- propojuje zařízení v síti ke komunikaci
	- je na třetí transportní vrstvě L2
	- vše dělá pomocí MAC
	- použití v LAN
- směrování
	- má za úkol směrovat pakety mezi sítěmi
	- k tomu se využívá router
		- ten tedy umožní komunikaci mezi jednotlivými LAN a WAN
	- vše dělá pomocí IP adres
	- transportní vrstva L3
## základní protokoly řízení komunikace
- L2
	- ARP
		- překlad IP na MAC
	- STP 
		- zabraňuje smyčkám v síti
	- LLDP
		- zjišťování sousedních zařízení
- L3
	- ICMP
		- diagnostika sítě
	- OSPF
		- routovací protokol
## MAC a IP v komunikaci
- mac 
	- fyzická adresa zařízení
	- 00:1A:2B:3C:4D:5E
- IP
	- adresa v rámci sítě
	- 192.168.0.1
- princip
	- data jsou vyslaná na cílovou IP adresu
	- pomocí ARP se zjistí MAC odpovídající IP adrese
	- poslání dat na MAC adresu

## směrovací algoritmy a protokoly
- RIP
- OSPF
- static routing
- default routing
## topologie
- star
	- nejčastější
- bus
	- zastaralá
- mesh
	- každý je propojen s každým
## funkce síťových zařízení

| zařízení | vlastnost                                  | vrstva |
| -------- | ------------------------------------------ | ------ |
| switch   | přepíná pomocí MAC adres, komunikace v LAN | L2     |
| router   | komunikace mezi LAN a mezi LAN a WAN       | L3     |
| bridge   | spojuje dvě L2 sítě                        | L2     |

------
# 9. Operační systém Windows
## architektura
- modulární architektura
	-  založená na hybridním jádře
- dvě hlavní vrstvy
	- User mode
		- spouštění uživatelských aplikací
		- část systémových služeb
	- Kernel mode
		- jádro
		- správce paměti
		- plánovač
		- ovladač
## Subsystémy
- Win32
	- hlavní prostředí
	- spouštění aplikací
- WSL
	- linuxové jádro ve windows
- Posix
	- kontabilita s UNIX
## systémové procesy
| proces       | vlastnost                    |
| ------------ | ---------------------------- |
| smss.exe     | spouští subsystémy           |
| csrss.exe    | konzole a GUI procesy        |
| winlogon.exe | přihlášení uživatele         |
| services.exe | spouští služby               |
| lsass.exe    | autentizace uživatele        |
| explorer.exe | GUI - start menu, taskbar... |

## bootování systému
- BIOS / UEFI
	- HW init
- bootmgr
	- načtení BCD
- winload.exe
	- načtení jádra
- kernel
- seasson 0 
- wininit.exe
- winlogon.exe
- explorer.exe
## serverové operační systémy

| proces            | vlastnost                         |
| ----------------- | --------------------------------- |
| active directory  | správa uživatelů, domén a politik |
| DHCP a DNS server | správa adresace a názvů           |
| Hyper-V           | virtualizace                      |
| remote desktop    | vzdálený přístup                  |
| server core       | serverová varianta bez GUI        |

-----
# 10. Operační systém linux

## linux vs GNU linux
- linux = jádro systému
- gnu linux = celý ekosystém, který ve své podstatě dává dohromady distribuci
	- povětšinou jsou do distribuce přidávány další nástroje
## architektura
- má monolitické jádro
- nicméně má i modulární rozšiřování 
- obsahuje
	- správu paměti
	- správu procesů
	- FS
	- síťování
	- ovladače
	- ....
- rozhraní jádra
	- vnější
		- mezi uživatelským programem a jádrem
	- vnitřní
		- interní api mezi moduly a jádrem
## boot proces
- BIOS nebo UEFI
	- HW inicializace
- booloader
	- načtení jádra
- kernel
	- inicializace GW, připojení FS
- init system
	- služby, mounty .....
## základní ovládání systému
- shell
	- interuptuje příkazu uživatele
	- různé varianty
		- bash
		- zsh
		- ...
	- skriptování, práce s proměnnými, pipes, práce s FS...
- systémové volání
	- funkce jádra
		- fork
		- exec
		- open
		- kill
	- ovládání HW a jádra
- signály
	- async oznámení procesům
	- sigkill
		- ukončení příkazu
	- sigterm
		- slušné ukončení
	- sigint
		- přerušení
## komunikace mezi procesy
- různé způsoby komunikace

| komunikace     | popis                          |
| -------------- | ------------------------------ |
| pipes          | jednosměrný kanál mezi procesy |
| named pipes    | trvalé pipes ve FS             |
| sockety        | síťová komunikace              |
| message queues | posílání zpráv mezi procesy    |
| shared memory  | sdílení paměti mezi procesy    |
| semafory       | synchronizace procesů          |
## démoni
- procesy v linuxu

| démon   | vlastnost                         |
| ------- | --------------------------------- |
| udev    | správa zařízení - nejdůležitější  |
| systemd | moderní init                      |
| crond   | spouštění procesu s nějakým časem |

## Správa paměti
- využití virtuální paměti
	- procesy nevyužívají fyzickou paměť ale virtuální
	- podpora swappingu, pagingu...
- defaultně se využívá demand paging
	- tzn načtení souborů až po té co jsou potřeba
- paměť se rozděluje na 
	- user space - pro aplikace
	- kernel space - pro OS
- cachování a bufferování
	- zrychlení načítání dat
- meminfo
	- ukazuje stav paměti
-------
# 11. Obecné principy IOT
## charakteristika
- IOT je souhrn zařízení která mají za úkol sběr dat ze sensorů a poté následnou reakci na tyto data
## složky IOT

| démon    | vlastnost                                                                         |
| -------- | --------------------------------------------------------------------------------- |
| sensory  | měření fyzikálních veličin                                                        |
| zařízení | modul který sbírá a zpracovává data, např arduino                                 |
| síť      | způsob jak komunikovat s cloudem, dalšími zařízeními atd.                         |
| cloud    | místo povětšinou mimo síť zařízení, může data ukládat, analyzovat, zpracovávat... |
| aplikace | uživatelské prostředí, kde je možné interagovat se zařízením                      |
## využití IOT
- průmysl - industry 4.0
- smart home
- zdravotnictví
- zemědělsví
- smart cities
- ....
## zpětná vazba
- jde ve své podstatě reakce IOT na data ze senzorů
- například spuštění světla pokud je okolní světlo nízké idk
## IoT soukromí a bezpečnost
- z důvodu práce s citlivými daty je nutné ji řešit
- co se jinak může stát
	- krádež dat
	- dostání se do sítě - takeover v síti
	- malvare
	- ...
- ošetření
	- šifrování
	- lepší autentizace a autorizace
	- aktuální firmware 
	- segmentace dat
## Referenční modely IoT
- 3-vrstvý model IoT

| démon    | vlastnost                      |
| -------- | ------------------------------ |
| fyzická  | senzory, aktuátory             |
| síť      | přenos dat                     |
| aplikace | zpracování dat, reakce na data |
- 4-vrstvý model IoT

| démon    | vlastnost                  |
| -------- | -------------------------- |
| percepce | senzory, aktuátory         |
| síť      | přenos dat                 |
| služby   | zpracování dat             |
| aplikace | provádění služeb uživateli |

- 5-vrstvý model IoT

| démon            | vlastnost                                        |
| ---------------- | ------------------------------------------------ |
| percepce         | senzory, aktuátory                               |
| síť              | přenos dat                                       |
| služby           | zpracování dat                                   |
| aplikace         | provádění služeb uživateli                       |
| vrstva podnikání | řešení životního cyklu, řízení celého ekosystému |

## analogový a digitální signál
- analogový jsou hodnoty napětí
	- hodnoty z nějakého fyzického zařízení
	- tzv spojitý signál
- digitální hodnoty jsou hodnoty čitelné pro počítač
	- např 0 a 1
	- tzv. diskrétní signál
- k převodu se využívají
	- AD převodníky
	- DA převodníky
## omezená zařízení
- nízký výpočetní výkon, paměť i baterie
- vytvořená za jedním účelem

# IoT bezpečnost a komunikace
## síťové technologie
- lokální
	- Wifi
	- bluetooth
	- zigbee
- širokopásmové
	- lorawan
## komunikační modely v IoT
- device to device
	- např pomocí zigbee
- device to cloud
	- přímé spojení s nějkým cloud serverem
- device to gateway
	- komunikace s nějakou mezivrstvou
- gateway to cloud
	- zařízení pošle data na GW, ta je shromáždí a pošle na cloud
## protokoly v IoT
- nižších vrstev - linková a fyzická
	- IEEE
	- WIFI, BLE, LoRa
- vyšších vrstev - aplikační 
	- MQTT
		- lehký, vhodný pro IoT
	- HTTP(S)
		- běžný ale na IoT zbytečně složitý
	- XMPP
		- průmyslové využití
## edge, fog, cloud computing
| démon | výpočty              | výhoda         | zařízení     |
| ----- | -------------------- | -------------- | ------------ |
| edge  | přímo na zařízení    | nízká latence  | raspberry PI |
| fog   | mezi edgem a cloudem | škálovatelnost | gateway      |
| cloud | v cloudu             | velký výkon    | AWS          |

## bezdrátové sítě
- povětšinou několik menších zařízení
	- propojené pomocí MESH
	- každé zařízení je limitováno výpočetně, paměťově a energeticky
## koncept smart
- snaha v podstatě vše mít "chytré"

| démon        | výpočty                    |
| ------------ | -------------------------- |
| smart home   | automatické ovládání       |
| smart city   | sběr a analýza dat z města |
| smart grid   | chytrá síť pro elektřinu   |
| smart health | monitorování pacientů      |
| ....         |                            |

## bezpečnost v IoT
- úroveň zařízení
	- bezpečné bootování
	- hesla
	- aktualizovaný firmware
	- HW bezpečnostní moduly
- úroveň komunikace
	- šifrování
	- ověření zařízení - certifikáty apod.
	- detekce neoprávněného přístupu
- úroveň aplikace
	- autentizace zařízení
	- logy
	- role v aplikaci
## posouzení hrozeb a zranitelností
- pokud posuzujeme je možné využít CVSS (common vulnerability scoring system)
	- ten má za úkol nám pomoci určit jak závažná hrozba je
- hrozba 
	- potenciální škodlivá událost
- zranitelnost
	- slabina
- proces analýzy
	- identifikace aktiv a dat
		- to co chráníme
	- identifikace hrozeb
		- např. DDOS
	- vyhodnocení rizika
		- pravděpodobnost x dopad
	- návrh ošetření
		- šifrování...
# principy objektového programování
## základní pojmy
- příkaz
	- něco co má program vykonat (instrukce)
	- např push do array, sečtení, zapsání do proměnnéj
- proměnná
	- místo v paměti do které se ukládají data a na kterou se dá odkazovat v rámci kódu
	- např. x = 1
- typ
	- určuje typ proměnné
	- aby bylo jasné jak bude vypadat hodnota v proměnné a jaké operace je s ní možné dělat
	- základní
		- int
		- string
		- boolean
		- float
	- "pokročilé"
		- vlastní type (TS) např "promenna" | true
			- hodnota muze byt jenom "promenna" nebo true
- funkce
	- souhrn příkazů, které povětšinou dohromady něco dělají
	- funkce je zaobaluje aby bylo možné tento souhrn funkcí znovupoužít
## principy objektového přístupu
- OOP má za úkol přiblížit programování víc fyzickému světu a vztahům v něm
- pojmy

| pojem       | vlastnost                                                            |
| ----------- | -------------------------------------------------------------------- |
| třída       | definice objektu (auto)                                              |
| objekt      | instance třídy (BMW)                                                 |
| atributy    | vlastnosti objektu                                                   |
| metody      | jednotlivé funkce které může daný objekt provádět                    |
| kontruktory | inicializují objekt z třídy                                          |
| destruktory | odebírají objekt z paměti                                            |
| interface   | předpis pro vlastnosti třídy, není možné z ní vytvořit rovnou objekt |

- základní principy
	- zapouzdření
		- skrytí vnitřní struktury objektu před okolím
		- aby nebylo možné libovolně měnit jakoukoliv proměnnou apod.
		- přístup do objektu pomocí getterů a setterů
			- aby přístup byl konzistentní
		- přístup lze omezit pomocí flagů
			- private - vidí jenom třída sama
			- protected - vidí třída a její potomci
			- public - vidí všichni
	- dědičnost
		- je možné aby jedna třída zdědila vlastnosti třídy druhé 
			- např. třída dům může dědit z třídy budova
	- polymorfizmus
		- pomocí interface je možné aby třídy měli stejné funkce
			- tyto funkce mají však jinou implementaci
			- protože interface nemůže implementovat funkce
	- abstrakce
		- skrytí detailů
		- zobrazení jenom důležitých informací
	 ![[Class-Notation.webp]]

----------
# datové struktury a jejich zpracování
## základní datové struktury
[pole](Software/Software#Datové%20struktury##Array)
[seznam](Software/Software#Datové%20struktury##seznam%20(list))
- objektová reprezentace
	- pole
		- java - `int[] pole = new int[10]`
		- TS - `const pole: number[] = []`
	- seznam
		- java - `List<String> seznam = new ArrayList()`
		- TS - `const seznam: {prop1: number, prop2: string} = {}` 
		- povětšinou mají definovanou class nebo interface
			- list stringu se tolik nehodi
## Základní algoritmy
- procházení
- hledání
- řazení
- filtrování, mapování...
## streamy a zpracování souborů
- z důvodu velikosti souborů není vždy možné celý soubor nahrát do RAM paměti
	- z toho důvodu se data streamují
- znamená to že data se postupně načítají (streamují)
## objektová persistence
- aby se objekty uchovaly
- k tomu se využívá ukládání na disk
	- ve speciálních formátech
	- textové 
		- csv
		- json
		- xml
	- binární
		- ObjectStreamOutput - java
	- databáze
		- hibernate
## formáty dat
- csv
	- hodnoty oddělené čárkou
	- dost často používané v exelu a podobných aplikacích
	- ve své podstatě jednoduše reprezentují tabulku
- JSON
	- JS formát
	- nejrozšířenější standard pro přenos dat na webu
	- key - value formát
- xml
	- umožňuje značkování pomocí vlastních tagů, podobné HTML
	- dříve se dost používalo místo JSON na webu
# tvorba uživatelského rozhraní
## komponenty UI
- samostatné stavební bloku ze kterých se UI skládá
- jedná se o např.
	- tlačítka
	- formy
	- tabulky
- komponenty mohou být i mnohem složitější a de facto by se i část celé webové stránky dala udělat jako komponenta
- hlavní výhodou využití komponent je jejich znovupoužitelnost a hlavně abstrakce HTML kódu
## layout
- dva hlavní druhy
	- flex
		- položky jdou za sebou, buď řádek nebo sloupec
	- grid
		- položky jsou v mřížce
		- je možné vynechávat políčka nebo si naopak políčka vybírat
- je možné využít i samostatných jednotek
	- to však nemusí být vždy žádoucí jelikož se tím povětšinou rozbije flexibilita
	- tyto jednotky se používají zejména u základních komponent
		- aby byly např stejně široké apod.
## responsivní design
- optimální začít designem pro mobil a poté přejít na pc
	- pc je mnohem jednodušší
		- zejména z důvodu že na něm programujeme
-  je možné ho dosáhnout pomocí responzivního layoutu
	- nebo css frameworky (tailwind)
	- a nebo samotným CSS
## událostmi řízené programování
- ve své podstatě jde o to co nastane pokud
	- někam kliknu 
	- přes něco přejedu
	- vyberu něco apod
## rozhraní a vnitřní třídy
- interface
	- předpis třídy
	- sama neimplementuje žádnou funkcionalitu
- vnitřní třídy
	- třída uvnitř jiné třídy
## [návrhové vzory](Software/Software#%20Architektonické%20a%20návrhové%20vzory)

# síťové a víceúlohové aplikace
- klient
	- někdo kdo odesílá požadavky a přijímá odpovědi
	- povětšinou FE
- server
	- někdo kdo vykonává tyhle požadavky
	- povětšinou BE
- protokol
	- standart pro komunikaci
	- HTTPS, dříve HTTP
- socket
	- propojení mezi klientem a serverem
	- nicméně "není závislý" na požadavku
	- používá se pro živou konverzaci
## principy komunikace v síti
- komunikace probíhá po vrstvách
- použití dvou protokolů
	- TCP
		- přenosy musí být stabilní a ucelené
		- např pro webovky
	- UDP
		- přenos nemusí být celiství
		- to však umožňuje plynulý přenos
		- např u videa nebo hovoru
## Víceúlohové aplikace
- aplikace které vykonávají více tasku najednou
- řešeno pomocí
	- vláken
	- procesů
	- async zpracování
- např. hry nebo webové aplikace s načítáním z API
## Typy serverů
- webový server
	- hostuje www stránky
- doménový server
	- hostuje vlastní dbs dns
- souborový
	- hostuje soubory
- databázový server
	- hostuje databázi
	....
## paralelní zpracování
- pro dosažení lepší výkonnosti
- např. načítám data a mezi tím můžu něco propočítavat

# publikování na webu
## značkovací, stylovací a scriptovací jazyky
- pro značkování se využívá HTML
	- ve své podstatě jde o vytváření struktury webu pomocí tagů
- ty se stylují pomocí CSS
- dohromady tedy tvoří statickou webovou stránku
- aby se přidala interakce je možné využít JS
## Responzivní design
- moderní přístup designu aplikací
- jsou designovány tak aby se jedna aplikace dala použít na všech zařízeních
- toho se dosáhne povětšinou díky CSS media queires
	- ty aplikují styl na základě nějaké podmínky, nejčastěji na základě šířky
## přístupnost
- napomáhá lidem s nějakým postižením v orientaci a aplikaci
- pomocí správně využitých html tagů a jejich labelů je možné aby čtečky byly schopně "přečíst" obsah
	- použití atributu alt
## návrh, vývoj, testování
- ve své podstatě někonečný loop životnosti aplikace
- vytvoření wireframe a design - tenhle krok je jenom při implementaci nové věci a to taky jenom občas
- vývoj dané featury podle designu, případně oprava stávajicí části
## DOM
- struktura webové stránky
- jedná se o strom
- většina frameworků využívá virtuální DOM
	- ten má za výhodu lepší reakce na interakci a výkonnost
## web api
- DOM api
	- práce s elementy na obrazovce
- Event api
	- reakce na event, např klik na tlačítko
- Fetch api
	- fetchování dat ze vzdáleného uložistě
- Storage api
	- ukládání dat do paměti prohlížeče
		- session storage
		- local storage
....
# objektové modelování
## účel
- účelem je pochopení návrhu systému před jeho implementaci
- pomáhá
	- komunikovat
	- snížit chybovost
	- zjednodušit údržbu
	- převést realitu na sw
## základní pojmy
- třída 
	- předpis / šablona pro to co má pak objekt dělat
		- implementace metod, funkcí, proměnných apod.
- Objekt
	- instance třídy v kódu
## [principy OOP](#%20principy%20objektového%20programování)

## analytický vs návrhový model
- analytický model
	- zachycení reality
	- zachycuje co systém má umět
		- ne jak se to implementuje
- návrhový model
	- návrh implementace
		- třídy
		- dědičnost
		- atributy
		- ....
## UML
- unified modelling language
- standardizovaný jazyk pro návrh sw systémů
- pět různých "příchutí"
	- logické
		- nejvíc zastoupené
		- modelování tříd, funkcí apod.
		- jejich vzájemné propojení
	- procesní
		- má počáteční a koncový bod
		- v podstatě ukazuje jak probíhají jednotlivé procesy v aplikaci
		- např přihlášení, platba apod.
	- vývojové
		- propojení komponent, modulů a podobných vývojových struktur
	- fyzické
		- jak je systém nasazen na HW
	- use case
		- standardizované zapsání požadavků zákazníka 
		- ukazuje hlavní use case aplikace
		- je nejvíc obecný
## vztahy
- asociace
	- vztah mezi dvěma třídami
- generalizace
	- dědičnost
- agregace
	- slabá forma vlastnictví
		- celek může fungovat bez části
- kompozice
	- silná forma vlastnictví
		- celek nemůže fungovat bez části