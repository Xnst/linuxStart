% Linuxintroduktion
% Niclas Stenberg
% niclas@nist.se



# Hur installerar jag program?

- "programvara"
- synaptic
- apt
- hämta källkod och kompilera
- snap
- flatpack
- appImage
- docker


# Programmen som finns

FOSS(Free and Open Source Software) 

- "betalar" genom att:
	- donera pengar
	- rapportera buggar
	- prata om det
	- använda det
	- hjälpa till at skriva kod
	- hjälpa till at skriva dokumentation
	- skriva program runt

De som betalar lönen till utvecklarna gör det för att de tjänar på
det.

# Hur vet jag vilka program som är bra?

- kort: internet
- sök efter funktion och lägg till "gpl"
- utbyteslistor:
	- https://alternativeto.net/platform/linux/


# Desktop och exempel på distro som använder

- gnome (ubuntu eller gnome-ubuntu)
- KDE (kubuntu)
- Xfce4 (xubuntu)
- Cinnamon (linux-mint)
- Mate (ubuntu mate)
- Openbox (Ubuntu Openbox)
- budgie (solus, budgieubuntu)
- pop!_OS (by system 76)
- pantheon (elementary os)

Typ alla funkar på ubuntu dock finns de såklart på andra bas OS också

# Köra windowsprogram på linux

- kolla om det går:
	- https://appdb.winehq.org/
- eller bara prova!
- PlayOnLinux 
- Lutris
- CodeWeaver (commercial)

kör med:

    wine program

# ssh client

    ssh [user@]server
	scp fil.txt  [user@]server:~/

nycklar

    ssh-keygen
	ssh-copy-id  [user@]server



# ssh server

kolla config-filen

    /etc/ssh/ssh_config
	
Kolla

    X11Forward
	passwordAuthentification


