## Erste Konfiguration

Der TrafficHandler kann entsprechend Konfiguriert werden.

Hierzu befindet sich im folgenden Verzeichnis

`opt/TrafficHandler/traffic_handler/conf` 

eine _settings.cfg_ Datei.

Diese sieht im Standard wie folgt aus:

``` 
#ERR-Fire Traffic Handler Settings

#SSL
#To enable an encrypted connection via SSL, the application requires a certificate and key.
#Please enter here the full name for cert and key e.g. server.key and server.crt
useSSL ="True"

cert = "certification/server.crt"
key = "certification/server.key"

#Host IP or FQDN
host = "0.0.0.0"

# SSL Port. Default HTTPS-Port is 443
# If useSSL is of "False" please use unsecure Port, like 80, 8181 ...
port = "443"

#Customized

#Add here Youre City- or Instancename.
city= "Deine Stadt" 

#Active here the login with password and username. If the value should stand on False, then to OAuth authentication is changed.
#The OAuth must be configured below.

LOGINBASIC= "True"
```

<br>

#### useSSL
_Default = true_

Hier kann die verschlüsselte Kommunikation aktiviert werden. Dafür ist innerhalb des Images ein SelfSign Zertifikat hinterlegt.
Dies kann prinzipell ausgetauscht werden, hierzu ist jedoch Wissen im Bereich Docker erforderlich.

#### host
_Default = 0.0.0.0_

Hier kann die IP-Adresse oder der Hostname des System eingetragen werden.


#### port
_Default = 443_

Hier kann ein Port definiert werden, worauf dann die Anwendung kommuniziert.
Soll der Port 80 oder 443 nicht genutzt werden, so muss ebenfalls die  `docker-compose.yml` angepasst werden. 
Hier muss innerhalb der ports der entsprechend neue Port definiert werden.

⚠️ Sollte die Server Firewall aktiv sein, sorgen Sie dafür, dass die entsprechenden Ports auch nach außen zugänglich sind.

#### city
_Default = Deine Stadt_

Hier kann ein Stadtname oder anderweitige Namen eingetragen werden. Diese werden im Login-Screen angezeigt, als auch im Footer
und auf der Systemseite. So kann man bei mehreren Systemen, diese direkt voneinander unterscheiden.

#### LOGINBASIC
_Default = True_

Hierrüber wird die Login Methode ausgewählt. Der TrafficHandler kann sowohl Authentifizierung über Benuterzname und Passwort, als auch über ein IAM-System (Identity & Access Management)
angebunden werden. Die Anbindung ans IAM setzt Fachwissen voraus. Innerhalb dieser Dokumentation, wird dies nicht explizit erklärt.

## Troubleshooting

### Logs
Bei besonderen Ereignissen innerhalb der Anwendung, werden Logeinträge erstellt.
Diese werden in einem _main.log_ festgehalten. Das Logfile wird im Standard aus dem Container rauskopiert und auf dem Server Lokal gespeichert.

Für Benutzer mit der Rolle ADMIN, steht innerhalb der Anwednung ein Ereignisprotokoll zur Verfügung. Somit ist kein Zugang zum Server zwingend erforderlich.

Das Logfile finden Sie lokal im folgenden Verzeichnisse

`opt/TrafficHandler/traffic_handler/logs` 

### Datenbank
Die Daten, welche über die Webseite aufrufbar sind, werden in einer lokalen Datenbank gespeichert.
Es handelt sich hierbei um eine SQLite Datenbank. Diese wird im Standard aus dem Container rauskopiert und auf dem Server Lokal gespeichert.

Die Datenbank finden Sie lokal im folgenden Verzeichnisse

`opt/TrafficHandler/traffic_handler/database` 