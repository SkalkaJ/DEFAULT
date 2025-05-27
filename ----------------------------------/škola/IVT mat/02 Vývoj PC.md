# 2. Vývoj PC

***Obsah otázky:*** historie počítačů a spínací prvky hradel; binární sčítačka; počítačová architektura, druhy počítačů

## Turing Completeness
- Turing complete = označení počítače, programovací jazyka apod. který může emulovat Turingův stroj
- Turingův stroj:
    - Teoretický stroj vymyšlený matematikem Alanem Turingem
    - zařízení, které dokáže simulovat jakýkoliv algoritmus, spočítat vše spočítatelné
    - nejjednodušší stroj na řešení algoritmů, velmi jednoduché kroky
    - moderní počítače fungují na stejný princip
    - zrodil se zde také koncept *programů*, které byly *uloženy v paměti* (x nebyly připojeny někde bokem)

## Dějiny počítačů

### Předchůdci
- Abakus (počítadlo)
- Logaritmická pravítka
- Mechanické sčítačky a odčítačky (např. Pascalina pro výpočet daní)
- 1833 - Charles Babbage vyvinul "Analytický stroj" (Analytical engine) - první programovatelný stroj pomocí **děrných štítků**
    - Babbage si najal matematičku **Adu Lovelace**, která pro něj programovala

### 0. generace 
- počítače s **reléovými** obvody (elektromagnetický spínač)
- 30. a 40. léta 20. století
- počítače Z1 (první!), Z2, Z3,  Harvard Mark I., II., český SAPO (Samočinný Počítač)
- hodně spínačů -> prostorově náročné

### 1. generace 
- počítače s **elektonkovými** obvody (vede proud ve vakuu)
- polovina 40. let - 50. léta
- počítač ENIAC - první počítač podobný těm dnešním, **Turing Complete**
- nebyly o moc menší, ale spánaly rychleji - několik set až 1000 operací za sekundu
- velká poruchovost (životnost elektronek), nespolehlivé, elektronicky náročné

### 2. generace 
- počítače s **tranzistorovými** obvody (polovodičová elektronika; používá se dodnes)
- druhá polovina 50. let - polovina 60. let
- počítače UNIVAC, EPOS
- počítače pronikají mimo vědu a univerzity
- objevují se první programovací jazyky: COBOL, FORTRAN
- menší a méně energeticky náročné spínače, mnohem větší výkon

### 3. generace 
- počítače s **integrovanými** obvody
- polovina 60. let - 70. léta
- počítače IBM, Siemens 4004
- rychlost řádově roste a počítače se zmenšují
- první podpora pro **multitasking**
- vznikají první mikropočítače, minipočítače (integrují se jen tranzistory)

### 4. generace 
- počítače s **mikroprocesory** - integruje celý obvod (cache, řadič, ALU, ...)
- od konce 70. let, vyvíjí se stále
- počítače se opět zmenšují a vznikají **osobní počítače**
- ikonický procesor **x86** - většina dalších používala jeho architekturu (Intel atd.)
- vs. procesory **ARM** - odlišná architektura, nejpoužívanější u mobilů a tabletů - nižší spotřeba
- grafická rozhraní

### 5. generace
- zatím jen **teoretické** modely 
- kvantový počítač
- biologické počítače / biopočítače - používají molekuly (např. DNA a proteiny) pro výpočty
- fotonové počítače - využívají fotony pro výpočty; rychlejší než elektrony

## Hradla

### Binární logika
- 1702, *G. W. Leibniz* - vymyslel systém, skládající se z řady nul a jedniček popisující nějaký problém; věřil, že život může být zjednodušen na řadu jednoduchých problémů
- 1854 navázal *George Bool* s **Boolean algebrou** (true/false) - AND, OR, NOT, NOR, XOR, NAND (lze z něj složit ostatní hradla)
- de Morganovy zákony:
    - Negace součinu `not (A and B)` = Součet negací `(not A) or (not B)`
    - Negace součtu `not (A or B)` = Součin negací `(not A) and (not B)`

### Binární sčítačka
- když počítáme pod sebe - často si "držíme jedničku" - to samé funguje i v sčítačce
- sečtení dvou binárních číslic - dva výstupy: součet a carry

#### Poloviční sčítačka
- sčítá bez ohledu na předchozí carry
- `A xor B` - součet, `A and B` - carry

| A   | B   | C = `(A and B)` | S = `(A xor B)` |
| --- | --- | --------------- | --------------- |
| 0   | 0   | 0               | 0               |
| 0   | 1   | 0               | 1               |
| 1   | 0   | 0               | 1               |
| 1   | 1   | 1               | 0               |

![](./HalfAdder.png)

#### Úplná sčítačka
- sčítá i s předchozím carry
- jednou sečteme A a B, podruhé sečteme předchozí carry a carry ze součtu A a B, a poté ORneme carry z obou součtů

![](./FullAdder.png)

# 2
## Vývoj PC: historie počítačů, spínací prvky hradel, binární sčítačka, počítačová architektura, druhy počítačů

**Historie počítačů**

Vývoj počítačů začíná už v dávné minulosti, kdy lidé používali jednoduché počítací pomůcky jako zářezy na kostech nebo abakus. První mechanický kalkulátor vznikl v roce 1624. Za otce počítačů je považován Charles Babbage, který v 19. století navrhl „analytický stroj“ – první univerzální programovatelný počítač. Jeho spolupracovnice Ada Lovelace je považována za první programátorku[2](https://cs.wikipedia.org/wiki/D%C4%9Bjiny_po%C4%8D%C3%ADta%C4%8D%C5%AF)[3](https://www.internetembezpecne.cz/ucebnice-informatiky/vznik-a-vyvoj-pc/).

Ve 20. století začal rychlý rozvoj elektronických počítačů. První číslicové počítače vznikly ve 30. letech, například Z1 Konráda Zuseho (Německo, 1938), který byl mechanický, později Z3 už využíval relé[4](https://www.historiepocitacu.cz/casova-osa-historie-pocitacu.html)[11](https://wiki.gml.cz/doku.php/informatika:maturita:1a). V USA vznikl slavný ENIAC (1946), který byl založen na elektronkách a znamenal začátek první generace počítačů[9](https://www.alza.cz/historie-pocitacu).

## Generace počítačů:

| Generace    | Hlavní technologie | Představitelé / stroje    | Období         |
| ----------- | ------------------ | ------------------------- | -------------- |
| 1. generace | Elektronky         | ENIAC, UNIVAC             | 40. – 50. léta |
| 2. generace | Tranzistory        | IBM 7090, český SAPO      | 50. – 60. léta |
| 3. generace | Integrované obvody | IBM 360                   | 60. – 70. léta |
| 4. generace | Mikroprocesory     | PC, Apple II              | od 70. let     |
| 5. generace | VLSI, AI           | moderní PC, superpočítače | od 90. let     |

**Spínací prvky hradel**

Počítače pracují s logickými obvody, které realizují základní logické operace (AND, OR, NOT, XOR atd.). Spínací prvky těchto hradel se během vývoje měnily:

- **Relé** – první elektromechanické počítače (pomalejší, mechanické části)[4](https://www.historiepocitacu.cz/casova-osa-historie-pocitacu.html)[11](https://wiki.gml.cz/doku.php/informatika:maturita:1a).
    
- **Elektronky** – rychlejší, ale velké a energeticky náročné (ENIAC)[13](http://www.bigyzr.cz/shared/clanky/2893/ICT-Pripravy/IS4_Pripravy_poc-systemy_10-11.pdf).
    
- **Tranzistory** – menší, rychlejší, úspornější (druhá generace počítačů)[13](http://www.bigyzr.cz/shared/clanky/2893/ICT-Pripravy/IS4_Pripravy_poc-systemy_10-11.pdf)[5](https://physics.mff.cuni.cz/kfpp/skripta/elektronika/kap6/6_2_4.html).
    
- **Integrované obvody** – umožnily miniaturizaci a masové rozšíření počítačů (od 70. let)[13](http://www.bigyzr.cz/shared/clanky/2893/ICT-Pripravy/IS4_Pripravy_poc-systemy_10-11.pdf)[5](https://physics.mff.cuni.cz/kfpp/skripta/elektronika/kap6/6_2_4.html).
    

**Binární sčítačka**

Binární sčítačka je základní kombinační logický obvod, který umožňuje sčítat čísla v binární soustavě. Nejjednodušší je **poloviční sčítačka** – má dva vstupy (bity), dva výstupy: součet a přenos do vyššího řádu. Logické funkce pro poloviční sčítačku:

- Výstup součtu: XOR (A ⊕ B)
    
- Výstup přenosu: AND (A ∧ B)[6](https://www.elektroraj.cz/2024/11/12/binarni-scitacka-na-stavebnici-saimon/)[7](https://www.vovcr.cz/odz/tech/552/page05.html)
    

**Úplná sčítačka** navíc zpracovává i přenos z předchozího řádu a je základem pro sčítání vícebitových čísel v aritmeticko-logické jednotce (ALU) procesoru[7](https://www.vovcr.cz/odz/tech/552/page05.html).

**Počítačová architektura**

Architektura počítače popisuje, jak jsou uspořádány a propojeny jeho základní části a jakým způsobem zpracovává data. Základní architektury:

- **Von Neumannova architektura** – data i program jsou uloženy ve stejné paměti, počítač je řízen sekvenčně řadičem, základní části: řadič, ALU, paměť, vstupní a výstupní zařízení[8](https://cs.wikipedia.org/wiki/Architektura_po%C4%8D%C3%ADta%C4%8De)[13](http://www.bigyzr.cz/shared/clanky/2893/ICT-Pripravy/IS4_Pripravy_poc-systemy_10-11.pdf).
    
- **Harvardská architektura** – oddělená paměť pro data a pro program, což umožňuje rychlejší přístup a vyšší bezpečnost, využívá se v jednočipových mikropočítačích a specializovaných zařízeních[8](https://cs.wikipedia.org/wiki/Architektura_po%C4%8D%C3%ADta%C4%8De)[13](http://www.bigyzr.cz/shared/clanky/2893/ICT-Pripravy/IS4_Pripravy_poc-systemy_10-11.pdf).
    

**Druhy počítačů**

Podle velikosti, výkonu a účelu rozlišujeme několik základních typů počítačů:

- **Mikropočítače** (osobní počítače, PC) – určeny pro jednoho uživatele, běžné v domácnostech a kancelářích[12](https://is.muni.cz/el/fi/podzim2004/PB151/um/0.html).
    
- **Minipočítače** – sdílí více uživatelů, často slouží jako uzly v sítích nebo pro řízení technologií[12](https://is.muni.cz/el/fi/podzim2004/PB151/um/0.html).
    
- **Mainframy (střediskové počítače)** – vysoký výkon, používají se ve velkých firmách, bankách, státní správě[12](https://is.muni.cz/el/fi/podzim2004/PB151/um/0.html).
    
- **Superpočítače** – nejvýkonnější počítače na světě, určené pro vědecké a technické výpočty, simulace a analýzy[12](https://is.muni.cz/el/fi/podzim2004/PB151/um/0.html).
    
- **Jednočipové počítače** (mikrokontroléry) – specializované na konkrétní úlohy, např. v domácích spotřebičích, automobilech, průmyslové automatizaci[13](http://www.bigyzr.cz/shared/clanky/2893/ICT-Pripravy/IS4_Pripravy_poc-systemy_10-11.pdf).
    

---

**Shrnutí**

Vývoj počítačů prošel od mechanických strojů přes relé, elektronky, tranzistory až po dnešní mikroprocesory a integrované obvody. Základem výpočtů jsou logické obvody, jako je binární sčítačka. Počítačová architektura určuje, jak počítač pracuje s daty a programy, a podle účelu a výkonu rozlišujeme různé druhy počítačů od jednočipových zařízení po superpočítače.