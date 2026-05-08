# Análisis de Datos y Segmentación de Clientes

**Entrega 2 · Rafael Ruiz Beltrán, Hugo Rojo & Leo Luka**

---

## Descripción

Proyecto de análisis cuantitativo estructurado en dos bloques: análisis de activos financieros (BTC, ETH, SPY) durante el periodo 2023–2024, y segmentación de perfiles de inversores retail mediante K-Means.

---

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `Graficas_Ruahu.ipynb` | Notebook principal con todo el análisis |
| `dataset_clientes_ruahu.xlsx` | Dataset de 800 clientes segmentados |
| `README.md` | Este documento |

---

## Requisitos

```bash
pip install yfinance pandas numpy matplotlib seaborn scikit-learn plotly colorama openpyxl
```

El proyecto está optimizado para **Google Colab**. En entornos sin conexión, el código genera automáticamente datos simulados con parámetros estadísticos equivalentes a los reales.

---

## Ejecución

Abrir `Graficas_Ruahu.ipynb` en Google Colab y ejecutar todas las celdas en orden. El notebook genera seis figuras PNG y un archivo `customers.csv` al finalizar.

---

## Estructura del notebook

| Sección | Contenido |
|---|---|
| 1 · Descarga de datos | Obtención de precios con `yfinance` para BTC-USD, ETH-USD y SPY |
| 2 · Estadísticas descriptivas | Retorno total, volatilidad anualizada, Sharpe ratio y máximo drawdown |
| 3 · Visualizaciones | Precios absolutos, comparativa normalizada (base 100), rendimientos diarios y volatilidad móvil (MM30) |
| 4 · Predicciones | Modelo de Paseo Aleatorio evaluado con MAE a horizontes de 1, 5, 10 y 15 días |
| 5 · Segmentación | Generación del dataset, visualización por segmento e interpretación de perfiles |

---

## Dataset de clientes

El archivo `dataset_clientes_ruahu.xlsx` contiene **800 registros sintéticos** de inversores retail distribuidos en tres segmentos. Los datos son ficticios y han sido generados con parámetros estadísticos coherentes con los descritos en el informe.

### Variables

| Variable | Tipo | Rango |
|---|---|---|
| `ID_Cliente` | Texto | CLI0001 – CLI0800 |
| `Edad` | Entero | 20 – 70 años |
| `Ingresos_Anuales_EUR` | Entero | 15.000 – 120.000 € |
| `Experiencia_Inversora_Anos` | Decimal | 0.5 – 35 años |
| `Tolerancia_Riesgo` | Entero | 1 (baja) – 5 (muy alta) |
| `Uso_Plataformas_Digitales` | Entero | 1 – 10 plataformas |
| `Tipo_Inversor` | Texto | 3 categorías |

### Segmentos

| Segmento | N | % | Edad media | Ingresos medios | Tolerancia |
|---|---|---|---|---|---|
| Especulador Digital | 240 | 30% | 28 años | 28.000 € | 4.2 / 5 |
| Inversor Pragmático | 300 | 38% | 40 años | 52.000 € | 2.7 / 5 |
| Conservador Experimentado | 260 | 32% | 57 años | 79.000 € | 1.5 / 5 |

---

*Proyecto académico · 2024*
