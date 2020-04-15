---
title: Práctica 6 - RestApi
layout: practice
permalink: /practice/restapi
api: api.json
---

# Práctica 6: RestApi

## Enunciado:

1. Extraer structured data de distintas páginas de manera genérica utilizando lo realizado en la práctica 5.
2. Guardar la información json obtenida de forma permanente en una base de datos (Ej. DynamoDB, MongoDB, Cassandra).
3. Exponer esos datos a través de un api rest.

## RestApi

```raml
{% include_relative {{page.api}} %}
```
