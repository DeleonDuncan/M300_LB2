# M300_LB2

# Einrichten der Umgebung

## Kriterien 1:

    1. Vagrant
    2. Visualstudio-Code
    3. Git-Client
    4. SSH-Key für GitHub  


### 1. Vagrant

Vagrant Version nach der installation:

      C:\Users\DeleonDuncan vagrant -v\
      Vagrant 2.2.3


### 2. Visualstudio-Code

Visual Studio wurde mit folgenden Extensions installiert.

  * Markdwon All in one
  * Vagrantfile Support
  * vscode-pdf
  


### 3. Git-Client

      AzureAD+DeleonDuncan@LAPTOP-JHJOJMAF MINGW64 ~
      $ git --version
      git version 2.20.1.windows.1



### 4. SSH-Key für Client erstellt
    
      SSH M300
      0a:5e:1f:93:f6:a5:e7:ea:18:35:64:2b:ca:2c:19:c0 
      Added on 18 Feb 2019 Last used within the last week — Read/write
      



<br></br>

## Kriterien 2:
      
     1. Github Account erstellt
     2. Git-Client verwendet
     3. Dokumentation als Mark Down vorhanden
     4. Persönlicher Wissenstand
     5. Wichtige Lernschritte
     

### 1. GitHub Account erstellt

![GitHub DeleonDuncan](https://github.com/deleonduncan)


### 2. Git-Client verwendet

Als Beispiel habe ich eine VM gestartet mit *Vagrant Up* in der Git Bash

      AzureAD+DeleonDuncan@LAPTOP-JHJOJMAF MINGW64 ~/Documents/TBZ/M.300/Vagrant
      $ vagrant up
      Bringing machine 'default' up with 'virtualbox' provider...
      ==> default: Checking if box 'ubuntu/xenial64' version '20190215.0.0' is up to date...
      ==> default: A newer version of the box 'ubuntu/xenial64' for provider 'virtualbox' is
      ==> default: available! You currently have version '20190215.0.0'. The latest is version
      ==> default: '20190221.0.0'. Run `vagrant box update` to update.
      ==> default: Clearing any previously set forwarded ports...
      ==> default: Clearing any previously set network interfaces...
      ==> default: Preparing network interfaces based on configuration...
          default: Adapter 1: nat
      ==> default: Forwarding ports...
          default: 22 (guest) => 2222 (host) (adapter 1)
      ==> default: Running 'pre-boot' VM customizations...
      ==> default: Booting VM...
      ==> default: Waiting for machine to boot. This may take a few minutes...
          default: SSH address: 127.0.0.1:2222
          default: SSH username: vagrant
          default: SSH auth method: private key
      ==> default: Machine booted and ready!
      ==> default: Checking for guest additions in VM...
          default: The guest additions on this VM do not match the installed version of
          default: VirtualBox! In most cases this is fine, but in rare cases it can
          default: prevent things such as shared folders from working properly. If you see
          default: shared folder errors, please make sure the guest additions within the
          default: virtual machine match the version of VirtualBox you have installed on
          default: your host and reload your VM.
          default:
          default: Guest Additions Version: 5.2.8_KernelUbuntu r120774
          default: VirtualBox Version: 6.0
      ==> default: Mounting shared folders...
          default: /vagrant => C:/Users/DeleonDuncan/Documents/TBZ/M.300/Vagrant
      ==> default: Machine already provisioned. Run `vagrant provision` or use the `--provision`
      ==> default: flag to force provisioning. Provisioners marked to run always will still run.

Anschliessend habe ich sie wieder mit *Vagrant Destory* zerstört

      AzureAD+DeleonDuncan@LAPTOP-JHJOJMAF MINGW64 ~/Documents/TBZ/M.300/Vagrant
      $ vagrant destroy
          default: Are you sure you want to destroy the 'default' VM? [y/N] y
      ==> default: Forcing shutdown of VM...
      ==> default: Destroying VM and associated drives...


### 3. Dokumentation als Markdown
 
Ich habe keinen Makrdown editor benutzt, sondern sondern direkt die README.md datei editiert. Diese Dokumentation sollte als Beweis ausreichen, dass ich sie in Markdown geschrieben habe.


### 4. Persönlicher Wissenstand

Themen            | Wissen
----------------- | -------------
Vagrant           | Vor diesem Modul kannte ich Vagrant noch nicht. VM's habe ich bisher immer Manuel aufgesetzt
VirtualBox        | Ich kannte VirtualBox als hypervisor. Ich wusste das es Open-Source ist. Trotzdem habe ich vorher immer VMWare             Workstation benutzt
VisualStudio-Code | Ich kannte und bentutze VSCode bereits als Editor. Vor allem wegen den Extensions finde ich ihn extrem mächtig. Man kann am einen Tag Powershell und am anderen mit Python ohne probleme, und mit Syntax Highlighting arbeiten.
Git-Client        | Git Client kannte ich vor diesem Modul, und ich hatte es auch schon mal installiert. Jedoch habe ich es nie aktiv genutzt.
SSH Keys          | Mit SSh-Keys habe ich schon im Geschäft zu tun gehabt. Sie sind etwas komplett vertrautes.


### 5. Wichtige Lernschritte

Vagrant:
        
		Wie schon erwähnt habe ich VM's immer Manuell aufgesetzt. 
		Nun da ich vagrant kenne, weiss ich dass es einen viel schnelleren Weg gibt. 
		Ich war überrascht, dass man mit einem File, dem *Vagrantfile*, eine VM mit der kompletten
		konfiguration starten und so schnell wieder zerströren kann. 
		Meiner Meinung nach ist das für Testfälle perfekt.
		

Git-Client:

		Ich habe Git-Client testweise schon benutzt. Aber ich fand
		es damals eher verwirrend mit dem Git Repo, dem Lokalen Repo, den commits,
		pulls oder dem origin master. Mittlerweile verstehe ich es recht gut,
		und die Verwaltung, ist nicht mehr so schwer wie auch schon.


<br></br>


## Kriterien 3:

	1. Bestehende VM aus Vagrant-Cloud einrichten
	2. Kennt die Vagrant Befehle
	3. Eingerichtete Umgebung ist Dokumentiert
	4. andere Vorgefertigte VM eingerichtet
	5. Projekt mit Git und Markdown dokumentiert
	


### 1. Bestehende VM aus Vagrant-Cloud einrichten

Ins Verzeichnis lam gewechselt, die VM gestartet

	vagrant up 


### 2. Kennt die Vagrant Befehle

Befehl            | Funktion
----------------- | -------------
vagrant up 	  | Startet vagrant Umgebung
vagrant resume    | Setzt eine suspendierte Maschine fort.
vagrant reload    | Startet die VM neu, liest das Config File neu ein
vagrant ssh       | Verbinden zu einer Maschine via SSH
vagrant halt      | Stopt die vagrant Maschine
vagrant suspend   | suspendiert eine VM
vagrant destroy   | Stopt und löscht die gesamte VM
vagrant -v        | Zeigt die vagrant Version an
vagrant status    | Gibt den Stataus einer VM aus.


### 3. Eingerichtete Umgebung ist Dokumentiert

In der Umgebung lam haben wir

* Web Server mit Apache und MySQL UserInterface Adminer
* Datenbank Server mit MySQL
* Die Verbindung Web - Datenbank erfolgt mittels Internen Netzwerk Adapter.
* Von Aussen ist nur der HTTP Port auf dem Web Server Erreichbar.

### 4. andere Vorgefertigte VM eingerichtet

	WebServer ist unter 192.168.55.101:80 erreichbar. Nicht mit Port 8080

	MySQL Server ist unter localhost:8080/adminer.php erreichbar.
	
	Mittels:
	Serveradresse 192.168.55.100 
	User:root 
	Passwort:admin 
	kann man sich einloggen.


### 5. Mittels Git & Markdown Dokumentiert

	Wie man sieht, habe ich das entsprechend dokumentiert.
	
	



## Kriterien 4:

	1. Firewall eingerichtet
	2. Reverse Proxy eingerichtet
	3. Zugang mit SSH-Tunnel abgesichert
	4. Sicherheitsmassnahmen sind dokumentiert.
	5. Testfälle
	
### 1. Firewall eingerichtet

	Firewall mit Vagrant up gestartet.
	
	Nach unsicherem SSH Key konnte ich mit : *Vagrant up --provision die VM neu laden
	
	Firewall Config:
	root@master:/etc/ufw# ufw status
	Status: active

	To                         Action      From
	--                         ------      ----
	22/tcp                     ALLOW       Anywhere
	80                         ALLOW       192.168.55.101
	22/tcp (v6)                ALLOW       Anywhere (v6)

	
### 2. Reverse Proxy eingerichtet	

	root@web01:/etc/apache2/sites-available# cat 001-reverseproxy.conf
	# Allgemeine Proxy Einstellungen
	ProxyRequests Off
	<Proxy *>
	      Order deny,allow
	      Allow from all
	</Proxy>

	# Weiterleitungen master
	ProxyPass /master http://master
	ProxyPassReverse /master http://master
	root@web01:/etc/apache2/sites-available#



### 3. Zugang mit SSH Tunnel abgesichert

	Ja
	

### 4. Sicherheitsmassnahmen sind dokumentiert

- [x] Firewall ist aktiv und regeln sind gesetzt.
- [x] Reverse Proxy läuft
- [x] Per SSH Tunnel abgesichert

### 5. Testfälle

Test 				| 		Soll 		| 		Ist		    | Analyse
------------------------------------------------------------------------------------------------------------------
Von Web Server, curl auf master | Der Webserver soll auf den 	| Der Webserver kann auf den Master | OK
				| Master zugreifen können.	| zugreifen.			    |
				|				|				    |
Von Web Server, curl auf DB	| Webserver sollte zugreifen 	| Webserver kann zugreifen.	    | OK
				| können.			|				    |
				|				|				    |
Von DB auf Master zugreifen	| Soll nicht zugreifen können.  | Kann nicht zugreifen.		    | OK
				|				|				    |
				|				|				    |
Von Master auf DB zugreifen	| Soll nicht zugreifen können.  | Kann nicht zugreifen.		    | OK

