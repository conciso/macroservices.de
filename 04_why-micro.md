---
layout: post
title: Why Micro?
description: Welche Vorteile haben Services mit einem möglichst kleinen Schnitt?
thumbnail: assets/images/pic05.jpg
nav-menu: true
---

Klassische Enterpriseanwendungen wurden lange Zeit mit mehrschichtigen monolithischen Architekturen implementiert.
Dabei hat sich jedoch gezeigt, dass es bei monolithischen Anwendungen sehr zeit- und kostenaufwändig ist, neue Features
zu implementieren. Denn die Komponenten sind oft gekoppelt. Zudem muss immer das Gesamtsystem ausgeliefert werden, was
in aller Regel nicht in hoher Frequenz und Geschwindigkeit möglich ist.

Gerade, wenn die Codebasis eine gewisse Größe erreicht hat (und immer weiter wächst), wird es immer schwerer,
Nebeneffekte und Auswirkungen zu überblicken. Gleichzeitig stehen sich bei den Änderungen in einer einzigen großen
Codebasis die Entwickler bzw. Teams gegenseitig auf den Füßen. Und Monolithen können immer nur als gesamtes System
skaliert werden, nicht gezielt einzelne Komponenten, was mit hohen Kosten verbunden ist.

Um diese Probleme zu beheben, kann man das Gesamtsystem in viele kleine Microservices aufbrechen, die sich autark
entwickeln, testen und liefern lassen. Microservices bieten zudem eine hohe Flexibilität in der Implementierung
(„Polyglot“) sowie gegenüber unsicheren Anforderungen, die häufigen Änderungs- und Lieferbedarf mit sich bringen.

Wenn schnelle und häufige Releasezyklen von hoher strategischer Bedeutung sind und die Organisation, in der das
Softwaresystem entsteht, mit entsprechend geschulten und cross-funktionalen Teams arbeitet, ist diese Form der
Softwarearchitektur sehr sinnvoll. Gerade, wenn sich die Funktionalität der Komponenten klar (fachlich oder logisch)
auf einzelne Services aufteilen lässt und gezielte Skalierbarkeit sowie hohe Implementierungsflexibilität hinsichtlich
Technologien und Frameworks gewünscht sind, sollte eine Microservices-Architektur ernsthaft in Betracht gezogen werden.

Auch für das Erreichen einer geringen time-to-market inklusive CI/CD und DevOps ist eine Microservices-Architektur
äußerst attraktiv und erlaubt ein evolutionäres oder Prototypen-basiertes Vorgehen: wenn ein einzelner Microservice
beispielsweise innerhalb von 14 Tagen von Grund auf neu implementiert werden kann, dann sind innerhalb kürzester Zeit
sogar grundlegende Anpassungen an der Anwendung möglich – etwas, das bei monolithischen Architekturen womöglich ein
wirtschaftliche Scheitern des gesamten Softwareprojekts nach sich ziehen würde.
