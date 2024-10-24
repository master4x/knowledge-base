Remotezugriff ermöglicht es, von einem entfernten Standort aus auf einen Computer oder Server zuzugreifen, um diesen zu verwalten oder zu steuern. Es gibt verschiedene Methoden, die entweder auf der Kommandozeile basieren oder eine grafische Benutzeroberfläche (GUI) verwenden.

# Kommandobasierter Remotezugriff
## SSH (Secure Shell)
- **SSH** ist ein Protokoll, das eine verschlüsselte Verbindung zu einem entfernten Rechner ermöglicht. Es wird häufig verwendet, um Server über die Kommandozeile zu verwalten.
- SSH bietet **Authentifizierung** durch Passwörter oder Public-Key-Verfahren und gewährleistet eine sichere Kommunikation, da der gesamte Datenverkehr verschlüsselt wird.
- Neben der Ausführung von Befehlen bietet SSH auch **Port-Forwarding** und **Dateiübertragung** (z. B. via SCP oder SFTP).

## Telnet
- **Telnet** ist ein älteres Protokoll, das ebenfalls den Zugriff auf entfernte Systeme ermöglicht, jedoch **keine Verschlüsselung** bietet.
- Es wird meist nur noch für **Netzwerktests** oder auf Geräten verwendet, die kein SSH unterstützen. Aufgrund der fehlenden Sicherheit ist Telnet für moderne Anwendungen ungeeignet.

| Merkmal           | SSH                                   | Telnet                    |
|-------------------|---------------------------------------|---------------------------|
| **Sicherheit**     | Verschlüsselte Verbindung             | Keine Verschlüsselung      |
| **Authentifizierung** | Public-Key und Passwort-basiert     | Nur Passwort-basiert       |
| **Port**           | 22                                   | 23                        |

# GUI-basierter Remotezugriff (Remote-Desktop)
## RDP (Remote Desktop Protocol)
- **RDP** ist ein von Microsoft entwickeltes Protokoll, das einen grafischen Zugriff auf einen entfernten Rechner ermöglicht. Es wird hauptsächlich auf **Windows-Systemen** verwendet und bietet die Möglichkeit, den Desktop des entfernten Rechners zu sehen und zu steuern.
- RDP unterstützt auch **verschlüsselte Verbindungen** und bietet zusätzliche Funktionen wie **Dateiübertragung**, **Druckerweiterleitung** und **Zwischenablagenfreigabe**.

## VNC (Virtual Network Computing)
- **VNC** ist eine plattformunabhängige Methode, um entfernte Systeme über eine grafische Oberfläche zu steuern. Es überträgt die Bildschirmdarstellung von einem Rechner zu einem anderen und ermöglicht die Interaktion mit Maus und Tastatur.
- VNC bietet keine **native Verschlüsselung**, allerdings kann es mit anderen Sicherheitsprotokollen wie SSH kombiniert werden, um die Verbindung abzusichern.

| Merkmal        | RDP                                 | VNC                                             |
| -------------- | ----------------------------------- | ----------------------------------------------- |
| **Plattform**  | Windows (nativ)                     | Plattformunabhängig                             |
| **Sicherheit** | Verschlüsselte Verbindung           | Keine native Verschlüsselung, SSH möglich       |
| **Funktionen** | Dateifreigabe, Druckerweiterleitung | Bildschirmfreigabe, Maus- und Tastaturkontrolle |
| **Nutzung**    | Admin- und Desktopzugriff           | Desktopzugriff                                  |
### TeamViewer
- **TeamViewer** ist eine kommerzielle Lösung für den Remotezugriff und die Fernwartung, die auf vielen Betriebssystemen verfügbar ist. Es ermöglicht den grafischen Zugriff auf entfernte Rechner und bietet zusätzlich **Chat**, **Dateiübertragung**, **VPN**-Funktionen und Sitzungsaufzeichnungen.
- TeamViewer verwendet **Ende-zu-Ende-Verschlüsselung** und ist besonders einfach in der Nutzung, da keine komplexen Netzwerkkonfigurationen notwendig sind.
