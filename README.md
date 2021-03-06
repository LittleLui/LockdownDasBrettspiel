# Lockdown! - Das Brettspiel

## Bauanleitung

(Fast) alles, was man braucht, um zu spielen, liegt im Verzeichnis `target`.  
Neben etwas A4-Papier, Klebstoff und Karton benötigt man nur noch Sleeves, falls man die Karten auf Papier statt Karton druckt, Halmakegel und kleine Chips.  
Ein 3D-Drucker sorgt für ein etwas haptischeres Spielerlebnis, ist aber nicht notwendig. Ein Drucker, der auch A3 drucken kann, spart Klebstoff beim Spielbrett.  
Wie das Spielmaterial fertig gebastelt aussieht, zeigen die Fotos in der Spielanleitung.  

 * Spielregeln.pdf - Die Spielanleitung.
 * playmat.pdf - Einmal pro Spieler ausdrucken.
 * Karten - 2 Varianten zur Auswahl:
   * cards-foldable.pdf - Einseitig auf Papier ausdrucken, an den grauen Linien ausschneiden, falten und in [passende Sleeves](https://www.amazon.de/gp/product/B017BRXU1A/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) stecken.
   * cards-double-sided.pdf - Doppelseitig auf Karton ausdrucken, an den grauen Linien ausschneiden.
 * Spielplan
   * board-separate\infection-track.pdf - Ausdrucken, passend zusammenkleben, zurechtschneiden.
   * board-separate\board-isometric.pdf - Das einzige A3-PDF. Auf A3 drucken, oder auf A4 und passend zusammenkleben.
   * tiles-isometric.pdf - Ausdrucken und auf festen Karton aufkleben. An den grauen Linien die 16 Plättchen des Stadtplans ausschneiden.
 * Spielfiguren: auch 2 Varianten zur Auswahl:
   * markers\3dprint - Spielfiguren/Marker zum 3D-drucken. Benötigt wird 1x virus.stl, und für n Spieler 3n+1 (brain.stl, heart.stl, task.stl) und ca. 10n coin.stl.
   * markers\2dprint.pdf - Alternative zum 3D-Druck: Ausdrucken, auf Karton kleben und ausschneiden. Sollte mehr als genug Marker für 6 Spieler enthalten.
   * Darüberhinaus braucht man für jeden Spieler noch zwei Halmakegel gleicher Farbe.

## Karten

Die Karten sind mit [countersheetextension](https://github.com/lifelike/countersheetsextension) für [Inkscape](https://inkscape.org/de/) gebaut. 
Die Rohdaten liegen in cards.json; ein kleines Sample zu Testzwecken, das möglichst alle Features der Templates abdeckt, in cards-minimal.json.
Countersheetextension benötigt die Inputdaten als CSV, generate.bat erzeugt diese (dazu benötigt man Python und chevron, letzteres lässt sich per `python -m pip install chevron` installieren):

	cards.json + cards-double-sided.mustache => cards-double-sided.generated.csv
	cards.json + cards-foldable.mustache => cards-foldable.generated.csv
	cards-minimal.json + cards-double-sided.mustache => cards-double-sided-minimal.generated.csv
	cards-minimal.json + cards-foldable.mustache => cards-foldable-minimal.generated.csv

Das entsprechende svg-template in Inkscape öffnen, und unter "Erweiterungen" -> "Boardgames" -> "countersheet" wählen.
Das passende generierte CSV auswählen, den images-Ordner src\cards\images auswählen, die Layoutoptionen auf "Full Registration Marks" und 5mm / 10mm / 5mm Bleed einstellen.
PDF-Output in ein passendes Verzeichnis einstellen und generieren. Dies erzeugt ein PDF pro Seite, zusammenfassen zb. mit NAPS2.

	cards-double-sided.generated.csv + cards-double-sided.svg => Für den doppelseitigen Ausdruck auf Karton.
	cards-foldable.generated.csv + cards-foldable.svg => Für den einseitigen Ausdruck auf Papier, zum falten und sleeven.

## Lizenz und Quellen

Spielregeln, Texte und eigene Grafiken unter [Creative Commons Namensnennung - Weitergabe unter gleichen Bedingungen 4.0 International Lizenz](https://creativecommons.org/licenses/by-sa/4.0/)  
Namensnennung bitte per Link auf [https://github.com/LittleLui/LockdownDasBrettspiel](https://github.com/LittleLui/LockdownDasBrettspiel)  
![Creative Commons Lizenzvertrag](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)  

### Elemente unter anderen Lizenzbedingungen

#### Karten-Hintergrundbilder
##### Die meisten von [Pexels](https://www.pexels.com/de-de/lizenz/) - zur freien Verwendung:
[Kaique Rocha](https://www.pexels.com/de-de/@kaiquestr)  
[Gustavo Fring](https://www.pexels.com/de-de/@gustavo-fring)  
[Skitterphoto](https://www.pexels.com/de-de/@skitterphoto)  
[CDC](https://www.pexels.com/de-de/@cdc-library)  
[Nathan Cowley](https://www.pexels.com/de-de/@mastercowley)  
[Guillaume Hankenne](https://www.pexels.com/de-de/@guihankenne)  
[Artyom Kulakov](https://www.pexels.com/de-de/@artyom-kulakov-1190754)  
[Christina Morillo](https://www.pexels.com/de-de/@divinetechygirl)  
[mali maeder](https://www.pexels.com/de-de/@mali)  
[Anna Shvets](https://www.pexels.com/de-de/@shvetsa)  
[Ketut Subiyanto](https://www.pexels.com/de-de/@ketut-subiyanto)  
[Andrea Piacquadio](https://www.pexels.com/de-de/@olly)  
[Field Engineer](https://www.pexels.com/de-de/@field-engineer-147254)  
[Katie Hollamby](https://www.pexels.com/de-de/@qwertypr)  
[Amine M'Siouri](https://www.pexels.com/de-de/@amine-m-siouri-1025778)  
[Anna Tarazevich](https://www.pexels.com/de-de/@anntarazevich)  
[RODNAE Productions](https://www.pexels.com/de-de/@rodnae-prod)  
[Tim Gouw](https://www.pexels.com/de-de/@punttim)  
[Expect Best](https://www.pexels.com/de-de/@expect-best-79873)  
[Maria Lindsey Multimedia Creator](https://www.pexels.com/de-de/@margemedia)  
[Taryn Elliott](https://www.pexels.com/de-de/@taryn-elliott)  
[sk](https://www.pexels.com/de-de/@rgsk97)  
[Pixabay](https://www.pexels.com/de-de/@pixabay)  
[Tim Mossholder](https://www.pexels.com/de-de/@timmossholder)  
[Max Fischer](https://www.pexels.com/de-de/@max-fischer)  
[Artem Beliaikin](https://www.pexels.com/@belart84)  
[Negative Space](https://www.pexels.com/@negativespace)  
[cottonbro](https://www.pexels.com/@cottonbro)  
[Helena Lopes](https://www.pexels.com/@wildlittlethingsphoto)  
[Sebastian Ervi](https://www.pexels.com/@sebastian-ervi-866902)  
[Maurício Mascaro](https://www.pexels.com/@maumascaro)  
[Adrianna Calvo](https://www.pexels.com/@adriannaca)  
[Victor Freitas](https://www.pexels.com/@victorfreitas)  
[Daniel Reche](https://www.pexels.com/@daniel-reche-718241)  
[Engin Akyurt](https://www.pexels.com/@enginakyurt)  

##### Andere Quellen:
event-demo.jpg: [© NDR Foto: Jörn Straehler-Pohl](https://www.ndr.de/nachrichten/hamburg/coronavirus/Protestierende-wollen-Corona-Massnahmen-aufheben,demo3124.html)  
event-locktown.jpg: [Der Standard / Foto:HO](https://www.derstandard.at/story/2000122124887/rohrkrepierer-viel-spott-fuer-neue-plattform-kaufhaus-oesterreich)  
event-press.jpg: [BKA/Andy Wenzel](https://www.cash.at/handel/news/coronavirus-massnahmenupdate-der-regierung-22251)  
measure-lockdown.jpg: [The Daily Telegraph via BBC](https://www.bbc.com/news/uk-scotland-51923262)  
event-disinfect.jpg: [Reuters (Image 46)](https://www.reuters.com/news/picture/inside-wuhan-epicenter-of-chinas-coronav-idUSRTS2ZL3I)  

#### Spielplan-Grafiken
[Car vector created by macrovector - www.freepik.com](https://www.freepik.com/vectors/car)  
[City vector created by macrovector - www.freepik.com](https://www.freepik.com/vectors/city)    
[Tree vector created by macrovector - www.freepik.com](https://www.freepik.com/vectors/tree)  
