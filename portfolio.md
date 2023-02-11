---
layout: page
title: Portfolio
permalink: /portfolio/
categories: [Ontology]
---

# Portfolio

## SPARQL Queries

Writing SPARQL queries for all kinds of information retrieval purposes.

```sparql
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

A more interesting SPARQL query:

```sparql
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

## Example Data

```turtle
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .

@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

@prefix dct: <http://purl.org/dc/terms/> .

@prefix gnd: <http://d-nb.info/gnd/> .
@prefix wd: <http://www.wikidata.org/entity/> .

@prefix gov-types: <http://gov.genealogy.net/types.owl#> .
@prefix gndo: <https://d-nb.info/standards/elementset/gnd#> .
@prefix ontohgis: <http://purl.org/ontohgis#> .

@prefix dmlr: <http://digikar.eu/resource/> .
@prefix dmlo: <http://digikar.eu/ontology/> .
#@prefix dmlv: <http://digikar.eu/vocabulary/> .

@prefix dmlv-place: <http://digikar.eu/vocabulary/place/> .


dmlv-place: a skos:ConceptScheme ;
  rdfs:label "Ortstypologie" ;
  skos:notation "pt" ;
  skos:prefLabel "Ortstypologie"@de ;
  skos:prefLabel "Place Typology"@en ;
  skos:description "Ortstypologie für DigiKAR."@de ;
  skos:hasTopConcept dmlv-place:st ;
  skos:hasTopConcept dmlv-place:at 
.

dmlv-place:st a skos:Concept ;
  rdfs:label "Siedlung" ;
  skos:notation "st" ;
  skos:prefLabel "Siedlung"@de ;
  skos:prefLabel "Settlement"@en ;
  skos:altLabel "Ortschaft"@de ;
  skos:altLabel "Locality"@en ;
  skos:inScheme dmlv-place: ;
  skos:exactMatch gov-types:120 # ? 
.

dmlv-place:vi a skos:Concept ;
  rdfs:label "Dorf" ;
  skos:notation "vi" ;
  skos:prefLabel "Dorf"@de ;
  skos:prefLabel "Village"@en ;
  skos:broader dmlv-place:st ;
  skos:inScheme dmlv-place: ;
  skos:exactMatch gov-types:55
.

dmlv-place:to a skos:Concept ;
  rdfs:label "Stadt" ;
  skos:notation "to" ;
  skos:prefLabel "Stadt"@de ;
  skos:prefLabel "Town"@en ;
  skos:broader dmlv-place:st ;
  skos:inScheme dmlv-place: ;
  skos:exactMatch gov-types:51
.
```
