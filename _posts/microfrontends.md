---
layout: post
title: Microfrontends
description: Ipsum dolor sit amet
image: assets/images/pic01.jpg
---

In der Softwareentwicklung sind Microservices schon länger gang und gäbe. Auch der Ansatz, unterschiedliche Themen von
unterschiedlichen Teams bearbeiten zu lassen, liegt nahe. Bei der Entwicklung zugehöriger Frontends und UI Themen werden
die Services daher oft nach Frontend- und Backend-Teams geschnitten. Das Thema Microfrontend stellt den "horizontalen"
Schnitt der Teams in Frage und zielt darauf ab, einen eher fachlichen, vertikalen Schnitt zu machen.

Die beiden Frontend- und Backend-Teams sollen zusammengeführt werden zu einem Team, das beides entwickelt, Frontend und
Backend. Eine dünne Integrationsschicht ist nun dafür zuständig, dass die Einzelteile der UI zu einem Ganzen
zusammengefügt werden und als eine Einheit agieren. Dieser Zuschnitt der Anwendung soll dem Nutzer natürlich nicht
auffallen. Um die User Experience also dennoch bruchfrei zu gewährleisten, wahren z.B. Pattern Libraries oder
Styleguides für alle Teams eine einheitliche UI und UX.

Für die Entwicklung gibt es bei dieser Art von Aufteilung unter anderem einen Geschwindigkeitsvorteil und kürze
Turnaround-Zeiten für verschiedene Fachlichkeiten. Die Frontend-Entwickler der einzelnen Teams sind nun „nur“ noch für
die UI der Fachlichkeit des eigenen Teams zuständig. Es gibt nicht mehr DAS Frontend-Team für die Gesamtintegration
aller Fachlichkeiten in die UI.

Die einfachste Form der Integration ist hier die Verlinkung verschiedener Systeme mit gleichem Erscheinungsbild.
Etwas komplexer ist z.B. eine Single-Page-Application aus verschiedenen Teilanwendungen. Die einzelnen Teile können
dann innerhalb des Microfrontend-Ansatzes in unterschiedlichen Frameworks geschrieben werden. Jedes Team kann selbst
entscheiden, welches Framework ihm am meisten liegt. Für die Gesamtanwendung ist es egal, ob dies Angular, React, Vue
oder etwas völlig anderes ist.

Eine genaue Abgrenzung der beiden Extreme (und allem, was dazwischen liegt) ist nicht notwendig. Microfrontends sind
keine feststehende Technologie, sondern ein Architekturmuster. Man kann im Browser rendern, klassisch im Backend oder
eben eine Mischung aus beidem.

Eine Herausforderung bleibt jedoch: Die Einzelteile müssen integriert werden. Es muss klar sein, wie Daten von einem
Team zum anderen geleitet werden. Dazu gibt es aber beinahe unzählige Möglichkeiten: von Datenlinks über ein Bus-System,
das im Browser lebt, bis hin zu gemeinsamen Store-Implementierungen.

Einzelne Elemente der verschiedenen Teams können hier zusätzlich als „Mini-Anwendungen“ bereitgestellt werden. Um zum
Beispiel auf der Bezahl-Seite des eigenen Online-Shops noch eben ein paar mehr Produkte vorzuschlagen, kann das
Produkte-Team eine Ansicht mit für den Kunden speziell zusammengestellten Produktlisten bereitstellen. Diese kann dann
vom anderen Team mit eigener Datenbasis und Darstellung integriert werden.

Generell lässt sich sagen, dass die Vorteile der autonomen Teams mit eigenen Entwicklungszyklen den Anforderungen an
die Integration und Architektur gegenüberstehen.
