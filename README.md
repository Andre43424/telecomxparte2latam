# Análisis de Cancelación de Clientes

## Descripción del Proyecto
Este proyecto identifica los factores clave que influyen en la cancelación de clientes y propone estrategias
basadas en datos para mejorar la retención. Utilizamos modelos de machine learning (Regresión Logística, Random Forest y KNN)
para predecir el riesgo de cancelación y analizar el impacto de diferentes variables.

- Preparar y limpiar los datos.
- Transformar variables categóricas en numéricas.
- Identificar y tratar el desbalance de clases.
- Entrenar y comparar modelos de clasificación.
- Interpretar resultados y extraer factores claves asociados al churn.

  ### Fuente y Variables
- **Archivo**: `datos_tratados.csv`
- **Variables relevantes**:
  | Variable | Tipo | Descripción |
  |----------|------|-------------|
  | `Cliente_cancelado` | Binaria | Target (1=Canceló, 0=No canceló) |
  | `Mayor_de_65_años` | Binaria | 1=Sí, 0=No |
  | `Tiene_Dependientes` | Binaria | 1=Sí, 0=No |
  | `Meses_Contratados` | Numérica | Antigüedad del cliente |
  | `Tipo_de_Contrato` | Categórica | "Month-to-month", "Annual", etc. |
  | `Metodo_Pago` | Categórica | "Tarjeta", "Transferencia", etc. |
  | `Cobro_Mensual` | Numérica | Monto facturado mensualmente |
  | `Gasto_Total` | Numérica | Gasto acumulado del cliente |

## 📌 Hallazgos Clave
- **Factores principales** que afectan la cancelación:
  - Antigüedad del cliente (`Meses_Contratados`)
  - Monto del cobro mensual (`Cobro_Mensual`)
  - Tipo de contrato (`Tipo_de_Contrato_Annual`)
- **Modelo con mejor rendimiento**: Random Forest (F1-Score: 0.77)
- **Variables más influyentes**:
  1. Meses contratados (22-28% de importancia)
  2. Cobro mensual (18-20%)
  3. Tipo de contrato anual (12-15%)
