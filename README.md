# Predicción de churn en telecomunicaciones

Proyecto integrador

**Estado:** Hito 1 (avance)

## Integrantes

- Patricio Rodriguez Delgado
- Romina Enriquez Martinez
- Anais Huayhuapuma De la cruz

## Problema de negocio

Una empresa de telecomunicaciones pierde cada mes a parte de sus clientes y
reparte su presupuesto de retención sin saber quién está por irse. El análisis
busca decidir a qué clientes ofrecerles una promoción, empezando por los de
mayor riesgo de darse de baja.

- **Pregunta analítica:** ¿qué clientes tienen más probabilidad de darse de baja?
- **Unidad de análisis:** un cliente por fila.
- **Variable objetivo:** `Churn` (sí / no).
- **KPI:** tasa de fuga = clientes que se dieron de baja / total de clientes × 100.
  Línea base: 26.54 % (1 869 de 7 043 clientes).

## Cuadernos (ejecutar en este orden)

| Orden | Cuaderno | Abrir |
| --- | --- | --- |
| 1 | `notebooks/01_carga_datos.ipynb`: carga y verificación de los datos | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sofiaenma14/churn-telecom-proyecto-integrador/blob/main/notebooks/01_carga_datos.ipynb) |
| 2 | `notebooks/02_comprension_preparacion.ipynb`: calidad, decisiones de preparación y particiones | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sofiaenma14/churn-telecom-proyecto-integrador/blob/main/notebooks/02_comprension_preparacion.ipynb) |

## Documentos del proyecto

- [Canvas del proyecto de datos](informes/Canvas_Proyecto_Datos_Hito1.docx)
- [Ficha CRISP-DM](informes/Ficha_Proyecto_CRISP-DM_Hito1.docx)
- [Presentación del avance (PDF)](informes/Hito1_Avance_Proyecto_Integrador.pdf)
- [Plan de modelado](informes/Plan%20de%20modelado.docx)

## Datos

- **Fuente:** Telco Customer Churn (Kaggle) —
  https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- **Fecha de obtención:** 22/10/2026
- **Contenido:** 7 043 clientes y 21 columnas (servicios contratados, tipo de
  contrato, cargos, meses de antigüedad y si se dio de baja).
- **Nota:** los datos son una foto de un solo momento, sin fechas.
- **Diccionario de datos:** [data/diccionario_datos.md](data/diccionario_datos.md)

## Estructura del repositorio

| Carpeta | Contenido |
| --- | --- |
| `data/` | Datos y diccionario de datos |
| `notebooks/` | Cuadernos ejecutables en Google Colab |
| `informes/` | Ficha CRISP-DM, canvas y plan de modelado |

## Reproducibilidad

- Los cuadernos se ejecutan de inicio a fin en Google Colab.
- Semilla aleatoria fija (42) declarada en el setup de cada cuaderno.
- Rutas relativas a la carpeta del repositorio.
