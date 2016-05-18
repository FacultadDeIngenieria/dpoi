---
title: Práctica 8 - Serverless
layout: practice
permalink: /practice/serverless
---

# Práctica 8: Serverless Scrapping

## Enunciado:

1. Extender el proyecto [Serverless Scrapping](https://github.com/FacultadDeIngenieria/serverless-scrapping).
  - Agregar ListSchemasAction. Esta acción deberá extender de ApplicationAction y listar todos los schemas disponibles en la aplicación.
  - Generificar ScrapUrlAction. La misma deberá utilizar el schema especificado al realizar el scrapping *¡implementar #fetchUrlContent correctamente!*.
2. Crear las tablas correspondientes en **DynamoDB**.
3. Crear una función **Lambda** con el código del proyecto extendido.
4. Especificar permisos de la función **Lambda** para leer y escribir en **DynamoDB**.
5. Crear un Scrapping API en **API Gateway** con los siguientes resources y métodos:
  - /schemas
    - GET: Listar schemas de la aplicación.
  - /scraps
    - GET: Listar scraps de la aplicación.
    - POST: Realizar un scrapping de la url dada con el schema especificado.
6. Exponer el API en un ambiente de test y probar el mismo desde Postman importando el descriptor *Swagger* del mismo.

## Bonus Point

1. Extender el proyecto [Serverless Scrapping](https://github.com/FacultadDeIngenieria/serverless-scrapping) con CreateSchemaAction. Esta acción deberá extender de ApplicationAction y crear un nuevo schema con el JSON schema especificado.
2. Extender el Scrapping API con la nueva funcionalidad:
  - /schemas
    - GET: Listar schemas de la aplicación.
    - **POST: Crear un nuevo schema en la aplicación.**
  - /scraps
    - GET: Listar scraps de la aplicación.
    - POST: Realizar un scrapping de la url dada con el schema especificado.