---
title: Práctica 6 - RestApi
layout: practice
permalink: /practice/restapi
schema: vademecum-product.schema.json
---

# Práctica 6: RestApi

## Enunciado:

1. Extraer información de distintas paginas de manera generica utilizando el schema de scrapping de la practica 5.
2. Guardar la información json obtenida de forma permanente en una base de datos.
3. Exponer esos datos a travez de un api rest.

## RestApi

Debera exponer los siguientes servicios:

- **GET /** : devuelte el listado de dominios disponibles.

```javascript
GET /
[
   {"url": "/prvademecum.com", "name": "prvademecum.com"},
   {"url": "/lanacion.com", "name": "lanacion.com"},
]
```

- **GET /{domain}** : devuelte el listado de paths disponible bajo ese dominio.

```javascript
GET /prvademecum.com
[
   {"url": "/prvademecum.com/products", "name": "Vademecum Product"}
]
```

- **GET /{domain}/{path}** : devuelte el listado de documentos disponibles.

```javascript
GET /prvademecum.com/products
[
   {"url": "/prvademecum.com/products/http://ar.prvademecum.com/producto.php?producto=16362", "name": "IBUPIRAC PFIZER"},
   {"url": "/prvademecum.com/products/http://ar.prvademecum.com/producto.php?producto=16365", "name": "UNICALM RAFFO"},
]
```

- **GET /{domain}/{path}/{url}** : devuelte el documento con todas sus properties.

```javascript
GET /prvademecum.com/products/http://ar.prvademecum.com/producto.php?producto=16362
{
   "title": "IBUPIRAC",
   "laboratory": "PFIZER",
   "abstract": "Analgésico, antiinflamatorio y antifebril.",
   "content", "Composición. Cada comprimido contiene: ibuprofeno 400mg..."
}
```


## Schema

Para saber bajo que path y con que nombre guardar los documentos, los schemas deben tener dos nuevos campos: *path* y *describes*:

- **path:** indica como se agrupan todos los documentos obtenidos al usar este schema.
- **describes:** indica que atributos se utilizan para describir el documento.

Ejemplo del nuevo Schema: [Vademecum Product Schema](../7-restapi/{{page.scheme}})

```javascript
{% include_relative {{page.schema}} %}
```
