# Sistema de Gestión de Naves Espaciales
Desarrollo en PHP para gestionar naves espaciales y misiones utilizando POO. Permite crear y asignar naves a misiones, iniciar misiones considerando el combustible, y visualizar información.

## Características

- **Creación y Gestión de Naves Espaciales:** Permite añadir naves espaciales a la base, cada una con propiedades como nombre, capacidad de combustible, consumo por kilómetro y kilómetros recorridos.
- **Gestión de Misiones:** Permite añadir misiones, asignar naves a estas misiones y gestionar su estado (Pendiente, En Curso, Completada).
- **Gestión de Bases Espaciales:** Incluye la creación de bases espaciales, la asignación de naves y misiones, y la iniciación de misiones si hay suficiente combustible en la nave asignada.
- **Visualización de Información:** Mostrar información relevante sobre las naves y misiones.
- **Manejo de Errores:** Controla errores como intentar iniciar una misión sin nave asignada o con insuficiente combustible.

## Clases Principales

1. **NaveEspacial**
   - Propiedades: Nombre, Capacidad de Combustible, Consumo de Combustible por Kilómetro, Kilómetros Recorridos.
   - Métodos: `get` y `set` para cada propiedad, `volar($kilometros)`.

2. **Mision**
   - Propiedades: Nombre, Distancia a Recorrer, Nave Asignada, Estado.
   - Métodos: `get` y `set` para cada propiedad, `iniciarMision()`.

3. **BaseEspacial**
   - Propiedades: Nombre, Ubicación, Lista de Naves, Lista de Misiones.
   - Métodos: `añadirNave(NaveEspacial $nave)`, `añadirMision(Mision $mision)`, `asignarNaveAMision(string $nombreNave, string $nombreMision)`, `iniciarMision(string $nombreMision)`.

## Consideraciones Adicionales

- Se pueden añadir planetas con propiedades como nombre y distancia desde la base, modificando las misiones para que se dirijan a un planeta.
- Se debe gestionar el combustible de las naves y su recarga de forma adecuada.
