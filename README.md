#  Trabajo doméstico y de cuidados no remunerado — perspectiva de género

**Universidad de Guanajuato | Programación en R | Maria Concepcepcion Cadena Sanchez**

---

##  Sobre este proyecto

El trabajo doméstico y de cuidados no remunerado ha sido históricamente
atribuido a las mujeres. Como señala Federici (2013), este trabajo no solo
se ha impuesto a las mujeres, sino que se ha adjudicado a su "naturaleza",
invisibilizándolo y excluyéndolo del reconocimiento económico y social.

Este proyecto busca analizar, a través de datos propios, cómo el trabajo
doméstico y de cuidados impacta en el bienestar de quienes lo realizan,
con especial atención a las desigualdades de género. Para ello se aplicó
una encuesta anónima (n = 42) y se utilizaron técnicas de análisis
estadístico en R.

---

## Objetivo

Busca identificar qué condiciones — género, maternidad o paternidad, empleo
remunerado y escolaridad — aumentan la probabilidad de experimentar una
alta carga subjetiva de trabajo doméstico y de cuidados no remunerado,
medida a través del impacto en el bienestar y el nivel de estrés reportados.

---

## Datos

- **Fuente:** encuesta propia de levantamiento, aplicada de forma anónima realizada para mi evaluacion intermedia
  
- **Tamaño de muestra:** 42 personas
- **Tipo de muestra:** no probabilística
- #Formulario digital con preguntas sobre tiempo dedicado
  al trabajo doméstico, nivel de estrés, impacto en el bienestar y
  frecuencia con que estas tareas impiden otras actividades

---

##  Metodología

Se utilizó un modelo de **regresión logística binaria (logit)**, el mismo
aplicado en clase con la base de identidad política. Este modelo permite
estimar la probabilidad de que ocurra un resultado dicotómico (0/1) a
partir de un conjunto de variables independientes.

**Variable dependiente**
- `resultado` = alta carga subjetiva
  - 1 si impacto en bienestar ≥ 7 **o** estrés ≥ 7 (escala 0-10)
  - 0 en cualquier otro caso

**Variables independientes**

| Variable | Descripción |
|---|---|
| `G` | Género femenino (1 = femenino, 0 = otro) |
| `H` | Tiene hijes (1 = sí, 0 = no) |
| `T` | Trabaja fuera de casa (1 = sí, 0 = no) |
| `E` | Estudia actualmente (1 = sí, 0 = no) |

La elección del outcome responde a una perspectiva de género feminista
que no reduce el análisis a las horas dedicadas, sino al impacto vivido
en el bienestar de las personas.

---

##  Gráficas

### 1. Probabilidad predicha de alta carga por género
Esta gráfica muestra la probabilidad de experimentar una alta carga de
trabajo doméstico y de cuidados según el género, si la persona estudia
y si tiene hijes. Las barras rosas representan a mujeres y las azules
a hombres. Se observa que las mujeres tienen una probabilidad más alta
en todos los escenarios, lo que evidencia la desigualdad de género en
la distribución del trabajo doméstico.

![Gráfica 1](https://github.com/Coni-CadenaSan/Evaluacion-final-ProgrmacionR/blob/main/Trabajo%20domestico.jpeg?raw=true)

---

### 2. Efecto de cada variable sobre la probabilidad de alta carga
Esta gráfica presenta los coeficientes del modelo logit para cada
variable independiente. Las barras rosas indican que la variable
aumenta la probabilidad de alta carga; las azules que la reduce.
Las barras de error muestran la incertidumbre de cada estimación.
Permite identificar qué factores tienen mayor peso en la experiencia
de sobrecarga doméstica.

![Gráfica 2](https://github.com/Coni-CadenaSan/Evaluacion-final-ProgrmacionR/blob/main/Trabajo%20domestico%202.jpeg?raw=true)

---

### 3. Distribución del nivel de estrés por género
El boxplot compara cómo se distribuye el nivel de estrés generado por
el trabajo doméstico y de cuidados entre hombres y mujeres. La línea
central de cada caja representa la mediana; la altura de la caja
muestra la dispersión de las respuestas. Una caja más alta y ubicada
hacia valores mayores indica mayor nivel de estrés reportado.

![Gráfica 3](https://github.com/Coni-CadenaSan/Evaluacion-final-ProgrmacionR/blob/main/Trabajo%20domestico%203.jpeg?raw=true)

---

### 4. Frecuencia con que el trabajo doméstico impide otras actividades
Las barras apiladas muestran, en porcentaje, con qué frecuencia el
trabajo doméstico y de cuidados impide realizar otras actividades
importantes como estudiar, trabajar, descansar o convivir, comparando
hombres y mujeres. Los colores van del verde (nunca) al rojo oscuro
(siempre), permitiendo ver qué grupo reporta mayor restricción en su
vida cotidiana.

![Gráfica 4](https://github.com/Coni-CadenaSan/Evaluacion-final-ProgrmacionR/blob/main/trabajo%20domestico%204.jpeg?raw=true)
---
Este trabajo fue mejorado en formato con apoyo de IA Claude de Antrophic y DeepSeek, las cuales fueron herramientas para poder realizar esta publicación de manera más estetica y profesional, sin embargo no fue utilizada para el análisis y el plantamiento del tema del problema o tema, el cual surge de un interes personal de la alumna.

```r
