# Jonas D. – Geoinformatik

Persönliche Webseite mit Vorstellung, Lebenslauf, Neuigkeiten und interaktiven Karten von Mainz, Sevilla und dem Bodensee.

## Live-URL

GitHub-Pages-Adresse: [https://survey-007-JD.github.io/](https://survey-007-JD.github.io/).

Vor der Abgabe den aktuellen Stand hochladen, GitHub Pages für dieses Repository aktivieren und die Adresse in einem privaten Browserfenster prüfen. Falls 404 erscheint, ist die Seite noch nicht veröffentlicht.

## Neuigkeiten bearbeiten

Die Meldungen stehen in [assets/news.json](./assets/news.json). Für eine neue Meldung einen vorhandenen Eintrag kopieren und `date`, `title`, `summary`, `image` und `imageAlt` anpassen. Lokal die Webseite über „Go Live“ öffnen, damit JavaScript die JSON-Datei laden kann.

## Übung 2 – Reflexion

1. **Light/Night Mode:** Die Funktion `setTheme()` in [index.html](./index.html) setzt `data-theme` am `<html>`-Element. Die CSS-Regel `:root[data-theme="dark"]` ersetzt dadurch die Farbvariablen des hellen Modus. Die Auswahl wird in `localStorage` gespeichert.
2. **Klick-Ereignisse:** `addEventListener('click', ...)` reagiert auf Klicks am Theme-Button und an den Tabs. Beim Button wird das Theme gewechselt; bei den Tabs ruft der Code `activateTab()` auf.
3. **Tabs:** Jeder Inhalt steht in einem `<section role="tabpanel">`. `activateTab()` zeigt das ausgewählte Panel an und blendet die anderen über das `hidden`-Attribut aus. `aria-controls` verbindet den Tab-Button mit seinem Panel.
4. **News:** `loadNews()` liest [assets/news.json](./assets/news.json) mit `fetch()` ein. `response.json()` wandelt die Datei in JavaScript-Daten um; `renderNews()` erzeugt daraus die Karten mit Bild, Datum, Titel und Kurztext.

## Übung 3 – Webkarten

Der Tab **„Übung 3“** in [index.html](./index.html) zeigt die Folium-Karten aus [maps/](./maps/) und eine Cesium-Karte mit den LoD2-Gebäuden von basemap.de.

- Die persönliche Punkte-Karte ist [maps/map_2_punkte.html](./maps/map_2_punkte.html) und zeigt Mainz, Pfullendorf und Ramsen (Pfalz).
- Die Reiseroute führt über Mainz, Berlin, Den Haag und Paris.
- Die Länderkarte hebt Deutschland, Schweiz, Österreich, Luxemburg, Niederlande, Belgien, Frankreich, Spanien, Portugal und das Vereinigte Königreich hervor.
- Für die erweiterte Visualisierung erstelle eine Karte in [Kepler.gl](https://kepler.gl/), exportiere sie als HTML und speichere sie als `assets/kepler_map.html`. Danach kann sie direkt im Übung-3-Tab eingebunden werden.
