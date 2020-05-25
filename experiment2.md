<!--
.. title: TuR: Tomcat Aufbau
.. date: 2018-11-19 09:00:00
.. tags: tur, puppet4
.. category: TuR
.. link:
.. description:
.. type: text
.. author: Judith Platzer
-->

<!--
TuR: Tomcat Aufbau
==================
-->

<div id="toc" />

Hier beschreibe ich, wie ein Tomcat Aufbau E-Umgebung zu erfolgen hat.     
Und weiter im Text.

<!-- TEASER_END -->

Voraussetzung
--------------

Server ist aufgesetzt (inkl. Apache) und 
es existiert bereits mindestens 1 Tomcat auf dem Server.


Tomcat Aufbau
-------------

## Beispiel: TuR Tomcat Aufbau

**Aufgabe 55:** Tomcat turmasterdata analog turqpp auf dezuepagap099 aufbauen

**Informationen:**  
* TuR E-Umgebung Server: dezuepagap099.porsche.org
* Tomcat turmasterdata aufbauen
* Tomcat turqpp existiert bereits   

## Ablauf

### Voraussetzungen

* puppet_site ist ausgecheckt im Verzeichnis "projects/puppet/puppet_site"
* puppet_hiera ist ausgecheckt im Verzeichnis "projects/puppet/puppet_hiera"


### Kurzbeschreibung der Aktionen

#### Anpassung auf Puppet4 Repository puppet_hiera

6. Wechsel auf Freeway Server  -> https://freeway.porsche.org/webapp/puppet_hiera -> Anmelden   
7. Projects -> puppet_hiera -> Merge Requests -> individuellen Branch aus Liste auswählen   
8. Merge nach **development**  -> Merge Request erstellen (Create Merge Request)
9. Mail an "fwmerge@daemons-point.com" > Betreff: Pull Request für <XXXXXX> > Angabe der URL des Merge Requests zum Reviewen
10. Review wurde durchgeführt (Daumen hoch) > Merge durchführen (Button: Merge)

### Aktivitäten auf dem Server

**Voraussetzung:** Pull Request für den Branch von "puppet_site" und "puppet_hiera" nach **development** wurde erfolgreich durchgeführt.

1. Anmelden an Server über ssh
2. Puppet Lauf starten (alternativ automatischen Puppet Lauf abwarten)
3. Dummy-War-File *dp-basic-v1.3.war* von dpserv.emea.porsche.biz:/home/uli auf dezuepagap099 kopieren.
4. war-File in Verzeichnis */srv/stage* kopieren 
5. Tomcat turmasterdata neu starten  
6. Der Tomcat turmasterdata wurde durchgestartet und läuft!        

Prüfung der WebMon CheckURL zum Schluß
