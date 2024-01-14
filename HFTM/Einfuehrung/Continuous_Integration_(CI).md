# Continuous Integration (CI)

---
>[⬅️**back**](./README.md)  

Continuous Integration (CI) ist ein Softwareentwicklungsprozess, bei dem die
Teammitglieder ihre Arbeit regelmäßig integrieren. Im Idealfall integriert jede
Person mindestens einmal am Tag, was zu mehreren Integrationen pro Tag führt.
Jede Integration wird durch einen automatisierten Build-Prozess geprüft, der auch
Tests umfasst, um Integrationsfehler so schnell wie möglich zu erkennen. Viele Teams
haben berichtet, dass die Zahl der Integrationsfehler deutlich gesunken ist und sie
dadurch schneller gemeinsame Software entwickeln können.

Der Hauptgedanke hinter CI ist, den langwierigen und mühsamen Integrationsprozess zu
vermeiden, der in der Vergangenheit stattfand und bei dem unabhängige Quellcode-Teile
zusammengeführt und Konflikte gelöst werden mussten. CI ermöglicht es Entwicklern, an
ihren individuellen Kopien der Codebasis zu arbeiten und ihre Änderungen schnell und
einfach zu integrieren. Durch die häufige Integration können potenzielle
Integrationsprobleme früher erkannt und behoben werden, was zu einem stabileren und
fehlerfreien Softwareprodukt führt.

Für die kontinuierliche Integration sind nicht unbedingt spezielle Tools erforderlich,
aber viele Teams finden es hilfreich, einen Continuous Integration Server zu verwenden.
Ein weit verbreitetes Open-Source-Tool ist CruiseControl, aber es gibt auch viele andere
CI-Server, sowohl Open-Source als auch kommerziell.

Bei der Implementierung von Continuous Integration geht es darum, den Build-Prozess zu
automatisieren, den Build selbst zu testen und sicherzustellen, dass jeder Entwickler
regelmäßig in die Mainline überträgt. Dazu gehört auch, dass die Hauptlinie regelmäßig
auf einer Integrationsmaschine gebaut wird und dass fehlerhafte Builds sofort behoben
werden. Ein schneller Build-Prozess, das Testen in einer Umgebung, die der
Produktionsumgebung sehr ähnlich ist, und der einfache Zugriff auf die neueste
Version der ausführbaren Datei sind weitere wichtige Aspekte der kontinuierlichen
Integration.

Zu den Vorteilen der kontinuierlichen Integration gehören ein geringeres Risiko,
eine bessere Kommunikation und Zusammenarbeit zwischen den Teammitgliedern,
schnelleres Feedback zu Integrationsproblemen und die Möglichkeit, neue Funktionen
schneller an die Benutzer/innen zu liefern. Außerdem hilft sie, Fehler früher im
Entwicklungsprozess zu erkennen und zu beheben, was zu einem stabileren und
zuverlässigeren Softwareprodukt führt.

## Questions

> Wozu brauche ich das?
> >Eine Versionskontrolle von Code/Files zu Bieten welches erlaubt mit anderen leuten zu kolaborieren  
> Weiter erlaubt es den Code/Files einfach fuer andere leute bereit zu stellen
>
> Was ist der Nutzen für ein Entwicklungsteam?
> > Es ermoeglicht genaue Zeitpunkte bereit zu stellen und somit genauere kontolle darueber zu haben welche version der eigenen files nun mit den anderen geteilt wird.
>
> Warum ist dieses alte Problem für mich heute noch relevant?
> > Heute ist git eine der beliebtesten und weitverbreitetsten Versionskontrollen welche verwendet wird. heutyutage ist dies noch immer relevant da tools wie O365 genaue commits nicht erlauben oder selbst entscheiden wann deise ausgefuert wurden.  
> > Weiter ist Git OS unabhaengig und kann somit heute auch inter Company und inter device verwendet werden.
>
> Wie begegne ich dem Thema heute, ev. in meiner täglichen Arbeit?
> > Durch meine arbeit als Systemtechniker in einer noncloud umgebng bin, benutze ich keine versions kontolle. Abgesehen von o365 welches ich fuer Dokumente und Onnotes benutze.

---
>[⬅️**back**](./README.md)
