# Proyecto-EDA

# instrucciones y objetivo

# Este proyecto consiste en tres etapas principales:
    1.	Análisis y exploración de los datos.
    2.	Tratamiento de los datos.
    3.	Manipulación y preparación de los datos.

     Análisis y exploración.
        Paso 1: Importar las librerías que se van a utilizar y mostrar las primeras y últimas 5 filas del dataset.

        Paso 2: Mostrar información sobre el dataset, qué tipos son, cuántos nulos hay, datos estadísticos.

        Paso 3: Mostrar información sobre las variables "objeto" y revisar si se pueden categorizar (todavía no se categorizan, solo se exploran)

        Paso 4: Mostrar información sobre las correlaciones (variables numéricas), la variable/columna objetivo es "SalePrice"

        Paso 5: Muestra de gráficas de las variables numéricas y categóricas.

     Tratamiento de los datos.
            Paso 1: Crear un límite para eliminar los datos nulos, mostrar las variables que harán eliminación a sus nulos y mostrar los conteos antes, eliminar los datos nulos y mostrar los conteos de nuevo.

            Paso 2: Si existen nulos aún, dependiendo de la gráficas anteriores, determinar si hay que imputar por medio de la moda, la mediana o la media; realizar la imputación.

            Paso 2.1 Eliminar columnas no relevantes antes de eliminar anomalias

            Paso 3: Analizar los datos numéricos, determinar si hay anomalías y utilizar el rango intercuartílico para tratarlos, mostrar gráficos antes y después del tratamiento, debe verse si la distribución se vio afectada.

            Paso 4: En base a la exploración previa (paso 3 del análisis y exploración), determinar si alguna columna puede ser categorizada y realizar la categorización.

            Paso 5: De las columnas categorizadas, buscar si hay inconsistencias, en caso de que las haya, hay que mostrarlas y tratarlas.

        Manipulación y preparación de los datos.
            Paso 1: Mostrar la matriz de correlación de nuevo, identificar las columnas que más esté correlacionadas con "SalePrice", mostrar numéricamente las 10 variables que estén correlacionadas más fuertemente a la variable objetivo

            Paso 2: Responder las preguntas.
                ¿Con las variables numéricas que se tienen es suficiente para predecir la variable objetivo? 
                ¿Alguna de las variables categóricas servirá realmente para determinar la variable objetivo? 
            
            Paso 3: Conversión de categórico a numérico. Hay que seleccionar las columnas que ya fueron categorizadas y hay que sacar su valor con un "one-hot encoder", luego hay que agregarlas al dataset y eliminar su columna categórica. Hay que mostrar de nuevo las correlaciones para ver si cambiaron las variables más correlacionadas con la variable objetivo.

            Paso 4: Conversión de las demás columnas objeto a numérico. Para ello se va a requerir un encoder más avanzado, usar la clase "MultiColumnLabelEncoder", el dataframe resultante va a ser la versión consolidada y completamente numérica.

            Paso 5: Mostrar la información del nuevo dataframe (numérico), mostrar que no contenga nulos, que todos los datos sean de tipo int/float/uint. Mostrar de nuevo las correlaciones, filtrar para que solo muestre las 10 más correlacionadas a la variable objetivo.

            Conclusiones acerca del análisis exploratorio y del dataset en general.

            Despues de realizar el EDA a este dataset, se puede concluir que la variable objetivo tiene muchisimas correlaciones significativas, si bien el tratar tantos datos no fue sencillo, tambien se puede dar cuenta, que muchas columnas no son relevantes; es decir habia muchos nulos por lo que tuve que filtrar algunas columnas, y aun despues de eso tuve que imputar o volver a analizar que muchas columnas ademas de no tener nulos, tenian muchos datos en cero y algunas otras no aportaban nada al analisis que se pretendia , por que opte por filtrar tambien esas columnas, de todo esto me percate al tratar anomalias pues me di cuenta que este tipo de datos en "0" me hacia tener que borrar muchos datos, y de no haber borrado esas columnas habria perdido mas del 50 % de los datos originales, en general fue sencillo manipular este dataset y en general puedo que concluir que se puede predecir con facilidad ala variable objetivo, pues esta relacionada significativamente con Overalqual, GrlivArea Y GarageCars, solo con estos datos podemos decir que el hecho de que la casa tenga garage tiene que ver mucho con el precio de una casa, eso sin mencionar el año en que fue construida, tambien por ejemplo el tipo de material de la fundacion, todas estas variables son muy significativas para determinar o predecir como se comporta el precio cuando mueves el valor de estas variables.

            Finalmente se obtuvo un df sin nulos, anomalias, solo datos numeriocs listo para usarse en un modelo de Machine Learning