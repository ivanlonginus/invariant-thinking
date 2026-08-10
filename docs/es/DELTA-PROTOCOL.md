# Protocolo DELTA

**Fuente canónica:** [`../../DELTA-PROTOCOL.md`](../../DELTA-PROTOCOL.md)

> Traducción informativa al español. La versión en inglés es la fuente canónica.

DELTA es el método operativo de Invariant Thinking. Su objetivo es reducir el reaprendizaje innecesario sin ocultar la novedad genuina.

## D — Decompose / Descomponer

Describe el sistema sin depender de su categoría de marketing. Registra actores, entradas, salidas, estado, transformaciones, límites, recursos, dependencias, modos de fallo y supuestos de confianza.

Preguntas clave:
- ¿Qué hace realmente el sistema?
- ¿Dónde se mantiene el estado?
- ¿Qué componentes se comunican?
- ¿Qué acciones cruzan límites de confianza o proceso?
- ¿Qué puede fallar de manera independiente?

**Salida:** una descripción estructural neutral.

## E — Extract / Extraer

Identifica restricciones e invariantes candidatos.

Preguntas clave:
- ¿Qué condiciones deben seguir satisfaciéndose independientemente de la implementación?
- ¿Qué restricciones vienen de la física, la información, la economía, la confianza o la definición del problema?
- Si el producto desapareciera mañana, ¿qué problema seguiría existiendo?

Todo invariante candidato debe declarar una transformación y un límite.

**Salida:** afirmaciones de invariantes candidatos.

## L — Link / Vincular

Relaciona la descomposición con conocimiento previo.

Preguntas clave:
- ¿Qué mecanismos o patrones ya son conocidos?
- ¿Qué sistemas anteriores comparten las relaciones relevantes?
- ¿La semejanza es estructural o solo visual o terminológica?

No fuerces un mapeo. Un componente sin correspondencia es información útil.

**Salida:** vínculos con modelos previos y áreas sin mapear.

## T — Test / Probar

Intenta demostrar que la transferencia propuesta no se sostiene.

Preguntas clave:
- ¿Dónde deja de funcionar la analogía?
- ¿Qué supuesto invariante realmente cambió?
- ¿Qué nueva restricción invalida el modelo anterior?
- ¿La escala cambia cualitativamente el mecanismo?
- ¿Existe una nueva capacidad que el modelo anterior no puede explicar?

Esta etapa evita el razonamiento de que "todo es lo mismo por debajo".

**Salida:** rupturas de analogía, correcciones de límites e invariantes rechazados.

## A — Acquire / Adquirir

Estudia el Delta de Aprendizaje restante.

Prioriza:
1. mecanismos genuinamente nuevos;
2. restricciones modificadas;
3. límites modificados;
4. semánticas de implementación que afecten la corrección;
5. detalles operativos necesarios para el trabajo actual.

Desprioriza la memorización que pueda recuperarse fácilmente y que no mejore el modelo estructural.

**Salida:** una agenda explícita de aprendizaje.

## Criterios de finalización

Un análisis DELTA es suficientemente completo para uso práctico cuando puede responder:
- ¿Qué cambió?
- ¿Qué permaneció verdadero?
- ¿Bajo qué transformación y límite?
- ¿Dónde se rompe la analogía?
- ¿Qué necesito aprender todavía?

## Señal de revisión

Si el análisis produce casi ningún Delta de Aprendizaje para un sistema genuinamente desconocido, considera que la abstracción puede ser demasiado amplia y repite **Test**.
