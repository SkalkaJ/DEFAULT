## 1 
- přenos, ukládání, zpracování, využití... počítače
- nejmenší jednotka bit
- adresář = organizace, struktura, hiearchie, strom
- soubor = sekvence dat
- OS = rozhraní, spojení SW a HW a uživatele
- operační paměť, ALU, řadič, vstup, výstup, I/O
- HARVARD- oddělená paměť, paralel, složitější
- NEUMANN- sdílená paměť, jednoduché, umiversální
- V binární soustavě
- ASCII = znakové sady
- UFT-8 = všechny jazyky, 1-4 bytů
- IEEE 754 = R čísla, znaménko+-, exponent 2^+-exp, mantisa
	- NaA, +-inf, +-0; 1 8 23; -126 -> 127
## 2
| Gen.   | Hlavní technologie | Představitelé / stroje      | Období         |
| ------ | ------------------ | --------------------------- | -------------- |
| před   | mechanika          | Abakus, Log prav, Pascalina | do 19.st.      |
| první  | mech. kalk.        | Anal. stroj, Babbage        | 19.st          |
| 0. gen | elmag. spínač      | Z1, Harv. mk 1, SAPO        | 30. - 40. léta |
| 1. gen | Elektronky         | ENIAC, UNIVAC               | 40. – 50. léta |
| 2. gen | Tranzistory        | IBM 7090, český SAPO        | 50. – 60. léta |
| 3. gen | Integrované obvody | IBM 360                     | 60. – 70. léta |
| 4. gen | Mikroprocesory     | PC, Apple II                | od 70. let     |
| 5. gen | VLSI, AI           | moderní PC, superpočítače   | od 90. let     |
- Turing = teoretický stroj, jakýkoli algoritmus, koncept programu v paměti
- bin. logika = AND, OR, NOR, XOR, NAND
- mikropočítače, minipočítače, servery, mainframy, superpočítače, jednočipové, kvantové (jiná technologie)
## 3
- desktop, mobilní, servery, real-time (debian)
- sigle/ multi-tasking, 1/ 1+users
- Virtual file system
- Win=NTFS, Linx=ext4, Mac=APFS/HFS+
- historie úprav, permise, metadata, komprese, šifrování
- Plocha, ikony, zástupci, lišta, start menu,... **záloha**
- časté pauzy, protahování, stání, správné periferie
## 4
- virtualizace, HyperV, oracle, VMware, HyperV, WSA
- unix - bezpečný, multitasking, multiuser, jednotný soub. sys; přenosný
	- web servery, db, cloud app,
	- FS: plain text soubory, ext4, /mnt, /run/media
	- Kernel, Shell, Utility system tools
	- /bin /boot /home /var /tmp /dev
	- .
## 5
- /chmod
## 6
- case, motherboard, CPU (úschova temp dat), RAM (aktuální temp data), SSD/HDD, GPU, 
  zvuková karta, síťová karta, zdroj PSU, periferie
- BIOS = nastavení
- **záloha**
- ISO, dvd, usb disk
- low/ high level formátování - magnety na HDD, rychlé/ celkové = přepis
- **[[RAID]]**, FSs, disk partitions
- účet, heslo, čas, jazyk, region, síť (static/ DHCP), aktualizace, zabezpečení, bloatware
- silné heslo, firewall, back-up, enkrypce, VPN, antivirus
- [[Návrh HW a SW pro různé typy využití PC]]
## 7
-  Personal Computer (micro), jednočip, super, mainframe
- kancl, osobní, herní, přenos, kompakt, výpočet, tvůrci, servery
- CMOS baterie
- [[RAID]] - Redundant array of independent disks, ztráta dat, 0,1,5,6,01,JBOD NAS
- Motherboard, CPU, GPU, RAM, PSU, Úložiště, chlazení, periferie: tiskárny, skenery, monitory
- x86-64/ARM - Apple, AMD, Intel
- tiskárny jehličkové, inkoustové, laserové
- LCD/LED
## 8
- schématický postup, přesné definované kroky, řešení
- širší působnost - kuchařky, návody
- rekurze, konečnost, elementárnost, determinovanost, obecnost, korektnost
- slovní, grafický (vývojový diagram), matematický, programovací zápis, struktorogram
- ![Vývojové diagramy – Základy informatiky pro střední školy](https://popelka.ms.mff.cuni.cz/~lessner/mw/images/a/a3/V%C3%BDvojov%C3%BD_diagram_m%C3%ADchan%C3%A1_vaj%C3%AD%C4%8Dka.svg)
- třízení, euklid, hashování, hledání faktoriálu
- sekvence, podmínky, cykly
## 9
- instrukce pro pc
- zápis algoritmů, program, interpretace technickými prostředky
- kompilátor, symboliské adresy, assembler, JSA v LMC
- interpretace/ kompilace

|Typ jazyka|Charakteristika a příklady|
|---|---|
|**Strojový kód**|Nejnižší úroveň, instrukce v binární/hexadecimální podobě, závislé na konkrétní architektuře procesoru.|
|**Assembler**|Symbolický jazyk, používá mnemotechnické zkratky instrukcí (MOV, ADD, SUB), stále blízko hardwaru.|
|**Vyšší programovací jazyky**|Abstrakce od hardwaru, srozumitelnější zápis, nezávislé na architektuře. Dělí se dále na:|
|- **Procedurální (imperativní)**|Program je posloupnost příkazů (C, Pascal, BASIC.|
|- **Strukturované**|Důraz na blokovou strukturu, cykly, podmínky (C, Pascal).|
|- **Objektově orientované**|Pracují s objekty, třídami (Java, C++, Python)|
|- **Deklarativní**|Popisuje, co má být provedeno, ne jak (SQL, Prolog).|
|- **Funkcionální**|Pracují s funkcemi jako základními stavebními bloky (Lisp, Haskell).|
|- **Logické**|Programování na základě logických vztahů (Prolog).|
- python: int, float, str, bool, list, dict, tuple, range, None
## 10
- instrukce, návod
- program čitelný, udržovatelný, testovatelný
- struktur -> sekvence podmínky cykly
- software, automatizace, práce s daty, kontrola hw, interface hw
- python -> moduly, snadný syntax, dynamické typy
- JSS -> asynchronní, weby, Node.js, mobilní aplikace
- C -> nízkoúrovňový, efektivní, hw
- abstrakce (úroveň), procedur/deklar, kompil/interpret, web/mob/PC, použití
- python: int, float, str, bool, list, dict, tuple, range, None
## 11
- paradigma, kód přidružen k datům, zapouzdření v objektech
- pravidlo DRY = dont repeat yourself, znovupoužitelnost, přehlednost, 
- class (třída) -> atributy, metody
- zapouzdření do jednoho objektu, dědičnost, polymorfismus, abstrakce
- události = uživatelská akce, event loop sleduje, onMouseMove, onClick, onChange.
- rozdíl = přístup k organizaci a řešení problémů
- double underscore, automatické volání, operator overloading, integrace s jazykem
## 12
- velikost: LAN, PAN, MAN (armáda, banky), WAN, GAN
- topologie: line, bus, star, ring, tree, mesh
- vztahy: P2P, klient-server, ISO/OSI, TCP/IP
![[bs3_1.gif]]
- porty, pakety, TCP/UDP(reliable/faster), 
- IP= identifikátor síťového rozhraní
- síťový port = TCP/UDP, transportní vrstva, 80, 443,...
- mac adress = fyzická adresa, při výrobě, LAN
- DHCP = protokol, auto konfigurace sítě, dynamická IP
- DNS = jména <-> IP adresy
- NAT = zabraňuje komunikaci ostatních zařízení přes internet s lokálním PC
- hub = posílá všemu okolo, switch = cílené posílání, router = switch + NAT + DHCP
- HESLO: 12 znaků, kombinace velkých malých písmen, čísel, speciálních znaků, unikátní, měnit
- firewall = monitoruje příchozí data, blokuje/ povoluje podle pravidel, bariéra
- šifrování = navštěvování stránek s podporou https/ssl
- antivirus = aktivní ochrana, Windows Defender
- aktualizovaný OS
## 13
- systém propojených počítačových sítí, umožňuje přenos dat, standardizované protokoly, pakety
- TCP/IP protokol, rozdělení na pakety a jejich následné směrování podle adres
- 69 ARPANET, v USA, spojení universit, vojenské účely = decentralizovaný systém, který přežije, protokol NCP
- 60, 70. léta vznik TCP/IP, rozšíření na více míst, IPv4
- 80. léta, zavedení TCP/IP, standard, celý svět, DNS
- Tim Berners-Lee 90 WWW, HTML, HTTP a první webový počítač... SERN
- email, poskytovatelé připojení, vyhledávače, webové stránky...
- dnes -> sociální sítě, celý svět, coud, bankovnictví
- služby: WWW, email, FTP, DNS, VoIP,...
![[TCPIP_Encapsulation.svg]]
- copyright: autor rozhoduje o využití v digitálním prostředí, komplikovaná ochrana
- licence: Open Source, End User Licence Agreement, Public Domain, Freeware, Closed Source, 
- nesdílet citlivý obsah, zmínit autora, 
## 14
- Identita = data reprezentujcí jednotlivce na internetu
- jméno, email, telefoní číslo, biometrická data, nákupy,...
- ověření: heslo, FaceID/otisk prstu, bezpečnostní tokeny (authenticator na mobilu, fyzické zařízení, USB token)
- datová schránka = úložiště pro výměnu dokumentů s úřady
- elektronický podpis = umožnujě ověření identity odesílatele, ochrana proti podvodu
- veřejný klíč ověřuje, soukromý tvoří data
- token = zařízení generující kódy na 2FA
- falešná/ neověřená digitální identita
- logy = záznam o přístupu a aktivitě na serverech a službách
- metadata = data o datech, čas vytvoření, poloha, typ zařízení, FOTKY,...
- Cookies = malé soubory prohlížeče, pohyb po webu, přihlašovací údaje, cílená reklama
- virtuální osobnost = může být jiná, než fyzická osoba, lepší verze sama sebe na sociálních sítích
- first/ third party cookies
- Algyritmy socek = personalizace obsahu, čas = peníze, pozornost, virální obsah, automatické filtrování = cenzura
## 15
- Internet  = globální síť počítačových sítí, TCP/IP protokol
- www = informační systém, vzájemné hyperlinkově propojené html
- doména = unikátní adresa, DNS překlad na IP, CZ.NIC
- webhosting = služba poskytující zpřístupnění stránek
- cloud = poskytování výpočetních/ úložiště služeb přes internet
- HTML, CSS, javascript = značkovací jazyk, HTML 5, CSS grafická podoba, 
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>Název dokumentu</title>
	</head>
	<body>
		
	</body>
</html>
```
- JS -> strana prohlížeče, interaktivita, funkcionalita
- integrace s HTML přes DOM = transformue html strukturu do objektů v JS
- h1, h2, p, b, i, br, a href=""
- PHP, Python, Ruby -> strana serveru, uživatel dostane jen už vygenerovanou stránku
- - nápad --> doména + webhosting --> připravit stránku, např. pomocí WordPress nebo HTML + CSS --> údržba
- webový server = odpovídá na HTTP požadavky, poskyt souborů, dynamický/ statický, **nginx**, generace HTML za pochodu
## 16
- 
## 17
- 
## 18
- přenos informací, software = vytváří grafiku prezentace, serii snímků
- MS Powepoint, google slides, Apple Keynote, LibreOffice Impress, Beamer v TeXu
- důležité -> téma, délka, účel, jednotnost prezentace... osnova, poznámky
## 19 Moderní Trendy
- GSM = mobilní sítě
- síť buňek (cells) na území, hexagony, BTS
- SIM = subscriber identity module
- LTE = long term evolution
- BTS = vysílače
- Internet of things = síť fyzických zařízení, vozidla, spotřebiče
- Smart home
- AI
- Průmysl 4.0 = nahrazení lidké práce plně automatizovanými systémy
- kybernetické systémy, digitalizace státu, ekonomiky
- zánik práce kvůli AI
- Návrat výroby z Číny zpět do Evropy a USA
## 20
- 
## 21
- 
## 22
- Modelování, CAD = softwareů§ůl
- TinkerCAD - v prohlížeči, jednoduchý
- OpenSCAD - open source, tvorba na základě skriptu
- Blender - pro 3D tvorbu obecně, hlavně rendery, stínování
- geometrie - modely z bodů, hran a stran
- .STL soubory, triangulace modelu = rozdělení stran na trojůhelníky
- .DAE, .OBJ, .FBX...
- textury = simulace povrchu materiálů
- Hlavně tisk:
- aditivní/ subtraktivní; plasty (PLA, PET, ABS), kovy, sklo, beton,...
- návrh -> slicing -> tisk -> postprocess
- Fused Deposition Modeling = tlačení plastu
- Selective Laser Sintering = spékání UV zářením
- Stereolitografie = tvrzení fotopolymeru UV zářením
- 3DCP
- podpory
- Prusa
## 23
- Práce s textem, vizualizace a tisk
- TABULKA níže, editory: vkládání, mazání, kód, nenáročné, rychlé, txt
- procesory: WYSIWYG, intuitivní, multimedia, kontrola pravopisu, spolupráce, docx
## 24

| ---              | typ souboru  | užití                          | příklady                     |
| ---------------- | ------------ | ------------------------------ | ---------------------------- |
| Textový editor   | plain text   | konfigurace, zdrojové kódy     | Vim, md, notepad, PSPad, VS  |
| Textový procesor | rich text    | dopisy, eseje, smlouvy         | Word, Libre, Writer, google  |
| DTP systém       | složité dok. | knihy, časopisy, vědecká práce | TeX, adobe InDesign, MS pub. |
- program pro sazbu, matematické výrazy, konfigurovatelnost
- Knuth 70. léta, The Art of Computer Programming
- nevhodný pro malé dokumenty (plakáty, vzkazy)
- Latex = sada maker, snadná sazba, definice nových maker, i bez znalostí, jednodušší
- Leslie Lamport
- struktura = značky
- zdrojový kód .tex -> překladač (PdfTeX, XeLaTeX,...) -> soubor .pdf
- příkazy skrze *\command_name*
- %komentář, **hlavička (preambule)**, tělo, enddocument
- documentclass, usepackage = balíčky, beamer,... \section
- \footnote = doplňující komentář
- \tableofcontents
## 25
- Tabulkový kalkulátor = zpracování numerických dat
- excel, google tabulky, iWork numbers, Libre office calc, Gnumeric
- statistika, vizualizace, účetnictví, ekonomie, věda
- .xls, .xlsx (zipované xml), .ods
- soubor = sešit, listy na liště
- buňky = různé datové typy a formát; možnost funkcí
- RANDBETWEEN(), SUMA(), MIN() MAX(), RANK.EQ()