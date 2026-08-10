# Invariant Thinking

**Un framework para aprender y razonar bajo cambio tecnológico acelerado.**

Invariant Thinking es un framework conceptual abierto para separar **estructura transferible** de **novedad específica de implementación**. Su objetivo es práctico: cuando aparece una tecnología nueva, no reaprender toda la superficie; identificar qué permanece estructuralmente verdadero, comprobar dónde deja de ser válido el paralelismo y concentrar el aprendizaje profundo en el **delta real**.

> Aprende lo que sobrevive al cambio.

## Estado

**Draft 0.1 — propuesta abierta.**

Invariant Thinking no se presenta como una teoría científica validada de la cognición. Se presenta como un framework estructurado, un vocabulario y un método repetible que pueden usarse, criticarse, extenderse y eventualmente evaluarse de forma empírica.

## Problema

En dominios técnicos de cambio rápido, herramientas, frameworks, APIs, interfaces y categorías de producto cambian más rápido de lo que una persona puede estudiar cada manifestación de forma independiente. Un aprendizaje centrado únicamente en implementaciones produce retrabajo cognitivo recurrente.

Invariant Thinking propone otra unidad de aprendizaje:

```text
producto -> implementación -> mecanismo -> patrón -> restricción -> invariante
```

El framework no afirma que toda innovación sea superficial. De hecho, obliga a buscar dónde una analogía falla y dónde comienza una novedad irreducible.

## Modelo central

### Invariant Stack

| Capa | Pregunta | Volatilidad típica |
|---|---|---:|
| L5 — Producto / Interfaz | ¿Con qué interactúa el usuario o desarrollador? | Alta |
| L4 — Implementación | ¿Cómo está construida concretamente la capacidad? | Alta |
| L3 — Mecanismo | ¿Mediante qué mecanismo funciona? | Media-alta |
| L2 — Patrón | ¿Qué organización recurrente resuelve esta clase de problema? | Media |
| L1 — Restricción | ¿Qué limita el espacio de soluciones? | Media-baja |
| L0 — Invariante | ¿Qué propiedad relevante permanece bajo la transformación definida? | Dependiente del contexto |

Un invariante válido debe declarar siempre:

1. la **propiedad**;
2. el **conjunto de transformaciones**; y
3. el **límite de validez**.

## Protocolo DELTA

1. **Decompose** — descomponer actores, estado, entradas, salidas, límites, recursos, transformaciones y dependencias.
2. **Extract** — extraer restricciones e invariantes candidatos.
3. **Link** — enlazarlos con conocimiento y patrones previos.
4. **Test** — intentar romper activamente la analogía o el supuesto invariante.
5. **Acquire** — aprender el delta irreducible restante.

Relación conceptual:

```text
sistema nuevo
- conocimiento previo correctamente transferible
= delta de aprendizaje
```

No es una ecuación cuantitativa.

## Cuatro preguntas canónicas

1. **¿Qué cambió?**
2. **¿Qué permaneció verdadero?**
3. **¿Bajo qué transformación y límite?**
4. **¿Dónde se rompe la analogía?**

Si la cuarta pregunta no tiene respuesta, el análisis está incompleto.

## Contribución propuesta

El proyecto no reclama haber inventado la invariancia, la abstracción o la transferencia de conocimiento. Su propuesta específica es combinar:

- **Invariant Stack**;
- **Transformation + Boundary** como contexto obligatorio;
- **Learning Delta** como objetivo del aprendizaje profundo;
- **DELTA Protocol**;
- **Invariant Maps** como artefacto reutilizable; y
- prueba explícita de **analogy breaks** para evitar reduccionismo.

La versión canónica de la especificación está en inglés en [`SPEC.md`](SPEC.md).
