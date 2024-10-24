**Automatisierung** ermöglicht es, wiederkehrende Aufgaben durch die Verwendung von Skripten und Shells zu automatisieren, ohne dass manuelle Eingriffe erforderlich sind. Dies spart Zeit, reduziert Fehler und sorgt für eine konsistente Ausführung von Prozessen.

# Verwendung von Skripten
Ein **Skript** ist eine Datei, die eine Reihe von Anweisungen oder Befehlen enthält, die automatisch nacheinander ausgeführt werden. Skripte werden häufig verwendet, um Aufgaben wie das Kopieren von Dateien, das Ausführen von Tests oder das Verwalten von Diensten zu automatisieren. 

Anwendungsbeispiele:
- Backup von Dateien erstellen
- Automatisiertes Deployment von Anwendungen
- Regelmäßiges Monitoring von Systemressourcen

# Systemabhängige Bordmittel 
Eine **Shell** ist eine Benutzerschnittstelle zum Betriebssystem, die verwendet wird, um Befehle einzugeben und Programme auszuführen. Shells wie die **Bash** (unter Linux) oder die **PowerShell** (unter Windows) sind mächtige Werkzeuge, um über die Kommandozeile auf Betriebssystemfunktionen zuzugreifen. In der Shell können Skripte direkt ausgeführt werden, um eine Vielzahl von Aufgaben zu automatisieren.

# Python-Skript
Hier ist ein einfaches Python-Skript, das alle Dateien vom **Desktop** und aus dem **Downloads**-Ordner in einen Ordner namens **Stuff** verschiebt. Falls der **Stuff**-Ordner noch nicht existiert, wird er automatisch erstellt:

```python
import os
import shutil

# Pfade zu Desktop und Downloads
desktop = os.path.join(os.path.expanduser("~"), "Desktop")
downloads = os.path.join(os.path.expanduser("~"), "Downloads")

# Pfad zum Zielordner "Stuff"
stuff_folder = os.path.join(os.path.expanduser("~"), "Stuff")

# Funktion zum Verschieben von Dateien in den "Stuff"-Ordner
def move_files_to_stuff(folder_path, stuff_folder):
    os.makedirs(stuff_folder, exist_ok=True)  
    for file_name in os.listdir(folder_path):
        file_path = os.path.join(folder_path, file_name)
        if os.path.isfile(file_path):  
            shutil.move(file_path, os.path.join(stuff_folder, file_name))

move_files_to_stuff(desktop, stuff_folder)
move_files_to_stuff(downloads, stuff_folder)

print("Alle Dateien wurden in den 'Stuff'-Ordner verschoben.")
```
