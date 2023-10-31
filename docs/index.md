# Traffic Handler Docker

## BETA Version! Bitte aktuell nur zu Testzwecken nutzen. Nicht Produktiv schalten.
⚠️ Bitte bachte das es sich um eine BETA-Version handelt. Wir empfehlen die Nutzung  einer VPN-Verbindung.

## Informationen
Das Ziel des Projekts ist es, das Fortschreiten der Digitalisierung im Feuerwehr- und Rettungswesen zu unterstützen. Besonders im Fokus stehen dabei kleine Einheiten, für die verfügbare Lösungen finanziell nicht tragbar sind. Die Software wird kostenlos zur Verfügung gestellt und läuft auf bestehender oder günstiger Hardware.

 

Der Traffic Handler von ERR-Fire verkörpert ein innovatives System, das dazu konzipiert ist, Verkehrsbeeinträchtigungen, langfristige Baustellen und vergleichbare Hindernisse zu erfassen und transparent darzustellen. Durch die umfassende Dokumentation dieser Faktoren ermöglicht das System eine optimierte Routenplanung bereits im Vorfeld der Anfahrt zur Einsatzstelle. Ein essentieller Aspekt dieses Systems ist die Benutzerverwaltung, welche eine präzise Steuerung der Zugriffsrechte ermöglicht. Diese differenzierten Berechtigungen erlauben es, einzelnen Nutzern spezifische Schreib- oder ausschließlich Leserechte zuzuweisen. Hierdurch wird die Integrität der hinterlegten Daten gewährleistet und ein Höchstmaß an Sicherheit erreicht.

Die Daten werden zentral in einer lokalen Datenbank gespeichert, wodurch Ihnen uneingeschränkte Kontrolle über Ihre Daten gewährt wird.

## Struktur

Das Projekt bildet drei Strukturen.
Einmal die API als eine Struktur, welche in Zukunft für weitere Dienste Schnittstellen bereitstellt.

Die zweite Struktur bildet das Backend, welches die Endpunkte pro Service als auch die Logik innehat.

Die dritte und letzte Struktur ist das Webfrontend.

![Die Struktur](../img/struktur.png)