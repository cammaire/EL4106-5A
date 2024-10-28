# EL4106-5A
Repositorio de proyecto semestral para el ramo EL4106-1 Primavera 2024, grupo 5A. Proyecto: Detección Temprana de Supernovas en ALeRCE - ZTF

Universidad de Chile

Facultad de Ciencias Físicas y Matemáticas

Departamento de Ingeniería Eléctrica

Detección Temprana de Supernovas en ALeRCE - ZTF (Resultados Preliminares)

Integrantes Grupo 5A: Nicolás Camousseight // Camila Maire

Profesor: Pablo Estévez

Auxiliar: Pablo Cornejo

Ayudantes: Diego Castillo // Andrés González // Sebastián Guzmán //Francisco Soto


Este repositorio contiene el código, datos y documentación del proyecto Detección Temprana de Supernovas en ALeRCE - ZTF. El objetivo de este proyecto es desarrollar un modelo de aprendizaje profundo capaz de detectar y clasificar supernovas en sus fases iniciales, utilizando los datos proporcionados por el Zwicky Transient Facility (ZTF) y el sistema de alertas de ALeRCE.


Descripción del Proyecto

Las supernovas son eventos astronómicos transitorios con una duración relativamente corta, y la posibilidad de detectarlas tempranamente permite a la comunidad científica realizar un seguimiento oportuno y obtener información crítica sobre la evolución estelar y la expansión del universo. En este proyecto, utilizamos una red neuronal convolucional (CNN) para procesar las imágenes de ciencia, referencia y diferencia de la primera detección de cada alerta, además de los metadatos asociados.


Estado del Arte

El proyecto se basa en la metodología de clasificación de ALeRCE, que aplica redes convolucionales para clasificar imágenes de eventos astronómicos en cinco clases: supernovas (SN), núcleos activos de galaxias (AGN), estrellas variables (VS), asteroides y falsas detecciones (bogus). Con un enfoque innovador que incluye rotaciones de las imágenes y la integración de capas de cyclic pooling, el modelo logra identificar patrones relevantes independientemente de la orientación de las imágenes.


Resultados Preliminares

Los resultados iniciales muestran una mejora en precisión y reducción de errores cuando el modelo es entrenado por más épocas (100), con una mejora notable en su capacidad de distinguir entre supernovas y otras clases de eventos. Los experimentos han permitido obtener una precisión general cercana al 94% en pruebas balanceadas.
Contenidos del Repositorio

    /code: Contiene el código fuente para el procesamiento de datos, construcción de la red neuronal y entrenamiento del modelo.
    /data: Carpeta destinada a almacenar las imágenes de entrada y otros datos requeridos para el entrenamiento (no incluido por privacidad).
    /results: Carpeta con los resultados obtenidos, incluyendo gráficos de precisión (accuracy) y pérdida (loss) por épocas, así como matrices de confusión.
    Informe_Proyecto.pdf: Documento del informe detallado del proyecto, con secciones de estado del arte, metodología, resultados preliminares y conclusiones.


Requisitos de Instalación

Para ejecutar el código, se requiere tener instalada una versión de Python >= 3.7 junto con las siguientes librerías:

    tensorflow >= 2.0
    numpy
    matplotlib
    scikit-learn

Las dependencias pueden instalarse ejecutando el siguiente comando:
pip install -r requirements.txt

Uso del Código

    Preprocesamiento de Datos: Ejecuta el script de preprocesamiento para organizar las imágenes en un diccionario que agrupa las imágenes de entrenamiento, validación y prueba en las categorías correspondientes.

    Entrenamiento del Modelo: Utiliza el script principal para entrenar la red neuronal con los datos preprocesados. Puedes configurar el número de épocas y otros hiperparámetros en el archivo de configuración.

    Evaluación del Modelo: Ejecuta los scripts de evaluación para generar las métricas de rendimiento, incluidas las curvas de precisión y pérdida, y las matrices de confusión para diferentes configuraciones de épocas.

