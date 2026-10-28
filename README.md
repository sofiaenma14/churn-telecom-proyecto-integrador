# Predicción de churn en telecomunicaciones

Proyecto integrador del curso **Herramientas para la Ciencia de Datos**
(Facultad de Negocios, UPC · Administración y Ciencia de Datos para Negocios).

**Estado:** Hito 1 (avance del examen parcial).

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

## Datos

- **Fuente:** Telco Customer Churn (Kaggle) —
  https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- **Fecha de obtención:** 22/10/2026
- **Contenido:** 7 043 clientes y 21 columnas (servicios contratados, tipo de
  contrato, cargos, meses de antigüedad y si se dio de baja).
- **Nota:** los datos son una foto de un solo momento, sin fechas.

## Estructura del repositorio

| Carpeta | Contenido |
| --- | --- |
| `data/` | Datos y diccionario de datos |
| `notebooks/` | Cuadernos ejecutables en Google Colab |
| `informes/` | Ficha CRISP-DM, canvas y documentos del proyecto |

## Reproducibilidad

- Los cuadernos se ejecutan de inicio a fin en Google Colab.
- Semilla aleatoria fija declarada en el setup de cada cuaderno.
- Rutas relativas a la carpeta del repositorio.
