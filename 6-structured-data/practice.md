---
title: Práctica 5 - Scrapping
layout: practice
permalink: /practice/scrapping
top: garba-ofertas.json
---

# Práctica 5: Scrapping

## Enunciado:
Implementar un structured data scrapper que retorne un **json-ld** con la data de una página dada.

Aplicar el scrapping al rango de páginas:

**http://www.lanacion.com.ar/{2351900..2352000}**

Y a las páginas:

[Listado Retail](/{{page.top}})

```javascript
{% include_relative {{page.top}} %}
```

## Requisitos:
- El programa deberá aceptar como parámetro una URL. El output del mismo deberá ser un *json-ld* válido.
