# 🐸 Wetterfrosch

Wetter- und Tourenplanungs-App als **einzelne HTML-Datei**. Sie kombiniert fünf Wettermodelle zu einer gemeinsamen Vorhersage, zeigt ein schnelles DWD-Regenradar und bewertet geplante Touren mit Wetter-, Lawinen- und Luftqualitätsdaten.

> **Hinweis:** Wetterfrosch ist ein privates Projekt für den Freundeskreis und ausdrücklich **kein professionelles Wetter- oder Sicherheitstool**. Die Anzeigen ersetzen weder amtliche Wetter- und Lawinenwarnungen noch eine eigene Einschätzung vor Ort. Die Nutzung erfolgt auf eigene Verantwortung.

---

## Inhalt

- [Überblick](#überblick)
- [Schnellstart](#schnellstart)
- [Funktionen im Detail](#funktionen-im-detail)
  - [Kopfbereich und Ortswahl](#kopfbereich-und-ortswahl)
  - [Tab „7d Vorhersage"](#tab-7d-vorhersage)
  - [Tab „24h Wetter"](#tab-24h-wetter)
  - [Tab „Regenradar"](#tab-regenradar)
  - [Tab „Gebietsvergleich" (Expertenmodus)](#tab-gebietsvergleich-expertenmodus)
  - [Tab „Tourplanung" (Expertenmodus)](#tab-tourplanung-expertenmodus)
  - [Tab „Tourbewertung" (Expertenmodus)](#tab-tourbewertung-expertenmodus)
  - [Speichern und Sichern](#speichern-und-sichern)
- [So entsteht die Vorhersage](#so-entsteht-die-vorhersage)
- [Datenquellen und Quellenangaben](#datenquellen-und-quellenangaben)
- [Datenschutz](#datenschutz)
- [Technik](#technik)
- [Grenzen und bekannte Einschränkungen](#grenzen-und-bekannte-einschränkungen)
- [Versionsverlauf](#versionsverlauf)

---

## Überblick

| Bereich | Was die App bietet |
|---|---|
| **Vorhersage** | 7-Tage-Übersicht und Stundenvorhersage, berechnet aus 5 Wettermodellen, auf die Höhe des gewählten Ortes angepasst |
| **Regenradar** | DWD-Radar der letzten Stunde plus etwa 2 Stunden Vorhersage, mit Regen-Info in Worten für den eigenen Ort und Punktabfrage per Tipp |
| **Touren** | Mehrtägige Tourenplanung (Wandern, Rad, Bergwanderung) mit Karte, Höhenprofil, Wetterbewertung je Etappe, Lawinenlage und Luftqualität |
| **Bedienung** | Auf dem Handy optimiert, zwei Ansichtsmodi (Anfänger/Experte), Favoriten und automatisches Speichern |

---

## Schnellstart

1. Die Datei `wetterfrosch.html` in einem aktuellen Browser öffnen (Chrome, Safari, Firefox, Edge). Eine Internetverbindung ist nötig, weil Wetterdaten und Bibliotheken online geladen werden.
2. Ort eingeben und auf **Suchen** tippen, oder mit dem Pfeil-Symbol den **eigenen Standort** nutzen.
3. Die App startet immer im **Anfängermodus** mit dem Tab **„7d Vorhersage"**.

**Veröffentlichen mit GitHub Pages** (optional): Die Datei als `index.html` ins Repository legen, unter *Settings → Pages* den Branch auswählen, fertig. Über HTTPS funktioniert auch die Standortabfrage des Browsers zuverlässig.

---

## Funktionen im Detail

### Kopfbereich und Ortswahl

- **Ortssuche** mit Live-Vorschlägen (Nominatim/OpenStreetMap, Photon als Ausweichdienst). Die Suche arbeitet weltweit.
- **Geländehöhe:** Zu jedem Ort wird die Höhe abgefragt. Die Modelldaten werden auf diese Höhe kalibriert, angezeigt als „Modelle kalibriert auf … m Höhe".
- **Eigener Standort** per Browser-Ortung.
- **Aktualisieren-Knopf** für einen neuen Datenabruf.
- **Speichern-Menü** (Lesezeichen-Symbol) für Favoriten und Sicherungsdatei, siehe [Speichern und Sichern](#speichern-und-sichern).
- **Statuszeile** mit Hinweis, wie viele der 5 Modelle verwendet wurden und welche nicht.
- **Ansichtsmodus:** *Anfänger* (aktuelles Wetter: 7d Vorhersage, 24h Wetter, Regenradar) oder *Experte* (zusätzlich Tourplanung und Tourbewertung). Auf dem Handy ist die Umschaltung hinter einem kleinen Knopf neben der Statuszeile eingeklappt, damit der Kopfbereich wenig Platz braucht.

### Tab „7d Vorhersage"

- **Detail-Tabelle nach Tagen** für 7 Tage: Wetter-Symbol, Höchst-/Tiefsttemperatur, Regenmenge mit Regenrisiko, Sonnenstunden, Wind und Böen mit Windrichtung, Sonnenauf- und -untergang sowie die Einigkeit der Modelle.
- **Tag antippen:** Ein Tipp auf eine Tageszeile öffnet direkt die Stundenvorhersage dieses Tages im Tab „24h Wetter".
- **Zeitverlauf-Grafik** „Temperatur & Niederschlag" für alle 7 Tage. Die Wochentage stehen mittig unter jedem Tag, mit Trennlinien zwischen den Tagen. Bei schmalen Displays erscheinen nur die Kürzel.
- Alle Werte sind **Ensemble-Mittelwerte** aus den verfügbaren Modellen.

### Tab „24h Wetter"

- **Tagesauswahl** als antippbare Chips für 7 Tage (Wochentag und Datum). Der erste Chip zeigt wie bisher die nächsten 24 Stunden ab jetzt, die übrigen jeweils den ganzen Kalendertag.
- **Detailvorhersage im 2-Stunden-Takt:** Wetter, Temperatur und gefühlte Temperatur, Regenmenge mit Risiko, Gewitterpotenzial (CAPE), Wind mit Richtung und Böen.
- **Grafik „Temperatur"** und **Grafik „Niederschlag & Risiko":** Der Mittelwert ist kräftig hervorgehoben, die Einzelmodelle sind farblich abgeschwächt dahinter zu sehen.
- **Zusammenfassung des gewählten Tages:** Temperatur (Minimum/Maximum), Niederschlag, Wind und Böen, Bewölkung, Sichtweite, Taupunkt und Gewitterpotenzial.
- **Sonnen-Kennzahlen:** Sonnenaufgang, Sonnenuntergang, Tageslänge und der modellierte UV-Index.

### Tab „Regenradar"

Das Radar zeigt die DWD-Messdaten (RV-Komposit, 1 km Auflösung, alle 5 Minuten) der letzten Stunde und eine Vorhersage von etwa 2 Stunden. Die Daten werden mit einer einzigen Anfrage geladen und direkt im Browser gezeichnet. Dadurch erscheint das Radar schnell, und das Abspielen lädt nichts nach.

- **Start:** Karte auf etwa 20 km um den Ort der App, Topo-Karte als Hintergrund, die Animation startet von selbst im Tempo „langsam".
- **Regen-Info in Worten** für den eigenen Ort, zum Beispiel „Regen beginnt in ca. 26 Min (18:50 Uhr) – leichter Regen" oder „Kein Regen in den nächsten 2 Stunden". Der Kasten färbt sich grün (trocken), blau (Regen) oder orange (mäßiger bis starker Regen) und enthält ein kleines Verlaufsdiagramm.
- **Punktabfrage:** Ein Tipp auf die Karte setzt einen Marker. Die Box darunter zeigt für diesen Punkt die Intensität zum gerade gezeigten Zeitpunkt, die Regen-Info in Worten und das Verlaufsdiagramm.
- **Steuerung:** Play/Pause, Zeitleiste mit „Jetzt"-Marke, Tempo (langsam, normal, schnell), Deckkraft, Kartenhintergrund (Topo, hellgrau, Straßen) und „Zum Ort".
- **Farbskala** von Hellblau über Blau, Grün, Gelb und Orange bis Rot, Magenta und Violett (Legende unter der Karte).
- **Nachladen:** Wird die Karte weit verschoben, lädt die App das Radar für den neuen Ausschnitt nach. Beim erneuten Öffnen des Tabs werden Daten, die älter als 5 Minuten sind, neu geholt.
- Das Radar deckt Deutschland und angrenzende Gebiete ab. Außerhalb erscheint eine entsprechende Meldung.

### Tab „Gebietsvergleich" (Expertenmodus)

- **Zehn Gebirgsgruppen im Vergleich:** Wettersteingebirge, Ammergauer Alpen, Karwendel, Bayerische Voralpen, Mangfallgebirge, Chiemgauer Alpen, Estergebirge, Walchenseeberge/Kocheler Berge, Rofan und Berchtesgadener Alpen. Jedes Gebiet hat einen festen Referenzpunkt auf typischer Wanderhöhe (im Quelltext in der Liste `AREAS` änderbar).
- **Kennzahlen je Gebiet** im Wanderfenster 07–19 Uhr, gemittelt über die Wettermodelle der App: Regenwahrscheinlichkeit (Ø und Maximum), Niederschlag, Sonnenstunden, Temperatur, Böen und Gewitterhinweis (CAPE).
- **Tage wählen:** ein oder mehrere Tage der nächsten Woche; bei mehreren wird der Durchschnitt pro Tag gebildet.
- **Sortierung:** „Regen + Sonne" (Summe der Platzierungen), „wenig Regen" oder „viel Sonne". Platz 1 ist als beste Wahl markiert.
- **Tipp auf ein Gebiet** lädt es in die normale Ansicht (7d Vorhersage, 24h Wetter usw.).
- **Grenze:** Ein Referenzpunkt steht für das ganze Gebirge; kleinräumig kann das Wetter deutlich abweichen.

### Tab „Tourplanung" (Expertenmodus)

- **Aktivität:** Wandern, Radfahren oder Bergwanderung. Die Aktivität bestimmt Grenzwerte und Geschwindigkeitsannahmen.
- **Mehrtagestouren** mit 1 bis 6 Tagen und frei wählbarem Startdatum.
- **Etappenplanung:** Für Tag 1 werden Start und Ziel festgelegt, das Ziel eines Tages wird automatisch zum Start des Folgetages. Zwischenpunkte sind möglich, und eine neue Zieleingabe ersetzt den bisherigen Kartenpunkt sofort.
- **Orts- und Zielsuche** für die Tour, bewusst auf Deutschland, Österreich, die Schweiz und Italien beschränkt, unabhängig von der allgemeinen Ortssuche.
- **Karte** mit den Etappen und **Höhenprofil**; Strecke, Höhenmeter im Anstieg und Abstieg sowie eine geschätzte Dauer je Etappe.

### Tab „Tourbewertung" (Expertenmodus)

- **Tourtauglichkeit je Etappe** als Punktwert von 0 bis 100 mit Einstufung von „Sehr gut" bis schlecht. Der Wert startet bei 100, und Abzüge entstehen unter anderem durch Hitze oder Kälte, Regenrisiko und -menge, Wind und Böen, Sicht, Gewitter (Wettercode und CAPE), Schnee und hohe UV-Belastung.
- **Bergwanderung:** zusätzlich Bewertung von Null- und Schneefallgrenze im Vergleich zur Tourhöhe.
- **Transparenz:** Die Abzüge werden einzeln mit Begründung angezeigt. Fehlen sicherheitsrelevante Daten, begrenzt die App den Wert nach oben und kennzeichnet die Datenqualität als vollständig, eingeschränkt oder kritisch.
- **Wetterwarnungen:** Etappen mit einem Wert unter 60 werden als Warnung hervorgehoben. Die Warnungen werden aus den Wetterdaten abgeleitet.
- **Beste Zeitfenster:** Pro Tag schlägt die App bis zu zwei zusammenhängende Zeitfenster von 3 bis 4 Stunden mit dem besten Wetter vor.
- **Wetterdetails je Etappe:** Temperatur, Windrichtung, Wind, Böen, Regenrisiko, Niederschlag, Sicht und Tourdauer.
- **Lawinenlage:** Amtliche Lawinenlageberichte werden nur bei eindeutiger Zuordnung des Gebiets übernommen und beeinflussen dann die Bewertung. Die Quellen sind unter [Datenquellen](#datenquellen-und-quellenangaben) aufgeführt.
- **Luftqualität** je Etappe (Open-Meteo Air Quality).

### Speichern und Sichern

- **Automatisches Speichern** von Ort, Ansicht und Tourplanung im Browser (lokal, `localStorage`). Beim nächsten Öffnen sind Ort und Tour wieder da. Die Ansicht startet unabhängig davon immer im Anfängermodus mit der 7d Vorhersage.
- **Favoriten:** Aktuellen Ort merken, später aus der Liste „Gespeicherte Orte" laden oder löschen.
- **„Ort und Tourplanung merken"** speichert beides gemeinsam.
- **Sicherungsdatei:** Als Datei sichern und wieder laden, zum Beispiel für den Wechsel auf ein anderes Gerät.
- Das Speichern-Fenster passt sich auf dem Handy der Bildschirmbreite an und ist scrollbar.

---

## So entsteht die Vorhersage

- **Fünf Wettermodelle** über Open-Meteo: ECMWF IFS (0,25°), GFS (USA), ICON (Deutschland), UKMO (Großbritannien) und GEM (Kanada).
- **Ensemble:** Die Modelle werden zeitlich aufeinander abgestimmt und zu Mittelwerten zusammengeführt. Bei Temperatur und Niederschlag kommen robuste Konsens-Verfahren zum Einsatz, die einzelne Ausreißer abschwächen.
- **Modellqualität:** Modelle mit unvollständigen oder unplausiblen Daten werden verworfen und in der Statuszeile genannt. Die App prüft außerdem, ob die Zeitachsen der Modelle übereinstimmen.
- **Modellübereinstimmung** fließt als Einschätzung in die Tagesübersicht ein.
- **Regenrisiko, Gewitterpotenzial (CAPE), Sicht, UV-Index, Taupunkt, Bewölkung und Schneefallgrenze** werden aus den jeweiligen Modellvariablen abgeleitet.
- **Reichweite:** Die Anzeige beträgt 7 Tage. Je nach Modell liegen Daten für 7 bis 16 Tage vor.
- **Regenradar** ist unabhängig von den Modellen. Es beruht auf echten Radarmessungen und einer Kurzfristvorhersage des DWD.

---

## Datenquellen und Quellenangaben

| Zweck | Quelle |
|---|---|
| Wettermodelle, Höhenabfrage | [Open-Meteo](https://open-meteo.com/) |
| Luftqualität | [Open-Meteo Air Quality](https://open-meteo.com/en/docs/air-quality-api) |
| Regenradar (RV-Komposit) | [Deutscher Wetterdienst (DWD)](https://www.dwd.de/), abgerufen über [Bright Sky](https://brightsky.dev/) |
| Ortssuche | [Nominatim / OpenStreetMap](https://nominatim.openstreetmap.org/), [Photon (Komoot)](https://photon.komoot.io/) |
| Kartenhintergründe | © [OpenStreetMap](https://www.openstreetmap.org/copyright)-Mitwirkende, [OpenTopoMap](https://opentopomap.org/) (CC-BY-SA), Esri |
| Lawinenlage | Amtliche Lawinenlageberichte, u. a. [lawinen.report / Albina](https://lawinen.report/) (Tirol, Südtirol, Trentino), [SLF](https://www.slf.ch/) (Schweiz), [Lawinenwarndienst Bayern](https://lawinenwarndienst.bayern.de/), [AINEVA](https://bollettini.aineva.it/) (Italien) |

Bitte beachte die jeweiligen Nutzungsbedingungen und Lizenzen der Dienste, besonders wenn die App öffentlich gemacht oder kommerziell genutzt werden soll. Die Open-Meteo-Daten sind für nicht-kommerzielle Nutzung frei (CC BY 4.0, Namensnennung erforderlich). Bright Sky ist ein inoffizielles Projekt, dessen Radar-Schnittstelle als experimentell gilt und sich ändern kann.

---

## Datenschutz

- Es gibt **keinen eigenen Server**, kein Benutzerkonto und kein Tracking. Alles läuft im Browser.
- Gespeichert wird nur **lokal im Browser** (Orte, Favoriten, Tourplanung, Einstellungen). Mit „Als Datei sichern" erzeugst du selbst eine Kopie.
- Beim Datenabruf gehen die **Koordinaten des gewählten Ortes** an die oben genannten Dienste (zum Beispiel Open-Meteo, Bright Sky, Kartenserver). Die Standortabfrage per Browser erfolgt nur nach deiner Freigabe.

---

## Technik

- **Eine Datei:** Die komplette App ist eine einzige HTML-Datei ohne Build-Schritt. Intern ist sie in Datenabruf, Auswertung (Ensemble, Tourbewertung, Warnungen), Darstellung (Diagramme, Karten) und Oberfläche gegliedert.
- **Bibliotheken aus dem Netz (CDN):** [Tailwind CSS](https://tailwindcss.com/), [Chart.js](https://www.chartjs.org/), [Leaflet](https://leafletjs.com/), [Lucide](https://lucide.dev/) (Icons) und [pako](https://github.com/nodeca/pako) (Entpacken der Radardaten).
- **Radar:** Das Radarraster liegt in einer Polarprojektion. Die App rechnet es über die vom Dienst gelieferten Eckpunkte in die Kartenprojektion um und färbt es per Farbtabelle ein. Die gesamte Animation läuft aus dem Speicher.
- **Handy-Optimierung:** Kompakter Kopfbereich, zweispaltige Kennzahlen, festgehaltene Tag-Spalte in der Tabelle, antippbare Tages-Chips und ein Speichern-Fenster, das sich an den Bildschirm anpasst.
- **Browser:** Aktuelle Versionen von Chrome, Safari, Firefox und Edge.

---

## Grenzen und bekannte Einschränkungen

- Wettermodelle sind Prognosen und können falsch liegen, besonders bei Gewittern und in Gebirgsregionen. Die Tourbewertung ist eine Orientierung, **keine Freigabe für eine Tour**.
- Das **Regenradar** deckt nur Deutschland und die Randgebiete ab, zeigt nur etwa 2 Stunden Vorhersage und hat eine Auflösung von 1 km. Es hängt von der experimentellen Schnittstelle von Bright Sky ab. Fällt diese aus, erscheint eine Fehlermeldung.
- **Lawinendaten** werden nur übernommen, wenn die Zuordnung zum Gebiet eindeutig ist. Sie ersetzen nicht den Blick in den amtlichen Lawinenlagebericht.
- **Zeitzonen:** Die Uhrzeiten der Wetterdaten werden in der Zeitzone des Browsers gelesen. Bei Orten weit außerhalb Mitteleuropas können „Heute", „Jetzt" und die Sonnenzeiten deshalb abweichen.
- **Tourplanung und -bewertung** sind auf Deutschland, Österreich, die Schweiz und Italien ausgelegt.
- Ohne Internetverbindung funktioniert die App nicht.

---

## Versionsverlauf

| Version | Änderungen |
|---|---|
| V10 | Start immer im Anfängermodus mit dem Tab „5d Vorhersage". 24h-Tab mit Tagesauswahl und neuer Reihenfolge, Mittelwerte hervorgehoben, Modellübereinstimmungs-Box und Hover-Detailbox entfernt. |
| V11 | Vorhersage auf 7 Tage erweitert. Ortssuche außerhalb der Tourplanung weltweit. Temperatur-Mittelwert wieder dünner. |
| V12 | Tagesauswahl ohne „Heute/Morgen/Übermorgen", nur noch Wochentag und Datum. |
| V13 | Tageszeilen der 7d-Tabelle antippbar, springen in die 24h-Vorhersage des Tages. |
| V14 | Handy: Speichern-Fenster nicht mehr abgeschnitten, Kennzahlen zweispaltig, feste Tag-Spalte in der Tabelle. |
| V15 | Tages-Chips statt Auswahlbox, einklappbare Ansichtsumschaltung und kompakterer Kopfbereich am Handy. |
| V16 | Neues DWD-Regenradar mit Regen-Info in Worten und Punktabfrage. |
| V17 | Kräftigere Farbskala im Radar. |
| V18 | Radar-Tempo standardmäßig „langsam". Windy vollständig entfernt. |
| V19 | Regenradar außerhalb des DWD-Gebiets: Satz und Balkendiagramm (−1 h bis +2 h, 15-Minuten-Raster, Open-Meteo-Modell, Ortszeit) statt Karte; auch Ersatz, wenn der Radar nicht erreichbar ist. |
| V20 | Neuer Tab „Gebietsvergleich" (Expertenmodus): zehn Alpengebiete nach Regenwahrscheinlichkeit und Sonnenstunden gereiht. |

---

*Stand: Version 20 · Oktober 2026*
