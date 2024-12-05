**POST RUN WRF**

**Descripción**

Este **repositorio** alberga una serie de proyectos desarrollados en un **entorno** **virtual** utilizando **Visual** **Studio** (**VS**) y el lenguaje de programación **Python**. Su propósito principal es mejorar y optimizar la generación de mapas, así como la extracción y procesamiento de datos, con un enfoque particular en el uso de información proporcionada por el modelo **meteorológico** **WRF** (**Weather Research and Forecasting**).

El repositorio incluye varios módulos clave que ofrecen funcionalidades específicas:

- **wind\_wrf\_gfs**: Analiza y procesa datos de viento utilizando las salidas de **WRF** y **GFS** para generar representaciones visuales o cálculos personalizados.
- **generate\_map**: Genera mapas detallados a partir de los datos **meteorológicos** y **geográficos** procesados.
- **generate\_json\_DoD**: Automatiza la creación de archivos **JSON** con información estructurada basada en datos del **Departamento de Defensa** (**DoD**).
- **generate\_json\_FAA**: Similar al módulo anterior, pero orientado a datos de la **Administración Federal de Aviación (FAA).**
- **search\_by\_icao**: Permite realizar búsquedas de datos específicos utilizando códigos **ICAO**.
- **search\_by\_FAA\_icao**: Facilita la búsqueda de información usando combinaciones de códigos **FAA** e **ICAO**.

Adicionalmente, el repositorio incluye los siguientes archivos esenciales para su correcta configuración y funcionamiento:

- **main.py**: Archivo principal que sirve como punto de entrada al proyecto, facilitando la ejecución de las funcionalidades de los módulos mencionados.
- **setup.ini**: Archivo de configuración que define rutas importantes para el entorno de ejecución.
- **requirements.txt:** Documento que especifica las dependencias necesarias para ejecutar el proyecto, permitiendo la instalación rápida y eficiente de las bibliotecas requeridas.

**Nota: Este proyecto está diseñado para usuarios interesados en el análisis meteorológico, la generación de mapas personalizados y la manipulación avanzada de datos meteorológicos y geoespaciales. Además, su estructura modular permite una fácil personalización y extensión para adaptarse a nuevas necesidades.**

**Tabla de Contenidos**

- Descripción
- Instalación
- Uso
- Contribuciones
- Licencia

**Instalación**
Sigue estos pasos para instalar y configurar el proyecto:

**1.** **Clonación del repositorio**

**2.** git clone [**https://github.com/Neroneitor/post_run_wrf.git**](https://github.com/Neroneitor/post_run_wrf.git)


- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 001](https://github.com/user-attachments/assets/96150794-0333-45cd-81f5-358422064037)



**3**. **Ingreso al entorno virtual global** Asegúrate de tener configurado tu entorno virtual global (**global\_post\_env)** y actívalo

  **Paso 1**: Ingreso y Activación de Conda en la Terminal

  - Abrir la terminal: Accede a la terminal desde tu sistema operativo.
  - Activar Conda: Ingresa el comando para activar Conda: “**conda acitvate**” 

  - ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 002](https://github.com/user-attachments/assets/c1747367-fd11-414f-9b0b-57c075432a5b)


**Nota: Asegúrate de que Conda esté correctamente instalado y configurado previamente.**

- Si el entorno **Conda** se activó correctamente, antes de nuestro nombre aparecerá "**(base)**", lo que indica que estamos dentro del entorno base de **Conda**.
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.003.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 003](https://github.com/user-attachments/assets/ad850bcf-43da-42eb-ba3c-a3bde5308f86)

**Paso 2**: Búsqueda de entornos virtual (**global\_post\_env**)

- Utiliza el comando de terminal “**conda env** **list**” para visualizar todos los entornos virtuales disponibles en tu equipo.
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.004.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 004](https://github.com/user-attachments/assets/bdcd37a6-afd9-484d-b0ea-e8912bcf2617)

- Buscaremos en la lista de nombres el entorno virtual global denominado "**global\_post\_env**".

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.005.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 005](https://github.com/user-attachments/assets/01b1b649-6d2d-4ce5-bd82-e7f7c4030d73)

**Paso 3:** activación de entorno virtual (**global\_post\_env**)

- Para activar el entorno virtual, utilizaremos el comando "**conda activate**" seguido de la ruta de nuestro entorno.
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.006.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 006](https://github.com/user-attachments/assets/2dd478cd-6f02-4150-8d26-ad6ea750ca04)

- En comando debería quedar de la siguiente manera **“conda activate /usr/local/miniconda 3/envs/global\_post\_env”** 
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.007.png)**
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 007](https://github.com/user-attachments/assets/a239a508-e322-4dd4-83fb-acf3a1596575)

- Luego de hacer este paso nuestro entorno quedara activado de manera correcta, para verificar esto el **“(base)”** cambiara por el nombre de nuestro entorno (**global\_post\_env**)

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.008.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 008](https://github.com/user-attachments/assets/f81c6522-bd73-473b-b530-6680aac92adf)


**Nota: Este entorno ya tiene las librerías necesarias, según el archivo requirements.txt, lo que asegura que el proyecto esté completamente operativo para su diseño y desarrollo. En caso de que el entorno virtual global no esté disponible o no funcione correctamente, puedes crear un entorno virtual específico para este proyecto. A continuación, se detallará el proceso de creación del entorno virtual e instalación de las librerías, en caso de que el entorno 'global\_post\_env' no sea funcional**

**Paso 1**: Usaremos el comando **“python3.10 -m venv”** para crear nuestro entorno virtual. En este caso, el entorno se llamará “**post\_env”**.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.009.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 009](https://github.com/user-attachments/assets/9ec51552-527b-4ad1-9ed4-498442865eb8)

**Paso 2:** Activar el entorno virtual utilizando el comando: **“source  post\_env/bin/actívate”**

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.010.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 010](https://github.com/user-attachments/assets/39f1cf48-bd12-47a1-b755-dd152058f837)

- Si el entorno virtual se activó correctamente, el nombre del entorno aparecerá entre paréntesis, por ejemplo, **(post\_env).
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.011.png)**
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 011](https://github.com/user-attachments/assets/2f001ba6-55ce-4d3f-834b-caad50fcde88)

**Paso 3**: Verifica las librerías instaladas de manera predeterminada utilizando el comando: **“pip list”**.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.012.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 012](https://github.com/user-attachments/assets/352dcc04-0244-4271-ab23-e26637fe8ad7)

- En este punto, aparecerá un mensaje de advertencia ("**WARNING**") que nos indicará la necesidad de actualizar una de las librerías predeterminadas. Para hacerlo, debemos ejecutar el siguiente comando**:  "pip install --upgrade pip ".**
- En la siguiente imagen, se muestra cómo debería lucir el proceso correctamente.


- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.013.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 013](https://github.com/user-attachments/assets/434902fc-4c11-4683-bd67-a5aa97027252)


**Paso 4:** En este paso, instalaremos las librerías necesarias para ejecutar el proyecto. Los nombres y versiones específicas requeridas para su correcto funcionamiento están detallados en el archivo denominado ***requirements.txt.*** Para instalarlas, utiliza el siguiente comando: **"pip install -r requirements.txt "**

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.014.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 014](https://github.com/user-attachments/assets/b7aa802a-ab7d-480f-a3d6-e06cb6d7c156)


- Una vez que se complete la instalación de las librerías, se mostrarán dos mensajes principales en la salida del proceso: el primero será **'Installing collected packages'**, lo que indica que los paquetes se están recopilando y preparando para su instalación. El segundo mensaje será **'Successfully installed'**, lo que confirma que la instalación de las librerías se ha realizado con éxito

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.015.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 015](https://github.com/user-attachments/assets/f493753c-a30a-47ed-b470-3006f2b3c9c7)


**Paso 5**: Por último, ejecutamos el archivo principal (**main**) del proyecto. Cabe destacar que este ejemplo se realizó desde la terminal del sistema operativo, pero también es posible hacerlo desde la terminal integrada de **Visual Studio (VS)**.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.016.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 016](https://github.com/user-attachments/assets/aecb733f-5b2f-4058-a958-3d19d47a983e)


4. <a name="_hlk184199915"></a>**Creación de carpeta para resultados** Para almacenar los archivos generados, crea una carpeta en el directorio principal del proyecto utilizando el comando **“mkdir documents\_post\_run”**. Alternativamente, puedes ir directamente a la ubicación donde clonaste el repositorio de GitHub y crear manualmente la carpeta **“documents\_post\_run”**. Esta carpeta está definida en el archivo setup.ini como el contenedor principal de todos los resultados generados por los procesos.
- En la siguiente imagen se muestra cómo debería quedar organizada la carpeta creada.
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.017.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 017](https://github.com/user-attachments/assets/297676da-f1d2-4a50-ab73-1a909ce564b3)

- En la imagen siguiente se muestra la visualización del archivo setup.ini, donde se redirigen los resultados a la carpeta **'documents\_post\_run'** según los diferentes usos.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.018.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 018](https://github.com/user-attachments/assets/56c52c81-3cff-432c-b3a7-59acadaef921)

5 **Uso**
El uso del proyecto se realiza mediante métodos **POST** enviados por **Postman**. Sigue estos pasos:

1. Asegúrate de haber completado los pasos de instalación.
2. Ejecuta el archivo principal del proyecto: python **main.py**
3. Utiliza Postman para enviar solicitudes al servidor configurado.

   3\.1 paso a paso para el uso y envió de solicitudes: 

   **Paso 1:** Ingresar al **Main** y buscar el **Endpoint** que vamos a utilizar. En este caso, como ejemplo, utilizaremos el **Endpoint** de Búsqueda por **ICAO**.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.019.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 019](https://github.com/user-attachments/assets/43dc82d9-eb30-4151-9ed6-a8495708e218)

**Paso 2**: Después de completar el **paso 1**, nos ubicaremos en la línea de código que inicializa el fragmento de código

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.020.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 020](https://github.com/user-attachments/assets/adc412c0-fbbd-4c8a-9da7-9656607f5a2a)

En esta parte, se encuentra la ruta **'/api/search\_by\_icao'**, a la cual se accederá mediante el método **POST**.

**Paso 3**: Una vez obtenida esta información, nos dirigimos a Postman, donde crearemos una nueva colección haciendo clic en el signo de más (+).

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.021.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 021](https://github.com/user-attachments/assets/98c00b59-26cd-480e-90f3-fe14317d270e)


Esto creará una nueva colección en la que trabajaremos nuestras solicitudes al **Endpoint**. Por defecto, la colección llevará el nombre **'New** **Collection'**. Luego de crearla, haremos **clic** derecho sobre el nombre para abrir las opciones de la colección. Esto desplegará una lista de opciones, de la cual seleccionaremos **'Add** **Request'**. Esto creará el espacio donde trabajaremos nuestra solicitud.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.022.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 022](https://github.com/user-attachments/assets/3a00ef00-67f7-4f8c-b3b8-4e91477a5f4a)

La cual se vería así:

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.023.png) 
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 023](https://github.com/user-attachments/assets/2e3e1143-3ce4-4010-ac7f-bfa740b4a654)

Haremos **clic** en este nuevo objeto, lo cual abrirá un formulario donde ingresaremos la información de nuestra solicitud

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.024.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 024](https://github.com/user-attachments/assets/34dc6456-00ae-4a06-bbd1-7dacca740e8e)

- **Paso** **4**: En este nuevo formulario, realizaremos la preparación necesaria para ejecutar nuestra solicitud.
- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.025.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 025](https://github.com/user-attachments/assets/a031f544-7398-4b2a-a081-718278b3fc83)

• **Paso 4.1** Ingresar la ruta junto con el puerto en el que se está trabajando, el cual generalmente se encuentra al final del archivo **Main**.

- **Puerto** en el que se está trabajando:
- 
  ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.026.png)
  ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 026](https://github.com/user-attachments/assets/ccf956c8-6ddc-46fc-89e6-d7cab25f70e2)

- **Ruta** del **Endpoint** en cual vamos a acceder:

  ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.027.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 027](https://github.com/user-attachments/assets/fa772762-a53f-409d-9b16-cd51b1794296)

- **Método** del **Endpoint** en cual vamos a acceder: 

  ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.028.png)
  ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 028](https://github.com/user-attachments/assets/bad05a3c-a290-4636-a6a9-3dc3ba3f0a8d)


- Además, se deberá solicitar al administrador la **URL** (en este caso, el ejemplo es **http://127.0.0.1:**) para poder continuar con el proceso. El resultado de este proceso debería ser el siguiente:

  ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.029.png)
  ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 029](https://github.com/user-attachments/assets/32c20770-ef49-40c9-b7f7-43b8784e103e)


Para cambiar el método, debemos hacer clic en el método y seleccionar el que ya está previamente definido en el **Endpoint**.

Paso 5: seleccionaremos la opción de **'Body'**.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.030.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 030](https://github.com/user-attachments/assets/bef8fb41-2cd6-4df6-a139-303d6ab1ceb2)


Después de esto, seleccionaremos la opción **'Raw'**, lo cual habilitará un campo en el que podremos ingresar los datos y la clave a seleccionar.

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.031.png)
- ![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 031](https://github.com/user-attachments/assets/774aa8d1-e17d-4222-853e-58fcda9030a0)

- En este campo ingresaremos los datos y la forma en la que los vamos a buscar.

  ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.032.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 032](https://github.com/user-attachments/assets/530b8207-afe3-4a37-a25f-3fcfa95282d7)

El resultado final se mostrará de la siguiente manera después de ejecutar los pasos descritos anteriormente. (**Este proceso ha sido tomado como ejemplo del proceso de búsqueda por ICAO en la API, enfocado en la organización y búsqueda de documentos DOD\_FLIP.**)

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.033.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 033](https://github.com/user-attachments/assets/3d504d6f-07c3-418b-a706-23f1c51f1ae6)

A continuación, se enviará el método **POST** para ejecutar las funciones mencionadas

- ![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.034.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 034](https://github.com/user-attachments/assets/dfb4f853-2910-46af-8844-733d36dea088)

Así es como se verá el **módulo** cuando los resultados del proceso estén listos al finalizar la ejecución

- .![](Aspose.Words.bebe987a-a083-4df8-a694-4a146bdd5bbf.035.png)
![Aspose Words bebe987a-a083-4df8-a694-4a146bdd5bbf 035](https://github.com/user-attachments/assets/3e0292d5-aa3f-4bff-b9e3-e76c9918f2a5)

1. Los mapas generados se almacenarán en la **carpeta documents\_post\_run**. Esto aplica a todos los archivos resultantes de la ejecución de los generadores de mapas.

5 **Contribuciones**
¡Las contribuciones son bienvenidas! Si deseas contribuir al proyecto:

1. Realiza un **fork** del repositorio.
- Crea una rama para tu contribución:
- **git checkout -b mi-nueva-funcionalidad**


1. Realiza tus cambios y confirma los **commits**:
- **git commit -m** **"**Agrega mi nueva funcionalidad**"**
- Envía un **pull push origin** mas el nombre de tu rama.

**Licencia**
Este proyecto está bajo la licencia MIT License.
