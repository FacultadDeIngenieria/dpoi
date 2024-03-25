---
title: Práctica 6 - RestApi
layout: practice
permalink: /practice/restapi
api: api.json
---

# Práctica: RestApi & GraphQL

## Enunciado:

Bajarse la [DB de IMDB](https://datasets.imdbws.com/) e importar cada parte en una tabla distinta DynamoDB ([detalle del Schema](https://developer.imdb.com/non-commercial-datasets/)).
Por cada entidad (7 en total), exponer tanto el listado paginado y un unico item por su identifier (7x2 en total).

Exponer las entidades desde una REST API y una GraphQL API, en dos implementaciones: una monolítica y otra con microservicios. Dando un total de 4 implementaciones.

Recomendamos el uso de NodeJS+Express para las REST APIs y de [Apollo](https://www.apollographql.com/docs/federation/) para GraphQL.