---
title: Práctica 4 - Scrapping
layout: practice
permalink: /practice/scrapping
top: top250.json
---

# Práctica 4: Scrapping

## Enunciado:
Implementar un structured data scrapper que retorne un **json-ld** con la data de una página dada.

Aplicar el scrapping al rango de páginas:

**http://www.lanacion.com.ar/{1885100..1885200}**

Y a las páginas:

[Top 250 IMDB](/{{page.top}})

```javascript
{% include_relative {{page.top}} %}
```

## Requisitos:
- El programa deberá aceptar como parámetro una URL. El output del mismo deberá ser un *json-ld* válido.
