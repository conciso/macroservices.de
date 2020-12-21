---
layout: post
title: Praxisbeispiel - Size matters
description: Bericht aus dem Projektalltag
image: assets/images/pic04.jpg
nav-menu: true
---

# Wann ist klein zu klein?

Bei einem unserer Kunden haben wir ein System nach den Paradigmen einer Microservice-Architektur entwickelt.
Dabei sind mit der Zeit recht viele unabhängige Services entstanden, die synchron über HTTP/JSON oder asynchron über
Messaging miteinander kommunizierten. Anfänglich konnten wir dadurch sehr gut parallel an mehreren Stellen gleichzeitig
arbeiten (meist ein oder zwei Entwickler pro Sprint pro Service) und waren begeistert von der Flexibilität, die dieses
Vorgehen gerade bei einem Projekt auf der grünen Wiese bietet.

Als dann aber der erste Livegang näher rückte, wurden nach und nach auch einige Schattenseiten unserer doch sehr klein
geschnittenen Services deutlich. Änderungen, die in alle Services eingebaut werden mussten (z.B. Security-Anforderungen),
oder der Umzug in ein neues, externes Cluster kosteten uns mehrere Wochen. Die schiere Masse der Services und die teils
unterschiedlichen Arten der Umsetzung bereits integrierter Anforderungen machten die Umsetzung sehr aufwendig.
Zudem hatten wir immer wieder Probleme mit Timeouts, welche wir durch den Einbau von Caching oder asynchroner
Verarbeitung lösen mussten.

Teams, die ihre Domäne nur auf eine Handvoll an Services aufgeteilt hatten, konnten dieselben Anforderungen innerhalb
weniger Stunden erfüllen. Darum haben wir umgedacht. Mittlerweile haben wir einige der Services, die im Grunde nur
Rest-Schnittstellen für eine Datenbank waren, in den einzigen konsumierenden Service integriert. An anderer Stelle
laden wir (statische) Daten, die von mehreren Services genutzt werden, nur einmal beim Start in den Speicher und
erreichen so einen wesentlich flüssigeren Betrieb und bessere Skalierbarkeit.

# Wann ist groß zu groß?

Unter anderem aufgrund dieser Erfahrung haben wir kurz darauf im selben Projekt, aber in einem anderen Team einen
komplett anderen Schnitt unserer Domäne gewählt. Diesmal haben wir nur zwei Services definiert (natürlich immer noch
in die Gesamtstruktur der Landschaft integriert). Auch hier konnten wir zu Beginn aufgrund des sehr diszipliniert
arbeitenden Teams sehr schnell und unabhängig voneinander entwickeln. Alles schien perfekt, als wir auch weitere
querschnittliche Anforderungen recht schnell und fast nebenbei erledigen konnten.

Allerdings merkten wir mit der Zeit, dass wir auch hier nicht unbedingt die ideale Größe gewählt hatten. Zum Beispiel
war die Fehlersuche bei Bugs viel aufwändiger, als im anderen Projekt. Als sich neue Kollegen in den Code einarbeiteten,
wurde zudem klar, dass die Module doch nicht so klar voneinander getrennt waren, wie ursprünglich geplant.

Nach einiger Überlegung teilten wir die beiden Services wieder weiter auf und trennten die Aufbereitung der extern
zugelieferten Daten von der eigentlichen Verarbeitung dieser Daten. Die beiden so entstandenen neuen Services verbanden
wir per Message-Queue. Durch diese Herangehensweise und die klare Trennung der Zuständigkeiten erreichten wir eine
bessere Skalierbarkeit der einzelnen Komponenten und eine Vereinfachung des Einbaus neuer Funktionalitäten sowie der
Anpassung einzelner Komponenten. Zudem wurde es einfacher, mit mehreren Entwicklern parallel zu arbeiten, da man sich
weniger Gedanken um mögliche Seiteneffekte oder Mergekonflikte machen musste.

# Fazit

Es braucht viel Fingerspitzengefühl, die richtige Balance aus Software-Performance und Team-Performance zu finden.
Der ideale Zuschnitt der Services wird manchmal auch erst im Verlauf eines Projekts deutlich. Darum ist es sehr wichtig,
bereits getroffene Entscheidungen immer mal wieder kritisch zu hinterfragen und ggf. zu korrigieren.
