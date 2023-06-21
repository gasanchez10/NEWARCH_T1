# Problema de Comunicaciones entre los sistemas (Software + Factoría (Sensores))

* Status: proposed
* Date: 2023-06-21

## Context and Problem Statement

Para revisar la analítica de datois arrojados por los sensores, se debe capturar y centralizar la información para hacerla disponible a los distintos sistemas.

## Decision Drivers

* RF3.1: CENTRO DE NOTIFICACIONES
* RF5: SENSORES IOT
* RF8: SISTEMA DE MENSAJERIA INTERNO

## Considered Options

* Estilo event driven
* Patrón builder

## Decision Outcome

Chosen option: "Estilo event driven", because Se basa en la detección, consumo y reaccieon a eventos

### Positive Consequences

* Consumo de eventos

### Negative Consequences

* No garantiza la entrega de los eventos
* Cantidad de eventos a incluir en un evento

## Pros and Cons of the Options

### Estilo event driven

Permite la notificación a la industria de eventos con base en los datos registrados por los sensores.

### Patrón builder

Abstrae la creación de un objeto complejo centralizando el proceso en un único punto.

* Good, because Permitira la fusión de datos
