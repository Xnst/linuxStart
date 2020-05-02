% Linux and bash



# filsystemet: De viktigaste katalogerna:

	/dev   - "devices" allt som är inkopplat hamnar här
	/etc   - configfiler för OSets program, default
	/home  - anvädarnas hemkataloger
	/media - ofta monteringspunkt under respektive användare när tex
	         usb kopplas in
	/opt   - ofta för externa program som installeras
	/proc  - "processerna" syns som filer
	/usr   - i stort sett alla program
	         /usr/bin - nästan alla program
			 /usr/share - programmens kataloger med det de behöver
	/var   - om programmen gör t.ex. filer hamnar det ofta här


# Användarna

## root

- kan allt!
- kan förstöra allt!

## user

- kan bara förstöra för sig själv

_**Så när programmet frågar efter lösenordet så ger du maskinen
root-rättigheter och programmet kan förstöra allt**_
## group

Allt och alla tillhör minst en grupp. Kolla i filen */etc/group*

## rättigheter

Med ls på långt format fås alla rättigheter, ägare osv

    ls -l
	-rw-r--r-- 1 niclas niclas 7,7K feb 19 11:06 /home/niclas/.bashrc

den första biten visar :

|- |rw-|r--|r--| 1 | niclas | niclas |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| typ | ägarrätt | grupprätt | allas rätt | - | ägare | grupp |
|  -  |  r = read | w = write | x = execute | - | - | - |





# struktur

<cmd> [-ihfxert] [var] [fil]

- wildcards funkar
	- ls w* / ls w[0-9] / ls w?

- "osynliga" filer börjar med en punkt: ex. .bashrc
- ~/ = hemkatalogen
- ./ = katalogen du befinner dig i
- ../ = katalogen ett steg ner

## tabbning

bash låter dig *tabba* dig fram.

    cd wer<TAB>

gör att werther fylls i, eller om flera wer* finns händer ingenting om
du inte slår TAB igen, då skrivs alla möjligheter ut.

## Case sensitive

file.txt $\ne$ File.txt


# Köra i terminalens bakgrund

sätt ett \& efter kommandot. Bra när GUI-program startas

    emacs&


# Osynliga filer och kataloger ofta config-saker

Kolla hemkatalogen med ls -a.


## .bashrc och .profile

Läses när man loggar in. Här sätts variabler och annat bra att ha.
i .bashrc sätts gärna aliases och prompt

    alias ls='ls -Fh --color=auto'
    alias l='ls -lFh --color=auto'
    alias la='ls -alFh --color=auto'
    alias lrt='ls -lrtFh --color=auto'
	alias lrs='ls -lrSFh --color=auto'
	alias lsd='ls -lrtFh|grep /'

	alias cd..='cd ..'
	alias cd-='cd -'
	alias df='df -h'
	alias hi='history'
	alias py='python3'


