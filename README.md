# Evaluation of the process for submitting official hydrocarbon reports

We received a lot of complaints about the constant delays in submitting official reports. This situation was affecting timely decision-making by the Board of Directors.

My goal was to evaluate the process, identify the root causes, quantify their impact and propose solutions to optimize the operational efficiency.

I designed a simple database in Microsoft Excel to record the events, dates, and times related to the process. Additionally, I used Power Query for data wrangling, cleaning, transformation and automation. Finally, using pivot table, I created the visualizations to explain the results. 

The analysis revealed that 84% of reports were sent late. Furthermore, five main activities in the process were linked to these delays. These findings gave the Board of Directors the root causes necessary to focus on improvements. After just one week, the improvements were implemented, and punctuality reached 95%.


# Evaluación del proceso de emisión de reportes oficiales de hidrocarburos

### Este proyecto busca identificar, analizar y comprender las causas detrás de los retrasos en la emisión de informes oficiales de hidrocarburos para ser mostrados a la dirección ejecutiva de la empresa y, potencialmente, mejorar el proceso.

![Proceso Contable](https://github.com/user-attachments/assets/0c591548-708d-4ef5-b8a2-0f6941c6a66b)

### 1. Revisión de base de datos

EL archivo ControlCartillasyProceso.xls consta de 220 días de registros donde se incluyen las actividades por hora generadas en el proceso del departamento para un total de 2698 filas y 3 columnas principales (control de cartillas, control de envió de informes y fallas en proceso). Todas estas columnas muestran registros de procesos dependientes de otros departamentos como producción, operaciones ATC y automatización AIT, adicional a procesos inherentes al departamento de contabilidad de hidrocarburos, todos son indispensables para el cumplimiento de las actividades del departamento mencionado.

Fue necesario agregar una tabla de validación para resaltar los días que no fueron entregadas algunas cartillas sin notificación, tales como Santa Rosa Planta, El Toco, Aguasay y Mata R; para posteriormente hacer su registro en la BD y recuento en las próximas etapas del análisis.

### 2. Transformación

Se generó un archivo llamado Proceso_Contable.xlsx, el cual utilizaría como data origen el archivo ControlCartillasyProceso.xls y mediante Power Query donde se realizaron transformaciones a la BD Original para ajustarlo al requerimiento de campos necesarios para el análisis, resultando en una tabla llamada HojaBase_Continua. Entre los campos agregados se tiene: Categorización de cada evento por departamento, agrupamiento de Horas y nombres del día.

### 3. Análisis

Mediante uso de tablas dinámicas se segmentaron diferentes eventos con diferentes responsables inherentes al proceso. (Archivo: Proceso_Contable.xlsx)

En la hoja Total_Eventos podemos encontrar tablas como:
- Tabla 2. Filtra los días donde los reportes fueron enviados fuera del horario requerido (posterior a las 02:00 p.m.)
- Tabla 6. Muestra la cantidad de eventos que causan retraso en el envío de reportes filtrados por día de la semana y grupo de horas. 

En la hoja Dpto_ATC podemos encontrar tablas como:
- Tabla 1. Cuenta todos los eventos inherentes a este departamento que influyeron en el retraso de la emisión de reportes oficiales. Filtrados desde la 1:30 p.m. ya que es considerada la hora desde la cual los eventos afectan el envío de reportes. 

### 4. Visualización

La hoja Resumen (Archivo: Proceso_Contable.xlsx) cuenta con todas las visualizaciones mostradas en el Reporte Final (Evaluación del proceso de emisión de reportes oficiales de hidrocarburos).
