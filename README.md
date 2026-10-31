# PARABOLA · Der schiefe Wurf

Eine deutschsprachige 3D-Physiksimulation für Desktop, Mobilgeräte und Meta Quest 3. Sie besteht aus einer einzelnen `index.html` und benötigt keinen Build-Schritt.

## Meta Quest 3 und GitHub Pages

1. Lade `index.html` und `README.md` in den Hauptordner des vorhandenen Repositories `Schieferwurf` hoch.
2. Öffne **Settings → Pages**.
3. Wähle unter **Build and deployment** `Deploy from a branch`, Branch `main` und Ordner `/ (root)`, dann **Save**.
4. Öffne nach dem Deployment die von GitHub Pages angezeigte HTTPS-Adresse im Meta-Quest-Browser und tippe auf **In VR erleben**.

WebXR verlangt einen sicheren Ursprung (HTTPS; localhost ist für lokale Entwicklung ebenfalls zulässig). Die Babylon.js- und GUI-Bibliothek werden zur Laufzeit von `cdn.babylonjs.com` geladen, deshalb braucht die Seite Internetzugriff.

## Lokal ansehen

`index.html` kann in einem aktuellen Browser geöffnet werden. Für VR-Tests oder lokale Entwicklung kannst du sie über einen lokalen Webserver bereitstellen, zum Beispiel mit Python: `python -m http.server 8000` im Ordner `schieferwurf`, dann `http://localhost:8000` öffnen.

## Bedienung

- Geschwindigkeit, Abwurfwinkel und Gravitation über die Regler einstellen.
- Umgebung über das Auswahlmenü wechseln: Alpenstation, Mars-Observatorium oder Arktisfeld.
- **Versuch starten**, **Pause**, **Weiter** und **Neu** steuern den Wurf.
- **Außen** schaltet die Orbitkamera ein; die Szene kann mit Maus oder Touch gedreht und gezoomt werden.
- **Mitflug** folgt dem Projektil aus der Perspektive des Fluges.
- **In VR erleben** fordert einen immersiven WebXR-Modus an. Dafür müssen Browser und Gerät WebXR unterstützen.

Die ideale Wurfbewegung wird analytisch ohne Luftwiderstand berechnet. Die Messwerte umfassen Flugzeit, momentane Flugweite, maximale Höhe, aktuelle Höhe und horizontale sowie vertikale Geschwindigkeitskomponenten.
