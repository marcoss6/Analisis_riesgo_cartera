# 📊 Análisis de riesgo de una cartera en R

Este proyecto permite calcular automáticamente la **rentabilidad**, **volatilidad** y el **Value at Risk (VaR)** de una cartera de acciones, utilizando distintos modelos de estimación de riesgo.

## 🧠 ¿Qué hace este script?

- Descarga datos de cotización desde Yahoo Finance
- Calcula:
  - ✅ Rentabilidades individuales y de la cartera
  - 📉 Volatilidad mediante modelos **RiskMetrics (EWMA)** y **EGARCH**
  - ⚠️ Value at Risk (VaR) por 4 métodos: **Normal**, **Histórico**, **RiskMetrics** y **EGARCH**
  - ✅ **Backtesting** de cada modelo de VaR
- Se genera automáticamente un informe completo en **HTML o PDF**

---

## 🔧 ¿Cómo se usa?

### Cambia solo estas líneas al inicio del archivo `.Rmd`:

```r
tickers <- c("REP.MC", "CABK.MC", "BBVA.MC", "SAN.MC", "NTGY.MC")       # Acciones a analizar
pesos <- c(0.30, 0.25, 0.15, 0.15, 0.15)                                # Pesos de la cartera
start_date <- as.Date("2024-01-01")                                     # Fecha de inicio
end_date <- as.Date("2024-12-31")                                       # Fecha de fin
