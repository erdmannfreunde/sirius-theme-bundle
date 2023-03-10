# Changelog

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
- In den ZIP-Archiven der Version 1.6.0 war irrtümlicherweise der Ordner `/files/nutshell/` inkludiert. Jetzt wird der Ordner wieder ausgeschlossen, sodass dieser durch die Installation der Nutshell-Extension  als Symlink von Contao angelegt werden kann.

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
