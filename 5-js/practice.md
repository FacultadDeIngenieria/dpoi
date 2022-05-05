---
title: Práctica 3 - JS
layout: practice
permalink: /practice/js
---

# Práctica 3: JS

## Enunciado:
Usar la página *users.xhtml* del trabajo práctico anterior y agregarle comportamiento implementando un servicio ajax que cargue los datos de la tabla de usuarios.

Cada fila de la tabla deberá mostrar los datos relevantes del objeto que provea el servicio. En cada fila mostrar links o botones para editar, expandir y remover el elemento.

## Servicio:
Usar Google Sheets API para leer datos de un sheet que tengan en su cuenta de la facultad.
Luego de crear un projecto en la cuenta de Google, va a requerir crear un "OAuth 2.0 Client ID" y un "API Key" en Google Cloud Platform. 
Esta es la guia de como usar la API: https://developers.google.com/sheets/api/quickstart/js#prereqs

## Json:
Todas las respuestas vienen dadas en formato Json. Desde Javascript se debe:

1. Pedir los datos.
2. Mostrar alguna leyenda o feedback mientras los datos están siendo cargados.
3. Parsear el resultado.
4. Chequear el estado.
5. Popular la tabla.

## Requisitos:
- La página debe ser html:
 - Las páginas deben ser validadas usando el W3G validator (html y css).
