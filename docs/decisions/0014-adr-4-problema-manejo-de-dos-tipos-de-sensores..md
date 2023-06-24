# Adr-4: Problema manejo de dos tipos de sensores.

* Status: proposed
* Date: 2023-06-24

Technical Story: Existen dos familias de sensores que dan un esquema de datos diferentes. Por tanto es necesario aplicar técnicas de data fusion

## Context and Problem Statement

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de
producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos
físicos de una factoría inteligente 4.0.

## Decision Drivers

* RF1: COMPONENTE DE VISUALIZACION
* RF4: BASES DE DATOS

## Considered Options

* Patrón de diseño abstract factory
* Estilo pipe and filter
* Patrón de diseño prototype

## Decision Outcome

Chosen option: "Patrón de diseño abstract factory", because Permite la fusion de datos sin clases definidas. Esto permitirá incorporar nuevos sensores eventualmente

### Positive Consequences

* Arquitectura escalable
* Reportar novedades en las líneas de trabajo

### Negative Consequences

* Tiempo de implementación elevado

## Pros and Cons of the Options

### Patrón de diseño abstract factory

PERMITE TRABAJAR CON OBJETOS DE FAMILIAS RELACIONADAS SIN ESPECIFICAR SUS CLASES CONCRETAS. TRABAJA CON MÚLTIPLES FAMILIAS DE PRODUCTOS

* Good, because Cataliza la lectura de distintos tiposd e información. Esto permite que se pueda cambiar el esquema de base de datos conforme se organiza la industria en una nueva metodologia de trabajo.
* Bad, because Se necesita mucho código para implementar la fábrica de forma correcta para garantizar la flexibilidad del sistema

### Estilo pipe and filter

UN FILTRO LEE FLUJOS DE DATOS DE SUS ENTRADAS Y GENERA FLUJOS DE DATOS A SUS SALIDAS

* Good, because Permite el tratamiento de datos de manera secuencial
* Bad, because Dificulta el manejo de errores en operación

### Patrón de diseño prototype

TIENE COMO FINALIDAD CREAR NUEVOS OBJETOS DUPLICÁNDOLOS

* Good, because Crear y eliminar objetos en tiempo de ejecución, permite definir un nuevo comportamiento a través de la composición de objetos (especificando el valor de sus variables).
* Bad, because Es una manera muy robusta de solucionar la creación de objetos costosos si no se crean muchos objetos de manera dinámica, oculta las dependencias del cliente, todas las clases tienen que implementar un método CLONE() para poder “crear” un nuevo objeto.

## Links

* Designing Software Architectures: A Practical Approach (SEI Series in Software Engineering), 2016.z
* https://somospnt.com/blog/149-patron-creacional-prototype#:~:text=Ventajas%3A%20Crear%20y%20eliminar%20objetos,el%20valor%20de%20sus%20variables).
