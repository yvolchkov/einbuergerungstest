# Anki Deck für den deutschen Einbürgerungstest (alle Bundesländer)

Dieses Skript scrapt die Fragen und Antworten für den deutschen Einbürgerungstest von http://oet.bamf.de/.
Die Daten werden in einer SQLite3-Datenbank gespeichert und anschließend exportiert, um sie mit Anki zu nutzen

- [Finales Anki-Deck auf AnkiWeb](https://ankiweb.net/shared/info/1428016787)
- [Finales Anki-Deck als .apkg herunterladen](https://github.com/ignamv/einbuergerungstest/releases)

## Nutzung

### Scraper

Installiere die benötigten Abhängigkeiten (aktuell nur Selenium):

```
pip install -r requirements.txt
```

Lade den [Geckodriver](https://github.com/mozilla/geckodriver/releases) herunter und führe das Skript
aus, wobei das Geckodriver-Verzeichnis im PATH enthalten sein muss, z. B.:

```
env PATH=$HOME/Downloads:$PATH python3 scrape.py
```

Wenn du unter Ubuntu einen Fehler über ein nicht zugängliches Profil erhältst,
versuche, ein temporäres Verzeichnis (TMPDIR) festzulegen:

```
mkdir tmp
env PATH=$HOME/Downloads:$PATH TMPDIR=./tmp python3 scrape.py
```

### Anki writer

Dieses Skript generiert eine CSV-Datei und ein Verzeichnis mit den Bildfragen:
```
python3 output.py
```

## Danksagungen

Vielen Dank an @nikste und @prepor für ihre Beiträge!
