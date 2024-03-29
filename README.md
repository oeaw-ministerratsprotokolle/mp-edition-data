# README for mp-edition-data

Repo for TEI XML data from the [Ministerratsprotokolle](https://www.oeaw.ac.at/ihb/forschungsbereiche/digitale-historiographie-und-editionen/forschung/ministerratsprotokolle-habsburgermonarchie) edition project that has been published on the web at <https://mrp.oeaw.ac.at/> already.

## Contents of this repo

### `TEI`

Contains [TEI](https://www.tei-c.org/) encoded XML files derived from custom XML of 70 years of governmental activity in the Austrian (1848-1867) and Austro-Hungarian (1867-1918) Minutes of Ministers’ Councils (*Ministerratsprotokolle*). 

All of this is in German language. 

The edition is ongoing, an overview of what is already published is available at <https://mrp.oeaw.ac.at/pages/volumes.html>. 

CAVEAT: The CMR series (= `TEI/MRP-3-0-*`) is based on archival sources that have partially been damaged. `tei:seg type="supplied-from-other-source` indicates that the textual content has been supplied from complimentary material such as the materials used for a session’s preparation. Empty `tei:div type="protocol"` point to documents that did not survive the 1927 palace of justice fire (<https://de.wikipedia.org/wiki/Wiener_Justizpalastbrand>).  

Keep this in mind when attempting any quantitative use of this data.

This release includes the following recently published volumes

- CMR II (ed. by Thomas Kletečka and Richard Lein), now also with `tei:pb/@facs` references to burnt material 
- CMR III/1 (ed. by Klaus Koch)
- CMR VIII/1 (ed. by Wladimir Fischer-Nebmaier @sviatoplok)

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

- a `tei:standOff`  containing rudimentary information about the ministers of the first series (`MRP-1-*.xml`) and references for the third (`MRP-3-*.xml`) series.
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

Zusätzlich sind die in `indices/standOff.xml` jeweils mit aktuellem Stand archivierten Entitätsdaten über die *Modulare Prosopographische Rgistratur* (MPR) unter <https://mpr.acdh.oeaw.ac.at/> öffentlich einsehbar und nachnutzbar. 

CAVEAT: Die CMR-Reihe (= `TEI/MRP-3-0-*`) basiert auf einem Quellenbestand, der teilweise dezimiert oder beschädigt ist. `tei:seg type="supplied-from-other-source"` zeigt an, dass der Textinhalt aus ergänzendem Material stammt, z.B. den Materialien zur Vorbereitung einer Sitzung, dem Ministervortrag u. dgl. Leere `tei:div type="protocol"` weisen auf Dokumente hin, die den Brand des Justizpalastes von 1927 nicht überlebt haben (<https://de.wikipedia.org/wiki/Wiener_Justizpalastbrand>).  

Beachten Sie dies, wenn Sie versuchen, diese Daten quantitativ zu nutzen.

## Note

Data curation for is done elsewhere. If you are interested in our docx => xsl => xml workflow, don’t hesitate to get in touch. 

## Quote the dataset

[![DOI](https://zenodo.org/badge/4568291.svg)](https://zenodo.org/badge/latestdoi/4568291)
https://zenodo.org/doi/10.5281/zenodo.4568291

Cf. the [Zenodo Ministerratsprotokolle Community](https://zenodo.org/communities/ministerratsprotokolle)


## License

This dataset is provided under CC-BY 4.0 as in the <./LICENCE.md> file.
