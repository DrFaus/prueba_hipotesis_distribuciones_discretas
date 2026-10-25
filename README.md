# Práctica interactiva de pruebas de hipótesis con distribuciones discretas

Aplicación web educativa para practicar **pruebas de hipótesis exactas con distribuciones binomial, hipergeométrica y de Poisson**, desarrollada como material de apoyo para estudiantes de **Gestión Empresarial**.

La herramienta está orientada a situaciones prácticas donde el estudiante debe identificar el modelo probabilístico adecuado, calcular el **valor-p exacto** y tomar una decisión estadística en el contexto del problema.

El objetivo no es únicamente sustituir valores en una fórmula, sino comprender cómo una distribución discreta puede utilizarse para evaluar evidencia contra una hipótesis nula.

---

## Características principales

- Banco de **150 casos prácticos**.
- **50 problemas binomiales**.
- **50 problemas hipergeométricos**.
- **50 problemas de Poisson**.
- **5 problemas aleatorios por intento**.
- Cada intento incluye siempre las tres distribuciones.
- Selección balanceada mediante esquemas **2–2–1**.
- **75 casos conducen a rechazar $H_0$** y 75 a no rechazarla.
- Casos contextualizados principalmente en **Gestión Empresarial**.
- Respuestas directas.
- Sin opción múltiple para el valor-p.
- **Modo estudio** con retroalimentación inmediata.
- Representación gráfica de la distribución y del área asociada al valor-p.
- Repaso únicamente de errores.
- Generación de reporte imprimible y exportable como PDF.
- Funciona completamente **offline**.
- Todo el proyecto está contenido en **un único archivo HTML**.
- No utiliza librerías externas.

---

# Objetivos de aprendizaje

La práctica busca que el estudiante sea capaz de:

1. Identificar si un problema corresponde a una distribución binomial, hipergeométrica o de Poisson.
2. Formular e interpretar $H_0$ y $H_1$.
3. Determinar la dirección de la prueba.
4. Calcular un valor-p exacto.
5. Comparar el valor-p con el nivel de significancia $\alpha$.
6. Decidir si se rechaza o no se rechaza $H_0$.
7. Interpretar la conclusión dentro del contexto empresarial.

---

# Estructura de cada problema

Cada reactivo evalúa tres componentes:

### 1. Identificación de la distribución

El estudiante debe seleccionar entre:

- Binomial.
- Hipergeométrica.
- Poisson.

### 2. Cálculo del valor-p

El estudiante debe calcular el **valor-p exacto** correspondiente a la hipótesis alternativa.

Se recomienda expresarlo con **cuatro decimales**.

### 3. Decisión

El estudiante debe decidir entre:

- Rechazar $H_0$.
- No rechazar $H_0$.

utilizando la comparación:

$$
p\text{-valor}<\alpha
$$

para rechazar la hipótesis nula.

---

# 1. Prueba exacta binomial

La distribución binomial se utiliza cuando:

- se realiza un número fijo de ensayos;
- cada ensayo tiene dos resultados de interés;
- la probabilidad bajo $H_0$ permanece constante;
- los ensayos pueden considerarse independientes.

Si:

$$
X\sim Bin(n,p_0),
$$

entonces:

$$
P(X=k)=
\binom{n}{k}
p_0^k
(1-p_0)^{n-k}.
$$

---

## Prueba de cola derecha

Por ejemplo:

$$
H_0:p=p_0
$$

$$
H_1:p>p_0
$$

El valor-p se calcula como:

$$
P(X\geq k_{\text{obs}}).
$$

---

## Prueba de cola izquierda

Si:

$$
H_1:p<p_0,
$$

el valor-p corresponde a:

$$
P(X\leq k_{\text{obs}}).
$$

---

## Contextos binomiales incluidos

Los problemas incluyen situaciones como:

- prueba del sorbo;
- preferencia de productos;
- conversión de campañas;
- recompra;
- renovación de membresías;
- abandono de carrito;
- entregas a tiempo;
- devoluciones;
- aceptación de propuestas;
- recomendación de servicios.

---

# Prueba del sorbo

Algunos reactivos utilizan situaciones inspiradas en la clásica **prueba del sorbo**.

Por ejemplo, una persona debe distinguir entre dos productos en varias pruebas independientes.

Si una persona no puede distinguir realmente los productos y existen dos posibilidades igualmente probables:

$$
H_0:p=0.50.
$$

Si el participante obtiene un número elevado de aciertos, puede evaluarse:

$$
H_1:p>0.50.
$$

El valor-p corresponde a la probabilidad, bajo $H_0$, de obtener tantos aciertos como los observados o más.

---

# 2. Prueba exacta hipergeométrica

La distribución hipergeométrica se utiliza cuando existe una población finita y la selección se realiza **sin reemplazo**.

También resulta especialmente útil cuando se condiciona a totales fijos para estudiar asociaciones entre grupos y decisiones.

La función de probabilidad es:

$$
P(X=k)=
\frac{
\binom{K}{k}
\binom{N-K}{n-k}
}{
\binom{N}{n}
}.
$$

donde:

- $N$ = tamaño total de la población;
- $K$ = número de elementos pertenecientes al grupo de interés;
- $n$ = número total de elementos seleccionados;
- $k$ = número observado del grupo de interés dentro de la selección.

---

# Aplicaciones de discriminación y preferencia

Una parte importante del banco hipergeométrico está orientada a situaciones de:

- posible discriminación;
- preferencias;
- asignaciones aparentemente sesgadas;
- selección de empleados;
- aprobación de candidatos;
- asignación de bonos;
- selección de proveedores;
- inversión entre sucursales;
- rechazo de solicitudes;
- asignación de prospectos.

La lógica consiste en preguntar:

> Si la selección fuera neutral, ¿qué tan probable sería observar una representación tan extrema como la obtenida?

---

## Ejemplo conceptual

Supongamos que una organización tiene:

- $N$ empleados;
- $K$ pertenecen al grupo A;
- se seleccionan exactamente $n$ empleados;
- sólo $k$ pertenecen al grupo A.

Si se investiga si el grupo A está siendo desfavorecido:

$$
H_0:\text{la selección es neutral respecto al grupo}
$$

$$
H_1:\text{el grupo A aparece menos de lo esperable bajo neutralidad}
$$

Entonces el valor-p se obtiene con la cola izquierda:

$$
P(X\leq k).
$$

---

## Preferencia a favor de un grupo

Si se investiga si un grupo aparece más veces de lo esperable:

$$
H_1:\text{representación mayor bajo la selección observada},
$$

se utiliza:

$$
P(X\geq k).
$$

---

# Interpretación importante

Una diferencia llamativa entre esta prueba y una comparación convencional de proporciones es que en la prueba hipergeométrica se **condiciona a los totales observados**.

Esto permite preguntar si la composición obtenida resulta extraordinaria dadas:

- la cantidad total de elementos;
- el tamaño del grupo;
- el número total seleccionado.

---

# 3. Prueba exacta de Poisson

La distribución de Poisson se utiliza para estudiar conteos de eventos dentro de un intervalo.

Si:

$$
X\sim Pois(\lambda_0),
$$

entonces:

$$
P(X=k)=
\frac{
e^{-\lambda_0}\lambda_0^k
}{
k!
}.
$$

---

# Detección de conteos atípicos

En este banco, los problemas de Poisson están orientados principalmente a determinar si **un único conteo observado resulta extraordinariamente alto o bajo** respecto a una tasa histórica.

Por ejemplo:

- quejas recibidas en un día;
- devoluciones por hora;
- cancelaciones;
- fallas de pago;
- llamadas recibidas;
- pedidos por minuto;
- reclamaciones;
- errores de captura;
- incidencias de inventario.

---

## Conteo atípicamente alto

Si históricamente:

$$
H_0:\lambda=\lambda_0
$$

y se desea detectar un incremento:

$$
H_1:\lambda>\lambda_0,
$$

entonces:

$$
p\text{-valor}=P(X\geq k_{\text{obs}}).
$$

---

## Conteo atípicamente bajo

Si:

$$
H_1:\lambda<\lambda_0,
$$

entonces:

$$
p\text{-valor}=P(X\leq k_{\text{obs}}).
$$

---

# Nota sobre Poisson y la prueba t

En algunos contextos empresariales podrían existir varias observaciones, por ejemplo:

- quejas durante varios días;
- ventas durante varias semanas;
- pedidos durante varios intervalos;
- incidencias durante múltiples jornadas.

Cuando existen suficientes observaciones, podrían utilizarse otros procedimientos estadísticos dependiendo del diseño y de los supuestos.

Una prueba t, por ejemplo, puede ser apropiada en determinados problemas de comparación de medias.

Sin embargo, **una prueba t no es universalmente superior a una prueba de Poisson**.

Cuando se dispone únicamente de:

- un solo conteo observado;
- una tasa histórica conocida $\lambda_0$;
- un fenómeno razonablemente modelable mediante Poisson;

puede utilizarse una **prueba exacta de Poisson** para evaluar si el conteo observado es extraordinariamente alto o bajo respecto a la tasa histórica.

---

# Valor-p exacto

La aplicación utiliza valores-p exactos obtenidos directamente de las distribuciones discretas.

La decisión se basa en:

$$
p\text{-valor}<\alpha.
$$

Si esto ocurre:

$$
\boxed{\text{Rechazar }H_0}
$$

En caso contrario:

$$
\boxed{\text{No rechazar }H_0}
$$

---

# Interpretación de la decisión

La aplicación evita interpretar:

> No rechazar $H_0$

como:

> Aceptar que $H_0$ es verdadera.

La conclusión correcta es que **la evidencia disponible no es suficientemente fuerte para rechazar la hipótesis nula al nivel de significancia utilizado**.

---

# Representación gráfica

Después de contestar en modo estudio o después de calificar, la aplicación muestra la distribución nula correspondiente.

La gráfica presenta:

- los posibles valores del conteo;
- la distribución bajo $H_0$;
- el valor observado;
- la región cuya probabilidad constituye el valor-p.

La región utilizada para calcular el valor-p aparece resaltada.

Esto permite relacionar el cálculo numérico con la interpretación geométrica de una prueba de hipótesis.

---

# Banco de reactivos

El banco contiene:

| Distribución | Casos |
|---|---:|
| Binomial | 50 |
| Hipergeométrica | 50 |
| Poisson | 50 |
| **Total** | **150** |

La mitad de los casos están construidos para producir suficiente evidencia para rechazar $H_0$ y la otra mitad para producir evidencia insuficiente.

| Resultado | Casos |
|---|---:|
| Rechazar $H_0$ | 75 |
| No rechazar $H_0$ | 75 |

---

# Estructura de cada intento

Cada intento contiene **5 problemas**.

Siempre aparecen las tres distribuciones mediante esquemas como:

- 2 binomiales, 2 hipergeométricos y 1 Poisson;
- 2 binomiales, 1 hipergeométrico y 2 Poisson;
- 1 binomial, 2 hipergeométricos y 2 Poisson.

El esquema cambia entre intentos para mantener una exposición equilibrada.

---

# Calificación

Cada problema contiene tres componentes evaluables:

1. Distribución correcta.
2. Valor-p correcto.
3. Decisión correcta.

Por tanto, un intento de 5 problemas contiene:

$$
5\times3=15
$$

componentes evaluables.

La calificación se muestra sobre 15 puntos.

---

# Modo estudio

Al activar **Modo estudio**, la aplicación proporciona retroalimentación una vez que el estudiante ha completado los tres componentes del problema.

La retroalimentación incluye:

- distribución adecuada;
- parámetros del modelo;
- dirección de la prueba;
- valor-p;
- comparación con $\alpha$;
- decisión estadística;
- interpretación del caso.

---

# Repaso de errores

Después de calificar puede utilizarse:

**Repasar sólo errores**

La aplicación muestra únicamente los problemas donde al menos uno de los tres componentes fue incorrecto.

Esto permite concentrar la práctica en los problemas que requieren revisión.

---

# Reporte

Después de calificar puede generarse un reporte que incluye:

- nombre del estudiante;
- número de intento;
- problema presentado;
- distribución seleccionada;
- distribución correcta;
- valor-p proporcionado;
- valor-p correcto;
- decisión seleccionada;
- decisión correcta;
- explicación;
- gráfica del valor-p.

El reporte puede guardarse como PDF mediante la función de impresión del navegador.

---

# Contextos de Gestión Empresarial

Los problemas están diseñados principalmente alrededor de situaciones como:

- contratación;
- selección de personal;
- promociones;
- asignación de bonos;
- proveedores;
- clientes;
- campañas;
- ventas;
- recompra;
- conversión;
- inventarios;
- atención al cliente;
- quejas;
- reclamaciones;
- entregas;
- devoluciones;
- cancelaciones;
- asignación de prospectos;
- decisiones administrativas;
- pruebas sensoriales;
- posibles sesgos o preferencias organizacionales.

El propósito es que las pruebas de hipótesis aparezcan asociadas a **decisiones reales o plausibles de gestión**, no únicamente a ejercicios algebraicos.

---

# Tecnologías utilizadas

La aplicación está desarrollada únicamente con:

- HTML5;
- CSS;
- JavaScript;
- Canvas API.

No requiere:

- instalación;
- conexión a Internet;
- frameworks;
- bibliotecas externas.

Todo el proyecto está contenido en **un único archivo HTML**.

---

# Ejecución

1. Descargar el archivo HTML.
2. Abrirlo en un navegador moderno.
3. Escribir el nombre del estudiante.
4. Resolver los 5 problemas.
5. Identificar la distribución.
6. Calcular el valor-p exacto.
7. Seleccionar la decisión.
8. Presionar **Calificar intento**.
9. Revisar la retroalimentación.
10. Opcionalmente generar el reporte en PDF.
11. Generar un nuevo intento para continuar practicando.

---

# Uso educativo

Esta herramienta está diseñada como apoyo para cursos de **Probabilidad y Estadística** en Gestión Empresarial.

Busca reforzar principalmente la siguiente secuencia de razonamiento:

1. **¿Qué fenómeno aleatorio estoy observando?**
2. **¿Cuál es la distribución adecuada bajo $H_0$?**
3. **¿Qué dirección plantea $H_1$?**
4. **¿Cuál es la probabilidad de observar un resultado tan extremo como éste bajo $H_0$?**
5. **¿La evidencia es suficientemente fuerte para rechazar $H_0$?**
6. **¿Qué significa esa conclusión dentro del problema empresarial?**

La intención es que el estudiante comprenda la prueba de hipótesis como una herramienta para evaluar evidencia y apoyar decisiones, no únicamente como una colección de fórmulas.

---

# Autor

Material educativo desarrollado para la enseñanza de Probabilidad y Estadística.
