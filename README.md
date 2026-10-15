# 🌲 Pinus-CO2: Inteligencia de Captura de Carbono y Valoración Financiera

## 📖 Descripción del Proyecto
Este repositorio contiene un ecosistema analítico de extremo a extremo (End-to-End) diseñado para auditar, procesar y visualizar el potencial de captura de carbono en una plantación forestal comercial (Predio Pericuara). 

El objetivo del proyecto es transformar los datos operativos de inventario forestal (mediciones de campo como diámetro y altura) en **métricas de negocio accionables**, cuantificando tanto la biomasa retenida como su valoración económica en el Mercado Voluntario de Carbono (VCM).

## 🚀 Impacto y Hallazgos de Negocio
A través del dashboard interactivo desarrollado en Power BI, se identificaron los siguientes insights clave para la gerencia técnica y financiera:
* **Capitalización Actual:** El rodal analizado (2,930 árboles) ha fijado con éxito **313.09 toneladas de CO2 equivalente**, representando un activo financiero inmediato de **$4,700 USD** (a un precio base de $15 USD/Ton).
* **Cuello de Botella Biológico:** El 84.13% de todo el CO2 capturado (263.3 toneladas) está concentrado en la clase diamétrica "Media" (10 - 15 cm de grosor).
* **Oportunidad Silvicultural:** Aunque la biomasa "Media" domina en volumen de árboles, el mayor valor económico unitario (más de $3,000 USD combinados) reside en la categoría de biomasa "Alta" (> 60 kg). Se recomienda ejecutar entresacas y raleos para liberar competencia y empujar el estrato medio hacia el estrato superior, maximizando el ROI del activo antes del turno de tala.

## 🛠️ Arquitectura y Tecnologías
El proyecto se divide en dos fases técnicas principales:

1. **Ingeniería de Datos (ETL) - Python:**
   * Limpieza de registros nulos y corrección de formatos regionales (decimales).
   * Feature Engineering aplicando metodologías y fórmulas alométricas del IPCC para *Pinus caribaea*:
     * *Volumen* a *Biomasa Aérea* (Densidad = 500 kg/m³, BEF = 1.3).
     * *Biomasa* a *Carbono Retenido* (Fracción de Carbono = 47%).
     * *Carbono* a *Dióxido de Carbono Equivalente (CO2eq)* (Factor = 3.67).
2. **Business Intelligence - Power BI:**
   * Modelado de datos e implementación de métricas DAX (Cálculo de ingresos, segmentación de estratos por altura y biomasa).
   * Diseño de interfaz UI/UX optimizada para lectura gerencial (Patrón Z).
