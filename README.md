<p align="center">
  <img src="06_Imagenes/sistema_fotovoltaico.png" width="70%">
</p>
<div align="center">


☀️ SISTEMA FOTOVOLTAICO AISLADO CON ALMACENAMIENTO

###  Diseño • Simulación • Almacenamiento • Análisis Energético

![Diseño](https://img.shields.io/badge/Energy-Design-blue?style=for-the-badge)
![Simulación](https://img.shields.io/badge/Simulation-PVsyst-success?style=for-the-badge)
![Almacenamiento](https://img.shields.io/badge/Energy-Storage-orange?style=for-the-badge)
![Análisis](https://img.shields.io/badge/Energy-Analysis-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

</div>



📌 Descripción

Proyecto de diseño y simulación de un sistema fotovoltaico aislado con almacenamiento energético, desarrollado mediante PVsyst V8.0.18.

El proyecto analiza la generación solar, demanda eléctrica, almacenamiento mediante baterías, pérdidas del sistema, energía excedente, energía faltante y desempeño energético.

El sistema fue modelado como una instalación fotovoltaica autónoma con almacenamiento, permitiendo evaluar su comportamiento energético durante un año completo. 


⚙️ Características principales

Parámetro	Valor
Tipo de sistema	Fotovoltaico aislado
Software	PVsyst V8.0.18
Potencia FV	1.16 kWp
Módulos FV	2 × 580 Wp
Configuración	1 string × 2 módulos en serie
Inclinación	20°
Azimut	0°
Demanda promedio	1.8 kWh/día
Batería modelada	6.1 kWh
Tensión de batería	50 V
Capacidad	134 Ah
Energía solar disponible	1656.36 kWh/año
Energía útil solar	654.94 kWh/año
Energía faltante	6.23 kWh/año
Energía excedente	961.46 kWh/año
Fracción solar	99.04 %
Performance Ratio	33.71 %


# 📸 Galería

### Tablero control con PLC y HMI instalados.
Tablero principal de control de procesos para una planta de tratamiento de aguas residuales que controla bombas y medidores de flujo, con PLC DELTA instalado automatizando todo el proceso.

<p align="center">
<img src="queretaro/tablero-control.jpeg" width="30%">

<img src="queretaro/interior-tablero.jpeg" width="30%">

</p>

☀️ Arreglo Fotovoltaico

El sistema está compuesto por 2 módulos fotovoltaicos de 580 Wp conectados en serie, obteniendo una potencia instalada de 1.16 kWp.

                 ☀️ RADIACIÓN SOLAR
                         │
                         ▼
                ┌─────────────────┐
                │    PV1 580 Wp   │
                └────────┬────────┘
                         │
                       SERIE
                         │
                ┌────────▼────────┐
                │    PV2 580 Wp   │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │  PROTECCIÓN DC  │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │      MPPT       │
                └────────┬────────┘
                         │
                  ┌──────┴──────┐
                  │             │
                  ▼             ▼
           ┌────────────┐ ┌────────────┐
           │  BATERÍA   │ │  INVERSOR  │
           │   6.1 kWh  │ │            │
           └─────┬──────┘ └──────┬─────┘
                 │               │
                 └───────┬───────┘
                         ▼
                 ┌──────────────┐
                 │   TABLERO AC │
                 └──────┬───────┘
                        │
                        ▼
                     🏠 CARGAS

Potencia instalada

580 Wp × 2 módulos = 1160 Wp
Potencia FV = 1.16 kWp



🔋 Sistema de Almacenamiento

El modelo original utiliza una batería de tecnología Lithium-ion NCA.

Características

Tensión nominal:      50 V
Capacidad:            134 Ah
Energía almacenada:   6.1 kWh
SOC mínimo:           10 %

La batería permite almacenar energía generada por el arreglo fotovoltaico y suministrarla posteriormente a las cargas.



🏠 Demanda Energética

El perfil de consumo utilizado en la simulación corresponde a cargas de tipo residencial.

Carga	Potencia	Uso
Lámparas	25 W	0.5 h/día
TV / PC / móvil	100 W	0.5 h/día
Electrodomésticos	250 W	0.5 h/día
Lavaplatos / lavadora	1200 W	Según perfil
Consumos en espera	—	Permanente

Consumo diario

Demanda promedio ≈ 1.8 kWh/día
Demanda configurada = 1812 Wh/día



🔌 Arquitectura del Sistema

                         ☀️
                  RADIACIÓN SOLAR
                         │
                         ▼
              ┌────────────────────┐
              │   ARRAY FV 1.16kWp │
              │    2 × 580 Wp      │
              └──────────┬─────────┘
                         │
                         ▼
              ┌────────────────────┐
              │ PROTECCIONES DC    │
              └──────────┬─────────┘
                         │
                         ▼
              ┌────────────────────┐
              │       MPPT         │
              └──────────┬─────────┘
                         │
              ┌──────────┴──────────┐
              │                     │
              ▼                     ▼
       ┌──────────────┐      ┌──────────────┐
       │    BATERÍA   │      │   INVERSOR   │
       │    6.1 kWh   │      │              │
       └──────┬───────┘      └──────┬───────┘
              │                     │
              │                     ▼
              │             ┌──────────────┐
              │             │ PROTECCIÓN AC│
              │             └──────┬───────┘
              │                    │
              └──────────┬─────────┘
                         ▼
                ┌─────────────────┐
                │   TABLERO AC    │
                └────────┬────────┘
                         │
                         ▼
                      🏠 CARGAS



📊 Resultados de la Simulación

Resultados anuales

Indicador	Resultado
Energía solar disponible	1656.36 kWh/año
Energía útil solar	654.94 kWh/año
Energía faltante	6.23 kWh/año
Energía excedente	961.46 kWh/año
Fracción solar	99.04 %
Performance Ratio	33.71 %



📈 Balance Energético

                    ENERGÍA SOLAR
                          │
                          ▼
                  1656.36 kWh/año
                          │
               ┌──────────┴──────────┐
               │                     │
               ▼                     ▼
        ENERGÍA ÚTIL              EXCEDENTE
        654.94 kWh                961.46 kWh
               │
               ▼
             CARGAS

El sistema presenta una fracción solar de 99.04 %, mientras que se registra una energía faltante anual de 6.23 kWh.

Una cantidad significativa de la energía disponible permanece sin utilizar debido principalmente a periodos en los que la batería alcanza su capacidad de almacenamiento.



📅 Comportamiento Mensual

Mes	Energía faltante
Enero	2.60 kWh
Febrero	0 kWh
Marzo	0 kWh
Abril	0 kWh
Mayo	0 kWh
Junio	0 kWh
Julio	0 kWh
Agosto	0 kWh
Septiembre	0 kWh
Octubre	0 kWh
Noviembre	0 kWh
Diciembre	3.63 kWh
TOTAL	6.23 kWh



📉 Análisis de Pérdidas

El análisis realizado mediante PVsyst permitió identificar las pérdidas presentes durante las diferentes etapas del sistema.

                IRRADIACIÓN SOLAR
                       │
                       ▼
             ┌──────────────────┐
             │ Irradiación      │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Pérdidas IAM     │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Conversión FV    │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Pérdidas térmicas│
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Cableado DC      │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Controlador MPPT │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Almacenamiento   │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Inversor         │
             └────────┬─────────┘
                      │
                      ▼
                    CARGAS

Principales pérdidas identificadas

* Pérdidas por nivel de irradiancia.
* Pérdidas por temperatura.
* Pérdidas por calidad de módulos.
* Pérdidas por mismatch.
* Pérdidas óhmicas del cableado.
* Pérdidas del convertidor.
* Pérdidas asociadas al almacenamiento.
* Energía no utilizada por batería completamente cargada.



🧰 Componentes

Nota: Los componentes siguientes corresponden a una propuesta comercial actual y no necesariamente a los equipos utilizados originalmente en la simulación.

☀️ Módulos Fotovoltaicos

JA Solar JAM72S30-580/LR

Potencia individual: 580 Wp
Cantidad: 2
Potencia total: 1.16 kWp

⚡ Controlador MPPT

Victron SmartSolar MPPT 150/45

Voltaje FV máximo: 150 V
Corriente máxima: 45 A
Potencia FV a 48 V: 2600 W
Eficiencia máxima: 98 %

🔋 Batería

Victron Lithium NG 51.2 V / 100 Ah

Tensión: 51.2 V
Capacidad: 100 Ah
Energía: 5.12 kWh

🔌 Inversor/Cargador

Victron MultiPlus-II 48/3000/35-32

Tensión DC: 38–66 V
Salida: 230 VAC
Potencia: 3000 VA
Potencia continua: 2400 W
Potencia pico: 5500 W



🛡️ Protecciones Eléctricas

El diseño conceptual considera:

* Seccionador DC
* Fusibles gPV
* Fusible de batería
* SPD DC Tipo 2
* SPD AC Tipo 2
* Interruptor termomagnético AC
* Puesta a tierra
* Tablero de distribución

La selección definitiva de protecciones debe realizarse considerando los valores reales de tensión, corriente, conductores y capacidad de interrupción.



💻 Software Utilizado

PVsyst V8.0.18

Utilizado para:

* Modelado del sistema fotovoltaico.
* Configuración del arreglo FV.
* Configuración de baterías.
* Definición de cargas.
* Simulación anual.
* Análisis de pérdidas.
* Evaluación energética.
* Análisis de fracción solar.
* Evaluación del desempeño del sistema.



📂 Estructura del Repositorio

📁 SISTEMA-FOTOVOLTAICO-AISLADO
│
├── 📄 README.md
│
├── 📁 01_Diagrama_Unifilar
│   └── 🖼️ diagrama_unifilar.png
│
├── 📁 02_PVsyst
│   └── 📄 Reporte_PVsyst.pdf
│
├── 📁 03_Memoria_Tecnica
│   └── 📄 Memoria_Tecnica.pdf
│
├── 📁 04_Calculos
│   ├── 📊 calculo_generacion.xlsx
│   ├── 📊 calculo_consumo.xlsx
│   └── 📊 calculo_bateria.xlsx
│
├── 📁 05_Fichas_Tecnicas
│   ├── 📄 Modulos_FV.pdf
│   ├── 📄 Controlador_MPPT.pdf
│   ├── 📄 Bateria.pdf
│   └── 📄 Inversor.pdf
│
└── 📁 06_Imagenes
    ├── 🖼️ pvsyst_01.png
    ├── 🖼️ pvsyst_02.png
    └── 🖼️ sistema_fotovoltaico.png

⸻

🎯 Objetivos del Proyecto

* Diseñar un sistema fotovoltaico aislado.
* Determinar la potencia fotovoltaica instalada.
* Caracterizar la demanda energética.
* Evaluar el almacenamiento energético.
* Simular el comportamiento anual mediante PVsyst.
* Analizar las pérdidas del sistema.
* Evaluar la fracción solar.
* Determinar energía excedente y faltante.
* Analizar el desempeño energético.
* Documentar técnicamente el proyecto.

⸻

🧠 Competencias Demostradas

⚡ Sistemas Energéticos

* Sistemas fotovoltaicos.
* Energías renovables.
* Generación eléctrica.
* Almacenamiento energético.
* Balance energético.
* Análisis de pérdidas.

💻 Simulación

* PVsyst.
* Modelado de sistemas FV.
* Simulación anual.
* Interpretación de resultados.
* Análisis de desempeño.

🔧 Ingeniería

* Dimensionamiento conceptual.
* Selección de componentes.
* Protecciones eléctricas.
* Diagramas unifilares.
* Análisis técnico.
* Documentación de proyectos.

⸻

📌 Verificaciones de Ingeniería

Para una implementación real deberán verificarse:

* Voc de los módulos conectados en serie.
* Corrección de Voc por temperatura.
* Isc real de los módulos.
* Capacidad de conductores.
* Caída de tensión.
* Selección de fusibles.
* Coordinación de protecciones.
* Selección de SPD.
* Capacidad de interrupción.
* Sistema de puesta a tierra.
* Compatibilidad entre MPPT, batería e inversor.
* Normativa eléctrica aplicable.

⸻

⚠️ Consideraciones Técnicas

El modelo original de PVsyst utiliza una batería de 6.1 kWh, mientras que la propuesta comercial considera una batería de 5.12 kWh. Por lo tanto, ambos sistemas no son exactamente equivalentes.

El modelo original también utiliza una salida de 230 V / 50 Hz, coherente con la ubicación utilizada en la simulación. Para una implementación en México sería necesario rediseñar y verificar la salida eléctrica conforme a las condiciones y normativa aplicables.

Este repositorio corresponde a un proyecto académico y de portafolio profesional. No sustituye un proyecto ejecutivo, memoria de cálculo certificada ni diseño eléctrico para una instalación real.

⸻

📚 Documentación del Proyecto

📄 Reporte original PVsyst
📄 Memoria técnica
📐 Diagrama unifilar
📊 Cálculos
📑 Fichas técnicas
🖼️ Capturas de simulación

⸻

👨‍💻 Autor

Oscar Arrieta Velasco

Ingeniería en Sistemas Energéticos y Redes Inteligentes

Instituto Politécnico Nacional — IPN

Áreas de interés

⚡ Sistemas Energéticos
☀️ Energías Renovables
🔋 Almacenamiento Energético
🤖 Automatización
💻 Simulación
📊 Análisis de Datos

⸻

<div align="center">

☀️ ENERGÍA RENOVABLE + INGENIERÍA + SIMULACIÓN

Diseño • Modelado • Análisis • Optimización

© 2026 Oscar Arrieta Velasco

</div>
