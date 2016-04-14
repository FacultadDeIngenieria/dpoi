---
title: Práctica 6 - RestApi
layout: practice
permalink: /practice/restapi
schema: vademecum-product.schema.json
---

# Práctica 6: RestApi

## Enunciado:

1. Extraer información de distintas páginas de manera genérica utilizando el schema de scrapping de la práctica 5.
2. Guardar la información json obtenida de forma permanente en una base de datos (Ej. MongoDB, Cassandra).
3. Exponer esos datos a través de un api rest.

## RestApi

Deberá exponer los siguientes servicios:

- **GET /** : devuelve el listado de dominios disponibles.

```javascript
GET /
[
   {"url": "/prvademecum.com", "name": "prvademecum.com"},
   {"url": "/lanacion.com", "name": "lanacion.com"},
]
```

- **GET /{domain}** : devuelve el listado de paths disponible bajo ese dominio.

```javascript
GET /prvademecum.com
[
   {"url": "/prvademecum.com/products", "name": "Vademecum Product"}
]
```

- **GET /{domain}/{path}** : devuelve el listado de documentos disponibles.

```javascript
GET /prvademecum.com/products
[
   {"url": "/prvademecum.com/products/ibupirac-pfizer-4021d1d09859fb19394919da043a2ef3", "name": "IBUPIRAC PFIZER"},
   {"url": "/prvademecum.com/products/unicalm-raffo-9fd637e31956ee1e3c86cf9db90d1100", "name": "UNICALM RAFFO"},
]
```

- **GET /{domain}/{path}/{slug-sha}** : devuelve el documento con todas sus properties.

```javascript
GET /prvademecum.com/products/ibupirac-pfizer-4021d1d09859fb19394919da043a2ef3
{
   "title": "IBUPIRAC",
   "laboratory": "PFIZER",
   "abstract": "Analgésico, antiinflamatorio y antifebril.",
   "content", "Composición. Cada comprimido contiene: ibuprofeno 400mg..."
}
```

## Schema

Para saber bajo qué path y con qué nombre guardar los documentos, los schemas deben tener dos nuevos campos: *path* y *describes*:

- **path:** indica como se agrupan todos los documentos obtenidos al usar este schema.
- **describes:** indica que atributos se utilizan para describir el documento.

Ejemplo del nuevo Schema: [Vademecum Product Schema](../7-restapi/{{page.schema}})

```javascript
{% include_relative {{page.schema}} %}
```
