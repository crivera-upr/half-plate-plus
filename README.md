# 🍽️ Half-Plate PLUS

Juego educativo interactivo sobre alimentación balanceada, impacto ambiental y desperdicio de alimentos — centrado en el paisaje alimentario de Puerto Rico. Desarrollado en el marco del curso ESGE 4995-043 de la Universidad de Puerto Rico (2026).

**Autor:** Christian Rivera Calderón  
**Programa:** Estudios Generales  
**Curso:** ESGE 4995-043, Universidad de Puerto Rico, 2026

**Demo:** [Ver Half-Plate PLUS →](https://crivera-upr.github.io/half-plate-plus/)

---

## Sobre el proyecto

Half-Plate PLUS nace de la intersección entre sistemas alimentarios, salud pública y sostenibilidad ambiental. La premisa es simple: construye un plato donde al menos la mitad sean frutas y vegetales. Pero cada decisión alimentaria tiene consecuencias visibles — calorías, costo, emisiones de CO₂, huella hídrica, nivel de procesamiento (NOVA) y riesgo de desperdicio — todas actualizadas en tiempo real.

La despensa incluye 63 alimentos centrados en Puerto Rico, desde productos locales como plátano verde, mofongo y gandules hasta artículos importados como brócoli y pasta. Cada item contiene datos nutricionales, ambientales y de costo investigados, con nombres bilingües inglés/español.

El proyecto integra el tema central del semestre: **pérdida y desperdicio de alimentos (FLW) y emisiones de metano**, a través de una capa de concienciación sobre desperdicios que muestra riesgo de deterioro, consejos de almacenamiento y una puntuación de riesgo de desperdicio por plato.

> ⚕️ **Aviso:** Esta herramienta es de carácter educativo exclusivamente. No provee consejo médico, nutricional ni dietético.

---

## Características

- **63 alimentos** organizados en 7 categorías: Vegetables, Fruits, Starches/Viandas, Grains, Protein, Dairy, Ultra-processed
- **6 métricas en tiempo real** por plato: conteo de frutas/vegetales, calorías, presupuesto, CO₂e, huella hídrica y conteo de ultra-procesados
- **Capa de desperdicio de alimentos** con badge de riesgo de deterioro (⚠️ alto · ⏳ medio · ✓ bajo), tooltips de almacenamiento y widget de riesgo de desperdicio con sistema de puntuación
- **3 modos de juego**: Sandbox (libre), Challenge (5 packs de retos) y Speedrun (30 segundos, 5 variantes)
- **6 logros** rastreados: Rainbow, Thrifty, Lite, Eco, Low Water, Minimal Waste
- **Filtro estacional** basado en el calendario tropical de PR (seca: dic–abr, lluviosa: may–nov)
- **Búsqueda bilingüe** por nombre en inglés o español
- **Guía interactiva** de 7 diapositivas con diagramas SVG (archivo separado)
- **Diseño responsivo** — funciona en móvil, tablet y escritorio
- **Aplicación standalone** — un solo archivo HTML, sin dependencias de servidor ni instalación

---

## Estado del proyecto — Versión 6.2

| Prioridad | Descripción | Estado |
|-----------|-------------|--------|
| I | Reconstruir capa de información (63 alimentos con fuentes) | ✅ Completada |
| II | Despensa centrada en PR (28 items locales, 7 categorías) | ✅ Completada |
| III | Guía de onboarding (7 diapositivas, archivo standalone) | ✅ Completada |
| IV | Rediseño visual (layout, tipografía, jerarquía) | 🔄 Pendiente |
| V | Capa de desperdicio/metano (badges, tooltips, widget, educación FLW) | ✅ Completada |
| VI | Identidad y límites (framing educativo, modal About) | ⚡ Parcial |
| VII | Rebalanceo de modos de juego | ⚡ Parcial |
| VIII | Extras opcionales (audio, animaciones) | 🔄 Pendiente |

### Resumen estadístico

```
63 alimentos · 7 categorías · 28 items locales de PR
6 métricas en tiempo real · 5 challenge packs · 5 speedrun variants
6 logros · 3 modos de juego · 7 diapositivas de guía
```

---

## Fuentes de datos

| Métrica | Fuente |
|---------|--------|
| Calorías | [USDA FoodData Central](https://fdc.nal.usda.gov/) — dominio público (CC0 1.0) |
| Emisiones CO₂ | Poore & Nemecek (2018), *Science* 360(6392), 987-992. Vía [Our World in Data](https://ourworldindata.org/environmental-impacts-of-food) |
| Huella hídrica | Mekonnen & Hoekstra (2011), [Water Footprint Network](https://www.waterfootprint.org/) |
| Clasificación NOVA | Monteiro et al., vía [FAO/PAHO](https://openknowledge.fao.org/handle/20.500.14283/ca5644en) |
| Precios | Estimados de retail en PR 2024–2025 (estimados para el juego, no datos verificados) |
| Desperdicio / Metano | [UNEP Food Waste Index 2024](https://www.unep.org/resources/publication/food-waste-index-report-2024) · [UNEP & CCAC Global Methane Assessment 2021](https://www.unep.org/resources/report/global-methane-assessment-benefits-and-costs-mitigating-methane-emissions) · [UNEP & FAO Sustainable Food Cold Chains 2022](https://doi.org/10.4060/cc0923en) |

---

## Desarrollo con inteligencia artificial

### Modelo utilizado

| Parámetro | Valor |
|-----------|-------|
| Modelo | Claude Opus 4, Claude Sonnet 4 |
| Proveedor | Anthropic |
| Interfaz | Claude.ai (conversacional) |
| Periodo de desarrollo | Abril–Mayo 2026 |

### Workflow de dos IAs

Este proyecto utilizó un flujo de trabajo colaborativo con dos asistentes de IA:

- **Claude (primario):** Ideación, redacción, desarrollo de código, sourcing de datos, decisiones estructurales, escritura creativa
- **ChatGPT (crítico):** Verificación, stress-testing, crítica, identificación de edge-cases, auditoría de código

Todas las decisiones de diseño, selección de contenido y dirección del proyecto fueron tomadas por el estudiante. Las IAs actuaron como herramientas de investigación, estructuración y desarrollo — no como autoridad en ninguna afirmación nutricional, médica o ambiental.

### Rol de la IA en el proyecto

- **Arquitectura de datos** — Diseño de la estructura de 63 alimentos con 15+ campos por item (nutricionales, ambientales, estacionales, de desperdicio)
- **Investigación de fuentes** — Localización y verificación de datos de USDA, Poore & Nemecek, Water Footprint Network, UNEP
- **Desarrollo frontend** — Implementación del HTML/CSS/JS standalone, sistema de drag-and-drop, métricas en tiempo real, modos de juego, capa de desperdicio
- **Diseño educativo** — Guía de onboarding con diagramas SVG, conexión FLW→metano, framing pedagógico
- **Control de calidad** — Auditoría de consistencia de datos, testing de game logic, estandarización de nombres bilingües

---

## Estructura del repositorio

```
half-plate-plus/
├── index.html                           # Aplicación web completa (standalone)
├── half-plate-plus-guide-v6_2.html      # Guía interactiva "How to Play" (7 diapositivas)
└── README.md                            # Este archivo
```

> **Nota técnica:** Ambos archivos HTML son autocontenidos (HTML + CSS + JS inline, sin dependencias externas). La guía se abre desde el botón "❓ How to Play" en la app y enlaza de vuelta a `index.html`.

---

## Uso

### Opción 1: Uso directo

Descarga o clona el repositorio y abre `index.html` en cualquier navegador moderno. No requiere servidor, instalación ni dependencias.

### Opción 2: GitHub Pages

Visita la demo en vivo: `https://crivera-upr.github.io/half-plate-plus/`

---

## Licencia

Proyecto académico — Christian Rivera Calderón, Estudios Generales, ESGE 4995-043, Universidad de Puerto Rico, 2026.

---

*Proyecto desarrollado en Puerto Rico · 2026*
*Con el apoyo de Claude AI (Anthropic) y ChatGPT (OpenAI) como herramientas de investigación y desarrollo*
