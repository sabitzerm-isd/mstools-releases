# Changelog

## v1.32.3 — 2026-10-04

- **Gruppen einzeln auf- und zuklappen**: Jede Gruppe mit Untergruppen hat in ihrer Überschrift zwei kleine Knöpfe –
  mit allen Untergruppen aufklappen bzw. zuklappen (Baum, Liste, Kompakt, Nur Icons). Der Zustand wird einmal gespeichert.
- Einstellungen: Beschriftung „Konfigurationsordner (Werkzeugliste)“ – die Protokolle liegen seit 1.26 je Benutzer.
- **Anleitung aktualisiert**: Untergruppen und Klappknöpfe, Baumansicht mit Farben, Sprache folgt HiCAD und übersetzte
  Werkzeuge, Version im Tooltip, Hilfe-Menü, Entwicklermodus mit GitHub-Stand statt Start-Dialog, stündliche
  Update-Prüfung, Zusammenarbeit mehrerer Programme an der Werkzeugliste; neue Bilder.

## v1.32.2 — 2026-10-04

- **Baumansicht farbig**: Hauptgruppen mit blauem Farbband (Verlauf, dunkelblauer Streifen links, blaue fette Schrift),
  Untergruppen zart blau hinterlegt. Die Auswahl – deren Symbole unten stehen – im HiCAD-Orange, ebenso beim Überfahren.

## v1.32.1 — 2026-10-04

- **Baumansicht**: Hauptgruppen (Stahlbau, Fassade, Holzbau, Daten, Kunden) sind immer als Band hinterlegt wie die
  Kopfzeilen der Liste. Die Auswahl – deren Symbole unten stehen – ist davon abgesetzt: kräftigeres Blau mit blauer Linie.

## v1.32.0 — 2026-10-04

- **Werkzeuge in allen Sprachen**: Titel und Beschreibung je Werkzeug auf Englisch, Französisch, Italienisch und
  Polnisch (tools.json: `texts` je Eintrag, Deutsch bleibt in title/description). MSTools zeigt sie in der aktuellen
  Sprache – Seitenleiste, Baum, Symbolbereich, Toolbox, Tooltip und Menü – und schaltet live mit HiCAD um; fehlt eine
  Übersetzung, gilt der deutsche Text.
- **Gruppennamen übersetzt** (tools.json: `groupTexts` je Pfadteil, z. B. „Stahlbau“ → „Steel construction“).
- **Eintrag-Dialog**: neuer Abschnitt „Übersetzungen“ mit Fahne, Titel und Beschreibung je Sprache; fehlt ein Titel,
  fragt MSTools beim Speichern nach.
- **MSTools-Block**: `// MSTools-Titel-en:`, `// MSTools-Beschreibung-fr:` usw. – füllt leere Übersetzungen.
- **Tooltip mit Version** – auch für Anwender ohne Entwicklermodus („Version 0.1.6“), ebenso im Menü.
- Alle 36 vorhandenen Werkzeuge und 11 Gruppen wurden übersetzt.
- Zusammenführen der tools.json übernimmt auch Gruppenübersetzungen anderer Schreiber.

## v1.31.1 — 2026-10-04

- **Baumansicht**: Version und GitHub-Stand (Entwicklermodus) stehen ganz rechts in der Zeile, wie in der Liste. Die
  Baumzeilen gehen dafür über die ganze Breite; die Auswahl markiert die ganze Zeile, Mausberührung hellblau.

## v1.31.0 — 2026-10-04

- **Versionshinweise in der Hilfe**: Hilfe ▾ → „Versionshinweise …“ zeigt die Neuerungen aller Versionen lesbar an.
  Die installierte Version ist grün markiert, neuere (noch nicht installierte) orange. Quelle ist die CHANGELOG im
  öffentlichen Release-Repo; ohne Internet die in MSTools eingebaute Fassung. Übersetzt in fünf Sprachen.
- **Update-Meldung**: neuer Link „Was ist neu?“ zeigt genau die Versionen zwischen der installierten und der neuen.
- Release-Text auf GitHub = Abschnitt der jeweiligen Version aus der CHANGELOG.

## v1.30.0 — 2026-10-04

- **Sprache folgt HiCAD live**: Stellt man in HiCAD die Sprache um, schaltet MSTools sofort mit um (Seitenleiste,
  Menüs, Fahne, übersetzte Dialoge). Ein Sprachwächter liest alle 2 s die drei Quellen exe\AppLanguage.txt, die
  Oberflächenkultur des HiCAD-Threads und ISD.Localization.AppLanguage.Current (geprüft in HiCAD 2027: alle drei lesbar).
  Eine frühere Wahl über die Fahne wird beim HiCAD-Wechsel aufgehoben; danach gilt wieder die HiCAD-Sprache, auch beim
  nächsten Start.

## v1.29.1 — 2026-10-04

- **Baumansicht wie „Bauwesen-Funktionen“ bedienen**: Oben im Baum startet ein **Doppelklick** das Werkzeug, ein einfacher
  Klick wählt es nur aus (unten erscheinen die Symbole seiner Gruppe). Unten im Symbolbereich startet weiter ein
  einfacher Klick.

## v1.29.0 — 2026-10-04

- **Untergruppen**: Der Gruppenname ist ein Pfad mit „/“ – „Fassade/Fußpunkt“, „Fassade/Kopf und Attika“,
  „Holzbau/Zapfen“, beliebig tief. Gleicher Pfadanfang = gemeinsamer Knoten (Reihenfolge des ersten Auftretens),
  gleich lautende Gruppen werden zusammengelegt. Das Dateiformat bleibt; ältere MSTools zeigen den Pfad als flache Gruppe.
- **Baum mit Symbolbereich** (neue Darstellung, Einstellungen → Darstellung): wie die HiCAD-Leiste
  „Bauwesen-Funktionen“ – oben Gruppenbaum mit Befehlen (16-px-Symbol, Klick startet), unten die Symbole der gewählten
  Gruppe samt Untergruppen mit Größenregler (16–64 px, gemerkt), Trennlinie verschiebbar. Im Entwicklermodus Version und
  GitHub-Stand im Baum.
- **Liste, Kompakt, Nur Icons** zeigen Untergruppen eingerückt mit eigener Kopfzeile; Zähler „(n)“ zählt alles darunter.
- Zugeklappte Zwischenknoten werden gemerkt (`settings.collapsedPaths`); Alles auf-/zuklappen und die Suche wirken auf
  alle Ebenen.
- **HiCAD-Menü**: Untermenüs je Pfadebene.
- Verschieben per Ziehen auf eine Gruppenkopfzeile legt in deren vollen Pfad ab (Liste/Kompakt/Nur Icons).

## v1.28.1 — 2026-10-04

- **Update-Meldung kam nicht**: HiCAD 2027 startete 80 s nach dem Release 1.28.0 und meldete „aktuell (1.27.0)“ –
  raw.githubusercontent.com lieferte trotz nocache-Parameter noch die alte version.json (GitHub hält auch die
  Zuordnung main → Commit bis 5 Minuten). Die Update-Prüfung liest jetzt zuerst über die GitHub-API (wie seit 1.17 die
  Paketliste), raw nur als Rückfall.
- **Prüfung auch während HiCAD läuft**: stündlich still; eine neue Version erscheint in der Statuszeile („? ▾ → Auf
  Update prüfen“), ohne Fenster mitten in der Arbeit. Übersprungene und bereits bereitgestellte Versionen nicht.

## v1.28.0 — 2026-10-04

Gleichzeitige Schreiber der tools.json (mehrere Claude-Chats tragen per Skript Kacheln ein, zwei HiCAD-Instanzen
teilen eine Datei). Befund: MSTools schrieb seinen alten Speicherstand zurück – Einträge verschwanden (Stützenstoß
02.10.), Versionen fielen zurück (Treppe 0.1.77 → 0.1.72, Gittermast 0.1.140 → 0.1.110 am 04.10.).

- **Zusammenführen statt Überschreiben**: Vor jedem Speichern liest MSTools die Datei frisch und arbeitet Änderungen
  von außen ein (neue, geänderte, verschobene, gelöschte Einträge, Einstellungen); hat MSTools dieselbe Stelle selbst
  geändert, gewinnt die eigene Änderung. Danach Nachkontrolle: geht eine fremde Id verloren, wird der vorige Stand
  zurückgeschrieben und das Speichern abgebrochen.
- **Sperre `tools.json.lock`** wie `99 Übergabe\werkzeuge\gemeinsam.py`: exklusiv anlegen, bis 30 s warten, nach
  120 s verwaist.
- **Automatisch neu laden**: Ein Dateiwächter bemerkt Änderungen anderer Programme (auch über `\\localhost\C$`) und
  baut die Seitenleiste neu auf – „Neu laden“ ist dafür nicht mehr nötig.
- **Unbekannte Felder bleiben erhalten** (z. B. künftige Felder neuerer Versionen oder von Skripten).
- UTF-8 ohne BOM wie bisher.

## v1.27.0 — 2026-10-04

- **Export ohne Protokolle und Sicherungen**: Beim Auflösen eines Werkzeugordners kommen die Ordner `logs`, `log`,
  `temp`, `tmp`, `obj`, `.git`, `.vs` sowie `*.log`, `*.bak` (auch die Sicherungen des Imports), `*.tmp`, `*.lock`,
  `desktop.ini` und `Thumbs.db` nicht mehr ins Paket. Bisher gingen z. B. Protokolle der Werkzeuge mit lokalen Pfaden
  an die Kunden. Einzeln eingetragene Dateien sind nicht betroffen. Probe: Fassadenkonsole und Bandgerüst ohne die 299
  Protokoll-/Sicherungsdateien gepackt.

## v1.26.0 — 2026-10-04

Rückmeldung M. Kast (Mail „MCP - Plugin-Tools“), Punkte für MSTools:

- **Zustimmung je Benutzer**: `MSTools_accepted.txt` liegt jetzt unter `%LOCALAPPDATA%\MSTools` statt neben der DLL
  in `exe\Plugins` (Serverinstallationen, mehrere Benutzer). Eine bestehende Zustimmung am alten Ort gilt weiter und
  wird beim ersten Start übernommen.
- **Protokolle nach `%LOCALAPPDATA%\MSTools\logs`** statt in den Konfigurationsordner unter custom – custom ist bei
  Kunden auf dem Server oft schreibgeschützt. Der Menüpunkt „Protokollordner“ öffnet den neuen Ort.
- **Windows-Textgröße** (Bedienungshilfen → „Text vergrößern“, z. B. 130 %): Seitenleiste und alle MSTools-Fenster
  skalieren mit; feste Fenstergrößen wachsen mit und bleiben auf dem Bildschirm. Prüfhilfe ohne Windows-Umstellung:
  Umgebungsvariable `MSTOOLS_TEXTGROESSE=130`.

## v1.25.0 — 2026-10-04

- **Kein Hochlade-Dialog mehr beim HiCAD-Start**: Im Entwicklermodus öffnet sich beim Start kein Fenster „Werkzeuge seit
  dem letzten Hochladen geändert“ mehr. Hochgeladen wird manuell über Export (dort „Nur geänderte“). Die Statuszeile
  meldet nur noch, wie viele Werkzeuge lokal neuer sind. Anwender ohne Entwicklermodus bekommen die Update-Meldung
  für ihre Werkzeuge wie bisher.
- **Version auf GitHub neben der lokalen Version** (nur Entwicklermodus): „GitHub 0.1.6“ rechts in jeder Zeile –
  grün gleich, orange lokal neuer (hochladen), blau GitHub neuer, grau noch nicht auf GitHub. Tooltip mit Kunde und
  Upload-Zeitpunkt. Geladen beim Start, mit dem Neu-laden-Knopf und nach dem Hochladen; offline bleibt die Anzeige leer.

## v1.24.0 — 2026-10-04

- **Lizenzmeldung: Adresse und Mailtext zum Kopieren**: Startet „Per E-Mail senden“ das falsche Mailprogramm, lassen
  sich die Empfängeradresse (**Adresse kopieren**) und der vollständige Anfragetext mit Seriennummer, HiCAD- und
  MSTools-Version, Kundennummer und Rechnername (**Text kopieren**) direkt aus dem Dialog übernehmen. Der Text steht
  sichtbar im Dialog und liegt nach „Per E-Mail senden“ zusätzlich in der Zwischenablage. Feste Dialoggröße, alle
  fünf Sprachen.

## v1.23.0 — 2026-10-04

- **Werkzeugversion in der Seitenleiste (nur Entwicklermodus)**: In den Darstellungen Liste und Kompakt steht rechts in
  jeder Zeile die Version des Werkzeugs (MSTools-Block bzw. Änderungsdatum). Werkzeuge ohne Versionsangabe bleiben leer.
  Beim Ausschalten des Entwicklermodus verschwindet die Anzeige sofort.

## v1.22.0 — 2026-10-03

- **Lizenzen verwalten im Plugin (Variante A, Entwicklermodus)**: Hilfe ▾ → „Lizenzen verwalten …“ bzw. Einstellungen →
  Entwickler. Lokales Register (`lizenz-register.json`, nur auf dem Entwicklerrechner) mit Kundennummer, Kundenname,
  HiCAD-Seriennummer, Häkchen „Freigegeben“ und Notiz; Spalte „Auf GitHub“ zeigt veröffentlicht / noch nicht
  veröffentlicht / wird entzogen. „Diese HiCAD-Seriennummer übernehmen“, Kundenname aus der Kundenliste des Exports.
- **„Speichern und Freigabeliste veröffentlichen“**: erzeugt `lizenzen.json` (nur Fingerabdrücke, ohne 5212), signiert
  mit dem geladenen Schlüssel und lädt per Git hoch (ein Commit, wie die Werkzeug-Pakete). Ohne Schlüssel nach Rückfrage
  unsigniert – im Testbetrieb in Ordnung.
- **Signierschlüssel** erzeugen oder laden (RSA-XML, gleiches Format wie der Tools Manager – es darf nur einen geben),
  Fingerabdruck anzeigen, öffentlichen Schlüssel kopieren. Der private Schlüssel bleibt in seiner Datei; im Register
  steht nur der Pfad.
- Lizenzmeldung zeigt auf dem Entwicklerrechner zusätzlich, für welchen Kunden die Seriennummer eingetragen ist.
- Weiterhin Testbetrieb: nichts wird gesperrt.

## v1.21.0 — 2026-10-03

- **Lizenz (Vorbereitung, Testbetrieb – sperrt nicht)**:
  - Beim ersten Start je HiCAD-Seriennummer erscheint „Lizenzdaten dieses Arbeitsplatzes“ mit Seriennummer, Status,
    **„Per E-Mail senden“** (fertige Anfrage an msabitzer@isdgroup.at) und „Kopieren“; jederzeit über Hilfe ▾ → Lizenz …
    In allen fünf Sprachen, feste Dialoggröße.
  - Prüfung gegen die Freigabeliste `lizenzen.json` (+ `.sig`) aus dem öffentlichen Repo, offline aus dem
    Zwischenspeicher. Format 1 eingefroren: nur SHA-256 der Seriennummern, keine Namen (siehe
    `docs/lizenz/Konzept-Lizenzfreigabe.md`). RSA-SHA256-Signatur, Prüfung aktiv, sobald der öffentliche Schlüssel
    aus dem Tools Manager eingetragen ist.
  - `settings.lizenzModus`: `test` (Standard), `aus`, `scharf`. Nur „scharf“ + sicher fremde Seriennummer sperrt den
    Skriptstart; 5212 (ISD intern) ist immer frei; nicht lesbare Seriennummer, fehlende oder ungültige Liste sperren nie.
- Konzept für Freigaben ohne Neu-Export, auch vom Handy (GitHub Actions bzw. Cloudflare Worker), mit Kosten und Datenschutz.

## v1.20.0 — 2026-10-02

- **Mehrsprachig (Schritt 1)**: Deutsch, Englisch, Französisch, Italienisch, Polnisch - die Sprachen des
  HiCAD-Sprachdialogs. Startsprache aus `<HiCAD>\exe\AppLanguage.txt` (1031/1033/1036/1040/1045), oben in der
  Seitenleiste ein **Fahnen-Knopf ▾** zum Umschalten; die Wahl wird gemerkt (`settings.sprache`). Fahnen als kleine
  Grafik, weil Windows Flaggen-Emoji in WPF nur als Buchstaben zeigt.
- Übersetzt: Seitenleiste (Werkzeugleiste, Suche, Menüs Zahnrad/Hilfe/Import, Gruppen, Leerzustand), Toolbox.
  Die Dialoge (Einstellungen, Export, Import, Werkzeug anlegen …) folgen im nächsten Schritt.
- Technik: `Loc` (Texte je Sprache) und Markup-Erweiterung `{l:T Schlüssel}`; ein Sprachwechsel schaltet sofort um.

## v1.19.1 — 2026-10-02

- Export-Dialog (auch aus der Startmeldung „Jetzt hochladen …“) deutlich größer: fast volle Bildschirmhöhe, bis
  1000 px breit, in der Größe veränderbar; die Werkzeugliste nutzt den freien Platz statt fester 320 px. Bisher musste
  man bei 28 Werkzeugen in der Liste und im Fenster scrollen.

## v1.19.0 — 2026-10-02

- **Änderungshinweis je Werkzeug**: „Von GitHub übernehmen“ hat die Spalte „Was ist neu“ (ganzer Text als
  Tooltip), die Startmeldung „Werkzeug-Updates verfügbar“ zeigt den Hinweis hinter dem Namen.
- Herkunft: Zeile `// MSTools-Änderung: …` im Skriptkopf (MSTools-Block, mehrere Zeilen werden verbunden; auch
  `MSTools-Aenderung`/`-Kommentar`) oder das neue Feld „Was hat sich geändert?“ im GitHub-Bereich des Export-Dialogs
  (gilt für alle gewählten Werkzeuge; die Skriptzeile hat Vorrang). Gespeichert als `kommentar` in `pakete.json`.

## v1.18.0 — 2026-10-02

- **Neue Werkzeug-Varianten werden automatisch erkannt** (Grundlage: die seit 1.17.0 selbst hochzählende Version).
  - **Entwicklermodus, beim HiCAD-Start:** Meldung „N Werkzeuge seit dem letzten Hochladen geändert“ mit
    „GitHub-Version → lokale Version“ je Werkzeug und Kunde; „Jetzt hochladen …“ öffnet den Export mit genau diesen
    Werkzeugen, dem passenden Kunden und angehaktem GitHub-Häkchen.
  - **Export-Dialog:** je Werkzeug „neu“ (noch nie hochgeladen), „geändert“ oder „aktuell“ gegenüber GitHub für den
    gewählten Kunden, Zusammenfassung darunter, Knopf „Nur geänderte“.
  - **Anwender, beim HiCAD-Start:** Meldung „N Werkzeug-Updates verfügbar“ (neu oder neuer für die eigene
    Kundennummer); „Übernehmen …“ öffnet „Von GitHub übernehmen“ mit Vorauswahl.
- Die Werkzeug-Prüfung läuft nach der MSTools-Update-Prüfung (nicht, solange ein MSTools-Update ansteht) und folgt
  derselben Einstellung „Beim Start von HiCAD auf neue Versionen prüfen“.
- `pakete.json` wird über die GitHub-API gelesen (kein 5-Minuten-Zwischenspeicher), sonst über die raw-Adresse.
- **Absicherung Werkzeugliste**: Läuft MSTools in einem Prozess mit virtualisiertem %APPDATA% (z. B. aus der
  Claude-App gestartet) und gibt es noch keine virtuelle Kopie der `tools.json`, griff die Erkennung aus 1.6.0 nicht.
  Seit 1.17.0 speichert das Laden still mit; das Ersetzen traf dann die echte Datei, die neue landete in der virtuellen
  Kopie, die gemeinsame Liste war weg (2026-10-02 14:08, aus der Sicherung wiederhergestellt). Jetzt prüft MSTools den
  Prozess selbst mit einer Probedatei und arbeitet dann immer über `\\localhost\C$\…`.

## v1.17.0 — 2026-10-02

- **MSTools-Block im Startskript**: Das Werkzeug sagt selbst, was dazugehört. Kommentarblock im Skriptkopf
  (vor `using`), alle Zeilen optional, Groß/Klein egal:
  `// MSTools-Version: …`, `// MSTools-Dateien: {HiCAD}\custom\…` (mehrfach, auch relativ zum Skriptordner),
  `// MSTools-Titel: …`, `// MSTools-Beschreibung: …`, `// MSTools-Icon: …`, `// MSTools-Gruppe: …`.
  Vorlage in README und Anleitung.
- **Automatisch, ohne Knopf**: Beim Wählen des Skripts belegt der Dialog Titel, Beschreibung, Icon, Gruppe,
  Version und Dateien aus dem Block vor. Beim Laden der Werkzeugliste (Seitenleiste, Toolbox; nur der Kopf,
  zwischengespeichert über die Änderungszeit), beim Öffnen von „Eintrag bearbeiten“ und vor jedem Export bzw.
  GitHub-Paket übernimmt MSTools **Version und Dateien** und speichert sie still in `tools.json`. Titel,
  Beschreibung und Icon bestehender Einträge bleiben, wie der Anwender sie gesetzt hat (nur leere werden gefüllt).
- Dialog: Steht der Block im Skript, ist die Dateiliste „aus dem Skript“ und nicht editierbar, „Neu erkennen“,
  „Datei…“ und „Ordner…“ sind ausgeblendet. Ohne Block läuft die bisherige Erkennung automatisch beim Öffnen
  und bei der Skriptwahl; neue Funde eines gespeicherten Eintrags kommen ohne Häkchen dazu.
- **Version zählt automatisch hoch**: Reihenfolge `MSTools-Version` aus dem Block, sonst das jüngste
  Änderungsdatum von Skript und allen zugehörigen Dateien/Ordnern als `JJJJ.MM.TT.HHMM` (nur Verzeichnisdaten,
  OneDrive-Platzhalter werden nicht geladen; `*.log`, `*.tmp`, `logs\` u. Ä. zählen nicht; über 5000 Dateien
  oder 2 s: nur Skript und DLLs). Erst wenn das nicht geht: `// Version:`-Kopfzeile, dann DLL-Version.
  Das Versionsfeld im Dialog ist nur noch Anzeige.
- **Versionsvergleich beim Import** (Datei und GitHub) über Zahlenteile (`1.0` = `1.0.0`, `1.2.3-beta` < `1.2.3`);
  ein Wechsel zwischen Versionsnummer und Änderungsdatum gilt als „aktualisiert“ bzw. „neuer“.

## v1.16.0 — 2026-10-02

- **Veröffentlichen auf GitHub nur noch mit Git**, ohne GitHub CLI und ohne Anmeldeknopf: Git nutzt die Anmeldung im
  Windows-Anmeldeinformationsspeicher (Git Credential Manager), die für jedes Programm gilt. Fehlt sie, öffnet Git
  beim Hochladen selbst sein Anmeldefenster.
- Pakete liegen jetzt im Repository unter `pakete/<kunde>/MSTools_<Kunde>_<Werkzeug>.mstools`; Dateien und
  `pakete.json` gehen in einem Push. Die Links in `pakete.json` zeigen auf genau den Commit
  (`raw.githubusercontent.com/<repo>/<commit>/…`), dadurch nie ein veralteter Stand aus dem GitHub-Zwischenspeicher.
  Wurde `main` inzwischen geändert, setzt MSTools einmal neu auf (`pull --rebase`) und versucht es erneut.
- Export-Dialog: Statuszeile „Bereit: lädt über Git … hoch“; Einstellungen: „GitHub-Zugang prüfen“ (Klon und
  `git push --dry-run`, ändert nichts).

## v1.15.1 — 2026-10-02

- **Version wird automatisch erkannt** (Dialog „Eintrag bearbeiten“ / „Neuen Eintrag hinzufügen“): beim Öffnen eines
  Eintrags, bei „Neu erkennen“ und bei der Wahl des Skripts. Quelle ist eine Kommentarzeile im Skriptkopf vor der ersten
  `using`-Zeile, z. B. `// Version: 1.2.0` (auch `//  Version 1.2`, `// Version 1.2.3-beta`, `* Version: 1.0` im
  Blockkommentar). Fehlt sie, gilt die Produkt- bzw. Dateiversion der Werkzeug-DLL (gleicher Namensstamm wie das Skript,
  z. B. `MSGehrung_Start.cs` → `MSGehrung.dll`, sonst die erste DLL der zugehörigen Dateien; `0.2.8+a266…` → `0.2.8`).
  Der Hinweis unter dem Feld nennt die Quelle; das Feld bleibt editierbar. Nicht erkannt: Hinweis, die Kopfzeile zu
  ergänzen, die Version bleibt von Hand gepflegt.
- **Export und GitHub-Veröffentlichung** erkennen die Version je Werkzeug vorher frisch und schreiben sie in Paket,
  `pakete.json` und `tools.json`, damit der Versionsvergleich beim Import stimmt.

## v1.15.0 — 2026-10-02

- **Importieren → „Von GitHub …“**: zeigt die veröffentlichten Werkzeug-Pakete mit Version auf GitHub, installierter
  Version, Status (neu / neuer / gleich / unbekannt), Kunde und Datum; neue und neuere des eigenen Kunden sind
  vorausgewählt. Entwicklermodus: alle Kunden mit Filter, sonst nur die eigene Kundennummer. Der Import-Knopf hat
  dafür ein Menü „Aus Datei …“ / „Von GitHub …“.
- **Export-Dialog**: GitHub-Bereich zeigt die Anmeldung (grün mit Kontoname bzw. rot mit Knopf „Bei GitHub anmelden“);
  nach der Anmeldung wird der Status neu geprüft. Den Knopf gibt es nur im Entwicklermodus (Export-Dialog und
  Entwicklerbereich der Einstellungen).

## v1.14.1 — 2026-10-02

- **GitHub-Anmeldung direkt aus MSTools**: Ist der Rechner bei GitHub nicht angemeldet, fragt der Export-Dialog
  „Jetzt anmelden?“ und öffnet die offizielle Anmeldung (`gh auth login --web`, Einmal-Code gleich in der
  Zwischenablage, danach `gh auth setup-git`). Nach dem Schließen des Fensters veröffentlicht MSTools die schon
  exportierten Pakete automatisch. Zusätzlich Knopf „Bei GitHub anmelden“ im Entwicklerbereich der Einstellungen.
  Fehlt GitHub CLI, bietet MSTools die Download-Seite an.
- Anlass: Eine Anmeldung, die in einer Konsole der Claude-App gemacht wurde, liegt in deren virtualisierter
  AppData-Kopie und gilt für ein normal gestartetes HiCAD nicht.

## v1.14.0 — 2026-10-02

- **Hilfe-Symbol** rechts oben in der Seitenleiste neben dem Zahnrad, angeordnet wie in HiCAD: Zahnrad ▾ und
  blaues Fragezeichen ▾. Das Symbol öffnet die Bedienungsanleitung (`exe\Plugins\MSTools\MSTools-Anleitung.html`,
  wird mit ausgerollt und liegt im Release-ZIP), der Pfeil ein Menü mit „Auf Update prüfen“ und „Über MSTools“.
- Zahnrad ▾: Einstellungen, Konfigurationsordner öffnen, Protokollordner öffnen, Neu laden.

## v1.13.0 — 2026-10-02

- **Werkzeug-Pakete direkt aus dem Plugin auf GitHub veröffentlichen** (nur Entwicklermodus): im Export-Dialog
  „Zusätzlich auf GitHub veröffentlichen (Paket-Update)“, standardmäßig an, die Wahl wird gemerkt. Je Kunde ein
  Release `pakete-<kunde>`, je Werkzeug eine Datei `MSTools_<Kunde>_<Werkzeug>.mstools`. Die Namen sind ASCII-sicher
  (ä→ae, ß→ss, Leerzeichen→_), weil GitHub Umlaute in Release-Dateien sonst eigenmächtig ersetzt und der Link nicht
  mehr passt; ohne Datum, damit ein erneutes Hochladen die alte Fassung ersetzt. Danach `pakete.json` mit einem Eintrag
  je Kunde und Werkzeug (neue Felder `werkzeug`, `titel`, `version`). Nutzt GitHub CLI und Git des Rechners, das
  Plugin speichert keine Zugangsdaten.
- **Paket-Update prüfen** findet alle neueren Werkzeug-Pakete der Kundennummer und spielt sie mit einer gemeinsamen
  Vorschau ein (bisher nur das neueste eine Paket).

## v1.12.0 — 2026-10-01

- **153 neue Icons** für Stahl-, Metall- und Fassadenbau im MSTools-Stil (Bestand blau, Aktion rot, 16/32/256 px):
  Profile, Stahlbau, Verbindungen, Blech, Geländer, Treppen, Tore & Türen, Fassade, Bearbeitung,
  Bemaßung & Zeichnung, Analyse & Prüfung, Daten & Export, Allgemein. Erzeugt mit `icons-source\gen_icons_c.py`.
- **Icon-Katalog** `icons-katalog.json` (neben den Icons): Titel, Kategorie und Suchbegriffe für alle 226 Bibliotheks-Icons,
  auch die bisherigen.
- **Icon-Auswahl** beim Anlegen/Bearbeiten: nach Kategorien gruppiert, Suchfeld (Titel, Name, Stichworte; mehrere Wörter,
  „gelaender“ findet „Geländer“), Kategorie-Auswahl und Trefferzahl. Icons aus importierten Paketen erscheinen unter
  „Eigene Icons“, Werkzeugleisten-Symbole nicht mehr.

## v1.11.1 — 2026-10-01

- Einstellungen > Darstellung: Fährt die Maus über „Liste“, „Kompakt“ oder „Nur Icons“, zeigt ein Tooltip eine kleine
  Vorschau mit Gruppenkopf und drei echten Einträgen aus der Werkzeugliste in dieser Darstellung.

## v1.11.0 — 2026-10-01

- **Konfiguration im HiCAD-Stamm**: ohne `config-dir.txt` liegen Werkzeugliste, Logs und Exporte jetzt in
  `{HiCAD}\custom\MSTools` (wird angelegt). Eine vorhandene `%APPDATA%\MSTools\tools.json` (mit customers.json und
  Sicherung) wird beim ersten Start einmalig dorthin kopiert, der alte Ordner bleibt liegen. Ist der custom-Ordner
  nicht beschreibbar, bleibt es bei `%APPDATA%\MSTools`. Installationen mit `config-dir.txt` ändern sich nicht.
- **Einstellungen aufgeräumt**: Abschnitte als Karten; neuer Abschnitt **Pfade** mit Konfigurations- und Exportordner
  (Ordner wählen, „Standard“, „Öffnen“). Ein geänderter Konfigordner gilt ab dem nächsten HiCAD-Start; MSTools kopiert die
  Werkzeugliste dorthin und schreibt `config-dir.txt` (bzw. entfernt sie beim Standard). Standard-Exportordner:
  `{HiCAD}\custom\MSTools\Export`.
- Bereich „Werkzeuge“ (Ordner durchsuchen) entfernt.
- Empfänger für Lizenzanfragen ist vorbelegt.
- **Entwicklermodus nur mit Passwort**; Update-Adresse, „tools.json öffnen“ und „Entwickler-Standard laden“ stehen jetzt
  im Entwicklerbereich und erscheinen nur bei eingeschaltetem Modus.
- Das Einstellungsfenster hat einen eigenen Eintrag in der Taskleiste.
- `deploy\publish.ps1 -OhneLiveAusrollen` (bzw. `MSTOOLS_KEIN_LIVE=1` beim Bauen) lässt die lokalen HiCAD-Installationen
  unverändert, um das Update über die MSTools-Meldung zu testen.

## v1.10.0 — 2026-10-01

- **Update-Prüfung beim HiCAD-Start**: MSTools fragt im Hintergrund die `version.json` auf GitHub ab und meldet sich
  nur, wenn es eine neuere Version gibt (offline oder ohne Antwort: nur ein Eintrag im Protokoll).
- **Herunterladen und übernehmen** direkt aus der Meldung (und aus Einstellungen > Auf Update prüfen): das Release-ZIP
  wird nach `%TEMP%\MSTools-Update\<Version>` geladen, geprüft (MSTools.dll mit passender Version) und übernommen,
  sobald HiCAD beendet wird — die DLL ist gesperrt, solange HiCAD läuft. Ziel ist der Plugins-Ordner der laufenden
  HiCAD-Installation, die alte DLL wird unter `…\vorher` gesichert, Protokoll `update.log`. Ohne Schreibrecht auf
  den Plugins-Ordner fragt Windows nach Administratorrechten. Werkzeugliste und Einstellungen bleiben unberührt.
- Weitere Knöpfe: „Später“, „Version überspringen“ (gemerkt in `update-uebersprungen.txt` im Konfigordner) und
  „Beim Start von HiCAD auf neue Versionen prüfen“ (auch in den Einstellungen; `settings.updateCheckOff`).
- `version.json` nennt jetzt zusätzlich die ZIP-Adresse (`"zip"`); `deploy\publish.ps1` legt erst das Release an
  und schreibt danach die `version.json`.

## v1.9.1 — 2026-10-01

- Seitenleiste: Name und Homepage-Link aus der Statuszeile entfernt, dort stehen nur noch HiCAD- und MSTools-Version.

## v1.9.0 — 2026-10-01

- **Export: je Werkzeug eine eigene Paketdatei** mit dem Werkzeugnamen im Dateinamen:
  `MSTools_<Werkzeug>_<Kunde|intern>_<JJJJMMTT>.mstools` (Leerzeichen und ungültige Zeichen werden zu `_`, Umlaute
  bleiben, höchstens 60 Zeichen; gleiche Titel bekommen die Id angehängt). Der Dialog nennt Anzahl und Beispielnamen.
- **Import: Mehrfachauswahl** (Strg/Umschalt). Eine Vorschau über alle gewählten Pakete, danach wird eines nach dem
  anderen eingespielt; nicht lesbare Pakete werden übersprungen und genannt.
- **Standard-Exportordner** (`settings.exportFolder`): Startordner für Export und Import, wird nach jedem Export auf den
  zuletzt verwendeten Ordner gesetzt.

## v1.8.2 — 2026-10-01

- Einstellungen: „Per E-Mail senden“ wurde rechts abgeschnitten (Kundenbefund). Die Seriennummer-Knöpfe brechen jetzt
  um, das Fenster ist breiter (540 px) und in der Größe veränderbar, Abbrechen/Übernehmen stehen fest in einer
  Fußleiste außerhalb des Bildlaufs; das Fenster ist höchstens so hoch wie der Bildschirm.

## v1.8.1 — 2026-09-30

- **Werkzeuge verschwinden nicht mehr, wenn die tools.json fehlt**: MSTools holt sie aus der Sicherung
  `tools.json.letzter-stand` (bei jedem Speichern mit Einträgen erneuert) oder der neuesten `tools.json.*`-Sicherung
  mit Einträgen zurück. Eine leere Datei wird nur noch bei einer frischen Installation angelegt; ein leeres
  Speichern bei fehlender Datei holt vorher die Sicherung. Anlass: ein fremdes Werkzeug hatte die tools.json
  von HiCAD 2027 umbenannt, MSTools legte eine leere an, alle 26 Werkzeuge waren weg.

## v1.8.0 — 2026-09-30

- **Toolbox und alle Dialoge im HiCAD-Stil** (Einstellungen, Export, Import, Neuer Eintrag, Ordner durchsuchen,
  Nutzungsbedingungen): Kopf- und Fußleiste mit Ribbon-Verlauf statt weißer Blöcke, Titel kleiner (HiCAD zeigt
  ihn im Fensterkopf), Abschnitte mit schmalem Marinebalken, Listen und Eingabefelder eckig mit feinem
  graublauem Rahmen.
- Knöpfe wie in HiCAD-Dialogen: Verlauf, Standardknopf mit blauem Rahmen und fetter Schrift, Hover im
  HiCAD-Orange. Werkzeugknöpfe eckig, erst beim Überfahren sichtbar.
- Toolbox: Gruppenköpfe wie in der Seitenleiste, Kacheln wie große Ribbon-Knöpfe, unten Statuszeile mit
  Farbmarke statt farbigem Block, 16-px-Symbole in der Werkzeugleiste.
- Rauchtest `deploy\ui_smoke_fenster.ps1` für Toolbox, Einstellungen und Nutzungsbedingungen (speichert nichts).

## v1.7.0 — 2026-09-30

- **Seitenleiste im HiCAD-Layout**, nachgebaut nach den Panes 3D-Teilestruktur und Feature von HiCAD 2027:
  Werkzeugleiste mit hellem Verlauf und 16-px-Symbolen, Trenner zwischen den Knopfgruppen, Zahnrad rechts
  außen; Hover im HiCAD-Orange des aktiven Ribbon-Reiters. Der doppelte Titel „MSTools“ im Inhalt entfällt
  (HiCAD zeigt ihn im Pane-Kopf, er wurde dort abgeschnitten).
- Gruppenköpfe wie HiCAD-Spaltenköpfe (Verlauf, Rahmen, fette Schrift, Anzahl in Klammern), Befehle als
  flache Listenzeilen mit Trennlinie und hellblauem Hover wie im Modellbaum statt einzelner Karten.
- „Toolbox öffnen“ als Ribbon-artiger Knopf, darunter eine Statuszeile wie unten im HiCAD-Fenster
  (Farbmarke + Text) statt des großen blauen Blocks.
- Werkzeugsymbole neu, pixelgenau auf dem 16-px-Raster (`icons-source\make_toolbar_icons.py`):
  Modellbaum-Zeilen mit rotem Pfeil (auf-/zuklappen), Ablage mit Pfeil (Import/Export), Neu laden,
  graues Zahnrad und Lupe wie in HiCAD.

## v1.6.0 — 2026-09-23

- **Kein „verschwundenes“ Skript mehr durch virtualisiertes %APPDATA%**: wird HiCAD aus einer App wie der
  Claude-Desktop-App gestartet, sieht es %APPDATA% als MSIX-Überlagerung und las eine veraltete Kopie der
  tools.json (Befund: Tankstellenüberdachung fehlte in HiCAD 2027, die echte Datei hatte sie). MSTools prüft
  jetzt über den echten Pfad hinter dem Dateihandle, ob die Datei aus `…\Packages\…\LocalCache` kommt, und
  liest und schreibt dann die echte Datei über `\\localhost\C$\…`. Das Log nennt Konfigordner und Umweg.
- **Befehle per Ziehen verschieben**, auch in eine andere Gruppe: Kachel ziehen, eine blaue Linie zeigt die
  Einfügestelle; auf einem Gruppenkopf abgelegt landet sie am Ende der Gruppe. Wird sofort gespeichert.
- **Gruppenköpfe klarer**: Band in Hellblaugrau mit Marinebalken links, fette Schrift, Anzahl als Kästchen.
- **HiCAD-nähere Optik**: eckige Kanten (2 px statt 6–16 px), hellgrauer Grund, Hover hellblau wie in HiCAD,
  Icon-Kasten weiß mit Rahmen.
- **App-Icons im HiCAD-Stil**: kräftigere Farben (Bestand blau, Aktion rot), eckige Linienverbindungen,
  bei 32 und 16 px dickere, deckende Linien. Die SVG-Quellen bleiben unverändert, der Build gleicht an
  (`MSTOOLS_ICON_ROH=1` baut die alte Optik zum Vergleich).
- Rauchtest `deploy\ui_smoke_pane.ps1`: baut die Seitenleiste ohne HiCAD auf und fotografiert sie.

## v1.5.4 — 2026-09-13

- Laden der tools.json mit Diagnose und Auffangnetz: liefert der Serializer 0 Gruppen, obwohl die Datei
  Einträge nennt, schreibt MSTools eine WARN-Zeile mit Dateigröße, Prüfsumme, Assembly-Ort, CLR und
  Kultur ins Log und liest die Datei ein zweites Mal über einen Text-Reader. Anlass: HiCAD 2027 zeigte
  „0 Gruppen“ aus einer Datei mit 22 Einträgen, die außerhalb von HiCAD einwandfrei gelesen wird.

## v1.5.3 — 2026-09-10

- Schutz gegen fremde Schreiber der tools.json: Fehlt die Datei beim Start (wird gerade von einem anderen
  Werkzeug neu geschrieben), wartet MSTools bis 1,5 s, bevor es eine leere Konfiguration anlegt. Und eine
  leere Konfiguration im Speicher überschreibt nie eine Datei, die Einträge hat; es werden dann nur die
  Einstellungen übernommen. Anlass: HiCAD 2027 zeigte 0 Gruppen, während eine zweite Sitzung die Datei
  im Sekundentakt neu schrieb.

## v1.5.2 — 2026-09-10

- Einstellungen → Konfiguration: zeigt den vollen Pfad der tools.json (Gruppen, Einträge, Skriptpfade,
  zugehörige Dateien), dazu „Ordner öffnen“, „Datei öffnen“, „Pfad kopieren“ sowie Icon- und Log-Ordner.
  Bei Umlenkung über config-dir.txt steht die umlenkende Datei dabei.

## v1.5.1 — 2026-09-08

- Einstellungen → HiCAD-Lizenz: „Kopieren“ und „Per E-Mail senden“ neben der Seriennummer. Die Mail enthält
  Seriennummer, HiCAD- und MSTools-Version, Kundennummer und Rechnername; Empfänger einstellbar
  (`settings.licenseEmail`). Gegenstück im Tools Manager 2.29.1: Feld „HiCAD-Seriennummer“ je Kunde,
  wandert beim Kundenpaket ins Manifest.

## v1.5.0 — 2026-09-08

### Update-Prüfung über GitHub und HiCAD-Lizenznummer
Muster aus „Teileattribute Masken“ (Gehirn: `30-wissen/hicad/plugin-update-und-seriennummer.md`).

- **Einstellungen → Update → „Auf Update prüfen“**: liest `version.json` aus dem öffentlichen Repo
  `sabitzerm-isd/mstools-releases` (Cache-Umgehung), vergleicht mit der laufenden Version, zeigt
  „Neue Version x verfügbar“ mit „Download öffnen“. Nur auf Knopfdruck, kein Automatik-Check.
- **„Paket-Update prüfen“**: liest `pakete.json` aus demselben Repo und sucht das neueste Paket für
  die Kundennummer des zuletzt importierten Pakets (ohne Kunde: „intern“). „Paket herunterladen und
  importieren“ lädt es in den Temp-Ordner und startet den normalen Import mit Vorschau.
- **Update-Adresse** in den Einstellungen überschreibbar (`settings.updateUrl`), leer = Standard.
- **Seriennummer anzeigen**: liest die Seriennummer der HiCAD-Lizenz über
  `ISD.Licensing.FeatureLicense.GetLicSerial` (Reflection, keine Referenz). Das ist die Nummer, die
  später die Lizenz an die Installation bindet; Abschnitt 4.8 der Spezifikation ist damit hinfällig.
- Nach jedem Import merkt sich MSTools Kundennummer und Erstellzeitpunkt des Pakets
  (`settings.customerNumber`, `settings.lastPackageCreated`).
- Export ohne Kunden möglich („intern“).
- `deploy\publish.ps1`: Release-ZIP (exe\Plugins\MSTools.dll + Icons), `version.json`, GitHub-Release
  `vX.Y.Z` in `mstools-releases`, Code-Push nach `sabitzerm-isd/mstools` (privat).

### Tests
80 Fälle (neu: Versionsvergleich, Paket-Feed, Export ohne Kunde).

### Build
- AssemblyVersion 1.5.0.0

## v1.4.0 — 2026-09-08

### Tool-Pakete: Export je Kunde, Import mit Sicherung (ohne Lizenz)
Spezifikation `docs/superpowers/specs/2026-09-08-mstools-pakete-und-lizenz-design.md`, Paket 1.
Die Lizenz (Paket 2) ist entworfen, aber bewusst noch nicht gebaut; Paketformat und
Konfiguration lassen den Platz dafür frei (`license.json` wird beim Lesen ignoriert).

- **Export** (Knopf in der Seitenleiste, nur im Entwicklermodus): Kunde wählen oder neu anlegen
  (`%APPDATA%\MSTools\customers.json`), Tools ankreuzen, Zielordner. Ergebnis
  `MSTools_<Kundennummer>_<Datum>.mstools` (ZIP): `manifest.json`, `files\…` relativ zu
  `{HiCAD}`, `icons\…`. Fehlt eine Datei, bricht der Export **vor** dem Schreiben mit Liste ab.
  Von mehreren Tools genannte Dateien liegen einmal im Paket (`shared`).
- **Import** (Knopf immer sichtbar): Vorschau je Tool mit „neu / aktualisiert / unverändert“
  (Vergleich über `version`) und Zahl der zu ersetzenden Dateien. Bestehende Dateien werden
  vorher als `<name>.<yyyyMMdd-HHmmss>.bak` daneben gesichert; fremde Dateien im Zielordner
  bleiben. Gemeinsame Dateien werden nur ersetzt, wenn die Paketdatei neuer ist. Bricht ein
  Kopiervorgang ab, bleibt die tools.json unberührt und die Meldung nennt das bereits Ersetzte.
- **Zugehörige Dateien je Eintrag** (`files` in tools.json): im Anlege-/Bearbeiten-Dialog
  automatisch erkannt (Ordner aus `Path.Combine(…,"custom","KI","<Ordner>")` und Pfad-Literalen,
  DLL-Namen aus Textliteralen samt ihren Referenzen aus den DLL-Metadaten, blanke Ordnernamen),
  von Hand ergänz- und streichbar. Sammelordner mit fremden Skripten (`custom\KI`, `Kunden`)
  werden nie als Ganzes vorgeschlagen. HiCAD-API-DLLs werden daran erkannt, dass sie in
  `exe` oder `exe\API` liegen.
- **Einmalige Migration** beim ersten Laden einer tools.json mit `schemaVersion` 1: leere
  Dateilisten werden über die Erkennung gefüllt (Log nennt die Einträge). Bitte im
  Bearbeiten-Dialog prüfen.
- **Ordner durchsuchen** (Einstellungen): listet alle `.cs` unter `custom\KI`, die in keinem
  Eintrag stehen; gewählte laufen nacheinander durch den Anlege-Dialog. `logs`, `assets`,
  `konfig`, `Test`, `.alt`, `.bak` sind ausgeblendet, zuschaltbar.
- **Version je Tool** (`version`): freies Feld im Dialog, steuert den Import-Vergleich.
- **Entwicklermodus** (`settings.developerMode`, Häkchen in den Einstellungen): zeigt Export und
  „Entwickler-Standard laden“. Beim Kunden aus.
- **Leerer Start**: fehlt die tools.json, startet MSTools ohne Einträge und zeigt einen Hinweis
  mit Import-Knopf. Die Entwickler-Einträge kommen nur noch über den Knopf in den Einstellungen.
- **Konfigordner umlenken**: `exe\Plugins\MSTools\config-dir.txt` (erste Zeile = Ordner,
  Umgebungsvariablen erlaubt). Vorlage `deploy\config-dir.txt.beispiel`. Damit lässt sich
  HiCAD 2027 als „leerer Kundenrechner“ betreiben, während 2026 die Entwicklerkonfiguration behält.

### Testfeld (Abnahme, Spezifikation 4.12)
1. In `C:\HiCAD\HiCAD_3200\exe\Plugins\MSTools\` die Datei `config-dir.txt` mit Inhalt
   `%APPDATA%\MSTools-Test` anlegen. 3200 starten: leere Seitenleiste, Import-Knopf.
2. In 3102 (Entwicklermodus ist gesetzt): Export, Testkunde 9999, ein Tool; zweites Paket mit fünf Tools.
3. In 3200 beide Pakete importieren, Tools starten. Zweiter Import: „unverändert“, `.bak` daneben.
4. Aufräumen: `config-dir.txt` löschen, `%APPDATA%\MSTools-Test` löschen.

### Tests
`tests\MSTools.Tests`: 76 Fälle (neu: Paket-Rundlauf, Installer mit Sicherung, Dateierkennung mit
echter DLL-Abhängigkeit, Ordnersuche, Kundenliste, ConfigEditor, Schema-Migration).
`deploy\ui_smoke_dialogs.ps1` baut Export-, Import-, Anlege- und Ordnersuche-Dialog ohne HiCAD auf.

### Bekannt / offen
- Das HiCAD-Menü wird erst beim nächsten HiCAD-Start neu aufgebaut; Seitenleiste und Toolbox
  sofort.
- Voest-Türkonfigurator hat kein Icon (`voesttuer`), war schon vor v1.2.0 so.
- Lizenz (Paket 2): `licensed`, `signing.key`, `licenses.json`, Signatur, Zustände, HiCAD-Lizenznummer.

### Build
- AssemblyVersion 1.4.0.0

## v1.3.0 — 2026-09-08

### Umbenennung: „HiCAD-HELP“ verschwindet aus allen Datei- und Ordnernamen

| Bis v1.2.0 | Ab v1.3.0 |
|---|---|
| `HiCAD-HELP.com.Tools.dll` / `.pdb` | `MSTools.dll` / `.pdb` |
| `HiCAD-HELP.com.Tools.sln`, `src\HiCAD-HELP.com.Tools.csproj` | `MSTools.sln`, `src\MSTools.csproj` |
| Namespace `HiCadHelp.Tools` | `MSTools` |
| `%APPDATA%\HiCAD-HELP-Tools\` | `%APPDATA%\MSTools\` |
| `exe\Plugins\HiCAD-HELP-Tools\icons` | `exe\Plugins\MSTools\icons` |
| `HiCAD-HELP.com.Tools_accepted.txt` | `MSTools_accepted.txt` |
| `tests\HiCadHelp.Tools.Tests` | `tests\MSTools.Tests` |

Die Fußzeile der Seitenleiste zeigt weiterhin die Website hicad-help.com.

**Migration beim ersten Start:** Fehlt `%APPDATA%\MSTools\tools.json` und existiert
`%APPDATA%\HiCAD-HELP-Tools\tools.json`, werden `tools.json` und `logs\` kopiert und
`settings.iconRoot` auf `{HiCAD}\exe\Plugins\MSTools\icons` umgeschrieben. Der alte Ordner
bleibt liegen. Die Nutzungsbedingungen erscheinen einmal neu, weil die Marker-Datei neben
der DLL neu heißt.

**Post-Build** entfernt in 3102, 3200 und im Toolbar-Ordner die alten Dateien
(`HiCAD-HELP.com.Tools.*`, Ordner `HiCAD-HELP-Tools`), sonst lädt HiCAD zwei Plugins.
Läuft HiCAD während des Builds, wird diese Installation übersprungen und beim nächsten
Build nachgeholt.

### Logo
Neues Plugin-Logo „Kachelraster C2“: drei Kacheln in blauer Kontur mit hellblauer Füllung,
eine rote Vollkachel mit Start-Dreieck. Gleicher Stil wie die Werkzeug-Icons (Stil B).
Quelle `icons-source\plugin-icon.svg`, Build wie bisher über `build_icons.py`.

### Tests
43 Fälle (neu: Migration des Konfigordners, `iconRoot`-Umschreibung, Pfadkonstanten).

### Build
- AssemblyVersion 1.3.0.0

## v1.2.0 — 2026-09-03

### Ein Plugin für HiCAD 2026 und HiCAD 2027
Dieselbe DLL und dieselbe `tools.json` laufen jetzt in `C:\HiCAD\HiCAD_3102` (31.2) und
`C:\HiCAD\HiCAD_3200` (32.0). Die API beider Versionen ist .NET Framework 4.8, eine
Neukompilierung war nicht nötig.

- **Platzhalter `{HiCAD}`** in `tools.json` steht für den Stammordner des HiCAD, in dem das
  Plugin gerade läuft. `scriptPath` und `settings.iconRoot` werden beim ersten Laden automatisch
  von `C:\HiCAD\HiCAD_3102\…` auf `{HiCAD}\…` umgeschrieben und sofort zurückgespeichert.
  Pfade außerhalb des HiCAD-Ordners bleiben absolut. Neue Einträge aus dem Hinzufügen-Dialog
  werden beim Speichern automatisch tokenisiert; der Dialog zeigt darunter, welche Datei im
  laufenden HiCAD startet.
- **HiCAD-Stamm** wird aus dem DLL-Ordner (`<Stamm>\exe\Plugins`) ermittelt, Rückfall ist der
  Pfad der laufenden hicad.exe. Die Registry (`HKLM\…\HiCAD\3\HomeDir`) wird **nicht** mehr
  verwendet, weil sie bei zwei Installationen nur eine kennt (`Common\HicadHome`, `Common\PathTokens`).
- Alle Pfadverbraucher (Skriptstart, Icons, Menü, Kacheln, „Im Explorer zeigen", Pfad kopieren)
  gehen über `PathTokens.Resolve`. Im Code steht `HiCAD_3102` nur noch als letzter Rückfall.
- **Fußzeile** in Seitenleiste und Toolbox zeigt „HiCAD 2027 (32.0) · MSTools 1.2.0".
- **Deploy** (`deploy\post_build_copy.ps1`) spiegelt DLL und Icons nach 3102, 3200 und in den
  Toolbar-Ordner und entsperrt die Dateien (`Unblock-File`). Ein nicht vorhandener Stamm wird
  übersprungen. Das Plugin lädt über die automatische Erkennung aus `exe\Plugins`; ein Eintrag
  in `Plugins.config` ist **nicht** nötig (in 3102 gibt es auch keinen).

### Skripte versionsneutral, Kopie nach 3200
`deploy\sync_custom_to_3200.ps1` spiegelt `custom\KI`, `custom\Attributübertragung` und
`Custom\MSGlasgelaender` von 3102 nach 3200 (ohne `logs`, entsperrt DLLs). Vorher wurden fünf
Skripte in 3102 so geändert, dass dieselbe Datei in beiden Versionen läuft
(Sicherungskopien `*.vor-v1.2.0.bak` liegen daneben):

| Skript | Änderung |
|---|---|
| `Wandhandlauf.cs` | `VariantenFeature.HiCadStamm()` liest zuerst den Prozesspfad, Registry nur noch als Rückfall; `Ablage` wird aus dem Stamm gebildet |
| `Gittertuere Konfigurator.cs` | wie Wandhandlauf |
| `Kunden\Schweissnaht3D.cs` | `VariantenFeature.HiCadStamm()` wie oben |
| `Passteil.cs` | neue Stamm-Funktion, `Ablage` aus dem Stamm |
| `Schiebetor Konfigurator.cs` | stamm-basierter Kandidat vor jedem festen 3102-Pfad (Assets, Konfig, Seite, Skriptdatei) |

`HicVersion="3102.2-440"` im Varianten-XML (Schweißnaht, Gittertüre, Schiebetor, Wandhandlauf)
ist **unverändert** und wird in HiCAD 2027 getestet (siehe Abnahme).

Neue Prüfwerkzeuge in `deploy\`:
- `compile_check.ps1` übersetzt jedes Skript mit csc.exe (C# 5) gegen die API einer HiCAD-Version.
  Ergebnis 2026-09-03: 20/20 gegen 3102, die fünf geänderten auch gegen 3200.
- `check_tools.ps1` prüft jeden `tools.json`-Eintrag gegen 3102 und 3200 (Skript, DLL-Kopfzeilen,
  Icon, offene Literale, Dubletten). Ergebnis: 21 Einträge, 0 Probleme. „Offene Literale" ist eine
  Heuristik: Zeilen mit `return`, `Add(`, `kandidaten` und `HicVersion` gelten als Rückfall.
- `ui_smoke.ps1` lädt die DLL außerhalb von HiCAD, baut Seitenleiste und Toolbox auf, prüft
  Filter und Pfade und rendert Bildschirmfotos.

### Icons Stil B und Vektorsymbole
- Alle 77 generierten Icons schlanker: Kontur 3,0 statt 4,5 px, Innenkanten 1,6 statt 2,4 px,
  hellere Flächentöne, kräftige Handstriche (Pfeile, Naht, Lupe) um 25 % reduziert. Nur
  Konstanten in `icons-source\stila.py`, Motive unverändert.
- Neu: `toolbar-reload`, `toolbar-settings`, `toolbar-add`, `toolbar-search` ersetzen die
  Textzeichen ↻ ⚙ ＋ in den Kopfzeilen. Neu gezeichnet: `glasgelaender` (lag bisher nur als
  PNG im 3102-Ordner, ohne Quelle). Ergebnis: 78 SVG, 234 PNG.
- ▼/▶ der Gruppenköpfe und ⚠ der Kacheln sind jetzt Vektorpfade (`GroupChevron`, `WarnMark` in
  `ModernStyles.xaml`), unabhängig von der Schriftart.
- Gruppenköpfe mit dünnem Farbstrich statt Farbblock, helle Zähler-Pille, Kachelrundung 6 px.

### Suchfeld
Oben in Seitenleiste und Toolbox. Filtert live über Titel und Beschreibung (Teilwort, Groß/Klein
egal). Gruppen ohne Treffer werden ausgeblendet, Gruppen mit Treffern angezeigt, ohne den
gespeicherten Klappzustand zu verändern. Esc oder das X leeren das Feld. Der Filter wird nicht
gespeichert.

### Tests
Neues Projekt `tests\HiCadHelp.Tools.Tests` (xunit, net48): 35 Fälle für `HicadHome`,
`PathTokens`, `ConfigLoader.MigratePaths` und `TileFilter`. Aufruf: `dotnet test tests\HiCadHelp.Tools.Tests`.

### Bekannt / offen
- Feldmann-Katalog des Glasgeländers ist in 3200 nicht eingebunden; der Eintrag startet dort und
  meldet den fehlenden Katalog (Katalogpflege in HiCAD).
- `HicVersion 3102.2-440` in vier Skripten ungetestet unter 3200.
- Dubletten in `tools.json` (`gartentor-konfigurator-2`, `wandhandlauf-2`, TEST/`gittertuer`) zeigen
  auf dieselben Dateien wie andere Einträge; Anwenderdaten, nicht entfernt.
- Die sieben Hilfs-DLLs neben den Skripten sind gegen die 3102-API gebaut und nur kopiert.

### Abnahme HiCAD 2027 (offen, 2026-09-04)

Vorab prüfen: Plugin erscheint in 3200 **ohne** Eintrag in `Plugins.config` (Auto-Erkennung wie in
3102). Erscheint es nicht, den Block aus `deploy\Plugins.config-snippet.xml` eintragen und neu starten.
Schiebetor: `custom\KI\Schiebetor\konfig` existiert in keiner Installation, deshalb arbeitet das
Skript in 3102 **und** 3200 mit dem Konfig-Ordner des Entwicklungsprojekts (bewusst nicht geändert).

| Eintrag | Ergebnis in 3200 |
|---|---|
| Formrohrende schließen | |
| Schweißnaht | |
| Gittertüre bauen | |
| Gartentor bauen | |
| Schiebetor | |
| Anschnitte gerade | |
| Wandhandlauf | |
| Passteil | |
| Glasgeländer | erwartet: Hinweis fehlender Feldmann-Katalog |
| Bohrungsanalyse | |
| Glas als DXF | |
| Stückliste | |
| Attributübertragung | |
| Wilplinger Schlaufengeländer | |
| Wilplinger Schlaufengeländer — Bemaßung | |
| WILP-Geländer Bogen | |
| Wiplinger Kombi | |
| WILP-Blechgröße ermitteln | |

### Build
- AssemblyVersion 1.2.0.0

## v1.1.0 — 2026-08-04

### Plugin heißt jetzt MSTools
„ISD" taucht nirgends mehr auf — weder in der Oberfläche noch in den DLL-Eigenschaften.
Umbenannt wurde nur die sichtbare Ebene; DLL-Name, Config-Ordner (`%APPDATA%\HiCAD-HELP-Tools`)
und Icon-Ordner bleiben unverändert, damit bestehende `tools.json` weiterlaufen.

- `Plugin.Name` / `Description`, Pane-Header, HiCAD-Menü, Toolbox-, Einstellungs- und
  Nutzungsbedingungen-Dialog → „MSTools"
- `AssemblyTitle` / `AssemblyDescription` / `AssemblyProduct` → „MSTools",
  `AssemblyCompany` → „Michael Sabitzer"
- Der historische Abschnitt weiter unten zur damaligen Umbenennung bleibt als Historie stehen

### App-Logo: fertig, aber gesperrt bis Mitte November 2026
Das neue Zeichen ist gebaut, wird aber **nicht ausgeliefert**. Es beruht auf dem neuen
HiCAD-Würfel, und der wird erst Mitte November 2026 öffentlich. Aktiv bleibt bis dahin das
bisherige blaue „H" mit Schraubenschlüssel.

Die Quelle liegt geparkt in `icons-source/_ab-november/plugin-icon.svg`. Dieser Unterordner
wird von `build_icons.py` nicht erfasst — das Skript sammelt `*.svg` nur direkt in
`icons-source/`, nicht rekursiv. Zum Umstellen genügt es, die Datei eine Ebene höher zu
kopieren und neu zu bauen; Anleitung in `icons-source/_ab-november/LIESMICH.md`.

Ableitung des neuen HiCAD-Würfels mit Rot-Weiß-Rot in der unteren linken Kachel:

- Rein geometrisches SVG, keine Rasteranteile — skaliert verlustfrei in jede Größe
- Maße am Original gemessen: Außenradius 125 auf 256er Fläche, Loch 0,512 × R, keine Konturen
- Der Ring besteht aus sechs Parallelogrammen; die Teilung je Würfelfläche verläuft
  **nicht radial**, sondern parallel zur Flächenkante — sonst ist der senkrechte Balken zu
  kurz und die Flagge läuft in ihn hinein
- Verläufe je Teilfläche über ein lineares Modell aus allen Pixeln des Originals gefittet;
  mittlere Abweichung zum Original 20,6 statt 32,9 bei einer Näherung aus Stichproben
- Quelle zusätzlich im 2. Gehirn abgelegt (`30-wissen/allgemein/mstools-logo.*`) zur
  Wiederverwendung in weiteren Werkzeugen

### Alle 72 Icons auf einen Stil gebracht
Der bisherige Satz war handgezeichnet und deshalb uneinheitlich: überall gleich dicke
Outlines, Einzelton-Füllungen ohne Tiefe, gemischte Perspektiven. Jedes Icon ist neu.

- **Erzeugt statt gezeichnet:** `icons-source/stila.py` enthält die Grundformen (Iso-Körper,
  Blech, Bohrung, Pfeil, Lupe, Maßlinie), `gen_icons_a.py` und `gen_icons_b.py` setzen die
  Icons daraus zusammen. Achsenlage, Flächentöne und Strichstärken sind dadurch bei allen
  identisch — genau das war von Hand nicht zu halten. Der Lauf ist reproduzierbar.
- **Drei Flächentöne je Körper** statt einer Füllung, Silhouette 4,5 px gegen Innenkanten
  2,4 px bei Deckkraft 0,45, Hintergrund transparent statt hellgrauer Kasten
- Projektweit dieselbe Isometrie: Breite (58, 33), Höhe (0, −96), Tiefe (74, −42)
- **Fünf fehlende Icons neu gezeichnet:** `gittertuere` (hatte vorher gar keines),
  `gartentor`, `wandhandlauf`, `passteil`, `attributuebertragung`
- **Zwei zusätzliche:** `schiebetor` und `stueckliste`. Diese beiden Einträge trugen bisher
  Behelfs-Icons (`generic-arrow-right` und `cad-pattern`) und lassen sich im Bearbeiten-Dialog
  umstellen — die `tools.json` wurde bewusst **nicht** angetastet.

### Vier verwaiste Icons ins Repo geholt
`attributuebertragung`, `gartentor`, `passteil` und `wandhandlauf` lagen ausschließlich im
HiCAD-Ordner und fehlten in Repo und Verteilordner — eine Neuinstallation hätte diese vier
Werkzeuge ohne Icon zurückgelassen. Die PNGs liegen jetzt in `deploy/icons/`, die Vorlagen
für den späteren Neuzeichnung in `icons-source/_vorlagen-fehlende/`.

**Offen:** `gittertuere` hat nach wie vor **kein** Icon — weder als SVG noch als PNG,
nirgends. Der Eintrag „Gittertüre bauen" läuft derzeit ohne Symbol.

## v1.0.18 — 2026-07-03

### Bugfix: Einträge mit fehlender Script-Datei waren nicht mehr bearbeitbar
Toolbox-Tiles waren bei fehlender Script-Datei per `IsEnabled` komplett deaktiviert — auf einem deaktivierten WPF-Button öffnet sich aber **kein Kontextmenü**, dadurch waren „Bearbeiten…"/„Löschen…" unerreichbar (Eintrag saß fest, z.B. „Wilplinger Schlaufeng. Bogen — Phase 1 Zylinder").

- Tiles (Pane + Toolbox) bleiben jetzt immer klickbar; fehlende Scripts werden **gedimmt** dargestellt (Opacity) plus ⚠-Badge
- Der Start wird im ViewModel abgefangen: Klick auf fehlendes Script → rote Status-Meldung statt Compiler-Fehler
- Kontextmenü: „Script-Datei öffnen"/„Im Explorer zeigen" sind bei fehlender Datei deaktiviert, Bearbeiten/Löschen/Pfad-kopieren immer verfügbar
- Der festsitzende Phase-1-Eintrag wurde aus `tools.json` und aus den Defaults (`DefaultConfigBuilder`) entfernt

### Tooltips: Name + Beschreibung
Neuer gemeinsamer Tooltip (`TileToolTip` in `ModernStyles.xaml`) für Pane- und Toolbox-Tiles:
- **Name** (fett, blau) + Beschreibung (grau) + roter Hinweis „⚠ Script-Datei nicht gefunden: …" bei fehlender Datei
- Menü-Tooltips zeigen ebenfalls Titel + Beschreibung (+ Fehlt-Hinweis, auch auf deaktivierten Items)

### Darstellungsmodi für die Seitenleiste (Einstellungen)
Neuer ⚙-Button im Pane-Header öffnet den Einstellungs-Dialog (`Ui/Settings/SettingsDialog`). Drei Modi, persistiert als `settings.paneDisplayMode` in `tools.json`:
- **Liste** (Standard) — Icon-Box + Name, wie bisher
- **Kompakt** — schmale Zeilen mit 18-px-Icons
- **Nur Icons** — Icon-Raster ohne Text; Name + Beschreibung erscheinen im Tooltip

### Neue Icons im HiCAD-Stil (blau=Bestand / rot=Aktion)
Vier neue SVGs ersetzen generische Platzhalter:
- `glas-als-dxf` (Glasscheibe → DXF-Dokument) statt `cad-chamfer`
- `wilp-gelaender-bogen` (Schlaufen auf Bogen-Blech) statt `ki-aktiv`
- `wilplinger-kombi` (Schlaufen auf gerade+Bogen-Blech) statt `cad-extrude`
- `wilp-blechgroesse` (Blech + Maßpfeile + Lupe) statt `cad-dimension`
- „Schweißnaht" nutzt jetzt das vorhandene `cad-weld` statt `generic-wrench`

### Icon-Auswahl im Hinzufügen/Bearbeiten-Dialog erweitert
21 zusätzliche Icons im HiCAD-Stil (blau=Bestand / rot=Aktion), damit die Symbol-Auswahl
für eigene Einträge deutlich größer ist. Der Picker liest automatisch alle `*-256.png` aus dem
icons-Ordner — kein Code, keine Registrierung; neue Icons erscheinen beim nächsten Öffnen des Dialogs.

- Verbindungen: `cad-bolt`, `cad-nut`, `cad-thread`, `cad-countersink`
- Stahlbau/Blech: `cad-notch` (Ausklinkung), `cad-miter` (Gehrung), `cad-unfold` (Abwicklung), `cad-bend` (Kantung)
- Zeichnung/Bemaßung: `cad-bom` (Stückliste), `cad-posnr` (Positionsnummer), `cad-angle-dim` (Winkel), `cad-measure` (Abstand)
- Analyse: `cad-collision` (Kollision), `cad-pointcloud` (Punktwolke)
- Export: `export-step`, `export-pdf`
- Allgemein: `cad-copy`, `cad-delete`, `generic-filter`, `generic-sync`
- Hinweis: `<text>` wird vom Skia-Renderer verschluckt (Font nicht garantiert) — Beschriftungen daher
  rein grafisch gelöst (z.B. Würfel = STEP vs. Zeilen = PDF, stilisierte „1" im Positions-Ballon).

### Plugin-Logo zentral (Marketing-Icon vorbereitet)
Das Plugin-Logo wird jetzt an allen Stellen aus `<iconRoot>\plugin-icon-{16,32,256}.png` geladen: Pane-Header, „Toolbox öffnen"-Button, Toolbox-Header + Toolbox-Fenster-Icon. Sobald das finale Marketing-Icon kommt: nur `icons-source/plugin-icon.svg` ersetzen + `build_icons.py` laufen lassen (oder die drei PNGs direkt tauschen) — kein Code-Änderung nötig, ↻ Reload genügt.

### Build
- AssemblyVersion 1.0.18.0

## v1.0.17 — 2026-05-14

### Strong-Name-Signing
Das Plugin wird ab dieser Version **strong-name-signiert** (.snk-Schlüssel im Repo) — wichtig damit Plugin-Verwaltungs-Tools die Identität + Version zuverlässig auslesen können (`PublicKeyToken=b2648ba517bf81ec`).

- Neue Datei: `src/HiCADHelpTools.snk` (Strong-Name-Key-Paar, via `sn.exe -k` generiert)
- `csproj`: `<SignAssembly>true</SignAssembly>` + `<AssemblyOriginatorKeyFile>HiCADHelpTools.snk</AssemblyOriginatorKeyFile>`
- AssemblyName, AssemblyVersion, FileVersion, ProductName, CompanyName lesen sich aus der DLL auch ohne HiCAD-Laufzeit (über `System.Reflection.AssemblyName.GetAssemblyName` bzw. `System.Diagnostics.FileVersionInfo`)

### Dual-Deploy: HiCAD-Live + Toolbar-Mirror
Bei jedem Build wird die DLL parallel an **zwei Ziele** kopiert:

1. `C:\HiCAD\HiCAD_3102\exe\Plugins\` — Live-Plugin für sofortiges Testen
2. `D:\01 Toolbar\99 Plugins\06 Plugin für Scripte\exe\Plugins\` — Distributions-Mirror für das Plugin-Verwaltungs-Tool

Struktur folgt dem `05 StepExport`-Muster:
```
06 Plugin für Scripte\
└── exe\
    └── Plugins\
        ├── HiCAD-HELP.com.Tools.dll
        ├── HiCAD-HELP.com.Tools.pdb
        └── HiCAD-HELP-Tools\
            └── icons\
                └── *.png  (126 Stück)
```

### Post-Build-Skript: PowerShell statt batch
Der Mirror-Schritt ist jetzt `deploy/post_build_copy.ps1` (PowerShell statt `.cmd`):
- Sauberer Umgang mit Umlauten in Pfaden (Ordner heißt "Plugin **für** Scripte")
- Pfadbestandteil mit Umlaut wird über `[char]0x00FC` codiert (Encoding-unabhängig)
- BOM-prefixed UTF-8 für zuverlässiges PowerShell-Parsing
- Failed-but-not-fatal-Logik bleibt: wenn HiCAD die DLL lockt, wird das Live-Deploy übersprungen, der Toolbar-Mirror trotzdem durchgeführt
- `SolutionDir` wird via `$PSScriptRoot/..` abgeleitet → robust gegen `$(SolutionDir)`-trailing-backslash-Quote-Probleme im MSBuild-Aufruf

### Build
- AssemblyVersion 1.0.17.0
- DLL beider Zielorte tragen jetzt `PublicKeyToken=b2648ba517bf81ec`

## v1.0.16 — 2026-05-11

### Alle Gruppen mit einem Klick auf/zuklappen
Zwei neue Icon-Buttons im Header (Pane + Toolbox) klappen mit einem Klick **alle Gruppen** auf oder zu. Praktisch für Video-Aufnahmen oder schnelles Aufräumen.

**Neue Icons im HiCAD-Stil:**
- **`toolbar-expand-all`** — drei zugeklappte Gruppen-Header (blau) mit Doppel-Chevron nach unten (rot) = „alle aufklappen"
- **`toolbar-collapse-all`** — aufgeklappte Gruppe mit Items (blau) und Doppel-Chevron nach oben (rot) = „alle zuklappen"

**Positionen:**
- **Pane:** neben dem `↻`-Reload-Button oben rechts, in 20×20-Größe
- **Toolbox:** im Header-Bar links neben „+ Hinzufügen", in 22×22

Klick speichert den Zustand sofort in `tools.json` (`isExpanded` pro Gruppe).

### Neue Commands
- `PluginPaneViewModel.ExpandAllCommand` / `.CollapseAllCommand`
- `ToolboxViewModel.ExpandAllCommand` / `.CollapseAllCommand`
- `ExpandAllIcon` / `CollapseAllIcon` Properties (via `IconResolver`) — Icon-Source ist datengebunden, dadurch wird der Cache nach Reload korrekt geleert

### Build
- AssemblyVersion 1.0.16.0

## v1.0.15 — 2026-05-11

### Gruppen auf-/zuklappbar (Video-Modus)
Gruppen-Header sind jetzt **klickbar** — Klick togglt zwischen aufgeklappt (▼) und zugeklappt (▶). So lassen sich für Video-Aufnahmen oder Demos einzelne Gruppen ausblenden, ohne dass sie ganz verschwinden.

- **Pane:** Klick auf Header-Pill → Tiles erscheinen/verschwinden, Pfeil-Glyph wechselt
- **Toolbox:** gleiches Pattern mit größerem Header
- **Zustand wird persistiert** in `tools.json` pro Gruppe (`isExpanded`-Feld)
- **Default neue Gruppen: aufgeklappt** (Rückwärtskompatibel — Gruppen ohne das Feld sind expanded)

### Schema-Erweiterung
`GroupConfig` hat ein neues Feld `isExpanded` (bool, default true). Bestehende `tools.json`-Dateien funktionieren weiter; bei nächstem Save wird das Feld pro Gruppe hinzugefügt.

### Build
- AssemblyVersion 1.0.15.0

## v1.0.14 — 2026-05-11

### Bearbeitungs-Dialoge auf v1.0.13-Niveau gehoben
AddItem-Dialog (Hinzufügen/Bearbeiten) und Nutzungsbedingungen-Dialog bekommen das gleiche moderne UI-Pattern wie Toolbox + Pane.

**AddItemDialog (Hinzufügen / Bearbeiten):**
- **Header-Bar** mit linkem blauen Marker + Titel („Neuen Eintrag hinzufügen" oder „Eintrag bearbeiten") + Untertitel-Hinweis „Pflichtfelder: Titel · Script-Datei · Gruppe · Icon"
- **Vier benannte Sektionen** mit eigenem blauen Marker links: „Allgemein", „Skript", „Gruppe", „Icon"
- **Field-Hints** unter jedem Feld erklären, was es bewirkt (z.B. „Erscheint als Tooltip auf dem Tile")
- **Browse-Button** mit 📁-Folder-Icon
- **Footer-Bar** mit Helper-Text links („Änderungen werden sofort in tools.json gespeichert…") + Buttons rechts
- Icon-Picker mit erhöhter Vorschaugröße (54 px) + dezenter Hover-Border

**TermsDialog (Erst-Start):**
- Selbe Header-Bar mit Marker + Untertitel
- Größere Schrift (12.5 pt, line-height 20) + Sub-Headings in Accent-Blau
- Akzeptanz-Checkbox in eigenem Bereich mit oberer Border-Trennlinie
- Footer mit Primary + Secondary Buttons (statt schwebenden Inline-Buttons)

### Neue Helper-Styles in `ModernStyles.xaml`
- `FieldLabel` — kleinerer Title-Style für Eingabe-Feld-Labels (12 pt SemiBold, Accent-Farbe)
- `FieldHint` — 11 pt Hilfetext in TextSecondary, wrappable
- `SectionDivider` — dünne 1 px-Trennlinie für Section-Übergänge

### Build
- AssemblyVersion 1.0.14.0

## v1.0.13 — 2026-05-11

### Gruppen-Header prominent hervorgehoben
Vorher waren die Gruppen-Namen nur kleine graue Captions (11pt). Jetzt deutlich präsent:

**Im Pane:**
- Heller blau-grauer Hintergrund (`#F1F5F9`) mit 6 px CornerRadius
- **4 px breiter blauer Marker links** als visueller Anker
- Gruppen-Name in 13pt Bold, AccentBrush-Farbe
- **Anzahl-Pill rechts** (blauer abgerundeter Badge mit weißer Item-Count-Zahl)

**Im Toolbox-Window:**
- **5 px breiter blauer Marker links** (größer, prominenter)
- Gruppen-Name 17pt Bold + Untertitel "N Eintrag/Einträge" in TextSecondary
- **Großer Anzahl-Pill rechts** (12 px CornerRadius, 13pt Bold weiße Zahl)

Visuell ist sofort klar, wo eine Gruppe anfängt und wie viele Items sie enthält.

### Build
- AssemblyVersion 1.0.13.0

## v1.0.12 — 2026-05-11

### Modernes UI-Design
Zentrales **`ModernStyles.xaml`** ResourceDictionary unter `src/Ui/Common/` mit konsistenter Design-Sprache, in Pane + Toolbox + Add-Dialog eingebunden.

**Farb-Palette:**
- Hintergrund `#FAFBFC` (sehr helles Blaugrau statt Standard-Grau)
- Surface (Cards) `#FFFFFF` mit dünnen `#E1E4E8`-Borders
- Primary `#0078D4` (Klick-Hover: `#106EBE`, Pressed: `#005A9E`)
- Text primär `#1F2937` / sekundär `#6B7280`

**Wiederverwendbare Styles:**
- `PrimaryButton` — abgerundeter blauer Button mit Hover/Pressed-States, kein Border, Cursor=Hand
- `SecondaryButton` — heller, mit feinem Border, Hover-Background
- `IconButton` — kreisförmig, Hover-Effekt, für `↻` o.ä.
- `PaneTileButton` — Card-Style mit `BorderHover` → blau-Highlight, sehr cleaner Look
- `ToolboxTileButton` — größere Cards mit 10 px CornerRadius
- `ModernTextBox` — 5 px CornerRadius, Focus-Highlight (Border wird primary-blau)
- `ModernComboBox` — größerer Padding, 32 px MinHeight
- `SectionHeader` — kleinere SemiBold-Caption für Gruppen-Titel
- `PaneTitle` + `ToolboxGroupHeader` — größere Bold-Titles

### UI-Änderungen im Detail

**Pane:**
- Header mit größerem Title + Icon-Button-Style für Reload
- Tiles als Cards: 40×40-Icon-Container mit Hintergrund-Box, Title rechts mit Ellipsis
- Gruppen-Header als dezente Caption (statt Expander)
- Footer mit abgerundetem Border (`CornerRadius=8`) — keine scharfen Ecken mehr
- Toolbox-Button am Boden mit 📦-Icon, größerer Padding

**Toolbox-Window:**
- Header-Bar oben mit großem Titel + Untertitel-Hinweis
- „+ Hinzufügen" als prominenter Primary-Button im Header
- „↻ Reload" als Secondary-Button
- Tiles als Card-Style mit Hover-Lift (blaues Border)
- Footer-Bar mit white-pill für TileSize-Anzeige

**AddItemDialog:**
- Header-Bar oben + Footer-Bar mit Buttons rechts unten (Material-Design-Pattern)
- Modern TextBoxen mit Focus-Border
- Icon-Picker mit größeren Vorschauen (52 px) und blauem Selected-State
- Buttons rechts unten: Abbrechen (Secondary) + OK (Primary)

### Build
- AssemblyVersion 1.0.12.0

## v1.0.11 — 2026-05-11

### Plugin umbenannt: ISD Austria Tools
Alle vom User sichtbaren Strings auf den neuen Namen umgestellt:
- `Plugin.Name` → "ISD Austria Tools"
- `AssemblyTitle`, `AssemblyProduct` → "ISD Austria Tools"
- `AssemblyCompany` → "ISD Austria"
- Pane-Header (TextBlock) → "ISD Austria Tools"
- Toolbox-Window-Title → "ISD Austria Tools — Toolbox"
- HiCAD-Menü Top-Level → "ISD Austria Tools"
- TermsDialog-Title + Überschrift → "ISD Austria Tools"

DLL-Dateiname (`HiCAD-HELP.com.Tools.dll`), AppData-Folder (`HiCAD-HELP-Tools`) und Acceptance-Datei bleiben aus Kompatibilitäts-Gründen unverändert — würde sonst alle bestehenden Konfigurationen und den `Plugins.config`-Eintrag invalidieren.

### Pane-Layout: Toolbox-Button fix am unteren Rand
Vorher: Toolbox-Button im Header oben — wenn der Status-Footer mehrzeilig wuchs (lange Fehlermeldung), wanderte alles weiter nach oben.

Jetzt: Pane hat **4 Rows** (Header, ScrollViewer*, Footer, **Action-Button**). Der `Toolbox öffnen…`-Button ist die letzte Zeile und bleibt **immer am unteren Pane-Rand fixiert** — egal wie der Status-Footer wächst. Header oben enthält jetzt nur noch den Title + den kleinen `↻`-Reload-Button rechts oben.

### Build
- AssemblyVersion 1.0.11.0

## v1.0.10 — 2026-05-11

### Use-Case-Icons mit deutlich mehr Rot-Anteil
Die spezifischen Skript-Icons hatten Rot nur in kleinen Markierungen — jetzt ist die Aktion-Komponente prominent sichtbar.

- **`ki-aktiv`** — Flüssigkeit + alle Blasen sind jetzt rot, größere LED mit Glanz-Strahlen.
- **`bohrungsanalyse`** — zwei große rote markierte Bohrungen mit Durchmesser-Maßpfeilen, deutlich größere rote Lupe (40 px Radius statt 22) mit eingezoomter roter Bohrung.
- **`gelaender-anschnitt`** — die abgeschnittenen Profil-Enden (am Stoß) sind jetzt komplett rot gefüllt; Schnittlinie als kräftiger 8 px roter Strich; Aktion-Pfeile größer.
- **`wilplinger-schlaufen`** — Schlaufen jetzt 9 px dick (vorher 6), kräftiger roter Handlauf 8 px mit Knoten-Punkten, **plus rotes hinteres Blech** als zweites Segment.
- **`wilplinger-schlaufen-bogen`** — komplett gefüllter roter Bogen-Bereich am Zylindermantel statt nur einer dünnen Kurve; größere Lupe (34 px) mit „R?"-Text; Achsen-Pfeil mit Z-Label.
- **`wilplinger-schlaufen-bemassung`** — fünf Maßlinien statt zwei (horizontal + vertikal pro Ansicht + Diagonal-Maß), dickere rote Pfeile, alle mit Maßzahlen.
- **`formrohr-end-cap`** — Endkappe deckend rot gefüllt (opacity 0.85 statt 0.55), zusätzlicher roter Aktion-Pfeil von oben „die Kappe wird aufgesetzt".
- **`plugin-icon`** — H-Logo mit prominentem rotem Schraubenschlüssel-Symbol diagonal + roter „Power"-LED.

### Status
- 120 PNGs deployt nach `…\Plugins\HiCAD-HELP-Tools\icons\`
- AssemblyVersion 1.0.10.0 (DLL funktional unverändert)

## v1.0.9 — 2026-05-11

### Icon-Bibliothek auf 40 Symbole erweitert
Konsistent im HiCAD-Pattern (Bestand blau, Aktion rot).

**Drei generic-Icons als Aktion umgefärbt:**
- `generic-wrench` — komplett rot (Werkzeug-Aktion)
- `generic-hammer` — komplett rot
- `generic-magnifier` — komplett rot (Suchen / Analysieren)

**16 neue CAD-spezifische Icons:**
- `cad-sketch` — Bleistift (rot) zeichnet Skizzen-Linien (blau gestrichelt)
- `cad-dimension` — Werkstück (blau) mit Maßlinie + Pfeilen + Maßzahl (rot)
- `cad-mirror` — Original-Profil (blau), Spiegelachse + Spiegelbild (rot)
- `cad-rotate` — Quader (blau), 270°-Rotationspfeil mit Spitze (rot)
- `cad-move` — Original gestrichelt (blau), neue Position (blau), Verschiebepfeil (rot)
- `cad-trim` — zwei sich kreuzende Linien (blau), Schnittpunkt mit X-Marker (rot)
- `cad-fillet` — L-Form (blau), Verrundungs-Bogen + R-Symbol (rot)
- `cad-chamfer` — abgekantetes Polygon (blau), Fasenkante mit Hilfslinien (rot)
- `cad-boolean-union` — Quader (blau) + überlappender Kreis (rot) + Plus-Symbol
- `cad-boolean-cut` — Quader (blau) mit gestricheltem Loch + Minus-Symbol (rot)
- `cad-beam` — Iso-I-Träger (rein blau, Standard-CAD-Element)
- `cad-sheet` — Iso-Blechteil mit Biegekante (rein blau)
- `cad-weld` — zwei Bauteile (blau) verbunden mit Zickzack-Schweißnaht (rot)
- `cad-drill` — Iso-Blech mit Bohrloch (blau), Bohrer + Pfeil von oben (rot)
- `cad-extrude` — 2D-Profil (blau), Extrusions-Tiefenpolygon + Richtungspfeil (rot)
- `cad-pattern` — Original (blau) + 8 Kopien im Raster (rot) mit Richtungspfeilen

### Status
Icon-Picker im AddItem-Dialog zeigt jetzt **40 Vorlagen** zur Auswahl. Die Symbole sind sofort live (PNGs deployt nach `…\Plugins\HiCAD-HELP-Tools\icons\`). Im Toolbox-Dialog `↻ Reload` drücken oder im Pane neu laden, dann sind die neuen Icons im Picker sichtbar.

### Build
- AssemblyVersion 1.0.9.0 (DLL funktional unverändert).

## v1.0.8 — 2026-05-11

### Icons im HiCAD-Stil: Bestand blau, Aktion rot
HiCAD-Konvention: bestehende Geometrie wird **blau** dargestellt, was die Bearbeitung bewirkt/markiert/anlegt **rot**. Alle Use-Case-Icons entsprechend überarbeitet:

- **`formrohr-end-cap`** — Profil bleibt blau (transparent), die hinzugefügte Endkappe ist jetzt **rot** mit gestrichelter Innen-Kontur in rot.
- **`bohrungsanalyse`** — Blech + Bohrungen blau; Lupe **rot**, plus roter gestrichelter Mess-Pfeil von einer Bohrung zur Lupe.
- **`gelaender-anschnitt`** — Posten + Lauf-Gurt blau; Anschnitt-Linie als kräftiger **roter** Strich mit zwei roten Aktion-Pfeilen, die auf die Schnittstelle zeigen.
- **`wilplinger-schlaufen`** — Pfosten + Frontblech bleiben blau; Schlaufen + oberer Handlauf jetzt in **rot** (= das was das Skript erzeugt).
- **`wilplinger-schlaufen-bogen`** — Zylinder blau; erkannte Bogen-Kurve, Achsen-Pfeil und Diagnose-Lupe alle in **rot**.
- **`wilplinger-schlaufen-bemassung`** — bereits korrekt (Maße rot).
- **`gelaender-anschnitt-bemassung`** — bereits korrekt.

Bei den **generischen Icons** wurden die Aktions-Symbole umgefärbt:
- **`generic-arrow-right`** — Pfeil komplett **rot** (Aktion).
- **`generic-play`** — Kreis blau, Play-Dreieck **rot**.

Die übrigen generic-Icons (`wrench`, `gear`, `hammer`, `cube`, `check`, `star`, `folder`, `magnifier`, `chart`, `lightbulb`, `database`, `code`, `document`, `calc`) bleiben blau, da sie keine Bearbeitungs-Semantik haben.

### Build
- AssemblyVersion 1.0.8.0
- Icons direkt nach `…\Plugins\HiCAD-HELP-Tools\icons\` deployt (PNGs sind nicht gelockt, auch wenn HiCAD läuft). DLL-Bump nur für Versions-Stempel — funktional unverändert.

## v1.0.7 — 2026-05-10

### Neue Funktion: Items bearbeiten + löschen
- **Rechtsklick auf Toolbox-Tile** → erweitertes Kontextmenü mit zwei neuen Einträgen:
  - **„Bearbeiten…"** — öffnet den AddItemDialog mit allen Feldern vorausgefüllt (Titel, Beschreibung, Pfad, Gruppe, Icon). Speichern verschiebt das Item bei Bedarf in eine andere Gruppe; ID bleibt stabil. Wird die Original-Gruppe leer, wird sie automatisch entfernt.
  - **„Löschen…"** — Sicherheitsabfrage („Eintrag wirklich löschen?"), dann Eintrag aus `tools.json` entfernen. Script-Datei selbst bleibt erhalten. Leere Gruppe wird automatisch aufgeräumt.
- **AddItemDialog** unterstützt Edit-Mode: Titel + OK-Button-Text sind ans `IsEditMode`-Flag gebunden („Eintrag bearbeiten" / „Speichern" statt „Neuen Eintrag hinzufügen" / „Hinzufügen").
- **AddItemViewModel** zweiter Konstruktor `(groups, iconRoot, existingItem, currentGroupName)` für Edit-Mode. Ursprungs-ID + Ursprungs-Gruppe werden im Result mitgeliefert, damit der Caller das Original gezielt entfernen kann.
- **ToolboxTileViewModel** kennt jetzt seine `GroupName` und exposed `EditCommand` + `DeleteCommand`. Constructor-Erweiterung um zwei `Action<ToolboxTileViewModel>`-Callbacks.

### Wichtig
Edit/Delete sind nur über den Toolbox-Dialog erreichbar (Rechtsklick auf Tile). Pane und Menü sind read-only — sie spiegeln nur die Konfiguration.

## v1.0.6 — 2026-05-09

### Neue Funktion: Items per Dialog hinzufügen
- **„+ Hinzufügen"-Button** im Toolbox-Footer (links neben „↻ Reload") öffnet einen Dialog zum Anlegen neuer Items.
- **AddItemDialog** mit Feldern: Titel, Beschreibung, Script-Pfad (Browse-Button öffnet Datei-Auswahl), Gruppe (Combo: existierende Gruppen oder „+ Neue Gruppe…" mit Eingabefeld), **Icon-Picker** als Grid mit allen verfügbaren Icons aus `iconRoot`.
- Beim Speichern: ID wird aus dem Titel slugifiziert (mit Umlaut-Übersetzung), Konflikte automatisch durch Suffix `-2`/`-3`/… aufgelöst. `tools.json` wird atomar geschrieben, danach Toolbox-Reload.
- Validierung: Titel + Script-Pfad + Icon sind Pflicht; Script-Datei muss existieren; bei neuer Gruppe ist der Name Pflicht.

### 14 mitgelieferte Beispiel-Icons
Generische SVGs im einheitlichen HiCAD-Stil — auswählbar im Icon-Picker:
- `generic-wrench` (Schraubenschlüssel)
- `generic-gear` (Zahnrad)
- `generic-hammer` (Hammer)
- `generic-cube` (3D-Würfel)
- `generic-arrow-right` (Pfeil rechts — Aktion)
- `generic-check` (grünes Häkchen)
- `generic-star` (Stern — Favorit)
- `generic-folder` (Ordner)
- `generic-magnifier` (Lupe)
- `generic-chart` (Säulendiagramm)
- `generic-lightbulb` (Glühbirne — Idee)
- `generic-database` (Datenbank-Symbol)
- `generic-code` (`</>`-Klammern)
- `generic-play` (Play-Button)
- `generic-document` (Dokument mit Eselsohr)
- `generic-calc` (Taschenrechner)

### Build
- `post_build_copy.cmd` failt den Build nicht mehr, wenn die DLL gerade von HiCAD gelockt ist — er warnt nur. Erlaubt Iteration, ohne HiCAD jedes Mal zu schließen.
- AssemblyVersion 1.0.6.0.

## v1.0.5 — 2026-05-09

### Neue Gruppe: Test
- Neue Gruppe **„Test"** ganz oben mit dem Test-Slot **KI Aktiv** (`C:\HiCAD\HiCAD_3102\custom\KI\Kunden\KI_Aktiv.cs`).
- KI_Aktiv ist der aktuelle Test-Slot: Inhalt wird vom KI-Assistenten bei jeder Iteration überschrieben — Plugin bindet die Datei dauerhaft ein, kein Strg+J nötig.
- Neues SVG-Icon `ki-aktiv.svg`: Erlenmeyerkolben mit blauer Flüssigkeit, aufsteigende Blasen, roter „Aktiv"-LED rechts oben.

## v1.0.4 — 2026-05-09

### Fix: Pane-Tile-Status wird live aktualisiert
- **Pane-Reload-Button** (↻) im Header neben "Toolbox öffnen…". Liest `tools.json` neu, leert IconCache, baut alle Tiles neu auf. Kein HiCAD-Restart mehr nötig wenn Skript-Dateien hinzugekommen sind oder Icons getauscht wurden.
- **`ScriptExists`-Refresh** nach jedem Script-Run: WPF wertet `IsEnabled`-Binding für alle Pane-Tiles neu aus, damit ein Skript das eine andere Datei erzeugt sofort die zugehörigen Tiles aktiviert.
- **`PaneTileViewModel.RefreshScriptExists()`** Methode für externes INPC-Triggering.
- `PluginPaneViewModel` nimmt jetzt `ConfigLoader` als Konstruktor-Argument für Reload-Funktion.

### Hintergrund
Vorher wurde `ScriptExists` (= `File.Exists`) nur einmal beim Plugin-Init evaluiert. WPF cached den Wert; ein nachträglich erstelltes Skript blieb ausgegraut bis HiCAD neu gestartet wurde.

## v1.0.3 — 2026-05-09


### Neue Gruppe: Kunden
- Neue Gruppe **„Kunden"** mit drei Wilplinger-Scripts aus `C:\HiCAD\HiCAD_3102\custom\KI\Kunden\`:
  - **Wilplinger Schlaufengeländer** — Schlaufengeländer mit Dialog (Schemabild, hinteres Blech in zwei Segmenten, Front-Blech-Länge anpassbar).
  - **Wilplinger Schlaufeng. Bogen — Phase 1 Zylinder** — Diagnose-Skript: erkennt Zylinder-Achse, Radius und Bogen-Bereich aus einer ausgewählten Facet.
  - **Wilplinger Schlaufengeländer — Bemaßung** — Erzeugt Zeichnungsblatt mit 3 Ansichten + 6 Demo-Bemaßungen.
- Drei neue SVG-Icons im technischen-isometrischen Stil (`wilplinger-schlaufen.svg`, `wilplinger-schlaufen-bogen.svg`, `wilplinger-schlaufen-bemassung.svg`).
- `DefaultConfigBuilder.KundenRoot` Konstante für Kunden-Skript-Pfade.

## v1.0.2 — 2026-05-08

### Refactoring
- **PluginPaths**: Zentrale Konstanten-Klasse für alle App-Pfade (`%APPDATA%\HiCAD-HELP-Tools\`, Log-Verzeichnis, Akzeptanz-Datei). Eliminiert Magic-Strings in `FileLogger`, `ConfigLoader`, `TermsService`.
- **ScriptLauncher**: Gemeinsamer Helper für Script-Ausführung mit Status-Feedback und MessageBox-Behandlung. DRY-Refactor von `PaneTileViewModel` und `ToolboxTileViewModel`.
- **ScriptStatusEvent**: Strukturiertes Status-Event statt String-Callback (enthält `Kind` + `Title` + `Message`).

### Performance
- **IconResolver**: Cache für geladene PNGs — vermeidet wiederholtes Disk-IO. `ClearCache()` wird bei Toolbox-Reload aufgerufen, damit neue Icons sichtbar werden.
- **StatusBrushes**: Statische, gefrorene `SolidColorBrush`-Instanzen für Status-States (Neutral / Running / Success / Error).

### UX
- **Visueller Status-State**: Pane- und Toolbox-Footer ändern Hintergrundfarbe je nach Script-Ausgang (HiCAD-Blau ruhend → Amber während Lauf → Grün bei Erfolg → Rot bei Fehler).
- **Pane Versions-Pill**: Foreground auf dunkles Blau (#1F3A5F) umgestellt — bleibt lesbar bei wechselnden Footer-Farben.

### Robustheit
- **Plugin.Dispose**: Schließt offene Toolbox-Window, falls noch geöffnet.
- **WindowGeometry**: Wenn Window minimiert geschlossen wird, werden Left/Top/Width/Height NICHT mehr persistiert (vorher: garbage values gespeichert).
- **Plugin.Version**: Liest jetzt aus Assembly statt hardcoded `new Version(1, 0, 0, 0)`.

### Build & Versioning
- AssemblyVersion + AssemblyFileVersion auf `1.0.2.0` angehoben.

## v1.0.1 — 2026-05-08

### Polish (basierend auf Final-Review)
- `PaneTileViewModel.Run()`: zeigt MessageBox bei Script-Fehler (war stumm — nur Status-Zeile).
- `PluginPaneControl.xaml`: Pane-Tile graut aus wenn Script-Datei fehlt (`IsEnabled={Binding ScriptExists}`).
- `PluginPaneViewModel`: Version aus Assembly statt hardcoded.
- `ConfigLoader.LastLoadFellBackToDefault`: signalisiert Fallback bei korrupter `tools.json`. Pane-Status zeigt entsprechende Warnung.
- `Plugin.OpenToolbox`: `Owner = HiCAD-MainWindow` (Minimize/Restore-Verhalten) + stale-ref clear vor neuer Window-Erstellung.
- `TermsDialog`: korrekter Klassenname `HiCAD.Scripting.HicadScriptCompiler` statt veraltetem `ISD.Scripting.ScriptCompiler`.
- `IconResolver`: Sichtbares graues X als Fallback-Icon (vorher: unsichtbares Transparent).
- README.md hinzugefügt.

## v1.0.0 — 2026-05-08

### Initial Release
- Plugin lädt 3 vorkonfigurierte Scripts (Stahlbau / Geländer / Analyse) aus `C:\HiCAD\HiCAD_3102\custom\KI\`.
- Drei UI-Pfade: HiCAD-Menü (UserMenu), Plugin-Pane (Sidebar), modeless Toolbox-Dialog.
- Toolbox-Dialog mit Größen-Slider 48–256 px, Reload-Button, persistierter Geometrie.
- Rechtsklick auf Toolbox-Tile: Script-Datei öffnen / Im Explorer zeigen / Pfad kopieren.
- JSON-Config in `%APPDATA%\HiCAD-HELP-Tools\tools.json` (autom. erzeugt mit Defaults).
- Bitmap-Pipeline: SVG-Sources + Python-Build-Skript erzeugen 16/32/256 px PNGs.
- Erst-Start-Nutzungsbedingungen-Dialog.
- Auto-Deploy Post-Build (DLL + Icons → HiCAD\Plugins).
- Diagnostisches File-Logging unter `%APPDATA%\HiCAD-HELP-Tools\logs\`.
