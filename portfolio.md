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
