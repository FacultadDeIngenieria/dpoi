---
title: Práctica 3 - JS
layout: practice
permalink: /practice/js
---

# Práctica 3: JS

## Enunciado:
Usar la página *users.xhtml* del trabajo práctico anterior y agregarle comportamiento implementando un servicio ajax que cargue los datos de la tabla de usuarios.

Cada fila de la tabla deberá mostrar los datos relevantes del objeto que provea el servicio (filtrar campos como id y created). En cada fila mostrar links o botones para editar, expandir y remover el elemento.

## Servicio:
El servicio está hosteado en Google App Engine y se accede a través del dominio: http://dpoi2012api.appspot.com/.

Los usos del servicio vienen dados en el mismo API a través de `/api/1.0/usage`.

El parámetro de filtering para el listado será `/api/1.0/list?credential=dpoi`.

Para simular tiempo en la carga de datos, se podrá invocar `/api/1.0/list_delay?credential=dpoi` y el resultado será idéntico al anterior con una pequeña demora.

## Json:
Todas las respuestas vienen dadas en formato Json. Desde Javascript se debe:

1. Pedir los datos.
2. Mostrar alguna leyenda o feedback mientras los datos están siendo cargados.
3. Parsear el resultado.
4. Chequear el estado.
5. Popular la tabla.

## Requisitos:
- La página debe ser xhtml 1.1:
 - Las páginas deben ser validadas usando el W3G validator (xhtml y css).
