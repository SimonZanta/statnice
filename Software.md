
# 1. Funkcionální programování

##  Programovací paradigmata

[Programovaci paradigmata](https://www.freecodecamp.org/news/an-introduction-to-programming-paradigms/)

* Určují strukturu, funkce a přístup, jak programovat

* Zvolení vhodného paradigmatu určuje, jak jednoduché bude daný úkol splnit, jelikož každé paradigma je vhodné pro jiný typ úkolu

* Paradigma není jazyk nebo nástroj, spíše určitý návod a set pravidel co jak proč dodržovat

* Je třeba si uvědomit, že určité jazyky jsou postavené na jednom paradigmatu, ale jiné mohou být multi-paradigmatické

| paradigma             | popis                                                                                                                                                                                                                                                                                                                  |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Imperativní           | Sada detailních instrukcí, které jdou po sobě. Příkladem je například                                                                                                                                                                                                                                                  |
| Procedurální          | Zděděné z Imperativního přístupu, ale s přidáním funkcí pro oddělení logiky                                                                                                                                                                                                                                            |
| Funkcionální          | Funkce jsou brané jako čisté funkce, je možné je tedy používat jako proměnné, vložné jako parametry nebo vrácené z jiných proměnných<br><br>Další vlastnost čisté funkce je že funkce závisí pouze na vstupu, produkuje stejný výstup jako vstup a neprodukuje žádné side effecty (nic se nemění mimo funkci samotnou) |
| Deklarativní          | Opak imperativního programování, namísto definování toho co má program dělat se definuje jaký výsledek má program dělat                                                                                                                                                                                                |
| Objektově orientované | Kombinuje různé přístupy a přidává jim možnost abstrakce, každá z entit obsahuje svoje vlastní funkce                                                                                                                                                                                                                  |
|                       |                                                                                                                                                                                                                                                                                                                        |
## Referenční transparentnost

* funkce vždy vrací stejný výstup pro stejný výstup
## Datové typy

* monoformní
	* jeden datový typ přiřazen
* polymorfní
	* obecný typ (let, const v JS)
## Částečná aplikace funkcí

* pokud se funkci předá méně argumentů než kolik očekává
* tím vznikne nová funkce
## Intenzionální zápis seznamů

* vytváření seznamů pomocí matematické funkce
* x <- [1..10]

----------------
# 2. **logické programování**

* založeno na definování **čeho** je v programu třeba dosáhnout namísto **jak** toho dosáhnout
## základní koncepty

* fakta - nějaká pravda (např. `rodic(karel, jan).` znamená, že Karel je rodič Jana).
* pravidla - Logické implikace tvaru `Hlava :- Tělo.`
* dotaz - otázky na které progream hladá odpověď `?- potomek(jan, karel).`
## Backtracking

- Pokud Prolog nenajde řešení, vrací se a zkouší alternativní cesty (**prohledávání do hloubky**).
## Reverzibilita logických programů

- Mnoho predikátů v Prologu je **reverzibilních** (lze je použít "oběma směry").
## Řízení průchodu programem

- Prolog prochází jednotlivé řádky programu **shora dolů**
- Řízení lze ovlivnit pomocí:
    - `!` – Zabrání backtrackingu
    - **`fail`** – Vynucení selhání
    - **`repeat`** – Vytvoří nekonečné možnosti backtrackingu.
## Hlavní odlišnosti od ostatních paradigmat

| Vlastnost           | Logické programování        | Imperativní / OOP   | Funkcionální                |
| ------------------- | --------------------------- | ------------------- | --------------------------- |
| **Styl**            | Deklarativní (co?)          | Imperativní (jak?)  | Funkcionální (transformace) |
| **Stav a proměnné** | Žádné přiřazení             | Měnitelný stav      | Neměnné hodnoty             |
| **Řízení toku**     | Backtracking                | Sekvence příkazů    | Rekurze, vyšší funkce       |
| **Typické použití** | Expertní systémy, parsování | Obecné programování | Matematické výpočty         |

## Možnosti použití logického programování
1. AI – Pravidla pro rozhodování (diagnostika, doporučení)
2. Přirozený jazyk – Gramatická analýza
3. Databázové dotazy – Složitější logické vztahy než SQL

----------------
# 4. Princip objektového návrhu

- jeden z nejrozšířenějších přístupů programování
- zaměřuje se na abstrakci kódu
	- hlavní vlastností je přiblížení programování fungování reálného světa
	- jelikož je možné definovat objekty a modelovat jejich vztahy
	- například `vehicle -> car -> volvo, skoda`
- oproti procedurálnímu vývoji umožňuje jednoduché modelování vztahů a využití několika instancí stejného kódu
## objekt x třída

- objekt je instancí třídy
- třída je šablona, která definuje metody a vlastnosti
## vlastnosti OOP
- abstrakce
	- skrývání složitosti pod dětské třídy
	- např aby auto neobsahovalo detailní metody pro fungování motoru
- synergie
	- vytváření tříd tak že se vzájemně doplňují
	- auto bude mít odkaz na metodu motor, ze které bude možné spustit funkci pro start motoru
- zapouzdření
	- pomocí zapouzdření se řeší možnost přístupu
		- `private`, `public`, `protected`
- dědičnost
	- možnost zdědění vlastností metody v metodě druhé
- polymorfizmus
	- umožňuje měnit chování tříd pomocí modifikátoru `overload` nebo `override` 
- doménový model
	- modelování systému podle reálné domény, např. E-shop: `Produkt`, `Košík`, `Objednávka`
- zatížení 
	- slabé zatížení
		- nízká závislost tříd na sobě = dobré
	- vysoké zatížení
		- vysoká závislost tříd = špatné
# Matematické principy počítačové grafiky

## Transformace

* popisují změny 2D a 3D objektů
* pomocí transformací je možné dělat různé změny
	* posun
	* rotace
	* změna velikosti
	* mirroring
	* jiná změna pozice vertexů
* transformace se provádějí pomocí 4D matice
	* důvod pro 4D matice je aby byla možnost je skládat
* Matice změny měřítka
 
![{\displaystyle \mathbf {S} ={\begin{pmatrix}S_{x}&0&0\\0&S_{y}&0\\0&0&1\\\end{pmatrix}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/c5eb4c62b1f6ad2c67db07c43c761557c5bd1fb9)

* Matice posunutí

![{\displaystyle \mathbf {T} ={\begin{pmatrix}1&0&P_{x}\\0&1&P_{y}\\0&0&1\\\end{pmatrix}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f378d39cbed6c9902779dd276bc1a54f3ad608d5)
## Homogenní souřadnice

* popisují pozici vektoru pomocí 3 nebo 4 vektorů x, y, (z), w
* jejich využití je pro transformace a manipulace s objekty v rámci scény a jeho prostoru
* mají tedy relativní hodnoty vzhledem k jednotkám scény
	* nemají tedy hodnotu např v px
	* 
## Zobrazovací řetězec

* průběh vykreslování jednotlivých framů v aplikaci
 
 vertex buffer -> vertex processor -> vertex shader -> triangle assembly -> rasterizace -> fragment shader -> tests (z-test) and blending -> screen

## camera control

* reprezentována pomocí pohledové matice
* ta obsahuje parametry
	* pozice
	* směr pohledu
	* up vector = určuju kde je směr nahoru
* každý frame se v zobrazovacím řetězci násobí tato matice s projekční maticí a maticí světa
	* díky tomu je možné s kamerou hýbat
 
# Rasterizace

* probíhá  skoro na konci a jedná se o vykreslení scény na obrazovku/canvas (**raster)
	* jedná se o převod vektorové reprezentace do rasteru
	* raster se skládá z pixelů, to jsou uniformní části rasteru
	* raster se dá reprezentovat jako matice
		* v každé "buňce" je obsažena hodnota, která reprezentuje barvu
		
* ### ukládání rasteru do různých formátů
	* rasterové
		* jpeg
		* png
		* bip
	* vektorové
		* svg
		
* ### základní grafické entity
	* bod
	* úsečka
	* trojůhelník
	
* ### algoritmy pro jejich vykreslení
	* bresenhammův algoritmus (úsečka, kružnice)
		* určí se bod A a B, kde A je vždy víc vlevo
		* při každém kroku se rozhoduje jestli se příští pixel vykreslí nahoru, dolů nebo směrem doprava
	* DDA
		* starší jak bresenhamm algoritmus
		* pro výpočet se používá rovnice y = kx + q
		
* ### Obrazově orientované algoritmy výplně
	* hranice výplně určují hranice objektu (povětšinou změna barvy)
	* flood fill
		* rekurzivní vyplňování
		* rekurzivně se vyplní vedlejší pixely
			* počet sousedních pixelů se určí podle druhu
		* hlavní nevýhoda je možnost buffer-overflow při nesprávném ukončení rekurze
		* dva druhy
			* čtyř sousední
			* osmi sousední
* ### Objektově orientované algoritmy výplně
	* scan line
		* jeden z nejznámějších
		* výplň probíhá po řádcích
		* vcelku jednoduchý algoritmus
			* výplň začíná poté co algoritmus přejede první "line"
			* výplň končí na následující line
			* ...
			* výplň opět začíná na následující line
			* algoritmus se tahle opakuje pro každý line
		* je třeba vyřešit problém s vrcholy, které by špatně mohly vyplnit řádek
# Zobrazení prostorové scény
* vizualizační řetězec
	* transformace objektů do MVP
	* projekce do 2D prostoru
	* řešení Z-bufffer
	* stínování a osvětlení
	* finální render
* ## řešení viditelnosti
	* malířův algoritmus
		* funguje na principu seřazení podle vzdálenosti od kamery
		* následovně se objekty vykreslují od nejvzdálenějšího k nejbližšího
			* ty se postupně překreslují
	* Z-Buffer
		* moderní přístup pro výpočet viditelnosti
		* využívá bufferu, tedy matice o stejné velikosti jako raster
		* do tohohle bufferu se zapisují vždy nové fragmenty, pokud je blíže
* ## výpočet osvětlení
	* má za úkol vypočítat barvu a intenzitu barvy v daném pixelu na závislosti pozice kamery nebo světla
	* výpočet světla je proveden na základě
		* pozice a typu světla
		* materiálu 
		* normály povrchu
		* pozice kamery
	* Phong light model
		* skládá se ze tří složek
			* ambientního osvětlení
				* ambience scény
					* aby scéna nebyla jenom černá
			* difůzní složky
				* určuje směr světla
			* spekulární složky
				* určuje odlesk 
		* výsledná barva se vypočítá součtem těchto složek
* ## vertex a index buffer
	* nejpodstatnější buffery v moderním vývoji
	* vertex buffer uchovává vlastnosti jednotlivých vertexů
	* index buffer uchovává propojení vertexů ve vertex bufferu
		* pomocí tohohle bufferu se spojují vertexy v model
* ## zobrazovací řetězec
	scéna
		↓
	MVP
		↓
	clipping
		↓
	rasterizace trojůhelníků
		↓
	fragment shader
		↓
	různé testy
		↓
	rasterizace

## optimalizace
* view frostum culling
	* nevyobrazení objektů mimo zobrazovací kužel kamery
* back face culling
	* nevyobrazení stran objektů, které nejsou viditelné
* occlusion culling
	* nevyobrazení objektů, které jsou zakryty dalšími objekty
* LOD
	* vytváření různé varianty modelů a jejich vyobrazení na základě vzdálenosti
* instancování 
	* renderování stejných objektů najednou jenom s jinou transformací

* ## moderní přístup
	 * dřív byl tzv fixní přístup
		 * ten využíval imperativního přístupu
		 * postupně se definovaly postupy a ty se taky prováděly
		 * dnešní přístup využívá shadery, které propočítávají většinu složitějších výpočtů
	 *  zobrazovací řetězec
		 * vertex shader
		 * tessalace (optional)
		 * geometry shader (optional)
		 * rasterizace
		 * fragment shader
		 * různé testy
## typy shaderů
| shader          | vlastnost                                     |
| --------------- | --------------------------------------------- |
| Vertex Shader   | transformace vrcholů                          |
| Fragment Shader | výpočet barvy fragmentu , osvětlení atd.      |
| Geometry shader | generování nových vertexů nebo nové goemterie |
| Compute shader  | využívané pro různé negrafické výpočty        |

## grafické knihovny 
*  vznikly aby se předešlo vniku zbytečného boiler plate kódu
* knihovny pro desktop použití
	* OpenGL - v dnešní době méně využívaný
	* Vulkan - openSource platforma, v dnešní době nejvíc využívaná
	* DirectX - platforma vytvořená MS, alternativa k vulkanu
* knihovny pro webové platformy
	* Three.js
	* WebGL
	* babylon.js
# Obrazová data
* využití zejména při převodu dat např ze snímače fotoaparátu
## Sampling
* vybírání hodnot ze spojitého signalu v pravidelných intervalech
* čím jemnější je sampling, tím je obraz více pixelovaný
		* a tedy i míň aliasovaný
## Kvantování
* používá se pro zaokrouhlení hodnot do konečného počtu úrovní 
* např. barvy na obrazovce můžou mít jenom konečný počet barev
## alias a anti-alias
* alias je viditelná hrana objektu
* anti-aliasing metody jsou metody které se pomocí vytváření barevného přechodu snaží zbavit viditelné hrany
	* SSAA
	* MSAA
	* TAA
	* FXAA
## předzpracování obrazu
* techniky které upravují obraz tak aby byl v určitém stylu
* např nastavením filteru, odstraněním šumu, normalizace osvětlení, změna rozlišení

### filtrace  obrazu

| Metoda               | Účel                                                  |
| -------------------- | ----------------------------------------------------- |
| Gaussovské rozmazání | Vyhlazení, odstranění šumu                            |
| Mediánový filtr      | nahrazení pixelu pomocí mediánu okolních pixelů       |
| průměrovací filtr    | podobný jako medián, jenom jednodušší ale méně přesný |
### intenzita světla

| Metoda                  | Účel                              |
| ----------------------- | --------------------------------- |
| Histogramová equalizace | Zlepšení kontrastu                |
| normalizace             | převod rozsahu pixelů na interval |
### edge detection + prahování

| Metoda                   | Účel                     |
| ------------------------ | ------------------------ |
| Sobel/Canny detekce hran | Zvýraznění kontur a hran |
| Prahování                | Segmentace objektů       |
## interpolace
* matematický výpočet jak získat přibližnou hodnotu mezi dvěma dalšími hodnotami
* vzorec
```
y(x) = y0 + (x-x0)*((y1-y0)/(x1-x0))
```
## histogram
* diagram který ukazuje na četnost různých hodnot v obraze
* pomocí tohoto diagramu je možné zjistit čeho je obrazu moc a poupravit to
	* tím je myšleno např. kontrast nebo intenzita jednotlivých barev
## segmentace a klasifikace obrazu
* používá se v rámci počítačového vidění
* Segmentace slouží k rozdělení obrazu na jednotlivé části (objekty atp.)
* Klasifikace potom ohodnotí jednotlivé segmenty
## komprese
* umožňuje zmenšit velikost výsledného obrázku
* dvě kategorie
	* ztrátová
		* nějaké informace zmizí
		* JPEG, WEP
	* bezztrátová
		* není ztráta informace
		* PNG, GIF
# Webové aplikace
## architektura
- jde o to jak je aplikace vnitřně poskládaná
	- komunikace mezi frontendem a backendem
	- databáze
	- zabezpečení
	- škálovatelnost
	- ...
- je třeba aby architektura byla dobře navrhnutá už od začátku
	- to zajistí že vývoj bude připraven na víc překážek
## komunikace mezi FE a BE
* FE je část aplikace která slouží zejména k tomu aby s ní interagoval uživatel, či aby pomocí ní získal požadovaná data
* BE je naopak část aplikace která zaznamenává či vydává zmíněná data pro frontend
	* také řeší zabezpečení, optimalizace načítání atd.
* FE a BE spolu komunikují zejména pomocí různých API či WebSocketů 
## požadavky a routování
* požadavky jsou vysílány z FE na BE
* mají různé flagy, které ovlivňují typ požadavku a to jestli obsahují data nebo ne
	* GET
		* požaduje od serveru na základě parametrů v url nějaká data
		* server pošle data
	* POST
		* posílá na server nějaká data zabalená v body parametru
	* DELETE
		* posílá požadavek na smazání nějakého záznamu
		* povětšinou obsahuje ID
	* PUT
		* úprava nějakého již vytvořeného záznamu
## routování se provádí pomocí vytvoření funkcí na BE
- tyhle funkce obsahují jednotlivé typy požadavků
	- následovně když se pošle požadavek na BE, je možné ověřit jestli funkce existuje a případně vrátit chybu pokud ne
## asynchronní model zpracování transakcí 
* poté co FE pošle požadavek na BE je nutné tento požadavek zaobalit do asynchronní funkce, která čeká na to než se ze serveru vrátí odpověď
* je nutné to dělat jelikož každý požadavek je jinak dlouhý a touto asynchronností se zajistí to že se vždy počká na vykonaní
* k tomu se používá nejčastěji JS async/await funkce
## Správa stavu ve webových aplikacích 
* stav se řeší povětšinou u komplexnějších aplikací
* jeho správa je závislá na volbě frameworku
	* Angular
		* řeší stav hlavně na úrovni komponent, je možné vytvořit service pro globální správu
	* React
		* stav se povětšinou řeší hlavně globálně, nicméně je možné ho uchovávat i v rámci komponent
## autentizace a autorizace
|Termín|Co to je|Přirovnání|
|---|---|---|
|**Autentizace**|Ověření **kdo jsi**|Kontrola tvé **identity / přihlášení**|
|**Autorizace**|Ověření, zda **máš oprávnění**|Kontrola **co můžeš dělat**|
## Zabezpečení
- je nutné využívat zabezpečení aby uživatelé nebo útočníci nebyli schopni narušit chod aplikace
- pro hodnocení nebezpečí se využívá openSource OWASP seznam
	- SQL Injection
		- vložení SQL kódu do inputu na FE a ten se pak vykoná na BE
	- XSS
		- vložení scriptu do stránky
	- CSRF
		- poslání požadavku pod jménem jiného uživatelé
	- ...
- pro zabezpečení je vhodné
	- validovat vstupy
	- aktualizovat knihovny
	- zapnout CORS
	- ochrana také na BE
	- případné cybersecurity testy 
## testování
- FE a BE je možné testovat
- testy mají zajistit že jednotlivé části aplikace fungují
- testy mají byt co nejvíc jasné, aby bylo možné zjistit jestli test prošel správně
- typy testů
	- E2E
		- větší testy
	- Unit
		- menší, víc specifické testy
	- Component
		- podobné jako unit, jenom pro FE komponenty
	- Smoke
		- nejméně přesné, nejvíc obecné
# Inversion of Control (IoC)
- ve své podstatě jde o to že se aplikace neřídí sama
	- je řízená pomocí frameworku
- to má za výhodu
	- nižší počet závislostí
	- jednodušší testování
- DI
	- konkrétní implementace IoC
	- injecting závislostí pomocí 
		- konstrukturu
		- setter
		- inject metody
- vztah IoC a DI
	- IoC je způsob řízení zvenku
	- DI je implementace IoC
# RESTful webové služby a mikroslužby
- způsob jak spolu aplikace komunikují po webu
- povětšinou pomocí HTTP
- základní vlastnosti
	- modulární - je možné je samostatně využívat
	- neopakované - aby nebylo několik stejných api
	- dostatečně abstraktní - možnost znovupoužít v dalších částech aplikace
## REST
- asi nejpoužívanější webová služba
- je stateless
	- server si nepamatuje stavy mezi požadavky
- response je ve formátu JSON
- velice jednoduchý a rychlý
- využívá HTTP metody
	- GET
	- POST
	- PUT
	- DELETE
	- ...
- využívá CRUD operace
	- CREATE
	- READ
	- UPDATE
	- DELETE
## SOAP
- formálnější a víc normalizovaný přístup
	- používáno v Enterprise aplikacích
- používá XML místo JSON
- pro komunikaci používá WDSL nebo UUID
- má prostředky pro lepší zabezpečení zpráv
	- víc advanced datové typy
- je možné ho spustit nad více protokoly
	- HTTP, SMTP ...
- obecně více složitý na práci
	- to má ale výhodu v
		- větší zabezpečení
		- šifrování
		- digitální podpisy
		- ...
## microservice
- každá služba v aplikaci je samostatná 
	- je tedy možné ji nasadit kamkoliv jinam
- každá z nich má vlastní databázi
- reprezentují jednotlivé funkční části
	- payment sevice
	- user service
- díky tomu je 
	- jednodušší škálovatelnost
	- nezávislá spolupráce teamů
	- jednodušší údržba
- zároveň ale
	- je třeba devOps
		- díky tomu kubernetes... 
	- vyšší složitost architektury
		- vyšší cena
# Architektonické a návrhové vzory
## SOA
- servisově orientovaná architektura
- aplikace je rozdělená do servis podle použití
	- service na uživatele, platby...
- umožňuje jednodušší správu autentizace
	- stačí se jednou přihlásit a na základě toho se udělí přístup do aplikace
- výhody
	- jednodušší znovupoužitelnost services
	- jednodušší codebase
		- lepší orientace
	- jednodušší scaling aplikace
## MVC
- model view controller
- model
	- obsahuje operace jako
		- logika
		- výpočty
		- databázové dotazy
		- validace
		- ...
	- podobné jako BE
	- ve své podstatě neví model odkud se funkce spustila
		- není tedy závislá na URL
	- je s ním možné použít ORM
		- v podstatě DJANGO
- view
	- reprezentace FE
	- vytváří vizuál pro uživatele
	- zápis normálně podle HTML + proměnné 
- controller
	- prostředník mezi modelem a view
	- má z úkol dostávat data / výpočty z modelu do view
## MVP
- stejný jako MVC, až na poslední
- presenter
	- ten je podobný jako controller
	- stejně jako controller vrací nějak naformátovaná data
		- na rozdíl od controlleru však rozhoduje i o tom co se bude dít s interakcí uživatele ve View
## MVT
- podobné MVC
- nicméně jsou dvě rozdílné vlastnosti
	- View
		- v tomto případě se chová spíše jako controller
		- tedy zpracovává a posílá požadavky
	- Template
		- slouží k zobrazení dat pomocí template
			- speciální soubor podobný HTML 
			- umožňuje však např
				- psát proměnné do html
				- psát různé kondice, loopy apod.
				- ...
## MVVM
- podobné MVC
- hlavně u FE frameworků
- view
	- opět čistě pro pohled na daty
- viewModel
	- slouží k získávání dat a správě logiky
	- pokud se něco změní ve viewModelu je automaticky změněn i view (two-way-binding)
## observer
- slouží k observování (pozorování) změn v
	- proměnné
	- requestu
	- ...
- tyhle změny pak automaticky upozorní odběratele (subscriber)
- s novými daty je pak různě nakládáno
# Datové struktury
- reprezentují řazení ukládání dat do paměti
## Array
- tzv pole
	- jedná se o úplně nejzákladnější datovou strukturu
	- jde o uspořádání dat do matice
		- základní array je o velikosti 1 x X
		- může být do velikosti X x Y
	- v jazycích jako je např Java
		- se vyskytuje jak pevná array
			- je tedy nutné předem definovat velikost, tato velikost se následovně vyhradí v paměti
	- naopak v jazyce JS
		- je array tzv. dynamická
			- nedefinuje se tedy předem velikost a je možné ukládat libovolný počet dat
	- přístup je pomocí indexu
		- tedy čísla pozice v pomyslné matici
		- rychlost O(1)
	- data je možné přidávat na 
		- konec
		- začátek
		- libovolný index
			- stávající data se na daném indexu přepíší
			- rychlost O(n) - uprostřed
## seznam (list)
- datová struktura kde každý node (jednotka)
	- v standartním listu
		- odkaz na následující node
	- v obousměrném listu
		- odkaz na následující  node
- je možné mazat nebo vkládat prvek na jakoukoliv pozici
- nicméně je pomalý v přístupu podle indexu
	- lepší je přístup pomocí hledání
## zásobník (stack)
- poslední dovnitř, první ven
- použití například pro undo operace
## fronta (queue)
- první dovnitř, první ven
## set 
 - struktura která obsahuje jenom unikátní hodnoty
## map
- ukládá hodnoty klíč - hodnota
- je možné hledat podle indexu nebo podle klíče
	- přístup přes klíč O(1)
# sortovací algoritmy
## bubble sort    
- jeden z nejjednodušších sortovacích algoritmů
- v podstatě jde o to že se vždy porovnávají dvě čísla
	- pokud je nalevo větší než napravo
		- prohodí se
	- tímto způsobem se v každé iteraci na konci objeví další největší číslo
- https://www.youtube.com/watch?v=xli_FI7CuzA
## insertion sort
- koukneme se na levý prvek aktuálního prvku
	- pokud je větší prohodíme je
	- takto prohazujeme do té doby dokud není prvek ve správném místě,
	- každý projetý prvek označíme jako seřazený
	- na konci by jsme měli mít seřazeno
- https://www.youtube.com/watch?v=JU767SDMDvA
## Selection sort
- začínáme opět zleva
- vybereme aktuální minimum
	- to je vždy první neseřazený prvek zleva
- projedeme celou array
	- do té doby dokud nenajdeme číslo menší než aktuální
	- poté je prohodíme
	- tento element označíme jako seřazený
- takhle cyklujeme dokud není seřazeno
https://www.youtube.com/watch?v=g-PGLbMth_g
## merge sort
- rekurzivní algoritmus
- v prvním kroku rekurzivně rozdělíme array na jednotlivé položky
- v druhém kroku každé dvě položky seřadíme a sloučíme
- v dalším kroku spojíme každé dvě seřazené array a sloučíme
	- takhle pokračujeme dokud nám nezbyde jedna seřazená array
- https://www.youtube.com/watch?v=4VqmGXwpLqc