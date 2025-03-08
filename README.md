# Detección de Anomalías en Créditos - Banco W

## Descripción del Proyecto
Este proyecto tiene como objetivo implementar un sistema de detección de anomalías en la cartera de microcréditos del Banco W. El sistema identifica comportamientos inusuales o potencialmente fraudulentos utilizando técnicas de analítica de datos, inteligencia artificial y machine learning. El enfoque principal es seleccionar una muestra de clientes de alto y bajo riesgo para auditoría, priorizando agencias y analistas con mayor perfil de riesgo.

El proyecto se enmarca en el contexto de auditoría interna del Banco W, donde se busca optimizar los procesos de revisión y mejorar la identificación de riesgos crediticios.

---

## Estructura del Repositorio

```
deteccion-anomalias-creditos/
├── data/                         # Carpeta para almacenar los datos
│   ├── historico_hallazgos.csv   # Datos históricos de hallazgos de auditoría
│   ├── colocacion_octubre_2024.csv # Datos de colocación de octubre 2024
│   └── README_data.md            # Descripción de los datos y su estructura
├── notebooks/                    # Jupyter Notebooks para análisis y modelado
│   ├── 01_analisis_exploratorio.ipynb
│   ├── 02_deteccion_anomalias.ipynb
│   └── 03_seleccion_muestras.ipynb
├── src/                          # Código fuente en Python
│   ├── data_preprocessing.py     # Script para preprocesamiento de datos
│   ├── anomaly_detection.py      # Script para detección de anomalías
│   └── risk_scoring.py           # Script para calificación de riesgo
├── results/                      # Resultados del análisis
│   ├── graficos/                 # Gráficos generados
│   └── muestras_seleccionadas/   # Muestras de clientes seleccionados
├── docs/                         # Documentación adicional
│   ├── contexto_proyecto.md      # Contexto del proyecto
│   └── metodologia.md            # Detalles de la metodología utilizada
├── requirements.txt              # Dependencias del proyecto
└── README.md                     # Este archivo
```

---

## Instalación y Uso

### Requisitos Previos
- Python 3.8 o superior.
- Librerías listadas en `requirements.txt`.

### Instalación
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/deteccion-anomalias-creditos.git
   cd deteccion-anomalias-creditos
   ```
2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

### Ejecución
1. **Preprocesamiento de datos**:
   Ejecuta el script de preprocesamiento para limpiar y preparar los datos:
   ```bash
   python src/data_preprocessing.py
   ```
2. **Detección de anomalías**:
   Utiliza el script de detección de anomalías para identificar comportamientos inusuales:
   ```bash
   python src/anomaly_detection.py
   ```
3. **Generación de muestras**:
   Ejecuta el script de calificación de riesgo para seleccionar las muestras de clientes:
   ```bash
   python src/risk_scoring.py
   ```

---

## Metodología

### 1. Análisis Exploratorio de Datos (EDA)
- Se realizó un análisis exploratorio para entender la distribución de los datos, identificar valores atípicos y correlaciones entre variables.
- Se aplicó el análisis de cajas y bigotes para calificar atributos de riesgo.

### 2. Detección de Anomalías
- Se utilizaron técnicas como:
  - **Ley de Benford**: Para identificar irregularidades en los dígitos de los montos de crédito.
  - **Modelos no supervisados**: Como Isolation Forest o DBSCAN, para detectar patrones inusuales.
  - **Reglas de negocio**: Como abonos de capital en el mismo mes del desembolso.

### 3. Calificación de Riesgo
- Se asignaron puntuaciones de riesgo a los clientes basadas en:
  - Datos atípicos y del cuarto cuartil.
  - Resultados de la detección de anomalías.
  - Segmentos de riesgo (por ejemplo, clientes jóvenes).

### 4. Selección de Muestras
- **Coming soon**

---

## Resultados
Los resultados del análisis se encuentran en la carpeta `results/`, incluyendo:
- Gráficos de distribución de riesgos.
- Listado de clientes seleccionados para auditoría.
- Identificación de las agencias con mayor riesgo.

---

## Contribuciones
Si deseas contribuir a este proyecto, por favor sigue estos pasos:
1. Haz un fork del repositorio.
2. Crea una rama para tu contribución (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -m 'Añade nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request.

---

## Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

---

## Contacto
Si tienes alguna pregunta o sugerencia, no dudes en contactarnos:
- **Nombre**: Jhonattan Reales, Josué cobaleda, Mateo Silva, Farid Sandoval
- **Email**: mateosilva1901@gmail.com, fcss11226@gmail.com, jhonatanreales21@gmail.com, **coming soon**...
- **LinkedIn**: Mateo Silva Lasso, Farid Camilo Sandoval Sarria **coming soon**...
