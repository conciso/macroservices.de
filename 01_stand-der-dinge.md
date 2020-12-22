---
layout: post
title: Der Stand der Dinge
description: Microservices, Nanoservices, Serverless, Big Ball of Mud – oder doch Macroservices?
thumbnail: assets/images/pic05.jpg
nav-menu: true
---

Microservices sind der große Architekturtrend der letzten Jahre. In Gartners Hypecycle 2020 befinden sich Microservices
im Pfad zur Erleuchtung. Auch Microapps sind beliebter denn je. In der Architektur scheint klar: '<strong>Kleiner ist besser</strong>'.
Obwohl – seit nicht nur in [Social Media](http://highscalability.com/blog/2020/4/8/one-team-at-uber-is-moving-from-microservices-to-macroservic.html)
der Begriff <strong>Macroservice</strong> die Runde machte, scheint das Denken in größeren Einheiten auch wieder auf dem Vormarsch.

Microservices, Nanoservices, Serverless, Big Ball of Mud – oder doch Macroservices? Na was denn jetzt, klein oder groß?
Immerhin eines lässt sich mit Sicherheit sagen: die Größe scheint entscheidend. Heuristiken wie
[Amazons 2-Pizza Teams](https://searchapparchitecture.techtarget.com/blog/Microservices-Matters/The-culture-of-microservices-Conways-law-and-two-pizza-boxes)
zielen ja auch genau in diese Richtung.

## Size does matter. But wait … does it?

Zoomen wir mal ein wenig heraus aus dem Bild. Egal, wie groß der Service ist – er ist Teil eines Systems von Services.
Viele Services agieren miteinander, erfüllen Aufgaben in einem Gesamten – und brauchen dafür Verbindungen zueinander.
Sie bilden ein System. Darum ist Architekturdesign schon immer auch Systemdesign. Und in Systemen geht es inhärent immer
um Abgrenzung: was ist drinnen, was ist draußen? Die Größe eines Services ergibt sich durch diese Abgrenzung.
Entscheidend ist die Frage, was sich innerhalb der Grenzen bewegt, was dazwischen und was außerhalb.

Und die Antwort auf diese Frage ist immer ein Kompromiss. Je größer die Services, desto weniger Verbindungen braucht es
zwischen ihnen. Und je kleiner die Services, desto mehr Verbindungen braucht es.

## Die Sache mit der Komplexität

Mehrere kleinere Services ergeben mehr Beziehungen. Wenige große Services ergeben weniger Beziehungen. Und diese
Verbindungen produzieren potentielle Problemstellen. Denn sie funktionieren nicht immer zuverlässig. Bedingt durch
unabhängige Laufzeits-, Deployment- und Lebenszyklen der Einzelteile fehlen Antworten oder werden falsche Antworten
weitergegeben. Je mehr Beziehungen zwischen Services gepflegt werden müssen, desto höher ist die Komplexität des Gesamtsystems.

Der Schlüssel liegt darum in der Herstellung einer ausgewogenen Balance.
Zwischen der Komplexität der Einzelteile und der des Gesamtsystems.

## Softwarearchitektur bedeutet auch Organisationsentwicklung!

Gleichzeitig sollten auch die sozi-technischen Aspekte des Systems betrachtet werden. Um beim Amazon-Beispiel zu bleiben:
wie groß sind denn eigentlich die zwei Pizzen? Minipizzen, Maxipizzen oder Familienpizza? Wie groß ist das Team, das einen Service betreut?

Auch Teams sind beschränkt in der Menge an inhärenter, technischer und organisatorischer Komplexität, die sie
verkraften können. Cognitive Load ist ein nicht zu unterschätzender, beschränkender Faktor. Und die viel beschworene
Team-Autonomie erhöht die Komplexität der Service-Systeme zusätzlich. Sicherlich ist die Autonomie ein zentraler Punkt,
wenn Teams schnell und effektiv arbeiten sollen. Nur – wir bauen Systeme! Daher müssen wir auch in Systemen denken.

Ein Service oder ein Team ohne Abhängigkeiten zu anderen kann qua definitionem kein Teil eines Systems sein.
Unabhängige Services gibt es nicht, eine Beziehung oder Abhängigkeit besteht immer.

Daher sprechen wir weniger über Größe – sondern über Abgrenzungen. Über sinnvolle Abgrenzungen, die eine Balance aus
Komplexität innerhalb eines Services und der im Gesamtsystem herstellen. Und die ist abhängig von den verfügbaren
Business Capabilities, den gewünschten User Journeys und den bestehenden Geschäfts- und Organisationsprozessen.
Nicht zu vergessen, manchmal auch notwendigerweise von technischen Treibern. Berücksichtigt man diese Aspekte,
bekommt die Größe an sich eine zweitrangige Rolle. Und man denkt mehr das System an sich.

## Fazit

Wir propagieren hier also kein Blueprint-Konzept für Macroservices. Wir möchten ihnen Ideen, Überlegungen und
Heuristiken zu unterschiedlichsten Gesichtspunkten guten Service-Designs an die Hand geben. In Form von Artikeln,
Diskussionen, Webinaren – fundiert, ausgewogen und regelmäßig aktualisiert.
