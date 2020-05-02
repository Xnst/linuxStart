% Linux and bash



# filsystemet: De viktigaste katalogerna:

	/dev   - "devices" allt som �r inkopplat hamnar h�r
	/etc   - configfiler f�r OSets program, default
	/home  - anv�darnas hemkataloger
	/media - ofta monteringspunkt under respektive anv�ndare n�r tex
	         usb kopplas in
	/opt   - ofta f�r externa program som installeras
	/proc  - "processerna" syns som filer
	/usr   - i stort sett alla program
	         /usr/bin - n�stan alla program
			 /usr/share - programmens kataloger med det de beh�ver
	/var   - om programmen g�r t.ex. filer hamnar det ofta h�r


# Anv�ndarna

## root

- kan allt!
- kan f�rst�ra allt!

## user

- kan bara f�rst�ra f�r sig sj�lv

_**S� n�r programmet fr�gar efter l�senordet s� ger du maskinen
root-r�ttigheter och programmet kan f�rst�ra allt**_
## group

Allt och alla tillh�r minst en grupp. Kolla i filen */etc/group*

## r�ttigheter

Med ls p� l�ngt format f�s alla r�ttigheter, �gare osv

    ls -l
	-rw-r--r-- 1 niclas niclas 7,7K feb 19 11:06 /home/niclas/.bashrc

den f�rsta biten visar :

|- |rw-|r--|r--| 1 | niclas | niclas |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| typ | �garr�tt | gruppr�tt | allas r�tt | - | �gare | grupp |
|  -  |  r = read | w = write | x = execute | - | - | - |





# struktur

<cmd> [-ihfxert] [var] [fil]

- wildcards funkar
	- ls w* / ls w[0-9] / ls w?

- "osynliga" filer b�rjar med en punkt: ex. .bashrc
- ~/ = hemkatalogen
- ./ = katalogen du befinner dig i
- ../ = katalogen ett steg ner

## tabbning

bash l�ter dig *tabba* dig fram.

    cd wer<TAB>

g�r att werther fylls i, eller om flera wer* finns h�nder ingenting om
du inte sl�r TAB igen, d� skrivs alla m�jligheter ut.

## Case sensitive

file.txt $\ne$ File.txt


# K�ra i terminalens bakgrund

s�tt ett \& efter kommandot. Bra n�r GUI-program startas

    emacs&


# Osynliga filer och kataloger ofta config-saker

Kolla hemkatalogen med ls -a.


## .bashrc och .profile

L�ses n�r man loggar in. H�r s�tts variabler och annat bra att ha.
i .bashrc s�tts g�rna aliases och prompt

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


