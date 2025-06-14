# 6. Stavba PC, instalace a konfigurace OS

***Obsah otázky:*** části PC, základní HW a SW části počítače, základ instalace a konfigurace OS (Windows či unixového typu). 

### Složení PC

#### Hlavní komponenty

1. **Základní deska *(mother board)*** - obvodová deska, na které jsou připojeny ostatní komponenty
2. **Procesor *(CPU)*** - centrální procesorová jednotka, provádí výpočty a zpracovává instrukce
3. **Grafická karta *(GPU)*** - zpracovává grafické informace a zobrazuje je na monitoru
4. **Operační paměť *(RAM)*** - dočasné úložiště dat pro aktuálně spuštěné programy, pomáhá rychlejšímu načítání, po restartu se vymaže
5. **Úložiště** - trvalé úložiště pro data a programy
	- **pevný disk *(HDD)*** - fyzický disk z něhož jsou data čteny pomocí mechanického ramene (levnější, zastaralé)
	- **polovodičový disk *(SSD)*** - neobsahuje pohyblivé části, rychlejší
6. **Síťová karta** - umožňuje připojení počítače k počítačové síti 
7. **Zdroj napájení *(PSU)*** - dodává energii všem komponentům v počítači
8. **Skříň *(case)***
9. **Chlazení, monitor, myš, klávesnice**

#### BIOS

- Basic Input/Output System = čip na základní desce, slouží pro přístup a nastavení PC
- obsahuje instrukce pro načtení základního HW, testuje zda je PC funkční
- po nalezení OS mu předá kontrolu nad PC
- poskytuje základní kontrolu nad HW, umožňuje konfiguraci systémového nastavením data, času, hesel atd.

#### OS

- základní program počítače, který umožňuje běh programů a komunikaci s HW

### Instalace a konfigurace OS

- zdroj instalace: může být DVD, USB disk nebo síťová instalace
- lze naintalovat na virtuální stroj (ISO soubory)

#### Formátování disku

1. **Nízkoúrovňové formátování (low-level formating LLF)**
	- pouze u HDD, připravuje disk na použití
    - dnes vždy prováděno výrobcem, uživatel nemůže provést
    - HDD se skládá z ploten na kterých jsou data ukládána do soustředných magnetických kruhů - stop, ty se dělí na sektory. Sektory jsou nejmenší zapisovatlné jednotky disku
    - LLF na disku tyto stopy a sektory vytváří magneticky

2. **Vysokoúrovňové formátování**
    - formátování zapíše na pevný disk (resp. na zvolený diskový oddíl) metadata soubory, která popisují prázdný souborový systém
    - máme na výběr mezi rychlým a celkovým formátováním 
        - rychlé pouze přepíše vyhledávací tabulku souborového systému, na disku zůstanou zapsána původní data, OS je vidí jako prázdná
        - celkové udělá to samé jako rychlé + přepíše všchna data na samé nuly, tím se provede i kontrola disku - odhalí se nefunkční sektory disku
    - při formátování můžeme zvolit allocation unit size - tj. nějaký násobek velikosti sektoru, tím se nastaví nová velikost nejmenší zapisovatelné jednotky
    - když se řekne *formátování*, myslíme vždy to vysokoúrovňové, není-li specifikovano jinak 
    - u SSD jiná architektura, ale funguje obdobně
    
#### Souborové systémy

- souborový systém je struktura, která organizuje a spravuje data na úložném zařízení, umožňuje ukládání, vyhledávání a manipulaci se soubory a adresáři
- při formátování disku musíme nastavit souborový systém, který bude disk resp. diskový oddíl používat
- NTFS (New Technology File System): Nejčastěji používaný souborový systém pro Windows. Podporuje velké soubory a disky, zabezpečení a kompresi dat.
- FAT32 (File Allocation Table 32): Starší souborový systém, omezený velikostí souborů do 4 GB a velikostí oddílu do 32 GB. 
- exFAT (Extended File Allocation Table): Moderní souborový systém, který je vhodný pro USB disky a paměťové karty. Podporuje větší soubory než FAT32.
- ext4: pokorčilý open-source žurnálovaný souborový systém. Podobný NTFS, často využíván na Linuxu

#### Dělení disku na oddíly (disk partitions)

- jeden pevný disk lze rozdělit na více oddílů (někdy také logických disků)
- dobré pro oddělení systémových a uživatelských dat
- dobré pro organizaci souboru, ochranu dat
- při manuálním dělení může dojít k naplnění kapacity jedné části a další zůstává nevyužita - nemusí dojít k maximálnímu využití potenciálu
- každý oddíl může mít vlastní souborový systém
- užitečné pokud chceme používat více operačních systémů a všechny bootovat z jednoho disku (*dual-booting*)

#### RAID

- technologie, která kombinuje více pevných disků do jednoho logického celku pro zvýšení výkonu a/nebo redundance (metoda zabezpeření dat proti selhání pevného disku):
- RAID 0 (Striping): Data jsou rozdělena mezi dva nebo více disků. Zvyšuje výkon, ale nemá redundanci. 
- RAID 1 (Mirroring): Data jsou zrcadlena na dva nebo více disků. Zvyšuje redundanci, ale ne výkon.
- RAID 5: Data a parita jsou rozloženy mezi tři nebo více disků. Nabízí dobrý výkon a redundanci.
- RAID 10 (1+0): Kombinace RAID 1 a RAID 0. Nabízí vysoký výkon a vysokou redundanci.

#### Hlavní nastavení při instalaci OS

- datum a čas, region, název počítače a uživatelské účty, jazyk, nastavení displeje, typ klávesnice, síť/připojení

#### Zabezpečení PC

- nastavení silného hesla, firewall (zamezuje neautorizovanou komunikaci), back-up (kopie důležitých dat), kryptování souborů, antivirus, VPN, ...

## [[Návrh HW a SW pro různé typy využití PC]]
####  Kancelářská práce

**Hardware:**
- Procesor (CPU): Intel Core i3 nebo AMD Ryzen 3
- Operační paměť (RAM): 8 GB
- Úložiště: 250 GB SSD (pro rychlý přístup k datům)
- Grafická karta (GPU): Integrovaná grafika (např. Intel UHD Graphics)
- Monitor: Full HD (1920x1080) s úhlopříčkou 21-24 palců
- Periferie: Kvalitní klávesnice a myš, případně tiskárna a skener
- Operační systém: Windows 10/11 nebo Linux (např. Ubuntu)
 
**Software:**
- Kancelářský balík: Microsoft Office 365 nebo LibreOffice
- E-mailový klient: Microsoft Outlook nebo Mozilla Thunderbird
- Prohlížeč: Google Chrome, Mozilla Firefox nebo Microsoft Edge
- Antivirus: Windows Defender nebo jiný antivirový program (např. Avast, Bitdefender)
- Další nástroje: PDF Reader (Adobe Acrobat Reader), nástroje pro správu úloh (Trello, Asana)

#### Práce v multimediálním grafickém studiu

**Hardware:**
- Procesor (CPU): Intel Core i7 nebo AMD Ryzen 7 (ideálně s více jádry a vyšším taktem)
- Operační paměť (RAM): 32 GB nebo více
- Úložiště: 1 TB SSD (pro rychlý přístup k datům) + 2 TB HDD (pro dlouhodobé ukládání)
- Grafická karta (GPU): NVIDIA GeForce RTX 3060 nebo AMD Radeon RX 6700 XT (pro práci s 3D grafikou a videem)
- Monitor: 4K rozlišení (3840x2160) s úhlopříčkou 27-32 palců a přesným podáním barev (např. Adobe RGB)
- Periferie: Grafický tablet (např. Wacom), kvalitní klávesnice a myš
- Operační systém: Windows 10/11 nebo macOS

**Software:**
- Grafický software: Adobe Creative Cloud (Photoshop, Illustrator, Premiere Pro, After Effects), CorelDRAW
- 3D modelování: Blender, Autodesk Maya, 3ds Max
- Video editace: DaVinci Resolve, Final Cut Pro (na macOS)
- Správa souborů: Adobe Bridge, Google Drive, Dropbox
- Antivirus: Windows Defender nebo jiný antivirový program (např. Avast, Bitdefender)

#### E-sport (hraní počítačových her na profesionální úrovni)

**Hardware:**
- Procesor (CPU): Intel Core i9 nebo AMD Ryzen 9 (pro maximální výkon)
- Operační paměť (RAM): 32 GB
- Úložiště: 1 TB NVMe SSD (pro rychlé načítání her a systému)
- Grafická karta (GPU): NVIDIA GeForce RTX 3080/3090 nebo AMD Radeon RX 6900 XT (pro vysoké fps a rozlišení)
- Monitor: 144Hz nebo vyšší obnovovací frekvence, Full HD nebo QHD (2560x1440), případně 4K pro high-end gaming
- Periferie: Mechanická klávesnice, herní myš s vysokým DPI, kvalitní sluchátka s mikrofonem
- Operační systém: Windows 10/11

**Software:**
- Herní platformy: Steam, Epic Games Store, Battle.net
- Komunikační nástroje: Discord, TeamSpeak
- Antivirus: Windows Defender nebo jiný antivirový program (např. Avast, Bitdefender)
- Optimalizační nástroje: MSI Afterburner (pro monitorování a přetaktování), Razer Cortex (pro optimalizaci výkonu)
- Streamovací software: OBS Studio, XSplit