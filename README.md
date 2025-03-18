# Data Lake Practice: Conexión entre Google Colab y AWS S3 con Apache Spark

Este repositorio contiene una práctica detallada que muestra cómo cargar datos desde **Google Colab** a **AWS S3**, procesarlos usando **Apache Spark**, y luego subirlos nuevamente a **AWS S3** en formato **Parquet**.

## Tecnologías Utilizadas

- **Google Colab**: Entorno de ejecución en la nube para código Python.
- **AWS S3**: Servicio de almacenamiento de objetos en la nube de Amazon.
- **Apache Spark**: Framework distribuido para procesamiento de datos masivos.
- **PySpark**: API de Python para trabajar con Apache Spark.
- **Parquet**: Formato de archivo para almacenamiento eficiente de grandes volúmenes de datos.

## Descripción del Proyecto

Este proyecto describe cómo cargar, procesar y almacenar datos a gran escala utilizando **Apache Spark** en un entorno distribuido. El flujo de trabajo incluye lo siguiente:

1. **Subir datos a AWS S3 desde Google Colab**  
   - Se cargan archivos de datos desde **Google Colab** a un contenedor de **Azure Blob Storage** utilizando la biblioteca `azure-storage-blob`.

2. **Conectar y procesar datos con Apache Spark**  
   - Configuración de un **SparkSession** para leer los datos desde **Azure Blob Storage** utilizando PySpark y realizar transformaciones sobre los datos.

3. **Convertir los datos a formato Parquet**  
   - Los datos procesados se convierten en formato **Parquet**, optimizando el almacenamiento y la velocidad de lectura.

4. **Subir los datos procesados a S3**  
   - Después de procesar y convertir los datos, se suben nuevamente a un contenedor de **AWS S3**.

     
## Requisitos
1. Google Colab: Entorno de ejecución para el código.
2. Apache Spark: Framework distribuido para el procesamiento de datos.
3. Python 3.x.
4. PySpark: Librería de Python para interactuar con Apache Spark.
5. boto3: SDK de Amazon Web Services (AWS) para interactuar con S3 desde Python.
6. azure-storage-blob: Biblioteca para interactuar con Azure Blob Storage.

## Instrucciones de Uso

1. Subir los datos a S3 desde Google Colab
2. Usa el código del notebook para cargar los datos desde Google Colab a un bucket de Azure Blob Storage utilizando boto3 y las credenciales adecuadas.
3. Configurar PySpark
4. Configura y conecta PySpark a tu entorno de Azure Blob Storage para leer los archivos almacenados.
5. Procesar los datos con Apache Spark
6. Realiza transformaciones en los datos, como limpieza, agregación, y conversiones necesarias.
7. Convertir a Parquet
8. Convierte el DataFrame procesado en Parquet para almacenamiento optimizado.
9. Subir el archivo a AWS S3
10.Después de procesar y convertir los datos, utiliza el código para subir los resultados al bucket de AWS S3.

## Contribuciones
Las contribuciones son bienvenidas. Si deseas mejorar este repositorio, por favor, abre un issue o realiza un pull request.

## Estructura del Repositorio

```plaintext
/
├── /src               # Código fuente para la carga de datos, procesamiento con Spark y subida a S3.
├── /notebooks         # Jupyter Notebooks que documentan paso a paso el proceso de carga, transformación y subida de los datos.
├── /config            # Archivos de configuración para la conexión a AWS S3 y Azure.
├── /data              # Datos de ejemplo para realizar las prácticas.

