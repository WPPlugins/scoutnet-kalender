=== Scoutnet Kalender ===
Contributors: muetze, derweed, lordq, okay75
Tags: Scoutnet, Scoutnetkalender, Scoutnet-Kalender, Scoutnet Kalender, Scoutnetwidget, Scoutnet-API, DPSG, DPSG-Kalender, VCP, BDP
Requires at least: 3.0
Tested up to: 4.7.2
Stable tag: 1.0.9
License: GPLv3
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Zeigt Termine und Details aus dem Scoutnet-Kalender in einem Widget, Artikeln und Seiten an

== Description ==

Zeigt Termine und Details aus dem Scoutnet-Kalender (https://www.scoutnet.de/kalender) in WordPress Seiten, Beitraegen und einem Widget an. Es sind keine iFrames, iCAL, oder Datenkonverteierung notwendig, die Daten kommen in Echzeit von der Scoutnet API. Das Plugin versteht Shortcodes fuer eigene Seiten und Beitraege und enthaelt ein templatefaehiges Widget fuer die Sidebar.

= Features =
* Einbindung mehrerer Kalender-IDs
* Einfaches Template-System zur Anpassung des Layouts
* Kommentierte Beispiel-Vorlagen
* Optionales AJAX-Widget-Template (sehr schnell)
* Verbandsunabhängig
* API-Proxy-Server in Einstellungen konfigurierbar (thx Andre)


== Installation ==

1. .zip file herunterladen, auspacken
2. Den Ordner "scoutnet-kalender" mit allen Dateien in das Pluginverzeichnis (/wp-content/plugins/) hochladen
3. Das Plugin im WordPress-Dashboard unter Plugins -> "Scoutnet Kalender" aktivieren
4. Das Widget kannst du dann sofort unter Design->Widgets in dein Theme einbinden.

Fuer Seiten und Artikel mit Terminen darauf gibt es einen Shortcode.

Unter den 'Einstellungen' kannst du die Standartwerte vorgeben und die Shortcodes nachschlagen.

== Frequently Asked Questions ==

= Das Plugin funktioniert bei meinem Hoster nicht =
Das kann sein. Guenstige Hostingangebote wie Strato, 1und1, Unitedinternet und aehnliche unterbinden ausgehende Verbindungen zu API-Diensten wie dem Scoutnet. Wechsle den Hoster (zum Beispiel www.data-systems.de) oder nutze die Proxy-Funktion in den Einstellungen.

= Wie nutze ich ein eigenes Template fuer eigenes HTML/CSS? =
Diese Anleitung gilt fuer die Inline-Anzeige und das Widget - nimm einfach die passenden Dateien.

1. Kopiere dein Template "scoutnet-kalender_[inline oder widget]_kalender_EXAMPLE_list.php" von scoutnet-kalender/templates/ in dein Theme-Verzeichnis (wp-content/themes/<deintheme>).
2. Benenne das Template um, z.B. "scoutnet-kalender_inline_kalender_MEINNAME_list.php"
3. Trage DIESEN Namen (achte dabei auf Klein-Grosschreibung) in das Widget/Shortcode ein
4. Fuege das CSS aus der EXAMPLE_style.css in deine "style.css" ein (oder formatiere selbst)

Du kannst diese Dateien nun in deinem Theme-Ordner bearbeiten, ohne das sie bei einem Update des Plugins ueberschrieben werden.

= Beispiele fuer eigene Templates =
Liegt in /templates/EXAMPLE. Kopiere diese in dein Theme-Verzeichnis und uebernimm den Inhalt der EXAMPLE_style.css in deine stlye.css.

= Welche Kalender-ID ist welche? =
Dazu findest du mehr Informationen unter: http://www.scoutnet.de/kalender/kurzanleitung.html

= Kann ich mir das Plugin Live ansehen? =
Aber sicher, zum Beispiel hier: http://www.dpsg-paderborn.de

= Kann ich Termine aus mehreren Kalendern anzeigen? =
Ja, kein Problem. Trage in deine Seite in den Shortcode die IDs getrennt durch Kommata ein.

= Das Widget funktioniert nicht, ich sehe nur den Ladehinweis! =
Schau nach, ob du ein Caching-Plugin im Einsatz hast das JS-Minify nutzt. Schalte die das minify/process fuer alle Seiten mit dem Widget aus.
Das 'process' Minify verschiebt das Javascript des Footers in den HEAD deines Dokumentes und macht damit die Funktion kaputt.


== Screenshots ==

1. Die Widget-Konfiguration
2. Das Widget (mit dem EXAMPLE-Template)


== Changelog ==

= 1.0.9 =
- Readme um Proxy-Settings erweitert
- Proxy-Settings Fehler in den optionen behoben
- 

= 1.0.8 =
- Typos
- Compatibility-Test WP 4.5.1

= 1.0.7 =
- Option zur Nutzung von Proxy-Servern hinzugefuegt (Danke André aus Bremen)
- API um Proxy-Variablen erweitert
- Noch mehr Tippfehler korrigiert
- Kompatibilitaet zu Wordpress 4.6

= 1.0.6 =
- Readme-Markup, no code Changes

= 1.0.4 =
- Fix: URLs to Scoutnet.de work now correctly

= 1.0.3 =
- Fix: Kommentar-Ausbau, Wordpress-Updatefehlersuche (das Repository mochte nicht)

= 0.2.5 =
- Fix: Tippfehler, Commit-Fehler

= 0.2.5 =
- Fix: Readme Tippfehler
- Fix: Falscher Pfad in ABSURL

= 0.2.4 =
- Fix: Falsche Ausgabe-Uhrzeit in Inline-Template (Danke Maxi)
- Change: Das Inline-Template EXAMPLE gibt jetzt anstatt 1970 als aenderungsdatum das Erstellungsdatum des Termins aus. Macht mehr Sinn (Danke Maxi)

= 0.2.2 =
- Fix: Readme angepasst, neue Release korrekt getaggt
- Fix: Tippfehler ohne Ende korrigiert
- Fix: Anpassung Doku

= 0.2.1 =
- Fix: Verwendung von "get_stylesheet_directory()" anstelle von "TEMPLATEPATH" fpr die Unterstuetzung von Child-Themes (Danke Tobi)
- Feature: Anpassung der Datenuebernahme fuer mehrere Kalender (z.B. Bezirkskalender und alle Stammeskalender) (Danke Tobi)

= 0.2.0 =
- Fix: Cleanup (doppelte Dateien entfernt)
- Feature: Template(s) deutlich verbessert (thx Fl!P, phil)
- Feature: URL-Verkuerzung in Inline-Template hinzugefuegt

= 0.1.9 =
- Fix: Termine im Widget sind um eine oder Zwei Stunden verschoben.

= 0.1.8 =
- Fix: CURL-Fehler in safe_mode PHP-Konfigurationen behoben

= 0.1.7b =
- Fix: Readme Markup fixes. Daemliche Umlaute.

= 0.1.7 =
- Erste "offizielle" Release
- Templates hinzugefuegt
- AJAX aktualisierung gegen "Stotterpages" gebaut
- Bugfixes
- Template-Bugfixes

= 0.0.1 =
* Code von muetze bekommen :)
