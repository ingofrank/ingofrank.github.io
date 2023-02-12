---
layout: page
title: Ontologie-Entwurfsmuster zur Modellierung der räumlichen Ausdehnung eines Ortes
permalink: /odp/presence/
categories: ODP
---

# Ontologie-Entwurfsmuster zur Modellierung der räumlichen Ausdehnung eines Ortes

 
  features and geometries --  a feature has a geometry (point, polygon) 


  GeoSPARQL class `Feature` aligned with CRMgeo class `SP1 Phenomenal Spacetime Volume` and GeoSPARQL class `Geometry` aligned with CRMgeo class `SP7 Declarative Place`  


CRMgeo  a short description of CRMgeo on its website:

> *CRMgeo* is a formal ontology intended to be used as a global schema for integrating spatiotemporal properties of temporal entities and persistent items. Its primary purpose is to provide a schema consistent with the CIDOC CRM to integrate geoinformation using the conceptualizations, formal definitions, encoding standards and topological relations defined by the Open Geospatial Consortium (OGC). In order to do this it links the CIDOC CRM to the OGC standard of GeoSPARQL.



## Schema-Diagramm


## Beispieldaten



## Competency Questions

1. Zu welchen Orten liegen Geodaten (Polygone etc.) vor?

2. Welche Geodaten gibt es zu einem Territorium?
3. Gibt es Geodaten zu Territorium X im WKT-Format?
4. Aus welcher Quellen stammen die Geodaten?
5. Zu welchen Territorien gibt es mehrere Geodaten aus verschiedenen Quellen?


## SPARQL-Beispielabfragen

```
PREFIX dmlr: <http://digikar.eu/resource/>
PREFIX dmlr-place: <http://digikar.eu/resource/place/>
PREFIX dmlr-document: <http://digikar.eu/resource/document/>
PREFIX crm: <http://www.cidoc-crm.org/cidoc-crm/>
PREFIX crmgeo: <http://www.ics.forth.gr/isl/CRMgeo/>
PREFIX geo: <http://www.opengis.net/ont/geosparql#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?place ?label ?geo WHERE {
  ?place a dmlo:Place ;
    crm:P166i_had_presence/crm:P167_was_within/crmgeo:P168_place_is_defined_by/geo:asWKT 
      ?geo ;
    rdfs:label ?label .
}
ORDER BY ?label
```


## OWL-Datei


## SHACL-Constraints


## Axiomatisierung


## Hinweise auf ähnliche Entwurfsmuster

CRM-Erweiterung CRMgeo zur Modellierung voneinander abweichenden Angaben zur territorialen Ausdehnung oder zu Grenzverläufen in verschiedenen historischen Quellen



## Relevante verfügbare Datensätze

- Germania Sacra 


