# Diccionario de datos — Proyecto integrador (Hito 1)

> Fecha de verificación de acceso: **22/10/2026**. Los datos se descargaron desde Kaggle y se revisaron
> (número de filas, número de columnas y código de verificación del archivo).
> Reglas: español, fechas en formato DD/MM/YYYY, codificación UTF-8.

---

## 1. `WA_Fn-UseC_-Telco-Customer-Churn.csv` — Dataset del proyecto

- **Para qué se usa:** es el dataset del proyecto (retención de clientes en telecomunicaciones, churn).
- **Fuente original:** Kaggle, *Telco Customer Churn* (autor: BlastChar). Son datos de ejemplo de IBM.
- **Enlace:** `https://www.kaggle.com/datasets/blastchar/telco-customer-churn`
- **Fecha de obtención:** 22/10/2026
- **Licencia:** según la página de Kaggle (revisada el 22/10/2026): «Archivos de datos © Autores originales». Se usa con fines académicos.
- **Tamaño:** 7 043 filas y 21 columnas. El archivo pesa 977 501 bytes (menos de 25 MB), así que se guarda en la carpeta `data/`.
- **Código de verificación del archivo (SHA256):** `88be4b93fbe0cc83421af1c503794c97c342eca914c1576db7c276e61d61358a`. Sirve para comprobar que el archivo no cambió.
- **Qué representa cada fila:** un cliente. La columna `customerID` no se repite (hay 7 043 códigos distintos).
- **Momento de los datos:** es una foto de un solo momento. No trae fechas.
- **Variable objetivo:** `Churn` (sí o no). `No` = 5 174 clientes y `Yes` = 1 869 clientes. El 26.54 por ciento de los clientes se dio de baja (1 869 de 7 043).
- **Datos faltantes:** no hay celdas vacías a simple vista. Pero `TotalCharges` tiene **11 casillas con un espacio en blanco**, que en la práctica son datos faltantes. Son clientes con 0 meses de antigüedad, que todavía no recibían su primera factura.

### Columnas

| Columna | Tipo | Valores o rango | Qué significa |
|---|---|---|---|
| `customerID` | texto | 7 043 códigos distintos | Código del cliente. No se usa para analizar. |
| `gender` | texto | `Male` (3 555), `Female` (3 488) | Género del cliente. |
| `SeniorCitizen` | número (0 o 1) | `0` (5 901), `1` (1 142) | Si el cliente es adulto mayor (1 = sí). |
| `Partner` | texto | `Yes` (3 402), `No` (3 641) | Si el cliente tiene pareja. |
| `Dependents` | texto | `Yes` (2 110), `No` (4 933) | Si el cliente tiene personas a su cargo. |
| `tenure` | número | 0 a 72 | Meses que lleva el cliente en la empresa. |
| `PhoneService` | texto | `Yes` (6 361), `No` (682) | Si tiene servicio de teléfono. |
| `MultipleLines` | texto | `Yes` (2 971), `No` (3 390), `No phone service` (682) | Si tiene varias líneas de teléfono. |
| `InternetService` | texto | `Fiber optic` (3 096), `DSL` (2 421), `No` (1 526) | Tipo de internet que tiene contratado. |
| `OnlineSecurity` | texto | `Yes` (2 019), `No` (3 498), `No internet service` (1 526) | Si tiene el servicio de seguridad en línea. |
| `OnlineBackup` | texto | `Yes` (2 429), `No` (3 088), `No internet service` (1 526) | Si tiene el servicio de respaldo en línea. |
| `DeviceProtection` | texto | `Yes` (2 422), `No` (3 095), `No internet service` (1 526) | Si tiene protección para sus dispositivos. |
| `TechSupport` | texto | `Yes` (2 044), `No` (3 473), `No internet service` (1 526) | Si tiene soporte técnico. |
| `StreamingTV` | texto | `Yes` (2 707), `No` (2 810), `No internet service` (1 526) | Si tiene televisión por internet. |
| `StreamingMovies` | texto | `Yes` (2 732), `No` (2 785), `No internet service` (1 526) | Si tiene películas por internet. |
| `Contract` | texto | `Month-to-month` (3 875), `One year` (1 473), `Two year` (1 695) | Tipo de contrato: mes a mes, de un año o de dos años. |
| `PaperlessBilling` | texto | `Yes` (4 171), `No` (2 872) | Si recibe la factura por internet, sin papel. |
| `PaymentMethod` | texto | `Electronic check` (2 365), `Mailed check` (1 612), `Bank transfer (automatic)` (1 544), `Credit card (automatic)` (1 522) | Forma de pago. |
| `MonthlyCharges` | decimal | 18.25 a 118.75 | Lo que paga el cliente cada mes. |
| `TotalCharges` | texto (hay que pasarlo a número) | 18.8 a 8 684.8, con 11 vacíos | Lo que ha pagado el cliente en total desde que llegó. |
| `Churn` | texto | `Yes` (1 869), `No` (5 174) | **Variable objetivo.** Si el cliente se dio de baja (`Yes`) o sigue con la empresa (`No`). |

---

## 2. Cosas a tener en cuenta

- `SeniorCitizen` viene como número (0 o 1). Las demás columnas de sí o no vienen como texto (`Yes` o `No`).
- `TotalCharges` se lee como texto por los 11 espacios en blanco. Para analizarla hay que pasarla a número.
- En las columnas de internet (`OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV` y `StreamingMovies`), los 1 526 clientes sin internet aparecen como `No internet service`. En `MultipleLines`, los 682 clientes sin teléfono aparecen como `No phone service`.
- Los datos no traen fechas. Por eso no se puede medir qué pasa en los 30 días siguientes. La columna `Churn` solo dice si el cliente ya se dio de baja o no.
- Si el archivo ya está en `data/` y su código SHA256 es el mismo de arriba, no hace falta descargarlo otra vez.
