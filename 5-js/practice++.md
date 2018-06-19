---
title: Práctica 3+ - JS
layout: practice
permalink: /practice/js++
---

# Práctica 3+: JS

## Enunciado:
Completar la funcionalidad anterior con el agregado de:

1. Crear: Permitir agregar items a la tabla. Utilizar el servicio `"url":"/api/1.0/create"`. El return de ese método debería ser el object a agregar.
2. Editar: Permitir editar un item particular. Utilizar el servicio `"url":"/api/1.0/update"`.
3. Expandir: Permitir visualizar la totalidad de datos de un item particular. Utilizar el servicio `"url":"/api/1.0/view"`.
4. Borrar: Permitir eliminar un item particular. Utilizar el servicio `"url":"/api/1.0/delete"`.

**Todos los servicios requieren una credencial**. Cada uno tendrá su credencial y esta estará compuesta por la primer letra del nombre y el apellido (ej. "pcolunga" | Idem repositorio). De esta manera, para el listado, creación, update, borrado y visualización se deberá siempre parametrizar el GET o el POST con la tupla `credential=pcolunga`.

## Servicio:
El servicio está hosteado en Google App Engine y se accede a través del dominio **http://dpoi2012api.appspot.com/**.
Los usos del servicio vienen dados en el mismo API a través de `/api/1.0/usage`.
Para simular tiempo en la carga de datos, se podrá invocar cualquier servicio con el keyword delay `/api/1.0/*****_delay?xxx=yyy` y el resultado será idéntico al anterior con una pequeña demora.

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
