---
title: Práctica - APIs
layout: practice
permalink: /practice/restapi
api: api.json
---

# Práctica: APIs

## Enunciado:

Bajarse la [DB de IMDB](https://datasets.imdbws.com/) e importar cada parte (7 en total) en una tabla distinta de DynamoDB ([detalle del Schema](https://developer.imdb.com/non-commercial-datasets/)).

Exponer las entidades desde una REST API y una GraphQL API, en dos implementaciones: una monolítica y otra con microservicios. Dando un total de 4 implementaciones.

Recomendamos el uso de NodeJS+Express para las REST APIs y de [Apollo](https://www.apollographql.com/docs/federation/) para GraphQL.

### Listado de GET endpoints para las REST APIs
1. /titles?offset=1&limit=100
2. /titles/{titleId}
3. /titles/{titleId}/akas
4. /titles/{titleId}/crew
5. /titles/{titleId}/episodes
6. /titles/{titleId}/principals
7. /titles/{titleId}/ratings
8. /names/{nameId}

### Ejemplo de query GraphQL

```
titles(offset: 1, limit: 100) {
  primaryTitle
    akas { // relate by titleId, ordered by ordering
	  title
	  region
	  language
	}
	crew { // relate by tconst
	  directors { // relate by nconst
	    primaryName
	  }
	  writers { // relate by nconst
	    primaryName
      }
	}
	episodes { // relate by parentTconst
	  title {
	    primaryTitle
	  }
	  seasonNumber
	  episodeNumber
	}
	principals { // relate by tconst, ordered by ordering
	  name { // relate by nconst
	    primaryName
	  }
	  category
	  job
	  characters
	}
	ratings { // relate by tconst
	  averageRating
	  numVotes
	}
}
```