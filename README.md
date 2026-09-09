# 🐸 Wetterfrosch V8

**Das pfiffige Schweizer Taschenmesser für dein Outdoor-Wetter**

Willkommen beim Wetterfrosch! Verabschiede dich von 08/15-Wetter-Apps. Der Wetterfrosch V8 ist eine mächtige, datenschutzfreundliche Single-HTML-App, die speziell für Outdoor-Fans, Bergsteiger und Tourenplaner entwickelt wurde. Er vereint 5 globale Wettermodelle und berechnet das Wetter passgenau für deine aktuelle Höhe.

## 🎯 Die Kernphilosophie

Warum noch eine Wetter-Anwendung? Weil der Wetterfrosch Dinge kann, an denen klassische Apps scheitern:

* **Ensemble-Vorhersage:** Statt sich auf ein Modell zu verlassen, analysiert die App zeitgleich 5 globale Top-Modelle (ECMWF, GFS, ICON, UKMO, GEM). Gibt es Abweichungen? Der Frosch sagt es dir!
* **Höhenpräzision:** Berg oder Tal? Die App kalibriert die Daten punktgenau auf die Höhenmeter deines Ziels.
* **Privatsphäre & Autarkie:** Alles läuft in einer einzigen HTML-Datei lokal in deinem Browser. Deine Daten gehören dir.

## 🎭 Zwei Modi: Für jeden das Richtige

Um dich nicht mit Daten zu erschlagen, bietet der Wetterfrosch zwei umschaltbare Ansichten (oben rechts zu finden):

* 🟢 **Anfänger-Modus:** Perfekt für den schnellen Alltag. Zeigt dir alles, was du für die nächsten Tage wissen musst, ohne komplizierte Fachbegriffe.
* 🏔️ **Experten-Modus:** Für Tourengeher und Alpinisten. Schaltet erweiterte Funktionen wie die mehrlagige Tourenplanung, Lawineninfos und Gewitterrisiko (CAPE) frei.

## 🗺️ Navigation & Tabs: Deine Werkzeuge

### 1. Die intelligente Suche
Tippe einfach oben in das Suchfeld. Der Wetterfrosch findet nicht nur Städte, sondern auch **Berggipfel, Almen, Hütten und Pässe** in der gesamten DACH-Region und Norditalien. Das kleine blaue Schild neben dem Treffer zeigt dir sofort die ermittelte Höhe an. Alternativ klickst du auf das GPS-Symbol, um deinen aktuellen Standort zu nutzen.

### 2. 3D Wetter (Trend)
Dein Blick in die Zukunft. Hier siehst du die Wetterentwicklung der kommenden Tage im Ensemble-Mittelwert. Die Detail-Tabelle verrät dir Sonnenstunden, Wind und vor allem den "Konsens" – also wie einig sich die 5 Modelle bei Temperatur und Regen sind.

### 3. 24h Wetter
Die Lupe für den aktuellen oder morgigen Tag. Mit detaillierten 2-Stunden-Takten, gefühlter Temperatur und dem CAPE-Wert (Gewitterpotenzial). Besonders praktisch: Die Modellübereinstimmungs-Anzeige warnt dich, wenn das Wetter unsicher ist.

### 4. Regenradar (Powered by Windy)
Eine interaktive Live-Wetterkarte. Du kannst zwischen dem echten Beobachtungsradar (was ist bisher passiert?) und der Niederschlagsprognose für die nächsten 24 Stunden umschalten. Auch Wind-, Temperatur- und Wolkenkarten stehen parat.

## 🧗 Die Experten-Werkzeuge (Nur im Experten-Modus)

Wenn du "Experte" aktivierst, wird der Wetterfrosch zum vollumfänglichen Expeditions-Planer:

* **Tab: Tourplanung:** Plane mehrtägige Wanderungen oder Radtouren. Das Geniale: Wählst du eine Mehrtagestour, wird das Ziel von Tag 1 automatisch zum Startpunkt von Tag 2. Die App zieht sich im Hintergrund ein detailliertes Höhenprofil für deine Route.
* **Tab: Tourbewertung:** Hier rechnet die App ab: Wie ist der Outdoor-Score deiner Route? Gibt es Wetterwarnungen für deine geplanten Etappen? Bei alpinen Zielen klinkt sich der Frosch sogar in amtliche Lawinenlageberichte ein und warnt vor heiklen Passagen.

## 💾 Speichern & Mitnehmen

Der Wetterfrosch ist zwar nur eine HTML-Datei, vergisst aber nichts, wenn du es nicht willst. Oben rechts unter dem Lesezeichen-Symbol findest du das Speichermenü:

* **Favoriten:** Speichere deine liebsten Orte und Berge mit einem Klick ab.
* **Session merken:** Speichert den aktuellen Ort, deinen Modus und sogar eine laufende Tourenplanung direkt im Browser (Local Storage).
* **Als Datei sichern:** Du wechselst das Gerät? Lade deinen Stand als kleine `.json` Datei herunter und importiere sie auf dem Handy oder Tablet einfach wieder!

> **💡 Pfiffiger Tipp:** Nutze die App am besten am PC zur großen Tourenplanung, exportiere die Sicherungsdatei, lade sie dir aufs Smartphone und öffne die HTML-Datei dort im Browser (z.B. Chrome oder Safari). So hast du offline die perfekte Vorbereitung dabei!

---

*Erstellt für die Wetterfrosch V8 Single-HTML-App.*  
*Kartendaten: © OpenStreetMap-Mitwirkende · Geocoding: Nominatim / Photon · Radar: Windy.com · Modelle: Open-Meteo*
