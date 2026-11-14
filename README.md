# Eigene Apps – Downloads

Fertige Pakete einiger meiner Programme für macOS und Linux. Der Quelltext liegt nicht hier.

| App | Was | Neueste Version |
|---|---|---|
| **Michi** 道 | Strecken für Laufen und Rad planen, Garmin-Export, Trainingsplan | [Releases](../../releases?q=michi) |

## Installieren

**macOS (11 oder neuer, Apple Silicon und Intel):** `.dmg` öffnen und die App in „Programme“ ziehen.
Die Apps sind nicht von Apple beglaubigt. Beim ersten Start deshalb: Rechtsklick auf die App → Öffnen. Auf neuerem
macOS einmal öffnen, dann Systemeinstellungen → Datenschutz & Sicherheit → „Trotzdem öffnen“.

**Linux (x86_64):** `.AppImage` ausführbar machen (`chmod +x`) und starten, oder das `.deb` installieren
(`sudo apt install ./michi_*.deb`, ab Ubuntu 22.04 bzw. Debian 12).

## Updates

Die Apps fragen beim ersten Start, ob sie nach neuen Versionen suchen sollen. Wenn ja, laden sie höchstens einmal
am Tag `<app>/latest.json` aus diesem Repo, ohne Kennung. Installiert wird erst nach einem Klick und nur, wenn die
Unterschrift zum Schlüssel passt, der in der App eingebaut ist (Tauri-Updater, minisign). Die Unterschrift ist an die
Versionsnummer gebunden; eine ältere Version lässt sich nicht als neue ausgeben.

## Prüfen

Jedes Release enthält `SHA256SUMS`:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

Die `.sig`-Dateien sind die Unterschriften für den Updater.

## Daten

Die Apps speichern alles nur auf dem eigenen Rechner. Es gibt kein Konto und keine Telemetrie.
