# Adr-3: Problema de Comunicaciones entre los sistemas (Software + Factoría (Sensores))

* Status: proposed
* Date: 2023-06-23

Technical Story: Para revisar la analítica de datois arrojados por los sensores, se debe capturar y centralizar la información para hacerla disponible a los distintos sistemas.

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

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

* Good, because LOS EMISORES NO CONOCEN A LOS CONSUMIDORES DE LOS EVENTOS
* Bad, because Pobre comprensibilidad: Puede ser difícil prever qué pasará en respuesta a una acción.
* Bad, because No hay garantía del lado del publicador, que el suscriptor responderá al evento.

### Patrón builder

ABSTRAE EL PROCESO DE CREACIÓN DE UN OBJETO COMPLEJO, CENTRALIZANDO
DICHO PROCESO EN UN ÚNICO PUNTO.

* Good, because Permite flexibilidad a la hora de hacer data fusion de otro tipo de sensores
* Bad, because Al ser un mecanismo centralizado, esto impide la descentralización o la fragmentación de las tomas de decisiones cuando se requiere que estas sean en función a solo una parte del objeto.

## Links

* Designing Software Architectures: A Practical Approach (SEI Series in Software Engineering), 2016.z
