### Hinweis
Wir empfehlen die Nutzung des Ordners _opt_ jedoch ist das die frei Wahl jedermanns.
Innerhalb der Dokumentation bedienen wir uns der einfachheitshalber an Beispielen, die innerhalb des _opt_ Ordner stattfinden.

### Vorbereitung

Zuerst muss ein Ordner innerhalb des Ordner _opt_ erstellt werden. Der Ordnername lautet
_TrafficHandler_

`mkdir TrafficHandler`

Im Folgenden laden Sie das aus dem GitHub-Repository das Release Paket herunter.
Das kann mittels der Downloadfunktion der Webseite realisiert werden, als auch auf dem Server mittels cUrl.

Wechseln Sie zuerst ins angelegte Verzeichnis:

`cd /opt/TrafficHandler`

Führen Sie nun den cUrl Befehl aus.

_Bitte achten Sie auf die Version innerhalb des Links!_

`curl -LO https://github.com/muffti-112/Traffic-Handler-Docker/releases/download/0.5.0-Beta/traffichandler-docker.tar
`

Entpacken Sie nun das im Verzeichnis befindliche _traffichandler-docker.tar_

`tar -xvf traffichandler-docker.tar`

### Start des Systems

Damit wäre das System fertig und bereit zum starten. Hierzu folgenden Befehl ausführen.

`docker-compose up -d`

Wir empfehlen vor dem Start die Konfiguration des Systems. Diese finden Sie auf der Seite Konfigurationen. 