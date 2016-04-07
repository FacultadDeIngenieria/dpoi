---
title: Práctica 5 - Scrapping
layout: practice
permalink: /practice/scrapping
schema: lanacion-article.schema.json
---

# Práctica 5: Scrapping

## Enunciado:
Utilizar el schema json de "La Nación Article" para extraer información del listado de páginas especificadas:

**http://www.lanacion.com.ar/{1885100..1885200}**

## Schema

[La Nación Article Schema](../6-scrapping/{{page.schema}})


```json
{% include_relative {{page.schema}} %}
```

## Requisitos:
- El programa deberá aceptar como parámetros el schema file y una URL. El output del mismo deberá ser un *schema compliant json object*.
