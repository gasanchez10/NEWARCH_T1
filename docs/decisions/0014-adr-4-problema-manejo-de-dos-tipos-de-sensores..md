# Adr-4: Problema manejo de dos tipos de sensores.

* Status: proposed
* Date: 2023-06-24

Technical Story: Existen dos familias de sensores que dan un esquema de datos diferente. Por tanto es necesario aplicar técnicas de data fusion

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

## Decision Drivers

* RF5: SENSORES IOT

## Considered Options

* Patrón de diseño abstract factory
* Estilo pipe and filter
* Patrón de diseño prototype

## Decision Outcome

Chosen option: "Patrón de diseño abstract factory", because comes out best.
