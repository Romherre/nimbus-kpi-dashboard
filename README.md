# Nimbus — Panel de KPIs (Demo, React)

Mini dashboard de producto para un SaaS B2B ficticio, pensado como pieza de portfolio para demostrar manejo de React (hooks) integrado con Chart.js.

> Datos y nombre de la empresa son simulados. No corresponde a ningún cliente real.

## Demo en vivo

https://romherre.github.io/nimbus-kpi-dashboard/

## Qué muestra

- 4 KPI cards: MRR, usuarios activos, churn rate, NPS.
- Gráfico de línea: evolución de MRR en los últimos 6 meses.
- Gráfico de dona: tickets de soporte por estado (mismo patrón que se usó en el panel de Sinergia Logística, ahora en React).
- Tabla: cuentas con riesgo de churn, con badges de severidad.

## Stack

- React 18 (vía CDN, hooks: useState, useEffect, useRef)
- Chart.js 4
- Sin build step: Babel Standalone transpila el JSX directamente en el navegador.

## Cómo verlo

Ver la demo en vivo arriba, o clonar el repo y abrir index.html directo con doble click. No requiere npm install ni servidor: el código de React está embebido en el propio index.html (Babel Standalone lo transpila en el navegador). js/app.jsx queda como referencia de lectura del mismo código, organizado en un archivo aparte.

## Por qué sin build (Vite/CRA)

Para esta pieza de portfolio se priorizó que cualquiera pueda abrirla con doble click y verla funcionando, sin pasos de instalación. La lógica de componentes (estado, efectos, limpieza de gráficos al desmontar) es la misma que se usaría con un build tradicional; migrarlo a Vite es directo si se necesita a futuro.
