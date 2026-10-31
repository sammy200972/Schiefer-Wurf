# PARABOLA · Der schiefe Wurf

Eine deutschsprachige 3D-Simulation des schiefen Wurfs. Sie läuft als einzelne `index.html` im Browser und kann über GitHub Pages auch auf der Meta Quest 3 geöffnet werden.

## Funktionen

- Regler für Anfangsgeschwindigkeit, Abwurfwinkel, Gravitation und Windgeschwindigkeit
- Luftmodus mit quadratischem Luftwiderstand und Vakuummodus ohne Luftwiderstand
- Wind: positiver Wert = Rückenwind, negativer Wert = Gegenwind; im Vakuum bleibt Wind wirkungslos
- Auswahl markanter Körperformen mit typischen CW-Richtwerten:
  - Vollkugel: 0,47
  - Halbkugel, rund voraus: 0,38
  - Halbkugel, flach voraus: 1,17
  - Halbkugelschale, offen voraus: 1,42
  - Scheibe, breit angeströmt: 1,28
  - Würfel, Fläche voraus: 1,05
  - Tropfenform: 0,05
  - Geschossform: 0,295
  - symmetrisches Profil: 0,045
- Drei Umgebungen: Alpenstation mit Bäumen und See, Mars-Observatorium und Arktisfeld
- Außenkamera, Mitflug, Pause und Messwerte für Flugzeit, Flugweite, Höhe und Geschwindigkeit
- VR-Start über WebXR

## Physikalisches Modell

Im Luftmodus wird der Widerstand proportional zu `CW · |v_rel| · v_rel` berechnet. `v_rel` ist die Geschwindigkeit des Körpers relativ zur Luft; dadurch beeinflusst Wind die Flugbahn. Im Vakuum wird der Widerstand auf null gesetzt. Für den Formvergleich verwendet diese Lernsimulation eine gemeinsame Bezugsmasse und Stirnfläche; der CW-Wert skaliert den Widerstand. Die angezeigten CW-Werte sind Richtwerte: Sie ändern sich unter anderem mit Reynolds-Zahl, Ausrichtung und verwendeter Bezugsfläche. Die Simulation ersetzt daher keine Messung eines konkreten Gegenstands.

## Auf GitHub Pages aktualisieren

1. Lade `index.html` und `README.md` herunter.
2. Öffne das Repository `sammy200972/Schiefer-Wurf` und wähle **Add file → Upload files**.
3. Wähle beide Dateien aus. Achte darauf, dass die HTML-Datei `index.html` heißt und im Hauptordner des Repositories liegt.
4. Scrolle zu **Commit changes** und bestätige den Commit. GitHub Pages veröffentlicht die neue Version automatisch.
5. Öffne die HTTPS-Seite im Quest-Browser und lade sie neu. Für den VR-Modus müssen Browser und Gerät WebXR unterstützen.

Die Pages-Quelle muss auf Branch `main` und Ordner `/(root)` zeigen. Babylon.js und die GUI-Bibliothek werden von `cdn.babylonjs.com` geladen; beim Öffnen ist daher Internetzugriff nötig.

## Bedienung

Stelle die Regler und Körperform ein und starte **Versuch starten**. **Außen** ermöglicht das Drehen und Zoomen der Szene; **Mitflug** folgt dem Projektil. Die Checkbox **Vakuum** schaltet den Luftwiderstand ab. Der Windregler reicht von Gegenwind (negative Werte) bis Rückenwind (positive Werte).
