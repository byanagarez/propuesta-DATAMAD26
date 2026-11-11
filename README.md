<div align="center">

# MADRID A TU MEDIDA

### ¿Y si pudieras descubrir dónde vivir según cómo quieres vivir?

**Sistema de recomendación residencial personalizado · DATAMAD 2026**

*Una propuesta para transformar datos abiertos de la Comunidad de Madrid en decisiones residenciales comprensibles, adaptadas y justificadas.*

![Portada conceptual del proyecto](assets/portada-datamad1.png)

**Estado:** propuesta de proyecto · **Ámbito:** Comunidad de Madrid · **Formato previsto:** aplicación web interactiva

</div>

---

## El problema

Elegir dónde vivir no depende únicamente del precio del alquiler. También importan las horas que dedicamos a desplazarnos, la accesibilidad a servicios, el entorno y nuestras necesidades particulares. Sin embargo, esta información suele estar dispersa entre distintas fuentes y resulta difícil de comparar.

**Madrid a tu medida** propone invertir el proceso habitual de búsqueda: en lugar de pedir a una persona que elija primero un municipio, **el sistema le recomienda zonas residenciales a partir de su perfil y sus prioridades**.

## ¿Cómo funciona?

**01 · Cuéntanos cómo vives** → **02 · Analizamos las alternativas** → **03 · Descubre tus tres zonas recomendadas**

```mermaid
flowchart LR
    A[Perfil y preferencias] --> B[Datos abiertos y cálculos]
    B --> C[Restricciones y comparación]
    C --> D[Tres recomendaciones explicadas]
```

### Datos de entrada y resultados

| **El usuario introduce (inputs)** | **La aplicación devuelve (outputs)** |
|---|---|
| Destino habitual de trabajo o estudio | Tres zonas recomendadas y explicación de cada elección |
| Presupuesto máximo mensual de alquiler | Alquiler estimado de una vivienda comparable |
| Tiempo máximo de desplazamiento por trayecto | Minutos por trayecto y horas mensuales de transporte |
| Días presenciales y medio de transporte | Coste mensual estimado de transporte y gasto conjunto |
| Preferencias: sanidad, naturaleza, educación, cultura | Accesibilidad a servicios relevantes y mapa comparativo |
| Preferencia por calidad ambiental | Indicadores ambientales con fecha y cobertura |
| Necesidades de movilidad reducida (opcional) | Indicadores de accesibilidad PMR **solo donde existan datos verificables** |
| Interés por la seguridad de la zona (opcional) | Contexto de seguridad territorial **solo si hay datos comparables** |

![Inputs del sistema a fondo](assets/portada-datamad2.png)

El salario no es obligatorio. La aplicación no solicita una zona residencial de partida: **encontrarla es su propósito**.

## Experiencia de usuario prevista

| Pantalla | Objetivo | Interacción principal |
|---|---|---|
| **1. Tu perfil** | Conocer necesidades y límites | Formulario visual, selectores y prioridades |
| **2. Buscando tu lugar** | Mostrar el proceso de comparación | Transición animada honesta, sin simular cálculos inexistentes |
| **3. Tus tres lugares** | Explicar recomendaciones | Tarjetas comparativas, indicadores y mapa interactivo |

```mermaid
flowchart TB
    subgraph S1[01 · TU PERFIL]
      A1[Destino laboral]
      A2[Presupuesto y tiempo máximo]
      A3[Días presenciales y movilidad]
      A4[Preferencias y necesidades PMR]
    end
    subgraph S2[02 · ANÁLISIS]
      B1[Filtrar zonas viables]
      B2[Calcular costes y tiempos]
      B3[Contrastar servicios y condiciones]
    end
    subgraph S3[03 · RESULTADOS]
      C1[Opción ahorro]
      C2[Opción menor desplazamiento]
      C3[Opción de equilibrio]
      C4[Por qué estas zonas + mapa]
    end
    S1 --> S2 --> S3
```

> Los nombres «ahorro», «menor desplazamiento» y «equilibrio» describen posibles perfiles de resultados, **no tres ganadores garantizados**: si los datos o las restricciones no permiten tres opciones diferentes, la interfaz lo explicará.

## Metodología: recomendaciones explicables

1. **Integración de datos.** Unificar indicadores de vivienda, transporte y equipamientos a una unidad territorial comparable (municipio o zona, según cobertura).
2. **Estimación comparable.** Calcular el alquiler de una vivienda de superficie de referencia, identificando año, fuente y límites de la estimación.
3. **Movilidad personalizada.** Estimar desplazamientos hacia el destino elegido y horas mensuales según días presenciales. Los horarios planificados no equivalen a tiempos reales garantizados.
4. **Filtros personales.** Excluir alternativas que superen el presupuesto de alquiler o el tiempo máximo declarado.
5. **Optimización multicriterio.** Identificar alternativas no dominadas mediante una **frontera de Pareto** en gasto mensual (alquiler + transporte) y tiempo mensual de desplazamiento.
6. **Adaptación y explicación.** Contrastar las opciones viables con las preferencias sobre servicios y entorno; seleccionar hasta tres alternativas diferenciadas mediante criterios documentados y mostrar ventajas, inconvenientes y procedencia de cada indicador.

**No asignaremos un precio arbitrario al tiempo libre.** Mostraremos por separado gasto y horas, y opcionalmente los euros ahorrados por cada hora adicional de desplazamiento entre dos alternativas.

### Dos dimensiones de especial interés

**Seguridad de la zona.** Se estudiará la disponibilidad de estadísticas públicas oficiales con cobertura territorial, período y denominadores comparables. Si solo existen cifras municipales o agregadas, no se atribuirán a barrios o calles ni se elaborará un «índice de seguridad» ficticio. Se evitará equiparar datos de denuncias con riesgo individual.

**Accesibilidad para personas con movilidad reducida.** Se priorizarán datos verificables de estaciones y paradas accesibles, ascensores, itinerarios peatonales y acceso a equipamientos. Un posible indicador medirá la proporción de destinos alcanzables mediante rutas documentadas como accesibles. **La ausencia de datos no se interpretará como falta de accesibilidad**, ni se presentarán rutas como accesibles sin validación.

## Fuentes de datos previstas


## Fuentes de datos previstas

| Dimensión | Dato introducido | Fuente candidata |
|---|---|---|
| **Economía** | Presupuesto máximo de alquiler | https://serpavi.mivau.gob.es/ |
| | Tamaño de vivienda deseado (m²) |  |
| | Número de habitaciones | |
| | Salario neto mensual (opcional) | |
| | Prioridad entre ahorrar y reducir desplazamientos | |
| **Movilidad** | Lugar de trabajo o estudio | |
| | Tiempo máximo por trayecto | |
| | Días presenciales por semana | |
| | Medio de transporte preferido | |
| | Disponibilidad de coche | |
| | Hora habitual de entrada | |
| | Tolerancia a transbordos | |
| | Necesidades de accesibilidad para personas con movilidad reducida (PMR) | https://www.madridaccesible.com/datos |
| **Servicios** | Importancia de tener un centro de salud cerca | |
| | Necesidad de hospital cercano | https://datos.comunidad.madrid/catalogos/#/dataset/centros_servicios_establecimientos_sanitarios?view=info |
| | Necesidad de centros educativos | https://datos.comunidad.madrid/catalogos/#/dataset/centros_educativos?view=info |
| | Importancia de supermercados y comercios | |
| | Importancia de bibliotecas y centros culturales | https://datos.comunidad.madrid/catalogos/#/dataset/centros_servicios_bibliotecarios_dependientes_cm_ayuntamiento_madrid?view=info |
| | Necesidad de instalaciones deportivas | |
| **Entorno** | Preferencia por parques y zonas verdes | |
| | Importancia de la calidad del aire | https://datos.comunidad.madrid/catalogos/#/dataset/calidad_aire_datos_meteo_mes?view=info |
| | Preferencia por zonas tranquilas | https://datos.comunidad.madrid/catalogos/#/dataset/SPA_28079_PLAN_ACCION_MATERIA_CONTAMINACION_ACUSTICA_2025?view=info |
| | Importancia de la seguridad de la zona | https://datos.gob.es/es/catalogo/ea0040772-delincuencia-y-victimizacion-en-la-comunidad-de-madrid |
| | Preferencia por entorno urbano o residencial | |
| | Preferencia por movilidad peatonal | |
| **Estilo de vida** | Frecuencia de actividades culturales | |
| | Frecuencia de actividad deportiva | https://datos.comunidad.madrid/catalogos/#/dataset/actividades_fisicas_frecuentes_por_sexo_y_edad?view=info |
| | Necesidad de desplazamientos nocturnos | https://datos.comunidad.madrid/catalogos/#/dataset/1919186?view=info |
| | Importancia de estar cerca de una estación | https://datos.comunidad.madrid/catalogos/#/dataset/infraestructura_transporte_publico?view=info |
| | Preferencia por servicios a poca distancia | https://datos.comunidad.madrid/catalogos/#/dataset/a7357488-d9f0-11ed-b370-34298f78123d?view=info |


**Compromiso DATAMAD:** incorporar efectivamente al menos un conjunto de datos del **catálogo oficial de la Comunidad de Madrid**, documentando su uso y transformación. Las fuentes son candidatas y se validarán por fecha, cobertura, licencia y granularidad antes de usarlas en resultados reales.

## Arquitectura técnica propuesta

```mermaid
flowchart LR
    A[Fuentes oficiales / GTFS / cartografía] --> B[ETL en Python o R]
    B --> C[Datos normalizados y precálculos]
    C --> D[Motor de recomendación explicable]
    D --> E[Web Astro + React + TypeScript]
    E --> F[Tarjetas, gráficos y mapa MapLibre]
```

- **Procesamiento:** Python/R, pandas/GeoPandas y formatos CSV/Parquet.
- **Movilidad:** datos GTFS y red peatonal; rutas precalculadas para destinos seleccionados cuando sea viable.
- **Motor:** filtros reproducibles, frontera de Pareto y reglas transparentes de selección.
- **Interfaz:** Astro + React + TypeScript; cartografía MapLibre y visualizaciones interactivas.
- **Despliegue previsto:** Vercel para la web; procesamiento pesado fuera del navegador.
- **Calidad:** pruebas con perfiles distintos, control de valores faltantes y trazabilidad de fuentes.

## Alcance y honestidad metodológica

Esta es una **propuesta en fase de diseño**, no una aplicación terminada. Las pantallas y ejemplos visuales son conceptuales. La cobertura de municipios, las fuentes de alquiler, la seguridad territorial y la accesibilidad PMR dependerán de la validación de los datos. Si una dimensión carece de información suficiente, se mostrará como **«dato no disponible»** y no afectará silenciosamente al resultado.

**Objetivo:** que cualquier persona pueda entender **por qué** se le recomienda un lugar y **qué compromisos** implica elegirlo.

---

<div align="center">

**DATAMAD 2026 · Propuesta de Ana y Giulio**

*Los datos no deberían decirte cómo vivir. Deberían ayudarte a elegir.*

</div>
