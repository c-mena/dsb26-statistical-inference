# Informe Técnico: Análisis Inferencial de Hábitos Universitarios

## Resumen Ejecutivo

El presente análisis evaluó los principales hábitos de vida de un cohorte universitario representativo ($n=150$). Mediante metodologías de inferencia y simulación de muestras, nos propusimos determinar si la población estudiantil cubre la necesidad básica de descanso (7 o más horas).

Los resultados estadísticos son concluyentes: con un altísimo nivel de rechazo (p-value < 0.05), el test _t de Student_ nos indica sistemáticamente que la población general de estudiantes duerme, en promedio, una cantidad inferior al umbral recomendado, confirmando formalmente nuestra Hipótesis Alternativa ($H_1$).

## Justificación Metodológica y Aplicación del Método Científico

- **Establecimiento del diseño empírico:** Partimos de una observación empírica sobre los elevados niveles de estrés y el supuesto cansancio crónico del estudiantado.
- **Generación representativa (Distribuciones):** Mediante funciones gaussianas generamos la variable continua de las horas de sueño (`sleep_hours`). Para otras incidencias más discretas, por ejemplo las comidas saludables en una semana (`healthy_meals_per_week`), nos decantamos de forma deliberada por la _Distribución de Poisson_, considerando que modela excelentemente la probabilidad de conteo de eventos independientes acotados a un margen de tiempo semanal.
- **Validación del Teorema del Límite Central:** Antes de inferir sobre la población general, aplicamos repetitivos remuestreos sobre el marco estocástico, confirmando que la media convergía a una distribución en forma de campana en base a la Media Poblacional Original, otorgándonos el peso científico suficiente para inferir a gran escala con muestras limitadas (pero $\ge 30$).

## Hallazgos e Interpretación Probabilística

1. **Intervalos de Confianza:** A través del uso estadístico, hemos fijado que, si aumentamos nuestro nivel de confianza al 99%, sacrificamos precisión al ensanchar el intervalo de horas estimadas (aumenta el margen de error). Para orientar las métricas internas de la universidad y tener balance asertivo, el intervalo construido al 95% arrojó un cimiento fuerte: la verdadera media poblacional recae sin dudas en un margen inferior a las 7 horas óptimas.
2. **Rechazos en Test de Significancia:** Se ejecutó inicialmente la $H_0$ de que "los universitarios duermen adecuadamente promedio $\ge 7$ horas". Al someter estos números al test _T de Student para una Muestra_, nuestra zona de rechazo castigó fuertemente el valor-p devolviéndolo en magnitudes microscópicas, permitiendo validar la hipótesis afirmativa de nuestra investigación en favor a replantear rutinas estudiantiles y la prevalencia de fatiga.

## Reflexiones Analíticas: Limitaciones del Estudio y Riesgos

- **Limites de la Simulación:** Para este desarrollo académico asumimos a través de semillas aleatorias (`np.random`) una distribución, sin embargo, en un ejercicio en el mundo material, variables de co-dependencia cruzada requerirían limpiezas extremas (sesgos de autorrespuesta de estudiantes en encuestas, encuestas abandonadas, etc.).
- **Errores Tipo I y II:** Si la Institución Universitaria invirtiera miles de recursos a partir de este estudio y accidentalmente hubiésemos incurrido en el _Error de Tipo I (Rechazar hipótesis nula verdadera)_, malgastaríamos fondos tratando un problema que biológicamente los estudiantes no cursaban. Para evitar tales desperdicios, hemos acudido a múltiples comparaciones matemáticas.

## Conclusiones y Recomendaciones

En el marco referencial del **Bootcamp**, queda expuesto que la inferencia estadística entrega un poderoso canal para transformar la intuición y conjetura en una base empírica irrebatible para la toma de decisiones.

**Recomendaciones derivadas a la Unidad Institucional:**

- Desplegar pausas modulares que inviten al estiramiento para compensar la fatiga del estudiantado (`weekly_exercise_hours`).
- Generar sondeos más masivos a futuro en donde se valide este estudio inicial contra datos empíricos de las planillas de enfermería en los campus.
- Formar programas de educación en higiene de sueño y optimización de las horas activas.
