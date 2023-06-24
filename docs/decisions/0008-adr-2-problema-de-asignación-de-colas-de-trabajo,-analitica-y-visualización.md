# ADR-2: Problema de asignación de colas de trabajo, analitica y visualización

* Status: proposed
* Date: 2023-06-23

Technical Story: Se requiere un algoritmo que permita optimizar el volumen de trabajo, así como un algoritmo que haga predicción de la falla de las líneas y asigne recursos de otras líneas.

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

## Decision Drivers

* RF2: ORDENES DE TRABAJO
* RF3.2: CENTRO DE NOTIFICACIONES
* RF6: ALGORITMOS DE OPTIMIZACION
* RF7: PREDICCION

## Considered Options

* Patron de microservicios
* Patron strategy

## Decision Outcome

Chosen option: "Patron strategy", because Permite garantizar el accuracy del modelo

### Positive Consequences

* Condiabilidad en los resultados

### Negative Consequences

* Baja latencia en el servicio

## Pros and Cons of the Options

### Patron de microservicios

Permite exponer servicios con funciones puntuales

* Good, because ORIENTADOS A FAVORECER LA ESCALABILIDAD EN ARQUITECTURAS
* Bad, because Complejidad de gestión de un gran número de servicios.
* Bad, because Necesidad de tiempo para poder fragmentar distintos microservicios.

### Patron strategy

Permite encontrar el mejor algoritmo entre un pool de opciones

* Good, because Permite garantizar el performance de un algoritmo predictivo
* Bad, because Incrementa el número de objetos de la aplicación
* Bad, because El cliente debe concer las diferentes estrategias y en qué se diferencian.

## Links

* Designing Software Architectures: A Practical Approach (SEI Series in Software Engineering), 2016.z
