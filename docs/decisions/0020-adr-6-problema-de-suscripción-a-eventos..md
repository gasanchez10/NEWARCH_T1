# Adr-6: Problema de Suscripción a eventos.

* Status: proposed
* Date: 2023-06-24

Technical Story: El software de la factoría 4.0 debe contar con un sistema de mensajería para la comunicación de los dispositivos IoT y los usuarios del software.

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

## Decision Drivers

* RF8: Sistema de Mensajería interno

## Considered Options

* PUBLISH-SUBSCRIBE
* OBSERVER

## Decision Outcome

Chosen option: "PUBLISH-SUBSCRIBE", because Permite que solo los interesados se suscriban

### Positive Consequences

* Envia mensajes no programados

### Negative Consequences

* N/A

## Pros and Cons of the Options

### PUBLISH-SUBSCRIBE

REMITENTES ENVÍAN MENSAJES NO PROGRAMADOS A SUSCRIPTORES

* Good, because Permite que los mensajes se envien solo a quien tiene interes en la información
* Bad, because Puede haber colapsos en las operaciones

### OBSERVER

DEFINE UNA DEPENDENCIA DE UNO-A-MUCHOS ENTRE OBJETOS

* Good, because Cuando un objeto cambia de estado se actualizan todos los objetos que dependen de el
* Bad, because Posible fuga de memoria.

## Links

* https://somospnt.com/blog/155-patron-de-comportamiento-observer#:~:text=Desventajas%3A%20La%20fuga%20de%20memoria,de%20basura%20no%20lo%20elimine.
