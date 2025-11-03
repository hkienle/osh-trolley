:::success
:handshake: Gerne Kommentieren: Rechts oben ![image](https://hackmd.io/_uploads/rJFniJu1eg.png =40x) anklicken. Oder Text markieren, dann kommt ein Popup.
:::
:::info
(c) Holger Kienle
License (if not stated otherwise below): [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
:::

[![hackmd-github-sync-badge](https://hackmd.io/S7o1KkemS8yVbEgkoFQbVw/badge)](https://hackmd.io/S7o1KkemS8yVbEgkoFQbVw)

# `tn-oshop-assessment` OSH Einkaufstrolley: Bewertungskriterien Prototyp

Basierend auf den Bewertungskriterien für die Jury werden die gewählten Ansätze reflektiert und der aktuelle Stand der Entwicklung des **OSH Einkaufstrolley** dargestellt.

## Offenheit & Dokumentation

Ziel der Dokumentation war es verschiedenen Ansätzen und Plattformen zu präsentieren und dabei deren jeweilige Stärken auszunutzen. Dadurch ist die Doku allerdings über verschiedene Plattformen verteilt und verlinkt und präsentiert sich dadurch nicht in einem Guss.

Die gewählten Plattformen:
- **HackMD:** Niederschwelliger, komfortabler Editor mit Markdown-Dialekt, ermöglicht kollaboratives Editieren und Chat/Diskussions-Verläufe. Einfaches Upload von Bildern und Einbinden von YouTube Videos. Sowohl interne Versionierung von Dokumenten und auch extern Versionierung via GitLab-Anbindung.
- **GitLab:** Versionierung von CAD/STL-Dateien, [HackMD-Versionierung](). Feedback zum Projekt via Issues.
- **Ente:** Teilen von [Photoalben](https://albums.ente.io/?t=n4gJSRmD9c#pEi8SqN4NvcUnWbeJyfcis1qUBdfnKazd1G65SL3a2p), primär "rohe" Fotostrecken.
- **YouTube:** [Erklär- und Bau-Videos](https://www.youtube.com/playlist?list=PLSxNMFG9ojQwhjzWL1CTtLxCqtKM5Zwmm), Kommentarfunktion mit Zeitreferenzierung.
- **Printables:** [CAD/STL-Dateien](https://www.printables.com/@hmk_292473/collections/2752290). Tracking von Mods und Bewertungen anderer Nutzer.

Der Trolley-Prototyp ist nicht als ein Produkt gedacht sondern als ein Baukastensystem von **Produkt-Varianten**. Der Trolley besteht aus 3 Baugruppen die relativ einfache "Andockpunkte" (Schnittstellen) haben:
1. **Rahmen:** Der Rahmen hält die Tasche und die Achse mit Rollen. Am Holzrahmen können niederschwellig Add-Ons angebracht werden (z.B. durch Bohren und Schrauben).
2. **Achse mit Rollen:** Die Achse ist ein Rundstab bzw. Schrauben aus Metall die an 2 Kanthölzern des Rahmens fixiert werden.
3. **Tasche:** Die Außenmaße der Tasche muss dem Rahmen entsprechend gewählt werden. Evtl. ist noch eine Halterung am Rahmen für die Tasche notwendig.

Durch die mechanischen Andockpunkte sind (ad-hoc) Mods und Add-Ons relativ einfach möglich. Einzelne Bauteile wie die Räder ermögliche Varianten in Form von Fertigteilen (COTS) vom Baumarkt/Amazon/AliExpress, 3D-Druck oder Recycling/Upcycling.

Die Doku ist modular aufgebaut mit dem Ziel, dass eine neue Variante mit relativ wenig Aufwand und Redundanz beschrieben werden kann. Dies wurde insbesondere für den Rahmen exemplarisch umgesetzt:

1. [Abstraktes Design des Rahmens](/@hkienle/frame-design/), unabhängig von konkreten Maßen -- dabei hilft das Gridbeam-System. Der Rahmen hat optionale Add-Ons, auch eine Form von Variabilität.
2. [Design des Rahmens mit Maßen](/@hkienle/frame-17x17/). Hiermit kann der Rahmen an sich gefertigt werden, allerdings ist noch nicht festgelegt welche Add-Ons und welche Achskonstruktion und Tasche das fertige Produkt haben wird.
3. [Konkreter Bau eines Rahmens](/@hkienle/frame-build-sturdy_cots/), erlaubt die Replizierung eines bereits gebauten Rahmens mit genauer Beschreibung der verwendeten Add-Ons, Design-Instantziierung und Bauteile (BOM).

## Nachhaltigkeit & Ressourceneffizienz 

Die Benutzung des Trolleys verspricht Nachhaltigkeit wenn er statt eines Autos etc. eingesetzt wird. Er kann auch Signalwirkung auf andere haben.

Die bisherigen Varianten des Trolleys sind nicht durchgängig auf Nachhaltigkeit hin optimiert, aber es gibt einige Aspekte in diese Richtung:

- Eine Rahmen-Variante benutzt z.B. Metall-Schrauben die bereits in einer Werkstatt in größerem Umfang vorhanden sind, somit viel kein CO2 durch Verschickung und Verpackung an. Da diese Schrauben allerdings Senkkopf haben wurden passende Ringe konstruiert und 3D gedruckt (relativ wenig Material, aber CO2>0).
- Eine Variante des Trolley verwendet einen bereits vorhandenen Weinkarton als Tasche, eine andere Variante verwendet alte Wahlplakate.
- Für eine Rahmen-Variante wurden Kanthölzer mit geringer Profildicke gewählt (13x13mm vs. z.B. 20x20mm) um an Materialvolumen zu sparen und es wurde einfaches und leichtes  Kiefernholz benutzt.

Es sind aber auch Varianten denkbar und gewollt, die **bewusst auf "Öko-Look" verzichten** indem z.B. ein neuer (Wein-)Karton verwendet wird oder neue, hochwertige PP-Hohlkammerplatten. Ebenso können hochwertigere Holzarten (Buche statt Kiefer) und schicke Messingschrauben gewählt werden. Durch einen hochwertigeren Look können potentiell andere "Käuferschichten" angesprochen werden.

## Community

Das Projekt wurde bisher wenig nach außen kommuniziert. Ziel war es zuerst konkrete Varianten "zum Anfassen und Erleben" zu entwickeln und dokumentieren -- und damit eine Diskussionsgrundlage zu schaffen.

Eine erste Variante wurde auf einer [Kunstaustellung in Berlin](https://gies.se/lange-nacht-der-bilder-2025-giesse/) präsentiert (LNDB, September 2025). Dort hatte ich den Eindruck, dass ein konkretes Objekt zu einem fruchtbaren Dialog zu OSH-Philosophie und Design/Konstruktions-Feedback führt.

Die anstehende [oSHOP-Konferenz](https://www.oshop-network.de/konferenz-2025/) soll dazu genutzt werden um mit OSH-Interessierten ins Gespräch zu kommen. Diese haben dann die Möglichkeit über GitLab Issues und Kommentarfunktionen von HackMD und YouTube öffentlich Input zu geben.

Es hätte sicher auch Vorteile gehabt Feedback früher einzuholen wo das Design noch offener war und ich als Entwickler auch mehr in der Lage gewesen wäre andere Ideen wohlwollend aufzugreifen. So wurden von mir gewisse "diktatorische" Entscheidugen getroffen, z.B. das Gridbeam-System aufzugreifen. Alternativen wurden nicht wirklich im Vorfeld analysiert da es mir gut gefällt, ich bereits weiß, dass ich damit produktiv arbeiten kann und Freude dabei habe. All das stärkt die Motivation in die Umsetzung zu kommen und sich damit (in meiner freien, unbezahlten Zeit) zu befassen.

Im positiven gesprochen, der Trolley ist momentan absolut nicht in Gefahr von [*design by committee*](https://en.wikipedia.org/wiki/Design_by_committee) :smirk:.

## Kreativität & Innovationsgrad 

Das Projekt nimmt als Startpunk ein (low-budget) Industrieprodukt und versucht es mit OSH-Prinzipien neu zu denken. Clevere Lösungen im Sinne traditioneller Innovationen von "höher, schneller, weiter" waren nicht das Ziel (siehe auch [Ivan Illichs *Tools for Conviviality*](https://en.wikipedia.org/wiki/Tools_for_Conviviality)).

Wichtige Impulse die dieses Projekt potentiell bringen kann sind:

- OSH muss in die Lebenswirklichkeit der Menschen kommen wenn es erfolgreich sein will. Dafür muss OSH auch "auf der Straße" sichtbar werden und zu Diskussionen/Reaktionen "provozieren".
Die Tasche hat dabei z.B. zusätlich das Potential als Werbefläche für OSH genutzt zu werden (QR code).
- Statt High-Tech, setzt der Trolley auf **niederschwellige Technik und Andockpunkte**. Er hat eine leicht nachvollziebare Mechanik und eine Konstruktion die zu diskutieren, experimentieren und modifizieren einläd.
    - Je nach Variante liegt der Schwerpunkt z.B. auf wenigen einfachen Werkzeugen und Normteilen oder auf 3D-Druck.
    - Denkbar sind dadurch kindergerechte Workshops und weniger technische Add-Ons wie künstlerische Verschönerungen durch Bemalungen und Umhäkelungen der Kanthölzer ([Yarn bombing](https://en.wikipedia.org/wiki/Yarn_bombing)).

## Technische Umsetzung & Entwicklungsfortschritt 

Der oSHOP-Wettbewerb hat den Anstoß dazu gegeben die Idee eines DIY-Einkauftrolleys möglichst konsequent nach OSH-Prinzipien umzusetzen. Zuvor war nur geplant gewesen einen einzigen Trolley zu bauen um diesen dann selbst einzusetzen nachdem es sich abgezeichent hatte, dass der existierende low-budget Hackenporsche nicht mehr lange durchhalten würde. Insofern hat der Wettbewerb stark geholfen den Fokus auf OSH zu legen und bei der Erstellung von OSH-Dokumentation praktische Erfahrungen zu sammeln.

Der Start des Projekts mit einem ersten Design-Prototyp wurde dann auch für die [Einreichung zum oSHOP-Wettbewerb](@hkienle/tn-oshop-proposal) entwickelt.

Der aktuelle Stand der Konstruktion:
- 2 Rahmenkonstruktionen: 13x13 und 17x17-Profile.
- 3 Achsaufhängungen: COTS-Metallteile und 3D-Druck.
- 2 Taschen Weinkarton (COTS) und Wahlplakat.

Die Dokumentation hinkt leider noch hinterher, soll aber bis zur oSHOP-Konferenz weitgehen vollständig sein (in einer ersten Fassung).

Praxistests und Belastungstests wurden noch gar nicht durchgeführt, diese sind bei einem mechanischen Produkt für nicht unbedingt technikaffine "Endverbraucher" aber essentiell. (Z.B., durch die ständigen Vibrationen bei der Benutzung können sich Schraubverbindungen über die Zeit lösen.)

## Methodik/Vorgehen

Es wurde keiner Design-Methodik oder ähnliches gefolgt. Im großen und ganzen konnten die Design-Ideenen ohne Hindernisse umgesetzt werden. Durch die längeren Entwicklungspausen gab es zwischendurch immer wieder zufällige Ideen die "hochgepopt" sind und Lösungen und neue Varienten ermöglicht haben.

Unerwartet zeitaufwändig waren die Rechere und der Einkauf von COTS-Bauteilen. Auch gab es Verzögerung durch den Kauf von Bauteilen (AliExpress) die dem "Flow" nicht förderlich waren. Bei AliExpress und Amazon (aber auch Baumarkt) gibt es immer wieder unvollständige und widersprüchliche Spezifikationen.

Hauptsächliche Treiber die das Projekt nach vorne gebracht habe waren (leider) Deadlines des Wettbewerbs :neutral_face:. Die größe Herausforderng war Zeitmangel und sich für das Projekt neu zu motiveren und gedankliches wiedereinfinden nach (Zwangs-)Pausen.

## Referenzen

- [Einreichung zum oSHOP-Wettbewerb](/@hkienle/tn-oshop-proposal)

