
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
	* 
 