# Adr-5: Problema envío información secuencial en sensores A

* Status: proposed
* Date: 2023-06-24

Technical Story: Proporcionar datos del estado de los dispositivos físicos de la factoría Detectar inconvenientes en la línea de producción de la factoría

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

## Decision Drivers

* RF5:  SENSORES IOT

## Considered Options

* Estilo pipe and filter
* Chain of responsability (Escogida)

## Decision Outcome

Chosen option: "Chain of responsability", because Añade flexibilidad

### Positive Consequences

* Reduce el acoplamiento

### Negative Consequences

* No garantiza la recepción

## Pros and Cons of the Options

### Estilo pipe and filter

Un componente lee flujo de datos en sus entradas y produce flujos de datos sobre sus salidas.

* Good, because Permite comprender el comportamiento de entrada / salida de un sistema como la composición del comportamiento de los filtros individuales.
* Bad, because Frecuentemente tienden a una organización de procesamiento batch

### Chain of responsability

permite pasar solicitudes a lo largo de una cadena de manejadores.

* Good, because Manejo del orden de los pasos
* Bad, because No garantiza la recepción

## Links

* https://somospnt.com/blog/149-patron-creacional-prototype#:~:text=Ventajas%3A%20Crear%20y%20eliminar%20objetos,el%20valor%20de%20sus%20variables).
* http://mariochau.blogspot.com/2014/04/pipes-and-filters.html
