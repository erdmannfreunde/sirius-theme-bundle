# Changelog

## 3.0.3 (01.10.2026)

- `theme.xml` aktualisiert. Wer das Theme ohne Demo importierte, bekam noch das Logo aus `files/demo`, den Footer-Link auf erdmann-freunde.de und den iconmonstr-Hinweis im Social-Media-Modul – in 3.0.1 und 3.0.2 waren diese Stände nur in den Demo-Daten korrigiert.
- Scroll-Animationen: Ist die Seite in einem Cross-Origin-iframe eingebettet, ist `rootBounds` `null` und das Script brach mit einem Fehler ab. Jetzt dient die Breite des Viewports als Rückfall.
- Lightbox: Der unsichtbare Text des Weiter-Buttons lautet jetzt „Nächstes“ statt „Nächtes“.
- PHP-Anforderung in der `composer.json` von Paket und Bundle von `^8.1` auf `^8.3` angehoben. Contao 5.7 setzt PHP 8.3 voraus, die bisherige Angabe war zu niedrig.
- Lizenzbedingungen § 6 Abs. 1 präzisiert: Kostenlos sind Updates für die Contao-Hauptversion, für die das Theme erworben wurde – alle LTS-Versionen dieser Hauptversion, bei Contao 5 also 5.3 LTS und 5.7 LTS, nicht aber spätere Contao-Hauptversionen. Das bisherige Beispiel „5.x“ ließ offen, ob die Theme- oder die Contao-Version gemeint ist.
- Lizenzbedingungen § 2 Abs. 4 und `CREDITS.txt`: Nicht alle Erweiterungen, die Composer nachlädt, stehen unter der LGPL. Hero-, Card- und Kontakt-Element stehen unter GPL-3.0-or-later, das Grid-Bundle unter MIT. `CREDITS.txt` führt jetzt alle Erweiterungen mit ihrer Lizenz auf.
- Falsche Lizenzangabe im Kopf von `js_nav--mobile.html.twig` korrigiert: Dort stand wie zuvor in der `navigation.js` „Lizenziert unter MIT OPEN SOURCE“.
- Verweise auf die alte Produktseite bei erdmann-freunde.de in der `composer.json` des Pakets und in den Kopfzeilen der SCSS-Dateien auf flow-contao-themes.de umgestellt.
- Demo-Inhalte: Auf der Seite „Elemente im Überblick“ stand bei Akkordeon und Slider noch „SIRIUS 2“.

## 3.0.2 (29.09.2026)

- Lizenzbedingungen liegen dem Paket jetzt bei: `LIZENZ-de.txt` als maßgebliche Fassung und `LICENSE-en.txt` als englische Übersetzung. Bisher enthielt das Paket keinerlei Lizenztext.
- Neue `CREDITS.txt` weist alle Bestandteile Dritter nach – Schriften, Icons und Demo-Bilder. Der vollständige Lizenztext liegt im Ordner `licenses/`, weil die Apache License 2.0 die Mitlieferung verlangt.
- Lizenzangabe in der `composer.json` von `LGPL-3.0-or-later` auf `proprietary` geändert. Die bisherige Angabe widersprach den Lizenzbedingungen. Das Theme-Bundle `erdmannfreunde/sirius-theme-bundle` bleibt davon unberührt und weiterhin LGPL.
- Social-Icons der Demo ausgetauscht. Die bisherigen Icons stammten von iconmonstr, dessen Lizenz ein nicht übertragbarer Einzelnutzer-Vertrag ist und die Weitergabe in einem verkauften Paket nicht deckt. Ersatz sind `brand-instagram` und `brand-linkedin` aus den Tabler Icons (MIT); das Facebook-Icon ist daraus zusammengesetzt, weil Tabler kein Icon im Kasten anbietet.
- Falsche Lizenzangabe im Kopf der `navigation.js` korrigiert: Dort stand „Lizenziert unter MIT OPEN SOURCE“ mit Verweis auf das Nutshell Framework, das unter LGPL-3.0-or-later steht.

## 3.0.1 (23.09.2026)

- Colorbox: Der Titel bekommt wieder die Sekundärfarbe. Das `!important` stand innerhalb von `var()` und machte die Anweisung ungültig.
- Demo-Inhalte aktualisiert: Impressum und Datenschutzerklärung nennen die Erdmann Digital GmbH und verweisen auf flow-contao-themes.de, der Copyright-Hinweis im Footer verlinkt dorthin.
- Das Logo der Demo kommt jetzt aus dem Theme (`assets/sirius-theme/img/logo.svg`) statt aus `files/demo`. Damit lässt es sich über den Theme Editor ersetzen.

## 3.0.0 (28.08.2026)

**SIRIUS 3 – für Contao 5.7 LTS.**

Das Bundle ist vom Metapaket zu einem vollwertigen Contao-Bundle geworden und
liefert die Theme-Templates jetzt selbst aus – als Twig unter `contao/templates`
statt als `.html5` im Projekt:

- `mod_article` und `be_tinyMCE` erben über `{% extends "@Contao/…" %}` von den
  Core-Templates und überschreiben nur noch, was SIRIUS wirklich ändert
- `j_colorbox`, `js_nav--mobile` und `js_animate-article` sind ebenfalls Twig;
  das vormals inline eingebettete JavaScript liegt als Datei im Theme und wird
  über `theme_js()` eingebunden
- `ce_sliderStop` entfällt – dafür gibt es seit Contao 5.3 die verschachtelten
  Inhaltselemente

Die Theme-Struktur liegt nicht mehr unter `files/`, sondern unter `layout/`.
Farben, Schriften, Abstände und Eckenradien lassen sich damit über den Theme
Editor der Theme Toolbox (ab `^4.2`) anpassen; drei Farbwelten sind als Presets
enthalten: Waldgrün, Terrakotta und Schiefer.

Die nicht mehr benötigte `_updates.scss` wurde entfernt.

## 3.0.0-RC2 (28.08.2026)

Die JavaScript-Templates binden ihre Dateien jetzt über `theme_js()` der Theme
Toolbox ein statt über einen festen Pfad. Damit wird der Theme-Name zur Laufzeit
aufgelöst, die Assets werden vor der Ausgabe nach `assets/` gespiegelt, und eine
fehlende Datei ergibt keinen toten Verweis mehr.

## 3.0.0-RC1 (24.08.2026)

**SIRIUS 3 – Vorabversion. Änderungen bis zur 3.0.0 sind möglich.**

Das Bundle ist vom Metapaket zu einem vollwertigen Contao-Bundle geworden und liefert die Theme-Templates jetzt selbst aus – als Twig unter `contao/templates` statt als `.html5` im Projekt:

- `mod_article` und `be_tinyMCE` erben über `{% extends "@Contao/…" %}` von den Core-Templates und überschreiben nur noch, was SIRIUS wirklich ändert
- `j_colorbox`, `js_nav--mobile` und `js_animate-article` sind ebenfalls Twig; das vormals inline eingebettete JavaScript liegt jetzt als Datei im Theme
- `ce_sliderStop` entfällt – dafür gibt es seit Contao 5.3 die verschachtelten Inhaltselemente

Basis ist Contao 5.7. Die Theme Toolbox wird ab `^4.2` vorausgesetzt: Sie bringt den Live-Editor mit und erwartet die Theme-Struktur unter `layout/` statt unter `files/`.

## 2.4.1 (18.08.2026)

Behebt einen in 2.4.0 eingeführten Fehler, bei dem Links in Card-Elemente nicht klickbar waren.

## 2.4.0 (23.03.2026)

Unterstützung für Contao 5.7 LTS. Standardmäßig wird nun Contao 5.7 bei Neuinstallationen als Basis verwendet. Bestehende Contao 5.3 Installationen können direkt über den Manager auf Contao 5.7 aktualisiert werden.

## 2.3.1 (16.08.2024)

- Theme auf Contao 5.3 LTS fixiert

## 2.3.0 (20.02.2024)

**Unterstützung für Contao 5.3 LTS**

SIRIUS unterstützt die neuen verschachtelten Inhaltselemente für Akkordeon und Slider. Im Artikel „Jobs“ gibt es zusätzlich eine beispielhafte Verwendung für das ebenfalls neue Element **Beschreibungsliste** (Description List).

In bestehenden Installationen können die Anweisungen nach dem Update auf Contao 5.3 aus der `_updates.scss` in die entsprechenden Dateien übernommen werden. Alternativ kannst du auch die komplette `_updates.scss` in dein Projekt kopieren und über die `default.scss` importieren.

## 2.2.1 (10.01.2024)

- Fehlerhafte Darstellung der Card-Elemente im Firefox (auf kleinen Bildschirmen) behoben

## 2.2.0 (07.09.2023)

- Kompatibilität zu Contao 5.2 hergestellt

## 2.1.0 (05.05.2023)

**NEU: Einführung des Dark Mode über Custom Properties.**

In bestehenden Installationen können die Anweisungen aus der `_updates.scss` in die entsprechenden Dateien übernommen werden. Alternativ kannst du auch die komplette `_updates.scss` in dein Projekt kopieren und über die `default.scss` importieren.

Wichtig: Neue Installationen mit SIRIUS 2.1.0 oder höher haben automatisch den Dark Mode aktiviert. Bitte berücksichtige deine Farbänderungen auch im dunklen Farbmodus.

## 2.0.1 (18.04.2023)

- Kleinere Anpassungen für Kontakt-Element (siehe `_updates.scss`)

## 2.0.0 (10.03.2023)

- Contao 5.1 Support

## 1.11.2 (07.12.2022)

- Entwickler Edition: postcss als Abhängigkeit ergänzt

## 1.11.1 (25.03.2022)

- PHP 8 Unterstützung
- Entwickler Edition: node und gulp aktualisiert

## 1.11.0 (15.02.2022)

- SIRIUS für Contao 4.13 aktualisiert
- Contao 4.12 Support eingestellt
- FIX: localconfig-Einstellungen lassen sich nun auch über die `config.yml` vornehmen

## 1.10.0 (20.09.2021)

- SIRIUS für Contao 4.12 aktualisiert
- Contao 4.11 Support eingestellt
- Entwickler Edition: node und gulp aktualisiert

## 1.9.0 (02.03.2021)

- Contao 4.10 Support eingestellt
- SIRIUS für Contao 4.11 aktualisiert
- SIRIUS unterstützt nun auch den TinyMCE 5 (Standard seit Contao 4.10)

## 1.8.2 (12.02.2021)

- Kompatibilität zum Contao Manager 1.4 bzw Composer 2 wiederhergestellt
- Contao 4.4 Support eingestellt

## 1.8.1 (13.10.2020)

- veraltete README entfernt

## 1.8.0 (18.08.2020)

- SIRIUS für Contao 4.10 aktualisiert

## 1.7.1 (20.04.2020)

- Animierte Elemente werden nun früher eingeblendet, in `j_animate-article.html5` außerdem über die Variable `contentOffset` geändert werden
- Auf Unterseiten wie Datenschutz und Impressum wird einheitlich die Navigation angezeigt

## 1.7.0 (20.02.2020)

- SIRIUS für Contao 4.9 aktualisiert

## 1.6.1 (22.01.2020)

- In den ZIP-Archiven der Version 1.6.0 war irrtümlicherweise der Ordner `/files/nutshell/` inkludiert. Jetzt wird der Ordner wieder ausgeschlossen, sodass dieser durch die Installation der Nutshell-Extension als Symlink von Contao angelegt werden kann.

## 1.6.0 (23.12.2019)

- SIRIUS verwendet nun das Hero-Element in Version 2. Dadurch lässt sich die Position des Textes innerhalb des Elements zuordnen. Außerdem ist die Überschrift nun auch wirklich als Headline ausgezeichnet (bspw. `<h1>`)
- SIRIUS SE: Die Server Edition verfügt nun ebenfalls über ein tinyMCE-Template, das z.B. Buttons im Editor auswählbar macht und diese auch grafisch hervorhebt
- Browser-Support: der Support für den IE und ältere Opera Versionen wurde eingestellt. Die entsprechenden Vendor-Prefixes (bspw. Opera und IE9) wurden entfernt. Bei Bedarf können diese über die .browserslistrc (SIRIUS EE) oder per Hand wieder hinzugefügt werden.
- gulp + Abhängigkeiten aktualisiert

## 1.5.0 (19.11.2019)

- Die Demo der Server-Edition lässt sich nun direkt über den Contao Manager installieren, s.a. hhttps://erdmann-freunde.de/dokumentationen/contao-themes/theme-installieren/server-edition/theme-mit-demo/
- Für die Instalallation _mit Demo_ und _ohne Demo_ gibt es nun getrennte ZIP-Archive

## 1.4.1 (14.11.2019)

- Theme-Bundle auf 4.8 aktualisiert

## 1.4.0 (04.11.2019)

- Optimierung der Onepage-Navigation: Beim Scrollen wird nun ein Offset berücksichtigt, der standardmäßig der Höhe des Headers entspricht. Der Offset kann aber auch über die `j_onepage_navigation.html5` manuell angepasst werden.
- Beim Card-Element werden nun auch Listen standardmäßig aus- und bei `:hover` eingeblendet.
