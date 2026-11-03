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
#### **Fórmula:**
```excel
=CONTARA(Ventas!A:A)
```

