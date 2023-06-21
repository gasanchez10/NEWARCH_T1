# Problema de asignación de colas de trabajo, analitica y visualización

* Status: proposed
* Date: 2023-06-21

## Context and Problem Statement

Se requiere un algoritmo que permita optimizar el volumen de trabajo, así como un algoritmo que haga predicción de la falla de las líneas y asigne recursos de otras líneas.

## Decision Drivers

* RF2: ORDENES DE TRABAJO
* RF3.2: CENTRO DE NOTIFICACIONES
* RF6: ALGORITMOS DE OPTIMIZACION
* RF7: PREDICCION

## Considered Options

* Patron de microservicios
* Patrón strategy

## Decision Outcome

Chosen option: "Patron de microservicios", because permite exponer servicios de manera desacoplada

### Positive Consequences

* Baja latencia en el servicio

### Negative Consequences

* Exige conocer el mejor algoritmo

## Pros and Cons of the Options

### Patron de microservicios

* Good, because Permite exponer de manera desacoplada multiples servicios de distintos algoritmos analíticos

### Patrón strategy

Permite encontrar el mejor algoritmo entre un pool de opciones

* Good, because Permite garantizar el performance de un algoritmo predictivo
* Bad, because Incrementa el número de objetos de la aplicación
* Bad, because El cliente debe concer las diferentes estrategias y en qué se diferencian.
