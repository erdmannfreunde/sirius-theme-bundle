# Changelog

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
