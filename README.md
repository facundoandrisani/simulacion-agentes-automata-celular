# Modelado Basado en Agentes (ABM): Segregación de Schelling, Modelo de Ising y MCMC

Este repositorio contiene la implementación computacional, el análisis teórico y las visualizaciones estocásticas correspondientes al **Trabajo Práctico de Simulación y Procesos Estocásticos** de la Licenciatura en Ciencias de Datos (Pontificia Universidad Católica Argentina - UCA, Rosario).

---

## Descripción del Proyecto

El **Modelado Basado en Agentes (ABM)** desplaza el análisis desde ecuaciones macroscópicas agregadas hacia la definición de reglas de comportamiento microscópicas a nivel individual. En este proyecto se explora cómo reglas locales simples generan patrones globales complejos (**comportamiento emergente**).

### Ejes de Investigación
1. **Dinámicas de Interacción Local (Schelling 50x50):** Comparación cuantitativa entre la búsqueda de la minoría (Dinámica 1, insatisfacción frustrada) y la búsqueda de la mayoría (Dinámica 2, segregación espacial).
2. **Análisis del Estado Frustrado:** Demostración formal de la pérdida de ergodicidad en Cadenas de Markov y su extrapolación a problemas socioeconómicos reales (Teorema de la Telaraña en mercados agropecuarios y ruteo dinámico de tráfico urbano).
3. **Dinámicas de Consenso (Modelo de Ising 2D):** Identificación de la transición de fase de segundo orden en la temperatura crítica de Onsager ($T_c \approx 2.269$) y visualización espacial de los 3 regímenes (Orden/Conformismo, Borde del Caos/Fractal, Anomia/Caos).
4. **Optimización Estocástica (MCMC & Simulated Annealing):** Restauración de la ergodicidad del sistema mediante el algoritmo de Metropolis-Hastings para alcanzar el mínimo global de descontento, incluyendo una **optimización topológica $\mathcal{O}(1)$** que reduce la complejidad temporal por iteración de $\mathcal{O}(N)$ a tiempo constante.

---

## Resumen de Resultados

| Modelo | Regla / Heurística | Descontento Inicial ($\rho_0$) | Descontento Final ($\rho^*$) | Estado Final |
| :--- | :--- | :---: | :---: | :--- |
| **Schelling Dinámica 1** | Minoría *greedy* | $64.36\%$ | $15.80\%$ | **Frustrado** (Mínimo Local) |
| **Schelling Dinámica 2** | Mayoría *greedy* | $35.64\%$ | $0.64\%$ | **Segregado** (Equilibrio) |
| **Ising $T = 1.5$** | Metrópolis ($T < T_c$) | — | — | **Fase Ordenada** (Polarización) |
| **Ising $T \approx 2.269$** | Metrópolis ($T = T_c$) | — | — | **Fase Crítica** (Borde del Caos) |
| **Ising $T = 4.0$** | Metrópolis ($T > T_c$) | — | — | **Fase Desordenada** (Anomia) |
| **Schelling MCMC** | Metrópolis + Annealing | $64.36\%$ | **$10.24\%$** | **Mínimo Global** (Ergódico) |

---

## Estructura del Repositorio

```text
├── automata-celular-mcmc.ipynb   # Notebook con todo el código ejecutable y análisis
├── docs/                                  # Informe formal en formato PDF (opcional)
├── requirements.txt                       # Dependencias del proyecto
├── .gitignore                             # Archivos ignorados por Git
└── README.md                              # Documentación del proyecto
```


## Integrantes del Equipo
* **Andrisani, Facundo**
* **Feser, Ignacio**
* **Lauria, Francisco**
* **Viccei, Tomás**

*Licenciatura en Ciencias de Datos — Pontificia Universidad Católica Argentina (UCA Rosario)*
