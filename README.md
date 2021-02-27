# README for mp-edition-data

Repo for TEI XML data from the [Ministerratsprotokolle](https://www.oeaw.ac.at/ihb/forschungsbereiche/digitale-historiographie-und-editionen/forschung/ministerratsprotokolle-habsburgermonarchie) edition project that has been published on the web at <https://mrp.oeaw.ac.at/> already.

## Contents of this repo

### `TEI`

Contains [TEI](https://www.tei-c.org/) encoded XML files derived from custom XML of 70 years of governmental activity in the Austrian (1848-1867) and Austro-Hungarian (1867-1918) Minutes of Ministers’ Councils (*Ministerratsprotokolle*). 

All of this is in German language. 

The edition is ongoing, an overview of what is already published is available at <https://mrp.oeaw.ac.at/pages/volumes.html>. 

#### File naming scheme

```
MRP-1-2-03-0-18500501-P-0334.xml
MRP-^Serie / Series
      ^Abteilung / section
        ^Band / volume
           ^Teilband / subvolume
             ^Datum / date
                      ^Typ[*P*rotokoll| / type 
                           *A*ndererProvenienz|
                           *S*eparatprotokoll]
                        ^Protokollnummer / consecutive number of protocol
                            ^Dateiendung / file extension
```

### `Indices`

This directory contains 

- a `tei:listPerson` containing rudimentary information about the ministers of the first series (`MRP-1-*.xml`)
- `abbr.json` Abbreviations used in the documents
- `glossdata.json` A list of less common words and their explanation


## About the data

Das [Institute for Habsburg and Balkan Studies der Österreichischen Akademie der Wissenschaften](https://www.oeaw.ac.at/ihb/forschungsbereiche/digitale-historiographie-und-editionen/forschung/) bearbeitet die Protokolle des Ministerrats Österreichs (1848–1867) und der österreichisch-ungarischen Monarchie (1867–1918). Die Protokolle des Gemeinsamen Ministerrates, der gesamtstaatliche Materien behandelte, werden an der [Ungarischen Akademie der Wissenschaften](https://tti.btk.mta.hu/en/) herausgegeben.

Die Protokolle, deren Originale am [Österreichischen Staatsarchiv](https://www.oesta.gv.at/) aufbewahrt sind, werden transkribiert, eingeleitet und wissenschaftlich in Kommentaren erschlossen. Seit Mitte 2020 ist eine nach offenen Standards (TEI-XML nach den Vorschlägen der [Text Encoding Initiative](https://tei-c.org/)) codierte und frei lizenzierte digitale Edition der bisher verfügbaren Bände unter <https://mrp.oeaw.ac.at/> online. Die digitale Edition beinhaltet auch Verweise auf Digitalisate von Gesetzestexten (<https://alex.onb.ac.at>) und Tageszeitungen (<https://anno.onb.ac.at>) sowie auf eine ebenfalls frei benutzbare Literaturdatenbank (via [Zotero](https://www.zotero.org/groups/2042149/mrp-bib/library)).

Diese Ministerratsprotokolle sind eine herausragende historische Quelle, die auch über den wissenschaftlichen Fachdiskurs hinaus relevant ist; die Kabinette behandeln sämtliche Politikbereiche, von Finanzen, der Errichtung neuer Infrastruktur, besonders Eisenbahnbau, Unterrichtswesen, Sprachfragen, bis zu individuellen Entscheidungen wie Pensionen, Gnadengaben oder Ordensverleihungen. 

Die Webapplikation bietet Zugänge über

- eine [Gesamtansicht](https://mrp.oeaw.ac.at/pages/toc.html?collection=editions) über alle verfügbaren Protokolle
- einen [Kalender](https://mrp.oeaw.ac.at/pages/calendar.html)
- die edierten [Bände](https://mrp.oeaw.ac.at/pages/volumes.html) der Edition
- die [wissenschaftlichen Einleitungen](https://mrp.oeaw.ac.at/pages/toc-introductions.html) zu den in den Bänden edierten Regierungsperioden
- die Registerdaten

Zusätzlich zu diesen Funktionalitäten erlauben API-Zugänge unter anderem: 

- Abfrage nach verfügbaren edierten Protokollen nach einem Zeitraum
- Ausgabe von Protokollvolltext
- Abfrage von Informationen aus den Personen-, Orts-, Institutionenregistern 
- Volltextsuche mit KWIC-Ergebnissen

Die API ist dokumentiert unter <https://mrp.oeaw.ac.at/api/api.html>. 

## Note

Data curation for is done elsewhere. If you are interested in our docx => xsl => xml workflow, don't hesitate to get in touch. 

## Quote the dataset

[![DOI](https://zenodo.org/badge/342235542.svg)](https://zenodo.org/badge/latestdoi/342235542)

Cf. the [Zenodo Ministerratsprotokolle Community](https://zenodo.org/communities/ministerratsprotokolle/?page=1&size=20)
