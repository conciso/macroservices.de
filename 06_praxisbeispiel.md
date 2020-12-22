---
layout: post
title: SIZE MATTERS – wann klein zu klein und groß zu groß ist
description: Interview mit Lars Winterhalter und Lukas Pradel
thumbnail: assets/images/praxis.jpg
nav-menu: true
---

##### Microservices scheinen die Lösung schlechthin zu sein … gibt es denn auch Situationen, in denen "klein" zu klein wird?

<blockquote>
<strong>Lukas</strong>: Ja, ganz so einfach ist es nicht. Mir fällt ein Beispiel bei einem unserer Kunden ein.
Dort hatten wir ein System ganz nach den Paradigmen einer Microservice-Architektur entwickelt.
Im Laufe der Entwicklungszeit sind dabei relativ viele unabhängige Services entstanden,
die synchron über HTTP/JSON oder asynchron über Messaging miteinander kommunizierten. 
</blockquote>

<blockquote>
<strong>Lars</strong>: Der Vorteil war klar, gerade zu Anfang konnten wir damit sehr gut parallel arbeiten, an mehreren Stellen gleichzeitig.
Meist mit ein oder zwei Entwicklern pro Sprint und Service. Ich erinnere mich noch, wie sehr uns die Flexibilität
begeistert hat, die diese Microservices gerade bei einem Projekt auf grüner Wiese bieten.
</blockquote>

<blockquote>
<strong>Lukas</strong>: Ja, daran erinnere ich mich auch. Aber als dann der erste Livegang näher rückte, wurden dann doch nach und
nach ein paar Schattenseiten der ziemlich klein geschnittenen Services deutlich.
Wir mussten in alle Services Security-Anforderungen eingebauen. Das kostete uns Wochen!
</blockquote>

<blockquote>
<strong>Lars</strong>: Der Umzug in das neue, externe Cluster war auch ziemlich zeitaufwendig.
Die schiere Masse der Services und die teilweise unterschiedlichen Arten der Umsetzung von bereits
integrierten Anforderungen machten die Umsetzung sehr aufwendig. Dann kamen noch Probleme mit Timeouts dazu.
Die mussten wir dann mit dem Einbau von Caching und asynchroner Verarbeitung lösen.
</blockquote>

<blockquote>
<strong>Lukas</strong>: Es war ziemlich auffällig. Teams, die ihre Domäne nur auf eine paar Services aufgeteilt hatten,
konnten dieselben Anforderungen innerhalb weniger Stunden erfüllen. Hier war also klein zunächst wirklich zu klein.
Darum mussten wir umdenken. Heute sind einige der Services, die im Grunde nur Rest-Schnittstellen für eine Datenbank
waren, in einen einzigen konsumierenden Service integriert.
</blockquote>

<blockquote>
<strong>Lars</strong>: Und statische Daten, die von mehreren Services genutzt werden, laden wir jetzt nur einmal, beim Start, in den Speicher.
Damit haben wir einen wesentlich flüssigeren Betrieb und eine bessere Skalierbarkeit erreicht.
</blockquote>

##### Und wie sieht es beim Gegenteil aus? Kann „groß" auch zu groß geraten?

<blockquote>
<strong>Lukas</strong>: Ja, auch das ist möglich, sogar im gleichen Projekt. Aufgrund der Erfahrung mit den zu kleinen Microservices
haben wir kurz darauf in einem anderen Team eine Domäne in nur zwei Services geschnitten. Komplett anders.
Selbstverständlich waren die Services immer noch in die Gesamtstruktur der Landschaft integriert.
</blockquote>

<blockquote>
<strong>Lars</strong>: Stimmt – und zu Beginn konnten wir auf hier aufgrund der ziemlich disziplinierten  Teams sehr schnell und
unabhängig voneinander entwickeln. Wir konnten auch noch weitere querschnittliche Anforderungen recht schnell
und fast nebenbei erledigen. Alles schien perfekt.
</blockquote>

<blockquote>
<strong>Lukas</strong>: Allerdings merkten wir mit der Zeit, dass wir auch hier nicht unbedingt die ideale Größe geschnitten hatten.
Zum Beispiel war die Fehlersuche bei Bugs viel aufwändiger als im vorherigen Projekt.
Und als sich dann ein neuer Kollege in den Code einarbeitete, wurde zudem klar,
dass die Module doch nicht so klar voneinander getrennt waren, wie wir das ursprünglich geplant hatten.
</blockquote>

<blockquote>
<strong>Lars</strong>: Nach erneuter Überlegung teilten wir die beiden Services wieder auf.
Wir trennten die Aufbereitung der extern zugelieferten Daten von der eigentlichen Verarbeitung dieser Daten.
Die beiden so entstandenen neuen Services verbanden wir nur per Message-Queue.
Durch die klare Trennung der Zuständigkeiten wurde die Skalierbarkeit der einzelnen Komponenten deutlich besser.
</blockquote>

<blockquote>
<strong>Lukas</strong>: Und auch der Einbau neuer Funktionalitäten oder die Anpassung einzelner Komponenten wurde deutlich einfacher.
Und es wurde einfacher, mit mehreren Entwicklern parallel zu arbeiten, da wir uns weniger Gedanken um Seiteneffekte
oder Mergekonflikte machen mussten.
</blockquote>

<blockquote>
<strong>Lars</strong>: Unser Fazit aus beiden Erfahrungen ist vor allem eines: Man braucht viel Fingerspitzengefühl, um die richtige
Balance aus Software-Performance und Team-Performance zu finden.
</blockquote>

<blockquote>
<strong>Lukas</strong>: Manchmal wird der ideale Zuschnitt der Services auch erst im Verlauf eines Projekts deutlich.
Darum ist es zweitens sehr wichtig, bereits getroffene Entscheidungen immer mal wieder kritisch zu hinterfragen und ggf. zu korrigieren.
</blockquote>

##### Danke für Eure Einblicke!
