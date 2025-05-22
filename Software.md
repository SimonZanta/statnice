
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
