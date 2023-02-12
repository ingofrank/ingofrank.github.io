---
layout: page
name: Punktkoordinaten eines Ortes
title: Ontologie-Entwurfsmuster zur Modellierung von Punktkoordinaten eines Ortes
permalink: /odp/centroid/
categories: ODP
---

# Ontologie-Entwurfsmuster zur Modellierung von Punktkoordinaten eines Ortes

Das Entwurfsmuster dient in erster Linie dazu, um Punktkoordinaten eines Ortes für die Darstellung von weiterer ortsbasierter Information über den Ort auf einer Karte. Die Ermittlung der Punktkoordinaten zur geographischen Verortung sollte nach einer Konvention erfolgen, wie dass z.B. die Position der Kirche als Zentrum eines Dorfs zur Bestimmung der Punktkoordinaten verwendet wird. Die Erfassung des Ortsmittelpunkts erfolgt praktischerweise anhand der Eigenschaft [`has centroid`](https://opengeospatial.github.io/ogc-geosparql/geosparql11/#hascentroi)]( aus der [GeoSPARQL-Ontologie](http://www.opengis.net/ont/geosparql). Die Angaben zur Quelle der Koordinaten (z.B. eine historische Karte) werden mit dem Entwurfsmuster für Quellenangaben erfasst. Sollte von der Konvention zur Ermittlung der Zentrumskoordinaten abgewichen werden müssen, sollte das entsprechend begründet in den Angaben vermerkt werden.

## Schema-Diagramm

![Schema-Diagramm](/img/dmlo-place-centroid.svg)


## Beispieldaten

```turtle
@prefix crm: <http://www.cidoc-crm.org/cidoc-crm/> .
@prefix dmlr-document: <http://digikar.eu/resource/document/> .
@prefix dmlr-place: <http://digikar.eu/resource/place/> .
@prefix frbroo: <http://iflastandards.info/ns/fr/frbr/frbroo/> .
@prefix geo: <http://www.opengis.net/ont/geosparql#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix sf: <http://www.opengis.net/ont/sf#> .

dmlr-place:hov_10001 a crm:E92_Spacetime_Volume ;
  rdfs:label "Abend" ;
  geo:hasCentroid [ a sf:Point ;
    crm:P70i_is_documented_in dmlr-document:hov ;
    geo:asWKT "POINT(12.408333 51.131944)" ] .
```


## Competency Questions

1. Zu welchen Orten liegen Punktkoordinaten vor?


## SPARQL-Beispielabfragen

```
PREFIX dmlr: <http://digikar.eu/resource/>
PREFIX dmlr-place: <http://digikar.eu/resource/place/>
PREFIX dmlr-document: <http://digikar.eu/resource/document/>
PREFIX crm: <http://www.cidoc-crm.org/cidoc-crm/>
PREFIX geo: <http://www.opengis.net/ont/geosparql#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?place ?label ?point WHERE {
  ?place a dmlo:Place ;
    geo:hasCentroid/geo:asWKT ?point ;
    rdfs:label ?label .
}
ORDER BY ?label
```


## OWL-Datei


## SHACL-Constraints


## Axiomatisierung


## Hinweise auf ähnliche Entwurfsmuster

- Die Klasse `E47 Spatial Coordinates` aus CRM könnte als Alternative in einem Entwurfsmuster verwendet werden.


## Relevante verfügbare Datensätze


## SPARQL-Beispielabfragen

```
PREFIX dmlr: <http://digikar.eu/resource/>
PREFIX dmlr-place: <http://digikar.eu/resource/place/>
PREFIX dmlr-document: <http://digikar.eu/resource/document/>
PREFIX crm: <http://www.cidoc-crm.org/cidoc-crm/>
PREFIX geo: <http://www.opengis.net/ont/geosparql#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?place ?label ?point WHERE {
  ?place a dmlo:Place ;
    geo:hasCentroid/geo:asWKT ?point ;
    rdfs:label ?label .
}
ORDER BY ?label
```


## OWL-Datei


## SHACL-Constraints


## Axiomatisierung


## Hinweise auf ähnliche Entwurfsmuster

- Die Klasse `E47 Spatial Coordinates` aus CRM könnte als Alternative in einem Entwurfsmuster verwendet werden.


## Relevante verfügbare Datensätze

```


## OWL-Datei


## SHACL-Constraints


## Axiomatisierung


## Hinweise auf ähnliche Entwurfsmuster

- https://opengeospatial.github.io/ogc-geosparql/geosparql11/spec.html#_property_geohascentroid
- Klasse `E47 Spatial Coordinates` in CRM


## Relevante verfügbare Datensätze
