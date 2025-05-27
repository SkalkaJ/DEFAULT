# 5. Práce s OS unixového typu

***Obsah otázky:*** Práce v příkazovém řádku, pohyb v souborovém systému, práce se soubory,  uživatelská práva, práce s procesy 

- práce buď v emulátoru terminálu nebo, pokud systém nemá GUI, tak přímo v TTY
- v CLI se vždy nacházíme v jedné složce
- pohyb v souborovém systému:
	- `pwd` - vypsat název aktuální složky
	- `ls` - vypsat soubory v aktuální složce (parametr `-a` pro zobrazení skrytých, `-l` pro výpis oprávnění, vlastníka...)
	- `cd <složka>` - přejít do jiné složky
	- `find` - rekurzivní výpis podsložek a souborů v současné složce
		- předáním výstupu pomocí `find | grep <hledaný text>` můžeme vyhledávat
- práce se soubory:
	- `touch` - vytvoření prázdného souboru
	- `echo "Text" > soubor.txt` - zápis do souboru (nahrazení)
	- `echo "Text" >> soubor.txt` - zápis do souboru (přidání)
	- `cat <soubor>` - vypsat obsah souboru
	- `cat <soubor1> <soubor2> ... <souborN> > <soubor>` - spojit N souborů a vypsat je do jednoho souboru
	- `rm <soubor>` - odstranění souboru
		- `rm -rf` - rekurzivní mazání (třeba složky)
	- `chmod <oprávnění> <soubor>` - změna oprávnění k souboru
		- zápis buď oktálový (3 číslice) nebo intuitivní <skupina>+-<oprávnění> (+x, go-rw)...
	- `chown <vlastník>:<skupina> <soubor>` - změna vlastníka a vlastnící skupiny
- práce s procesy:
	- `ps` - vypsat procesy v současném shellu
		- pokud běží aplikace, můžeme ji upozadit s Ctrl+Z a poté bude v tomto výpisu
		- vrátit se můžeme příkazem `fg`
	- `ps aux` - vypsat všechny procesy
	- `top` - průběžně aktualizovaný výpis seznamu procesů co na počítači běží
		- často nainstalovaná i nadstavba `htop` - textové uživatelské rozhraní, umožňuje ukončovat procesy
	- `kill <proces>` - ukončit proces
		- každý proces má PID (process ID)
		- pokud se proces neukončuje, můžeme udělat `kill -9 <proces>` - signál SIGKILL se moc nedoporučuje - možná ztráta dat
	- `pkill <název procesu>` - ukončit proces podle jeho názvu
- práce se sítí:
	- `ping <adresa>` - ozkoušení přístupu na nějaký server
	- `curl` - provedení HTTP požadavku
	- `ssh` - vzdálený přístup k CLI jiného serveru
- ostatní:
	- `sudo` - povýšení na administrátorské (root) oprávnění, uživatel musí mít povolení v `/etc/sudoers`
	- `shutdown` - vypnutí počítače
	- `reboot` - restart počítače
	- `logout` - odhlášení
	- `exit` - ukončení sezení shellu

# Práce s OS unixového typu – příkazový řádek, pohyb v souborovém systému, práce se soubory, uživatelská práva, práce s procesy

**Práce v příkazovém řádku (CLI)**

Unixové systémy (např. Linux, FreeBSD) se tradičně ovládají pomocí příkazového řádku (CLI – Command Line Interface), který umožňuje rychlou a efektivní práci se systémem[9](https://www.like-it.sk/cz/n/183/zaklady-prace-s-prikazovou-radkou-v-linuxu-a-unixu.html)[12](https://www.nuc.elf.stuba.sk/lit/ldp/01/010-04.HTM). Příkazový interpret (shell, např. bash) zobrazuje výzvu (prompt), kde uživatel zadává příkazy.

**Pohyb v souborovém systému**

Unixové systémy používají hierarchický souborový systém s kořenovým adresářem „/“[3](https://is.muni.cz/el/sci/podzim2014/C2110/um/C2110-Lesson-02_CZ006.pdf)[14](https://wiki.ubuntu.cz/z%C3%A1kladn%C3%AD_p%C5%99%C3%ADkazy). Základní příkazy pro pohyb:

- `pwd` – vypíše aktuální adresář.
    
- `ls` – vypíše obsah adresáře. Přepínače:
    
    - `ls -l` – podrobný výpis (včetně práv a vlastníka).
        
    - `ls -a` – zobrazení všech souborů včetně skrytých (začínajících tečkou).
        
    - `ls -F` – rozliší typy souborů (adresář `/`, spustitelný soubor `*`)[2](https://www.pslib.cz/milan.kerslager/Z%C3%A1kladn%C3%AD_p%C5%99%C3%ADkazy_Unixu)[14](https://wiki.ubuntu.cz/z%C3%A1kladn%C3%AD_p%C5%99%C3%ADkazy).
        
- `cd [adresář]` – změna aktuálního adresáře (např. `cd /home/uzivatel`).
    
- `cd ..` – přechod o úroveň výš.
    

**Práce se soubory**

Základní operace se soubory a adresáři:

- **Vytvoření souboru:** `touch soubor.txt` nebo `echo "text" > soubor.txt`
    
- **Zobrazení obsahu:** `cat soubor.txt` (pro větší soubory `less` nebo `more`)
    
- **Kopírování:** `cp zdroj cíl` (např. `cp soubor1.txt soubor2.txt`)
    
    - `cp -r adresar1 adresar2` – rekurzivní kopírování adresářů[2](https://www.pslib.cz/milan.kerslager/Z%C3%A1kladn%C3%AD_p%C5%99%C3%ADkazy_Unixu)[4](https://www.websupport.cz/podpora/kb/zaklady-prace-se-soubory-a-slozkami-v-linuxovem-prikazovem-radku/).
        
- **Přesun/přejmenování:** `mv starý_název nový_název` nebo `mv soubor1 adresar/`[3](https://is.muni.cz/el/sci/podzim2014/C2110/um/C2110-Lesson-02_CZ006.pdf).
    
- **Mazání:** `rm soubor.txt`
    
    - `rm -r adresar/` – rekurzivní mazání adresáře a jeho obsahu[3](https://is.muni.cz/el/sci/podzim2014/C2110/um/C2110-Lesson-02_CZ006.pdf).
        

**Uživatelská práva**

Unixové systémy jsou víceuživatelské a každý soubor/adresář má nastavená přístupová práva pro vlastníka (user), skupinu (group) a ostatní (others)[5](https://cs.wikipedia.org/wiki/P%C5%99%C3%ADstupov%C3%A1_pr%C3%A1va_v_Unixu)[10](https://www.pslib.cz/milan.kerslager/P%C5%99%C3%ADstupov%C3%A1_pr%C3%A1va_v_Linuxu). Oprávnění:

- **r** (read) – čtení
    
- **w** (write) – zápis
    
- **x** (execute) – spuštění souboru / vstup do adresáře
    

Zobrazení práv:  
`ls -l` vypíše práva ve formátu např. `-rwxr-xr--` (první trojice vlastník, druhá skupina, třetí ostatní)[5](https://cs.wikipedia.org/wiki/P%C5%99%C3%ADstupov%C3%A1_pr%C3%A1va_v_Unixu)[10](https://www.pslib.cz/milan.kerslager/P%C5%99%C3%ADstupov%C3%A1_pr%C3%A1va_v_Linuxu).

Změna práv:  
`chmod [práva] soubor`

- Symbolicky: `chmod u+x soubor.sh` (přidá spuštění vlastníkovi)
    
- Oktalově: `chmod 755 soubor.sh` (vlastník vše, ostatní čtení a spuštění)[5](https://cs.wikipedia.org/wiki/P%C5%99%C3%ADstupov%C3%A1_pr%C3%A1va_v_Unixu)[10](https://www.pslib.cz/milan.kerslager/P%C5%99%C3%ADstupov%C3%A1_pr%C3%A1va_v_Linuxu)
    

Změna vlastníka/skupiny:

- `chown uživatel soubor`
    
- `chgrp skupina soubor`
    

**Práce s procesy**

Proces je běžící instance programu. Unix umožňuje multitasking – více procesů najednou[13](https://www.kiv.zcu.cz/~safarikj/vyuka/os/prednasky/prednaska03.pdf)[15](http://phoenix.inf.upol.cz/~krajcap/courses/2023LS/OS1/tutorial09.pdf).

- **Zobrazení procesů:**
    
    - `ps` – vypíše procesy uživatele
        
    - `ps aux` – vypíše všechny procesy v systému[11](https://www.itnetwork.cz/linux/zaklady/linuxovy-terminal-bash-prace-s-procesy)[15](http://phoenix.inf.upol.cz/~krajcap/courses/2023LS/OS1/tutorial09.pdf)
        
    - `top` – interaktivní sledování běžících procesů (CPU, paměť)[7](https://www.guru99.com/cs/managing-processes-in-linux.html)[11](https://www.itnetwork.cz/linux/zaklady/linuxovy-terminal-bash-prace-s-procesy)
        
- **Spouštění procesů na pozadí:**
    
    - `program &` – spustí proces na pozadí
        
    - `jobs` – vypíše úlohy spuštěné z aktuálního shellu[8](https://people.ischool.berkeley.edu/~kevin/unix-tutorial/section12.html)[16](https://cs.wikipedia.org/wiki/%C5%98%C3%ADzen%C3%AD_%C3%BAloh_\(Unix\))
        
    - `fg %číslo` – přesune úlohu do popředí
        
    - `bg %číslo` – přesune úlohu na pozadí
        
- **Zastavení a ukončení procesu:**
    
    - `kill PID` – ukončí proces podle jeho ID (PID)[7](https://www.guru99.com/cs/managing-processes-in-linux.html)[11](https://www.itnetwork.cz/linux/zaklady/linuxovy-terminal-bash-prace-s-procesy)[8](https://people.ischool.berkeley.edu/~kevin/unix-tutorial/section12.html)
        
    - `kill -9 PID` – vynucené ukončení
        
    - `CTRL+C` – přerušení procesu v popředí
        
    - `CTRL+Z` – pozastavení procesu v popředí (lze obnovit `bg` nebo `fg`)[11](https://www.itnetwork.cz/linux/zaklady/linuxovy-terminal-bash-prace-s-procesy)
        
- **Priorita procesů:**
    
    - `nice -n hodnota příkaz` – spustí proces s danou prioritou
        
    - `renice hodnota -p PID` – změní prioritu běžícího procesu[7](https://www.guru99.com/cs/managing-processes-in-linux.html)