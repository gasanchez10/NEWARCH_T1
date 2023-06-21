# Problemas de almacenamiento y actualización de la Base de datos

* Status: proposed
* Date: 2023-06-16

## Context and Problem Statement

Se debe tener un componente para la visualización de datos del proceso productivo. Adicionalmente, se debe contar un sistema de almacenamiento (Base de datos) en donde logre almacenar todos los datos arrojados por los sensores de IoT.

## Decision Drivers

* RF1: COMPONENTE DE VISUALIZACION
* RF4: BASES DE DATOS

## Considered Options

* Estilo event driven

## Decision Outcome

Chosen option: "Estilo event driven", because Es el estilo más a fin a la necesidad del sistema

### Positive Consequences

* Reportar novedades en las líneas de trabajo

### Negative Consequences

* No se puede garantizar la entrega de información asociada a eventos

## Pros and Cons of the Options

### Estilo event driven

El sistema requiere conocer los eventos en las distintas lineas de operación tal que la información este disponible en el centro de información.

* Good, because Es el único estilo a fin disponible
* Bad, because N/A

## Links

* Documentación de clase "Arquitectura de nuevas tecnologías"
