📊 **Dashboard de Valoración Económica de Cambios de Cobertura - Río Orteguaza**                                                      
<img width="108" height="50" alt="image" src="https://github.com/user-attachments/assets/06393ce0-b276-4e85-8aca-bdb73f99d4ec" />
                                                       


Dashboard interactivo que visualiza los cambios de cobertura terrestre en la cuenca del Río Orteguaza, basado en datos de MapBiomas Colombia (2010-2020).

🔗 Enlaces Directos
🌐 Dashboard Visualizable: https://mauroalejandro220779.github.io/Rio-Orteguaza/dashboard_orte_tabs.html

💻 Código Fuente: https://github.com/Mauroalejandro220779/Rio-Orteguaza

🛠️ Tecnologías Utilizadas
* R (Lenguaje de programación estadística)
* flexdashboard (Framework para dashboards interactivos)
* RMarkdown (Documentos reproducibles)
* ggplot2 (Visualizaciones estáticas)
* plotly (Gráficos interactivos)
* dplyr (Manipulación de datos)

📁 Archivos Principales

- `1_procesamiento.R` - Filtrado y cálculo de cambios de cobertura
- `2_dashboard_orte_tabs.Rmd` - Código del dashboard  
- `2_dashboard_orte_tabs.html` - Dashboard compilado
- `diccionario_clases.csv` - Categorías de cobertura
- `cambios_orteguaza.csv` - Resultados de análisis

🔄 Flujo de Trabajo Reproducible

## Ejecutar el script de procesamiento

**Paso 1: Procesamiento de Datos**

source("Preparacion Datos Orteguaza.R")
Este script:

* Descarga datos de MapBiomas Colombia
* Filtra por la cuenca del Río Orteguaza
* Calcula cambios de cobertura 2010-2023
* Genera el archivo cambios_orteguaza.csv

**Paso 2: Generación del Dashboard**

Compilar el dashboard
rmarkdown::render("dashboard_orte_tabs.Rmd")



📊 Métricas Analizadas - Transición 2010 - 2020

* Transformaciones Bosque a Agricultura
* Agua a Agricultura
* Vegetación Natural a Agricultura
* Bosque a Área sin vegetación
* Bosque a Minería.
* Cálculo de pérdida económica por servicios modelados mediante InVest (Captura de Carbono y Retención de Sedimentos)

⚙️ Instalación y Uso Local
Prerrequisitos

install.packages(c("flexdashboard", "rmarkdown", "ggplot2", 
                   "plotly", "dplyr", "readxl", "tidyr"))

## Ejecución completa
**Clonar repositorio**

git clone https://github.com/Mauroalejandro220779/Rio-Orteguaza.git

**Ejecutar en R**

source("Preparacion Datos Orteguaza.R")
rmarkdown::render("dashboard_orte_tabs.Rmd")

🔍 Datos Fuente

Los datos originales fueron obtenidos de:

MapBiomas Colombia: https://mapbiomas.org/
Colección 2.0 - Transiciones por cuencas hidrográficas
Período: 2010-2020

📋 Notas Metodológicas

Filtrado por columna unidad-hidrografica = "Río Orteguaza"
Clasificación basada en diccionario_clases.csv
Métricas en hectáreas (ha)
Procesamiento realizado en R 4.3.1

🤝 Contribuciones
Las contribuciones son bienvenidas. Para cambios importantes:

1. Fork el proyecto
2. Crea una rama para tu feature (git checkout -b feature/NuevaFeature)
3. Commit tus cambios (git commit -m 'Add NuevaFeature')
4. Push a la rama (git push origin feature/NuevaFeature)
5. Abre un Pull Request

📝 Licencia
Este proyecto está bajo la Licencia MIT. Ver el archivo LICENSE para más detalles.

👥 Autor
Mauro A. Reyes Bonilla - https://github.com/Mauroalejandro220779

Contacto: mauro.reyes@socrates.org

🔄 Actualización
Para actualizar el dashboard:

Modificar los scripts de procesamiento o dashboard
Ejecutar Preparacion Datos Orteguaza.R y luego dashboard_orte_tabs.Rmd
Subir los cambios al repositorio
GitHub Pages se actualiza automáticamente

