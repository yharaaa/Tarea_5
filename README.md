# [Tarea 5: Introducción a la Optimización](URL)


Este repositorio contiene .

## 1. **Parte 1: Maximización/Minimización**

### Descripción
Esta tarea resuelve un problema de optimización utilizando la librería **PuLP** para minimizar el costo total de suplementos nutricionales. El objetivo es determinar la cantidad mínima de dos suplementos, VegaVita y HappyHealth, necesarios para cumplir con los requisitos nutricionales establecidos.

### Conclusiones Parte 1: 
- Optimal Solution: 1.20 (costo mínimo total en dólares)
- HappyHealth: 2.0 (tabletitas de HappyHealth)
- VegaVita: 3.0 (tabletitas de VegaVita)

## 2. **Parte 2: Multicriteria Decision-Making**
En esta parte se realiza una comparación multicriterio para evaluar diferentes países en función de tres criterios: Costo de vida, Dificultad del idioma y Posibilidades de empleo. Los países a evaluar son Brasil, España, USA y Alemania.

### Conclusiones Parte 2: 
- COSTO DE VIDA tiene un peso global de 0.614.
- DIFICULTAD DEL IDIOMA tiene un peso global de 0.268.
- POSIBILIDAD DE EMPLEO tiene un peso global de 0.117.
⚠️ no se logró identificar el país optimo 😞

## 3. **Parte 3 Benchmarking: Análisis de Ejecución Presupuestal y Eficiencia en Municipalidades de San Martín, Perú**

Este proyecto analiza la ejecución presupuestal de las municipalidades del Departamento de San Martín, Perú, durante el año 2022. Utiliza indicadores clave como el [Presupuesto Inicial Asignado (PIA), el Presupuesto Modificado (PIM)](https://apps5.mineco.gob.pe/transparencia/Navegador/default.aspx?y=2022&ap=ActProy), [el avance de ejecución del presupuesto, ingresos y gastos](http://webinei.inei.gob.pe/anda_inei/index.php/catalog/779), y calcula la eficiencia de las municipalidades utilizando el modelo DEA (Análisis Envolvente de Datos).

## Descripción de los Datos

El archivo `data_muni.csv` contiene los siguientes campos clave:

- **idmunici**: Código de la municipalidad (identificador único).
- **PIA**: Presupuesto Inicial Asignado para el año 2022.
- **PIM**: Presupuesto Modificado asignado para el año 2022.
- **Avance**: Porcentaje de avance en la ejecución del presupuesto.
- **C96**: Ingreso total de la municipalidad durante el año 2022.
- **C97**: Gasto total de la municipalidad durante el año 2022.

***Área de trabajo:*** Este análisis se centra exclusivamente en las municipalidades del Departamento de San Martín, Perú.

## Resultados

- **Benchmarking y Análisis de Frontera**

*Municipalidad 221001: MUNICIPALIDAD PROVINCIAL DE TOCACHE*
Por cada unidad de gasto, genera 1.005 unidades de ingreso, lo que muestra un equilibrio entre ingresos y gastos.
Tiene un presupuesto inicial muy alto comparado con su avance de ejecución.

*Municipalidad 220901: MUNICIPALIDAD PROVINCIAL DE SAN MARTIN - TARAPOTO*
Por cada unidad de gasto, genera 1.24 unidades de ingreso, lo que indica que está generando más ingresos que gastos.
Su presupuesto inicial es más moderado en comparación con su ejecución.

*Municipalidad 220802 (primer registro): MUNICIPALIDAD DISTRITAL DE AWAJUN*
rate_IngresoPorGasto: 2.806, lo que indica que por cada unidad gastada, la municipalidad obtiene aproximadamente 2.8 unidades de ingreso. Esto sugiere que la municipalidad tiene una situación muy favorable en cuanto a generación de ingresos frente a sus gastos.
rate_PIAPorAvance: 144,447.85, lo que muestra que la municipalidad tiene un presupuesto inicial (PIA) muy alto en comparación con el avance de ejecución del presupuesto. Esto podría implicar que aún hay mucho presupuesto disponible sin ejecutar.

*Municipalidad 221004 (segundo registro): MUNICIPALIDAD DISTRITAL DE SHUNTE*
rate_IngresoPorGasto: 1.604, lo que indica que por cada unidad gastada, la municipalidad obtiene aproximadamente 1.6 unidades de ingreso. Aunque es menor que el primer municipio, sigue mostrando una relación positiva entre ingresos y gastos.
rate_PIAPorAvance: 19,549.22, lo que indica que tiene un presupuesto inicial moderado comparado con su avance de ejecución. Esto sugiere que la municipalidad está avanzando en el uso de su presupuesto.

- **Regresión Tobit**  

*Estadísticos del Modelo:*

- Pseudo R-squared: El valor de -3.460 es negativo, lo que es poco común en modelos de regresión, pero puede ocurrir con el modelo Tobit debido a la naturaleza de la censura en los datos. Este valor puede no ser el mejor indicador de la bondad de ajuste en este tipo de modelos.

- Log-Likelihood: El valor de 99.8 muestra la log-verosimilitud del modelo. Un valor más alto sugiere que el modelo está bien ajustado, aunque compararlo con el valor del LL-Null (22.4) también es importante. El LL-Ratio (154.8) y su p-valor de 0.000 sugieren que el modelo tiene un ajuste significativo y explica una parte considerable de la variabilidad en los datos.

- AIC y BIC: Ambos valores negativos (AIC: -195.6, BIC: -190.9) son indicadores de la calidad del modelo, con valores más bajos generalmente indicando un mejor ajuste.
