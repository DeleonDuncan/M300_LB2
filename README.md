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

Test 			| Analyse
------------------------------- | --------
Webserver kann curl auf master machen. | OK
Webserver kann curl auf DB machen.     | OK
DB kann nicht auf master zugreifen     | OK
Master kann nicht auf DB zugreifen     | OK



# Modul 300-LB2  MySQL & Nextcloud mit Einbindung von Webmin

## MySQL & Nextcloud

vagrantfile:

Das standard Passwort für die Vagrant vm ist: p/w vagrant/vagrant

	Vagrant.configure("2") do |config|

	  config.vm.box = "ubuntu/xenial64"

	  # Creates a public network, which generally matches the bridged network.
	  # config.vm.network "public_network"
	  config.vm.network "private_network", ip:"192.168.10.101" 
	  config.vm.network "forwarded_port", guest:8080, host:8080, auto_correct: true

	  # Share an additional folder to the guest VM.
	  # config.vm.synced_folder "../data", "/vagrant_data"

	  config.vm.provider "virtualbox" do |vb|
	     vb.memory = "2048"
	  end

	  # Docker Provisioner
	  config.vm.provision "docker" do |d|
	   d.pull_images "mysql"
	   d.pull_images "nextcloud"
	   d.run "nextcloud_mysql", image: "mysql", args: "-e MYSQL_ROOT_PASSWORD=admin -e MYSQL_USER=nextcloud -e MYSQL_PASSWORD=admin -e MYSQL_DATABASE=nextcloud --restart=always"
	   d.run "nextcloud", image: "nextcloud", args: "--link nextcloud_mysql:mysql -p 8080:80 --restart=always"
	  end
	end
	


Zuerst setze ich die VM und das Netzwerk auf.
	
	config.vm.box = "ubuntu/xenial64"

	config.vm.network "private_network", ip:"192.168.10.101" 
	config.vm.network "forwarded_port", guest:8080, host:8080, auto_correct: true


Ich verwende zwei Images.

	d.pull_images "mysql"
	d.pull_images "nextcloud"

Anschliessend führen wir MySQL mit folgednen Parameter aus:

* MYSQL_ROOT_PASSWORD=admin
* MYSQL_USER=nextcloud
* MYSQL_PASSWORD=admin
* MYSQL_DATABASE=nextcloud

Für Nextcloud werden folgende Parameter verwendet:


* --link nextcloud_mysql:mysql
* -p 8080:80
* --restart=always


## Webmin

Webmin ist eine webbasierte Schnittstelle zur Systemadministration für Unix. Mit jedem modernen Webbrowser können Sie Benutzerkonten, Apache, DNS, File Sharing und vieles mehr einrichten. Webmin macht es überflüssig, Unix-Konfigurationsdateien wie /etc/passwd manuell zu bearbeiten, und lässt Sie ein System von der Konsole aus oder aus der Ferne verwalten.


Zuerst müssen wir das Webmin Repository hinzufügen, sodass wir über unseren Packet Manager Webmin installieren können.

Wir öffnen diese File mit Vim, stelle fest, dass man es editieren kann.(Berechtigung)

    sudo vim /etc/apt/sources.list

Dann ergänzen wir diese URL zu unterst in diesem File
    /etc/apt/sources.list

    . . . 
    deb http://download.webmin.com/download/repository sarge contrib


Speichere das File und schliesse Vim

Zunächst müssen wir diesen GPG Key hinzutügen, dass unser System dem Repository vertraut

    wget http://www.webmin.com/jcameron-key.asc
    sudo apt-key add jcameron-key.asc

Dann updaten wir den Package Manager dass er das neue Repository hat

    sudo apt update 

Dann installieren wir Web:

    sudo apt install webmin 

Wenn die installation Fertig ist, haben wir diesen Output:

	Webmin install complete. You can now login to 
	https://your_server_ip:10000 as root with your 
	root password, or as any user who can use `sudo`.
	
	
