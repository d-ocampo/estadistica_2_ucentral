**Principales Comandos en Google Colab**

Google Colab es una herramienta poderosa para trabajar con Python en la nube, especialmente para el análisis de datos y la programación en machine learning. Aquí tienes una lista de algunos comandos útiles:

1. **Crear un Nuevo Notebook**: Para crear un nuevo cuaderno en Google Colab, puedes hacer clic en "Archivo" -> "Nuevo cuaderno" o usar el atajo de teclado `Ctrl + Shift + N`.

2. **Ejecutar una Celda**: Para ejecutar una celda de código en Google Colab, puedes hacer clic en el botón de reproducción en el lado izquierdo de la celda o usar el atajo de teclado `Shift + Enter`.

3. **Agregar una Nueva Celda**: Para agregar una nueva celda en Google Colab, puedes hacer clic en el botón `+ Texto` o `+ Código` en la parte superior del cuaderno, o usar los atajos de teclado `Ctrl + M B` para insertar una nueva celda debajo o `Ctrl + M A` para insertar una nueva celda arriba.

4. **Ejecutar Todo el Cuaderno**: Para ejecutar todas las celdas en un cuaderno, puedes hacer clic en "Entorno de ejecución" -> "Ejecutar todas" o usar el atajo de teclado `Ctrl + F9`.

5. **Conectar con Google Drive**: Puedes montar tu Google Drive en Google Colab para acceder a tus archivos. Usa el siguiente comando:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

6. **Instalar Dependencias**: Si necesitas instalar paquetes adicionales, puedes usar el comando `!pip install` seguido del nombre del paquete. Por ejemplo:

   ```python
   !pip install pandas
   ```

7. **Subir Archivos**: Puedes subir archivos desde tu computadora local a Google Colab utilizando el siguiente comando:

   ```python
   from google.colab import files
   uploaded = files.upload()
   ```

8. **Descargar Archivos**: Para descargar archivos generados en Google Colab a tu computadora local, puedes usar el siguiente comando:

   ```python
   files.download('example.csv')
   ```

**Principales Funciones con Pandas**

Pandas es una biblioteca de Python ampliamente utilizada para manipulación y análisis de datos. Aquí tienes algunas de las funciones más utilizadas:

1. **Crear un DataFrame**: Puedes crear un DataFrame de pandas pasando un diccionario de listas o un diccionario de diccionarios:

   ```python
   import pandas as pd

   data = {'Nombre': ['Juan', 'María', 'Luis'],
           'Edad': [25, 30, 35],
           'Ciudad': ['Madrid', 'Barcelona', 'Sevilla']}

   df = pd.DataFrame(data)
   ```

2. **Cargar Datos desde un Archivo**: Puedes leer datos desde un archivo CSV, Excel, u otro formato utilizando funciones como `pd.read_csv()`, `pd.read_excel()`, etc.

   ```python
   df = pd.read_csv('datos.csv')
   ```

3. **Mostrar las Primeras Filas**: Para ver las primeras filas de un DataFrame, puedes usar el método `head()`:

   ```python
   df.head()
   ```

4. **Seleccionar Columnas**: Puedes seleccionar una o varias columnas de un DataFrame utilizando su nombre:

   ```python
   df['Nombre']
   ```

5. **Filtrar Filas**: Puedes filtrar filas basadas en condiciones específicas:

   ```python
   df[df['Edad'] > 25]
   ```

6. **Agregar Nuevas Columnas**: Puedes agregar nuevas columnas calculadas a un DataFrame:

   ```python
   df['Nueva_Columna'] = df['Edad'] * 2
   ```

7. **Agrupar y Resumir Datos**: Puedes agrupar datos basados en una columna y calcular estadísticas resumidas:

   ```python
   df.groupby('Ciudad').mean()
   ```

8. **Exportar Datos a un Archivo**: Puedes guardar un DataFrame en un archivo CSV, Excel, etc.:

   ```python
   df.to_csv('nuevo_datos.csv', index=False)
   ```

Estos son solo algunos de los comandos y funciones básicas en Google Colab y Pandas. ¡Hay muchas más para explorar y aprender!