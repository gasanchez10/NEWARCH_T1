# ADR 1: Problemas de almacenamiento y actualización de la Base de datos

* Status: proposed
* Date: 2023-06-23

Technical Story: Se debe tener un componente para la visualización de datos del proceso productivo. Adicionalmente, se debe contar un sistema de almacenamiento (Base de datos) en donde logre almacenar todos los datos arrojados por los sensores de IoT.

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

## Decision Drivers

* RF1: COMPONENTE DE VISUALIZACION
* RF4: BASES DE DATOS

## Considered Options

* Estilo event driven

## Decision Outcome

Chosen option: "Estilo event driven", because Es el único estilo arquitectónico orientado a la detección de eventos

### Positive Consequences

* Arquitectura escalable
* Reportar novedades en las líneas de trabajo

### Negative Consequences

* No se puede garantizar la entrega de información asociada a eventos
* No hay mucho soporte de recuperación en caso de falla parcial.

## Pros and Cons of the Options

### Estilo event driven

LAS ARQUITECTURAS DIRIGIDAS POR EVENTOS SE BASAN EN LA DETECCIÓN, CONSUMO Y REACCIÓN A EVENTOS

* Good, because Permitirá el sensado de los distintos sensores en ambas lineas de trabajo, así como escalar la arquitectura a actuadores en función de los eventos.
* Bad, because En ocasiones no se puede garantizar la integridad de la información. Por lo anterior, no se tiene suficiente garantía de que se registren todos los eventos en la factoria

## Links

* Designing Software Architectures: A Practical Approach (SEI Series in Software Engineering), 2016.z
