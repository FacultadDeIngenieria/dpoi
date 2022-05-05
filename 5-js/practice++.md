---
title: Práctica 3+ - JS
layout: practice
permalink: /practice/js++
---

# Práctica 3+: JS

## Enunciado:
Completar la funcionalidad anterior con el agregado de:

1. Crear: Permitir agregar un item a la tabla (agregando un row al sheet).
2. Editar: Permitir editar un iteam particular (editando el row existente del sheet).
3. Expandir: Permitir visualizar la totalidad de datos de un item particular.
4. Borrar: Permitir eliminar un item particular (borrando el row existente del sheet). 

**Todos los servicios requieren una credencial**. Cada uno tendrá su credencial y esta estará compuesta por la primer letra del nombre y el apellido (ej. "pcolunga" | Idem repositorio). De esta manera, para el listado, creación, update, borrado y visualización se deberá siempre parametrizar el GET o el POST con la tupla `credential=pcolunga`.

## Servicio:
Usar Google Sheets API para leer y editar datos de un sheet que tengan en su cuenta de la facultad. Luego de crear un projecto en la cuenta de Google, va a requerir crear un "OAuth 2.0 Client ID" y un "API Key" en Google Cloud Platform. Esta es la guia de como usar la API: https://developers.google.com/sheets/api/quickstart/js#prereqs

## Json:
Todas las respuestas vienen dadas en formato Json. Desde Javascript se debe:

1. Parsear el resultado,
2. Chequear el estado,
3. Actualizar la tabla.

## Tabla:
La tabla deberá renderear los datos que el servicio provea, utilizando un html que valide xhtml 1.1 y utilice una hoja de estilos externa. Los formularios para la carga, visualización y edición deberán residir en la misma página, **no se deberá navegar a traves de múltiples páginas**.

## Requisitos:
- La página debe ser html 5:
 - Las páginas deben ser validadas usando el W3G validator (html y css).
