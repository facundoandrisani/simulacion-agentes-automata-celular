# Modelado Basado en Agentes (ABM): SegregaciÃ³n de Schelling, Modelo de Ising y MCMC

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![UCA](https://img.shields.io/badge/Universidad-UCA-red.svg)](https://uca.edu.ar/)

Este repositorio contiene la implementaciÃ³n computacional, el anÃ¡lisis teÃ³rico y las visualizaciones estocÃ¡sticas correspondientes al **Trabajo PrÃ¡ctico N.Âº 3 de SimulaciÃ³n y Procesos EstocÃ¡sticos** de la Licenciatura en Ciencias de Datos (Pontificia Universidad CatÃ³lica Argentina - UCA, Rosario).

---

## ðŸ“Œ DescripciÃ³n del Proyecto

El **Modelado Basado en Agentes (ABM)** desplaza el anÃ¡lisis desde ecuaciones macroscÃ³picas agregadas hacia la definiciÃ³n de reglas de comportamiento microscÃ³picas a nivel individual. En este proyecto se explora cÃ³mo reglas locales simples generan patrones globales complejos (**comportamiento emergente**).

### Ejes de InvestigaciÃ³n
1. **DinÃ¡micas de InteracciÃ³n Local (Schelling 50x50):** ComparaciÃ³n cuantitativa entre la bÃºsqueda de la minorÃ­a (DinÃ¡mica 1, insatisfacciÃ³n frustrada) y la bÃºsqueda de la mayorÃ­a (DinÃ¡mica 2, segregaciÃ³n espacial).
2. **AnÃ¡lisis del Estado Frustrado:** DemostraciÃ³n formal de la pÃ©rdida de ergodicidad en Cadenas de Markov y su extrapolaciÃ³n a problemas socioeconÃ³micos reales (Teorema de la TelaraÃ±a en mercados agropecuarios y ruteo dinÃ¡mico de trÃ¡fico urbano).
3. **DinÃ¡micas de Consenso (Modelo de Ising 2D):** IdentificaciÃ³n de la transiciÃ³n de fase de segundo orden en la temperatura crÃ­tica de Onsager ($T_c \approx 2.269$) y visualizaciÃ³n espacial de los 3 regÃ­menes (Orden/Conformismo, Borde del Caos/Fractal, Anomia/Caos).
4. **OptimizaciÃ³n EstocÃ¡stica (MCMC & Simulated Annealing):** RestauraciÃ³n de la ergodicidad del sistema mediante el algoritmo de Metropolis-Hastings para alcanzar el mÃ­nimo global de descontento, incluyendo una **optimizaciÃ³n topolÃ³gica $\mathcal{O}(1)$** que reduce la complejidad temporal por iteraciÃ³n de $\mathcal{O}(N)$ a tiempo constante.

---

## ðŸ“Š Resumen de Resultados

| Modelo | Regla / HeurÃ­stica | Descontento Inicial ($\rho_0$) | Descontento Final ($\rho^*$) | Estado Final |
| :--- | :--- | :---: | :---: | :--- |
| **Schelling DinÃ¡mica 1** | MinorÃ­a *greedy* | .36\%$ | .80\%$ | **Frustrado** (MÃ­nimo Local) |
| **Schelling DinÃ¡mica 2** | MayorÃ­a *greedy* | .64\%$ | .64\%$ | **Segregado** (Equilibrio) |
| **Ising $T = 1.5$** | MetrÃ³polis ($T < T_c$) | â€” | â€” | **Fase Ordenada** (PolarizaciÃ³n) |
| **Ising $T \approx 2.269$** | MetrÃ³polis ($T = T_c$) | â€” | â€” | **Fase CrÃ­tica** (Borde del Caos) |
| **Ising $T = 4.0$** | MetrÃ³polis ($T > T_c$) | â€” | â€” | **Fase Desordenada** (Anomia) |
| **Schelling MCMC** | MetrÃ³polis + Annealing | .36\%$ | **.24\%$** | **MÃ­nimo Global** (ErgÃ³dico) |

---

## ðŸ“ Estructura del Repositorio

`	ext
â”œâ”€â”€ Trabajo_Practico_N3_Simulacion.ipynb   # Notebook con todo el cÃ³digo ejecutable y anÃ¡lisis
â”œâ”€â”€ docs/                                  # Informe formal en formato PDF (opcional)
â”œâ”€â”€ requirements.txt                       # Dependencias del proyecto
â”œâ”€â”€ .gitignore                             # Archivos ignorados por Git
â””â”€â”€ README.md                              # DocumentaciÃ³n del proyecto
`

---

## ðŸš€ InstalaciÃ³n y EjecuciÃ³n

### Prerrequisitos
Tener instalado Python 3.8+ y Jupyter Notebook o JupyterLab.

### 1. Clonar el Repositorio
`ash
git clone https://github.com/TU_USUARIO/abm-schelling-ising-mcmc.git
cd abm-schelling-ising-mcmc
`

### 2. Instalar Dependencias
`ash
pip install -r requirements.txt
`

### 3. Abrir y Ejecutar el Notebook
`ash
jupyter notebook Trabajo_Practico_N3_Simulacion.ipynb
`

---

## ðŸ‘¨â€ðŸ’» Integrantes del Equipo
* **Andrisani, Facundo**
* **Feser, Ignacio**
* **Lauria, Francisco**
* **Viccei, TomÃ¡s**

*Licenciatura en Ciencias de Datos â€” Pontificia Universidad CatÃ³lica Argentina (UCA Rosario)*