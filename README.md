## Analisis-Dataset-de-Ventas

### 1. Descripcion
Recibimos un Dataset con muchos errores e inconsistencias al cual le realizamos una limpieza y trasformacion enorme usando las herramientas de power wuery, y luego se realizo el analisis obteniendo las KPIs importantes, investigando patrones y anomalias que nos den un analisis mas preciso y presentando el dashboard que respalde los hallazgos.

### Dashboard
<img width="1393" height="587" alt="image" src="https://github.com/user-attachments/assets/be962acc-80bf-41d1-bf4c-6bfc2fce25b2" />


### 2. Objetivo
Realizar el proceso de limpieza, trasformacion y analisis de datos del dataset usando power wuey y Excel, dando a conocer los conocimientos tecnicos y pensamiento analitico usando estas herramientas.

### 3. Herramientas
- Power Query.
- Excel.

### 4. Fuente
- Dataset Original: [Dataset Ventas.zip](https://github.com/user-attachments/files/34056589/Dataset.Ventas.zip)

### 5. Metodologia

#### 5.1 Limpieza y Trasformacion de Datos
Obtenemos nuestros datos realizaremos la limpieza y trasformacion dentro de Excel usando Power query y lo que se realizo en este paso es lo siguiente.
- Encabezado de Columna: las primeras dos filas de la tabla eran datos erroneos por lo que se eliminaron y se colocaron los respectivos encabezados a cada columna que venian uncluidos en la fila 3.
<img width="1780" height="152" alt="image" src="https://github.com/user-attachments/assets/01acf840-33bc-4e49-84f2-71df6c3250ed" />

- Filas Vacias: En la investigacion de datos vacios detectamos que habian muchas filas completamente vacias por lo que se filtraron y obtuvimos una tabla mas limpia y completa.
<img width="1806" height="521" alt="image" src="https://github.com/user-attachments/assets/95a3d6fb-4443-474c-8b20-5b4a6f082d93" />

- Colummnas Vacias: en la mima exploracion se detecto comumnas completamente vacias por lo que se eliminaron.
<img width="1691" height="602" alt="image" src="https://github.com/user-attachments/assets/66e78850-a179-4107-91ad-962f821c73bb" />

- Datos nulos o erroneos: dentro de los campos Precio, Costo y Cantidad se encontraron incosistencias en los datos la forma en la que procedimos fue filtrar esos datos que eran 5 en total, se tomo esta decicion debido a que es un proyecto practico de ser proyecto real se buscaria correjir esos datos y tener registros completos.

- Correccion de Datos: En el campo Cod.Vendedor se encontro incisistencia de los datos ya que al filtrar un vendedor encontramos ese nombre con mas de un codigo de vendedor por lo que se debio de realizar un procedimiento en el que cada vendedor tubiera un codigo unico.
<img width="915" height="622" alt="image" src="https://github.com/user-attachments/assets/d1487f57-656a-4d75-b4dd-c1386a42c674" />

- Inconsistencia con Nombres: En los campos Vendedor y Cliente se encontraron datos en los que hay errores de escritura por lo que se reemplazarmo los datos erroneos por los datos correctos.

- Formato de Datos: Correccion del tipo de datos en todas las colummnas y en la colummna fecha se encontraron dos tipos de fechas por lo que se cambio el tipo de fecha para tener todos los datos con el mimo tipo de fecha.

### 5.2 KPIS
Despues de la limpieza y trasformacion de datos, podemos enfocarnos en obtener las KPIs relevantes y poder obtener informacion importante para explicar los hallazgos y metricas.

- Cantidad de Ventas:
```excel
=CONTARA(Ventas!A:A)
```
- Productos vendidos:
```excel
=SUMA(Ventas!K:K)
```
- Media de productos vendidos por venta:
```excel
=PROMEDIO(Ventas!K:K)
```
- Ventas Totales:
```excel
=SUMA(Ventas!M:M)
```
- Costo Total:
```excel
=SUMA(Ventas!L:L)
```
- Margen de Ventas:
```excel
=E12-E16
```
- Margen Porcentual de Ventas:
```excel
=E20/E12
```
- Margen Porcentual en costos:
```excel
=E20/E16
```

### 5.3 Dashboard
El contenido del dashboar es el siguiente:
- KPIs relevantes: Ventas Totales, Costos Totales, Margen, Margen Porcentuaal.
- Grafico de barras de comparacion anual de las ventas totales.
- Grafico de barras horizontal que muestar las ventas totales por cada vendedor.
- Grafico de barras horizontal con las ventas por categoria.
- grafico de barras con la variacion interanual en forma de porcentaje.
- Grafico de barras donde muestra los años y volumen que vendio cada vendedor.

<img width="1255" height="566" alt="image" src="https://github.com/user-attachments/assets/177e4724-3c15-4d79-848c-08a3150de57e" />


## 6. Hallazgos
- El 40% de la fuerza de ventas (Francisco Chávez, María González, María Jesús Cuesta y Pilar Pinilla) concentra el 72.27% del ingreso total ($2,347,118.90$). Se sugiere diseñar un plan de retención para estos perfiles clave y evaluar programas de capacitación para dinamizar el rendimiento del 60% restante de la fuerza comercial.

- El 35% de las categorias (Bebidas, Carnes Enlatadas, Frutos Secos, Golosinas y Sopas) impulsa el 75% de las ventas totales de la empresa . El 65% restante de las categorías genera únicamente el 25% de los ingresos. Esto evidencia la necesidad de diseñar estrategias comerciales focalizadas (como campañas cruzadas o revisión de mix de productos) para potenciar el rendimiento de las categorías de baja rotación y equilibrar el portafolio.

- Tras consolidar un periodo de expansión acelerada en 2020 (+65.44%) y un mantenimiento estables en 2021 (+5.54%) con un pico de facturación de $1,150,523.40$, el año 2022 experimenta una contracción severa del -69.77% frente al periodo anterior, cayendo incluso un -47.22% por debajo del nivel base de 2019.

- La auditoría cruzada de transacciones por vendedor demuestra que el desplome del $-69.77% en 2022 no obedeció a una contracción del mercado, sino al cese de operaciones del 70% de la fuerza de ventas (7 de 10 vendedores registraron cero transacciones en el periodo). La facturación del año fue sostenida de forma aislada por solo 3 agentes (Francisco Chávez, Jesús Escolar y Juan Carlos Rivas), evidenciando una crisis crítica de retención de talento y desatención de cuentas clave.

### 7. Retos
Dentro de cada proyecto que realizo siempre hay retos nuevos que desafian mis habilidades y mas que estancarme me ayudan a pulir y mejorarlas, los retos que mas me exigieron enfoque fueron los siguientes:
- Limpieza de datos: es el primer proyecto el cual su esncenario principal era lo muy desrodenado, inconcestente ycon errores de datos que mas dificil de correjir ha sido, sin embargo a lo largo de toda esta limpieza y trasformacion he logrado mejorar mucho el encontrar inconsistencias y ser mas detallista a la hora de tener los datos completamente listos para analizar.
- Formulas: he mejodaro mucho a loa largo de la construccion de estos proyecto y una de las partes que aun no tengo muy dominado son las formulas, mas del lado de sintaxis ya que muchas veces tengo claro la logica y como aplicarla y son detalles los que me faltan por pulir el resto todo en orden.
- Siempre el mostrar los hallazgos me ayudan a mejorar mi analisis y en eset caso no fue la excepcion, el investigar datos relevantes, sacar conclusiones, de ser nesesario recomendaciones es la escencia de este rol y el poder tener datos que respalden lsa conclusiones me anima mucho a seguir mejorando mis habilidades.

## 7. Archivo proyecto completado
- [Analisis-Ventas.zip](https://github.com/user-attachments/files/34327953/Analisis-Ventas.zip)

