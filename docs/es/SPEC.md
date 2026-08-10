# Especificación del Invariant Thinking Framework

**Versión:** 0.1-draft  
**Estado:** Propuesta abierta  
**Idioma canónico:** Inglés  
**Fuente canónica:** [`../../SPEC.md`](../../SPEC.md)

> Esta es una traducción informativa al español. La especificación en inglés es la versión normativa. Si existe una diferencia semántica entre ambas versiones, prevalece la versión en inglés.

## 1. Propósito

Invariant Thinking Framework (ITF) define una forma disciplinada de razonar sobre sistemas desconocidos o cambiantes distinguiendo el conocimiento estructural transferible de la novedad específica de una implementación.

El framework está pensado para dominios donde las manifestaciones cambian con suficiente rapidez como para que reaprender repetidamente cada implementación desde cero resulte ineficiente.

## 2. Alcance

ITF especifica:

- un vocabulario para comparación estructural;
- un modelo de análisis por capas (Invariant Stack);
- requisitos para formular afirmaciones de invariancia;
- el Protocolo DELTA para analizar sistemas desconocidos;
- un artefacto Invariant Map para documentar un análisis; y
- expectativas de validación y falsación.

ITF no prescribe un currículo, no garantiza un aprendizaje más rápido y no afirma leyes cognitivas universales.

## 3. Lenguaje normativo

Las palabras **DEBE (MUST)**, **NO DEBE (MUST NOT)**, **DEBERÍA (SHOULD)**, **NO DEBERÍA (SHOULD NOT)** y **PUEDE (MAY)** indican requisitos dentro de esta especificación. Describen conformidad con este framework, no necesidad científica.

## 4. Definiciones centrales

### 4.1 Sistema

Un objeto de análisis delimitado cuyo comportamiento, estructura, implementación o uso se compara con otro estado, sistema o modelo.

### 4.2 Transformación

Un cambio definido desde un estado, representación, implementación, interfaz, arquitectura o contexto de un sistema hacia otro.

Una transformación **PUEDE (MAY)** cambiar algunas propiedades mientras preserva otras.

### 4.3 Invariante

Una propiedad considerada relevantemente inalterada a través de un **conjunto de transformaciones especificado**, dentro de un **límite especificado**.

Una afirmación de invariancia conforme a ITF **NO DEBE (MUST NOT)** expresarse como una afirmación no cualificada de que algo "nunca cambia".

### 4.4 Límite de Invariancia

El contexto dentro del cual se pretende que una afirmación de invariancia sea válida. Puede incluir dominio, actor, escala, modelo de amenazas, modelo de ejecución, restricciones físicas u otros supuestos.

### 4.5 Delta de Aprendizaje

El conocimiento que sigue siendo genuinamente necesario después de identificar y validar el conocimiento previo correctamente transferible.

El Delta de Aprendizaje es conceptual; ITF 0.1 no define una medida numérica para él.

### 4.6 Ruptura de Analogía

Una condición bajo la cual un mapeo estructural propuesto deja de preservar la propiedad relevante para el análisis.

Un análisis conforme **DEBE (MUST)** intentar identificar al menos una ruptura de analogía, un mapeo fallido o una condición de frontera.

## 5. Invariant Stack

ITF utiliza seis capas analíticas. No se afirma que sean ontológicamente universales; constituyen una descomposición práctica.

### L5 — Producto / Interfaz

El producto con nombre propio, superficie, sintaxis, API, modelo de interacción o capacidad externamente visible.

### L4 — Implementación

La realización concreta de una capacidad, incluidas librerías, decisiones de runtime, algoritmos, detalles de despliegue y composición interna.

### L3 — Mecanismo

El proceso mediante el cual se produce un resultado: paso de mensajes, indexación, caching, replicación, renderizado, scheduling, etc.

### L2 — Patrón

Una organización recurrente de mecanismos que aborda una clase de problemas: cliente/servidor, observer, pipeline, pub/sub, event loop, actor model, etc.

### L1 — Restricción

Una condición que limita las soluciones posibles: latencia, memoria finita, confianza, consistencia, fallos, ancho de banda, concurrencia, costo, regulación, límites físicos, etc.

### L0 — Invariante

Una propiedad relevante que permanece preservada a través de la transformación analizada, dentro del límite declarado.

## 6. Afirmación de invariancia válida

Una afirmación de invariancia válida según ITF **DEBE (MUST)** identificar todos los elementos siguientes:

- **Propiedad** — qué se afirma que permanece verdadero.
- **Transformación** — qué está cambiando.
- **Límite** — dónde aplica la afirmación.
- **Razonamiento o evidencia** — por qué se espera que la propiedad persista.
- **Condición de ruptura** — un caso en el que la afirmación puede dejar de sostenerse.

Ejemplo:

> En aplicaciones multiusuario que ejecutan comportamiento privilegiado en el servidor, la necesidad de aplicar autorización permanece a través de transformaciones desde endpoints REST hacia server actions mediadas por un framework, salvo que el límite de ejecución desaparezca o que todas las acciones pasen a ser no privilegiadas y no específicas del usuario.

## 7. Protocolo DELTA

Un análisis ITF conforme **DEBERÍA (SHOULD)** seguir el Protocolo DELTA en este orden:

1. **Decompose** — descomponer el sistema objetivo.
2. **Extract** — extraer restricciones e invariantes candidatos.
3. **Link** — vincularlos con modelos previos.
4. **Test** — poner a prueba los mapeos y sus límites.
5. **Acquire** — adquirir el Delta de Aprendizaje restante.

Véase [`DELTA-PROTOCOL.md`](DELTA-PROTOCOL.md).

## 8. Invariant Map

Un análisis ITF reutilizable **DEBERÍA (SHOULD)** registrarse como un Invariant Map que contenga:

- objeto de análisis;
- propósito;
- contextos de origen y destino;
- transformación;
- límite;
- descomposición;
- invariantes candidatos;
- vínculos con modelos previos;
- propiedades modificadas;
- rupturas de analogía;
- delta de aprendizaje;
- incógnitas;
- notas de confianza y evidencia.

Véase [`../../maps/template.yaml`](../../maps/template.yaml).

## 9. Reglas de validación

Un análisis es más sólido cuando:

- distingue semejanza de invariancia;
- define la transformación en lugar de comparar categorías vagas;
- declara supuestos y límites;
- registra contraejemplos;
- distingue hechos conocidos de inferencias;
- actualiza el mapa cuando aparece evidencia contradictoria.

## 10. Requisito antirreduccionista

ITF **NO DEBE (MUST NOT)** utilizarse para concluir que un sistema nuevo no aporta "nada nuevo" simplemente porque algunas propiedades de menor nivel puedan mapearse a conceptos anteriores.

La existencia de invariantes compartidos no implica mecanismos, implementaciones, capacidades, economía, escala o consecuencias idénticas.

## 11. Principio de Abstracción con Pérdida

Toda abstracción suprime variación. Una abstracción solo es útil cuando la variación descartada es irrelevante para la tarea de razonamiento en cuestión.

Por tanto, los análisis ITF **DEBEN (MUST)** tratar la abstracción excesiva como un modo de fallo y no como una señal de sofisticación.

## 12. Versionado

Los cambios a definiciones normativas **DEBERÍAN (SHOULD)** proponerse mediante RFCs y registrarse en [`../../CHANGELOG.md`](../../CHANGELOG.md).

El framework utiliza versiones públicas de estilo semántico para comunicación, pero las versiones anteriores a 1.0 continúan siendo experimentales.
