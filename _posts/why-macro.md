---
layout: post
title: Why Macro?
description: Lorem etiam nullam
image: assets/images/pic03.jpg
---

Wir kennen alle viele gute Gründe für Microservices und warum Monolithen oft nicht der richtige Weg sind.
Es wurde lange auf wirklich jeder einzelnen Konferenz als die Lösung für fast alle Probleme verkauft.

Mircoservices haben jedoch nicht nur viele Vorteile, die mein Kollege in [Why Micro?](./why-micro.html)
sehr gut beschrieben hat.

Der Schnitt ist hier sehr entscheidend. Es ist allerdings nicht immer sinnvoll möglich, eine saubere fachliche und
funktionale Trennung so klein zu gestalten, dass wir von Microservices sprechen können. Ein künstliches Kleinschneiden
der Services erhöht nur unnötig die Komplexität und die Abhängigkeiten von Services.

Was gerade bei Enterpriseanwendungen beim Schneiden der Services oft vergessen wird, ist der Overhead, der mit jedem
Microservice im Konzernumfeld entsteht. Wir sprechen hier auch über nicht funktionale Anforderungen, die so komplex und
umfangreich sein können, dass das Implementieren der Businesslogik eines Microservices nur noch einen kleinen Teil des
Aufwandes ausmacht. Dazu kommen Themen wie Betriebsführung, Dokumentation und Wartung.

Time-to-Market ist auf den ersten Blick bei Microservices unschlagbar. Wir können sehr gut kleine Änderungen vornehmen
und schnell und häufig Deployments durchführen. Dieser Vorteil kann aber auch zum Nachteil werden, wenn wir neue
Features entwickeln. Umso mehr Microservices betroffen sind, desto mehr organisatorischer und technischer Overhead
kommt hinzu.