# 🐸 Wetterfrosch V8.7

## Wetter, Tourplanung und Tourbewertung für Outdoor- und Bergtouren

**Wetterfrosch** ist eine kompakte Wetter- und Outdoor-Anwendung für alle, die vor einer Tour nicht nur wissen möchten, **wie das Wetter wird**, sondern auch, **wann und unter welchen Bedingungen eine geplante Tour sinnvoll durchführbar ist**.

Die Anwendung verbindet Wettervorhersagen, Modellvergleich, Regenradar, manuelle Tourplanung und eine nachvollziehbare Tourbewertung. Für Bergtouren werden zusätzlich Höhenlage, Nullgradgrenze, Schneefallgrenze und – soweit verfügbar – die amtliche Lawinenlage berücksichtigt.

> **Wichtig:** Der Tour-Score ist eine technische Orientierungshilfe und ersetzt keine eigene Erfahrung, aktuelle Vor-Ort-Beurteilung oder amtliche Warnungen.

---

## ✨ Was kann Wetterfrosch?

### 🌤 3d Wetter
Die 3-Tage-Ansicht gibt einen schnellen Überblick über die Wetterentwicklung.

Sie eignet sich insbesondere für die erste Frage:

> **Wie entwickelt sich das Wetter in den nächsten Tagen?**

---

### 🕐 24h Wetter
Die 24-Stunden-Ansicht ermöglicht die detaillierte Betrachtung eines konkreten Tages.

Sie enthält unter anderem:
- Modellübereinstimmung
- Temperaturentwicklung
- Niederschlagsentwicklung
- Zusammenfassung
- detaillierte Stundenprognose
- Windrichtung und Böen
- Niederschlagsrisiko

Der Modellvergleich hilft dabei, die Unsicherheit einer Wetterprognose besser einzuschätzen.

---

### 🌧 Regenradar
Das Regenradar dient zur Beurteilung der aktuellen Niederschlagsentwicklung und der kurzfristigen Wettertendenz.

Für eine konkrete Tour ist es besonders hilfreich, kurz vor dem Start noch einmal die Niederschlagsentwicklung zu prüfen.

---

### 🗺 Tourplanung
Die **Tourplanung ist vollständig manuell**.

Es ist **keine GPX-Datei erforderlich und es gibt keinen GPX-Upload**.

Eine Tour kann direkt über Startpunkt, Zwischenetappen und Ziel geplant werden. Als Orte können neben klassischen Ortsnamen auch relevante alpine Punkte wie Berge und Hütten verwendet werden.

Die Planung unterstützt unter anderem:
- Wanderungen
- Bergwanderungen
- Radtouren
- Touren mit mehreren Tagen
- Start, Zwischenetappe und Ziel
- automatische Berechnung der Punkt-zu-Punkt-Daten innerhalb der Planung
- Wetter- und Sicherheitsinformationen für die relevanten Tourpunkte

Für alpine Touren können auch Regionen der Alpen einschließlich **Norditalien** berücksichtigt werden.

---

### 🥾 Tourbewertung
Die **Tourbewertung** ist der zentrale Bereich für die Beurteilung der geplanten Tour.

Hier werden die für die jeweilige Tour relevanten Wetter- und Sicherheitsfaktoren zusammengeführt.

Dazu gehören insbesondere:
- Temperatur und gefühlte Temperatur
- Niederschlagswahrscheinlichkeit
- Niederschlagsmenge
- Wind
- Windrichtung
- Böen
- Sichtweite
- Wetterlage
- Gewitterindikatoren
- Schneefall
- Nullgradgrenze
- Schneefallgrenze
- Luftqualität
- amtliche Lawinenlage, soweit verfügbar

Zusätzlich wird nach Möglichkeit das **günstigste Zeitfenster des Tages** ausgewiesen.

---

# 🚀 Schnellstart

## 1. Ort auswählen

Einen Ausgangspunkt, Berg, eine Hütte oder einen anderen relevanten Punkt suchen.

Alternativ kann – sofern der Browser die Standortabfrage erlaubt – die aktuelle Position verwendet werden.

## 2. Wetter prüfen

Für den schnellen Überblick zunächst **3d Wetter** verwenden.

Für einen konkreten Tourtag anschließend **24h Wetter** öffnen.

## 3. Tour planen

In **Tourplanung** die Tour manuell zusammenstellen:

1. Startpunkt festlegen
2. optional eine Zwischenetappe festlegen
3. Ziel festlegen
4. bei Bedarf weitere Tage planen
5. die geplanten Etappen prüfen

Eine GPX-Datei muss dafür **nicht** vorhanden sein.

## 4. Tour bewerten

In **Tourbewertung** die Gesamtbewertung und die einzelnen Wetter- und Sicherheitsfaktoren prüfen.

Besonders bei Bergtouren sollten nicht nur der Gesamt-Score, sondern auch Lawinenlage, Gewitter, Wind/Böen, Sicht sowie die Höhenparameter betrachtet werden.

## 5. Günstigstes Zeitfenster prüfen

Wenn mehrere Zeitfenster möglich sind, zeigt Wetterfrosch, wann innerhalb des betrachteten Tages die günstigeren Bedingungen erwartet werden.

---

# 📊 Wie entsteht der Score?

Der Score startet grundsätzlich bei:

**100 Punkte = Ausgangswert**

Von diesem Ausgangswert werden erkannte ungünstige Bedingungen abgezogen.

Die Bewertung ist damit **kein Prozentwert für die Wahrscheinlichkeit eines erfolgreichen Tourverlaufs**, sondern ein regelbasierter Orientierungswert.

## Bewertete Faktoren

| Faktor | Bedeutung |
|---|---|
| Temperatur / gefühlte Temperatur | thermische Belastung |
| Niederschlagswahrscheinlichkeit | Risiko, dass Niederschlag auftritt |
| Niederschlagsmenge | erwartete Niederschlagsbelastung |
| Wind | allgemeine Windbelastung |
| Böen | zusätzliche Belastung und Sicherheitsrisiko |
| Sichtweite | Orientierung und Fernsicht |
| Wetterlage | z. B. Schauer oder Gewitter |
| CAPE / Gewitterindikatoren | Hinweis auf konvektive Gewittergefahr |
| Schneefall | winterliche bzw. alpine Belastung |
| Nullgradgrenze | Einordnung relativ zur Tourhöhe |
| Schneefallgrenze | Einordnung relativ zur Tourhöhe |
| Luftqualität | zusätzliche Belastung bei ungünstigen Werten |
| Lawinenlage | zusätzliche alpine Sicherheitsbewertung |
| Datenverfügbarkeit | verhindert eine scheinbar präzise Bewertung bei fehlenden sicherheitsrelevanten Daten |

---

# 👁️ Sichtweite

Die Sicht wird in die Bewertung einbezogen.

Grundprinzip:

- **≥ 15 km:** keine Abwertung
- **10–15 km:** geringe Abwertung
- **5–10 km:** moderate Abwertung
- **2–5 km:** deutliche Abwertung
- **1–2 km:** starke Abwertung
- **< 1 km:** sehr starke Abwertung

Eine Sichtweite von beispielsweise **22,6 km** wird daher **nicht negativ bewertet**.

---

# ❄️ Nullgradgrenze und Schneefallgrenze

Bei Bergtouren werden diese Werte nicht als isolierte Zahlen bewertet.

Entscheidend ist der Abstand zwischen der jeweiligen Grenze und der **Tourhöhe**.

Beispiel:

> Tourhöhe: ca. 1.790 m  
> Nullgradgrenze: ca. 3.011 m

Die Nullgradgrenze liegt damit deutlich über der Tourhöhe. Daraus entsteht **keine negative Bewertung wegen einer zu niedrigen Nullgradgrenze**.

Dasselbe Prinzip gilt für die Schneefallgrenze.

So wird verhindert, dass eine hohe Nullgrad- oder Schneefallgrenze fälschlicherweise als schlechte Bedingung interpretiert wird.

---

# 🌧️ Niederschlagsrisiko

Die Niederschlagswahrscheinlichkeit ist ein wichtiger Faktor der Tourbewertung.

Sie wird jedoch zusammen mit der erwarteten Niederschlagsmenge betrachtet.

Beispielsweise ist

> 60 % Niederschlagswahrscheinlichkeit + 0,1 mm Niederschlag

anders zu bewerten als

> 60 % Niederschlagswahrscheinlichkeit + mehrere Millimeter Niederschlag.

Der Score bewertet daher nicht ausschließlich die Prozentzahl.

---

# 💨 Wind und Böen

Wind und Böen werden getrennt betrachtet.

- durchschnittlicher Wind beschreibt die allgemeine Windbelastung
- Böen bilden kurzfristige Spitzenbelastungen ab

Stärkere Böen können den Score daher deutlich stärker beeinflussen als ein vergleichsweise moderater Mittelwind.

---

# ⛈️ Gewitter

Gewitterindikatoren werden gesondert berücksichtigt.

Dazu gehören unter anderem Wettercodes und – sofern verfügbar – konvektive Parameter wie CAPE.

Eine erkannte Gewitterlage kann den Score deutlich reduzieren.

> Ein hoher Score sollte niemals als Freigabe verstanden werden, wenn gleichzeitig eine aktuelle amtliche Gewitter- oder Unwetterwarnung besteht.

---

# 🏔️ Lawinenlogik in V8.7

Die Lawinenbewertung wurde bewusst von der normalen Datenqualität getrennt.

Es werden unterschiedliche Situationen unterschieden.

### 1. Amtliche Lawinenstufe vorhanden

Wenn eine aktuelle amtliche Gefahrenstufe verfügbar ist, wird sie in die Sicherheitsbewertung einbezogen.

Höhere Gefahrenstufen führen zu einer deutlich strengeren Bewertung.

### 2. Außerhalb der offiziellen Ausgabesaison

Wenn für eine Region saisonbedingt kein täglicher Lagebericht ausgegeben wird, bedeutet das **nicht automatisch „gefahrlos“**.

Gleichzeitig wird dieser bekannte saisonale Zustand **nicht pauschal mit einer künstlichen Score-Abwertung bestraft**.

Stattdessen wird ein erklärender Hinweis angezeigt.

### 3. Lagebericht momentan nicht verfügbar

Kann ein aktueller Bericht grundsätzlich erwartet werden, ist aber momentan nicht abrufbar, wird dies als relevante Datenunsicherheit behandelt.

Die Anwendung zeigt einen entsprechenden Hinweis und bewertet die Situation konservativer.

### 4. Region nicht eindeutig bestimmbar

Kann die offizielle Lawinenregion geografisch nicht eindeutig zugeordnet werden, wird keine erfundene Gefahrenstufe verwendet.

Die Unsicherheit wird ausdrücklich angezeigt und konservativ berücksichtigt.

---

# 🧮 Warum mehrere Faktoren?

Eine Tour kann gleichzeitig:

- hervorragende Sicht,
- wenig Wind,
- aber hohe Niederschlagswahrscheinlichkeit

haben.

Oder:

- gutes Wetter,
- aber starke Böen.

Oder:

- gutes Wetter,
- aber eine ungünstige Lawinenlage.

Der Score ist deshalb eine **Zusammenführung mehrerer Faktoren**.

Das Prinzip bleibt nachvollziehbar:

> **100 Punkte Ausgangswert → erkennbare Abzüge → nachvollziehbarer Endwert**

Sicherheitsbegrenzungen werden nicht versteckt angewendet, sondern in der Score-Transparenz kenntlich gemacht.

---

# 🕐 Bestes Zeitfenster

Wetterfrosch untersucht innerhalb des verfügbaren Vorhersagezeitraums günstige Zeitfenster.

So kann beispielsweise sichtbar werden, dass eine Tour am Vormittag ungünstiger und am Nachmittag besser bewertet wird.

Das Zeitfenster ist eine zusätzliche Entscheidungshilfe und keine Garantie.

Bei der endgültigen Beurteilung müssen auch sicherheitsrelevante Informationen berücksichtigt werden.

---

# 🎯 Bedeutung des Scores

Der Score ist als **Orientierungsskala von 0 bis 100** gedacht.

| Score | Orientierung |
|---:|---|
| **90–100** | sehr gute Bedingungen |
| **75–89** | gute Bedingungen |
| **60–74** | brauchbar / erhöhte Aufmerksamkeit |
| **40–59** | kritisch |
| **20–39** | sehr kritisch |
| **0–19** | äußerst ungünstig |

Diese Klassen sind **keine amtlichen Gefahrenklassen**.

Insbesondere bei Bergtouren können einzelne Faktoren wichtiger sein als der Gesamtscore.

---

# ⚠️ Datenqualität und Vertrauensanzeige

Wetterfrosch unterscheidet zwischen der eigentlichen Wetterbewertung und der Qualität der verfügbaren Daten.

Fehlen relevante Werte, soll nicht einfach so getan werden, als wäre die Prognose vollständig.

Betroffen sein können beispielsweise:
- Sicht
- Wind
- Böen
- Niederschlag
- Gewitterindikatoren
- Schneefall
- Nullgradgrenze
- Schneefallgrenze

Die Bewertung kann dann konservativer ausfallen und einen entsprechenden Hinweis anzeigen.

Die **Vertrauens-/Konsistenzanzeige ist keine statistisch validierte Erfolgswahrscheinlichkeit**. Sie beschreibt vor allem die Übereinstimmung der verfügbaren Wettermodelle bzw. Eingangsdaten.

---

# 🔎 Modellkonsens

Wettermodelle können unterschiedliche Ergebnisse liefern.

Beispiel:

- Modell A: 10 km/h Wind
- Modell B: 12 km/h
- Modell C: 11 km/h

→ hohe Übereinstimmung.

Anders:

- Modell A: 10 km/h
- Modell B: 25 km/h
- Modell C: 45 km/h

→ größere Unsicherheit.

Wetterfrosch nutzt den Modellvergleich deshalb als zusätzliche Information.

Der entscheidende Punkt der aktuellen Scorelogik:

> **Die angezeigten konsolidierten Wetterwerte und die Werte, aus denen der Score berechnet wird, sollen zusammenpassen.**

Dadurch werden widersprüchliche Einzelmodell-Abzüge vermieden.

---

# 🥾 Beispiel einer Tourbewertung

Eine Bergtour weist beispielsweise folgende Bedingungen auf:

- Sicht: **22,6 km**
- Wind: **8 km/h**
- Böen: **24 km/h**
- Regenrisiko: **43 %**
- Niederschlag: **0,0 mm**
- Nullgradgrenze: **3.011 m**
- Schneefallgrenze: **2.318 m**
- Schneefall: **0,0 mm**
- keine starke Gewitterlage

Für Sicht, Wind, Böen, Niederschlagsmenge sowie die Höhenlage der Nullgrad- und Schneefallgrenze besteht damit kein Grund für künstliche starke Abzüge.

Das Niederschlagsrisiko kann dagegen zu einer moderaten Abwertung führen.

Wenn gleichzeitig kein täglicher Lawinenbericht ausgegeben wird, weil die offizielle Ausgabesaison beendet ist, wird dieser saisonale Zustand **nicht automatisch mit einer pauschalen Score-Grenze bestraft**. Stattdessen erscheint ein erklärender Hinweis.

---

# 🛡️ Sicherheitshinweis

Wetterfrosch ist ein Planungs- und Orientierungstool.

Besonders im alpinen Bereich können sich Bedingungen innerhalb weniger Stunden erheblich verändern.

Der Score kann niemals:
- die tatsächliche Situation vor Ort ersetzen
- persönliche Erfahrung ersetzen
- eine amtliche Warnung ersetzen
- eine Lawinenbeurteilung ersetzen
- die Beurteilung von Gelände, Exposition und Schneedecke ersetzen

Vor dem Start sollten immer die aktuellen amtlichen Wetter-, Unwetter- und Lawineninformationen sowie die Verhältnisse vor Ort geprüft werden.

> **Sicherheitsinformation schlägt Score.**

---

# 🧑‍💻 Technischer Hintergrund

Wetterfrosch V8.7 ist als einzelne HTML-Anwendung aufgebaut.

Die Oberfläche, Tourplanung und Scoreberechnung laufen in der Anwendung. Für Wetter-, Orts- und Sicherheitsinformationen werden externe Datenquellen verwendet.

Daraus ergeben sich typische Abhängigkeiten:
- Internetverbindung kann erforderlich sein
- externe APIs können ausfallen
- Daten können verspätet oder unvollständig sein
- Änderungen externer Schnittstellen können Funktionen beeinflussen

---

# 📌 Empfohlener Ablauf

**1. 3d Wetter**  
→ Wetterentwicklung prüfen

**2. 24h Wetter**  
→ konkreten Tourtag detailliert ansehen

**3. Tourplanung**  
→ Start, Zwischenetappe und Ziel manuell festlegen

**4. Tourbewertung**  
→ Score und Einzelparameter prüfen

**5. Bestes Zeitfenster**  
→ günstigen Zeitraum auswählen

**6. Warnungen / Lawinenlage**  
→ sicherheitsrelevante Informationen kontrollieren

**7. Eigene Entscheidung treffen**

---

## 🐸 Kurz gesagt

**Wetterfrosch soll nicht einfach sagen: „Ja“ oder „Nein“.**

Die Anwendung soll zeigen:

> **Welche Faktoren sprechen für die Tour, welche dagegen, wie vollständig und konsistent sind die verfügbaren Daten und wann sind die Bedingungen innerhalb des Vorhersagezeitraums am günstigsten?**

Damit wird aus einer reinen Wetter-App ein **praktisches Planungswerkzeug für Outdoor- und Bergtouren**.
