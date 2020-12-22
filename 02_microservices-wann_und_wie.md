---
layout: post
title: Microservices - Wann und Wie?
description: Welche Voraussetzungen muss ich für Microservices erfüllen?
thumbnail: assets/images/pic06.jpg
nav-menu: true
---

Eine Microservices-Architektur bietet sich vor allem dann an, wenn Bedarf für schnelle, häufige und unabhängige
Deployments von lose gekoppelten Komponenten besteht. Dementsprechend ist eine vollautomatische Continuous
Integration/Continuous Delivery-Pipeline inklusive automatisierter Tests mit hinreichender Abdeckung obligatorisch.
Ein testgetriebenes Vorgehen sowie Trunk-based Development sind die logischen Konsequenzen. Weitere wichtige Treiber
können auch ein Polyglot-Szenario, also Komponenten in unterschiedlichen Programmiersprachen und Frameworks, und
Omnichannel (Web/Desktop/Mobile) sowie hohe Skalierbarkeit sein.

### Auf jeden Fall sollte sichergestellt sein, dass eine klare logische, fachliche oder funktionale Trennung der Komponenten vorliegt.

Am häufigsten aber werden die Voraussetzungen an die Organisation unterschätzt, in der die Microservices entwickelt
und betrieben werden. Der Schnitt der Teams und die Gestaltung der Organisation sind mindestens ebenso wichtig wie
technische Abwägungen (Conway’s Law). Ein Microservice muss immer von genau einem Team verantwortet werden.
Dabei sollte ein einziges Team nicht zu wenige und nicht zu viele Microservices gleichzeitig (cognitive load) entwickeln.
Es muss klare und etablierte Kommunikationskanäle zwischen den Teams geben. Die Teams brauchen ausreichend
Synchronisationspunkte und eine transparente Strategie für die Produktentwicklung (z.B. in Form von Epics, Journeys und Initiativen).
Und sie benötigen Erfahrung im Umgang mit (hoch-)verteilten Systemen in Cloud-Umgebungen.
