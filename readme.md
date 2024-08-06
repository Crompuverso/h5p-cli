Un conjunto de herramientas basadas en h5p, enfocadas en la creación de videos interactivos

Para usar, asegúrate de antes tener [git](https://git-scm.com/downloads), [NodeJS](https://nodejs.org/en) and **npm** (usualmente incluido en NodeJS) instalados.  
SAlgunos de los comandos listados aquí funcionan mejor en Linux y MacOS. En Windows se recomienda ejecutarlos dentro de [git bash](https://git-scm.com/download/win) o **powershell**. 

# INSTALACIÓN

Desinstale cualquier instancia anterior del kit de herramientas h5p-cli.
```
npm uninstall -g h5p-cli
npm uninstall -g h5p
```
Instálelo mediante npm 
```
npm install -g h5p-cli
```
o instálelo desde su repositorio.
```
git clone https://github.com/Crompuverso/h5p-cli.git
cd h5p-cli
npm install
cd ..
npm install -g ./h5p-cli
```
Ahora puede utilizar `h5p` como comando global.  

# GUÍA DE INICIO RÁPIDO

> [!IMPORTANT]
> Los comandos se ejecutan en relación al directorio de trabajo actual.  
> Puedes crear múltiples directorios de trabajo cada uno con diferentes configuraciones de librerías.  

0. Crea una nueva carpeta para tu primer entorno de desarrollo H5P y cambia a ella tu directorio de trabajo actual.  
```
mkdir mi_primer_entorno
cd mi_primer_entorno
```

1. Instale las bibliotecas básicas de H5P.
```
h5p core
```

2. Instale una biblioteca H5P como h5p-interactive-video.
```
h5p setup h5p-interactive-video
```
Esto es necesario para ejecutar y editar tipos de contenido en la biblioteca "h5p-interactive-video".  
Puedes instalar otras librerías listadas por `h5p list` de la misma manera.  
Por ejemplo, `h5p setup h5p-video` instala la librería "h5p-video" y sus dependencias. 
> [!NOTE]
> Puedes [leer más información sobre la creación de bibliotecas aquí](assets/docs/setup.md).

3. Inicia el servidor de desarrollo.
```
h5p server
```
Ahora puede utilizar su navegador para ver, editar, eliminar, importar, exportar y crear nuevos tipos de contenido.  
> [!IMPORTANT]
> Recuerda que la carpeta donde ejecutas el servidor H5P es donde el servidor buscará las librerías. Si ejecuta los comandos de instalación en otra carpeta, el servidor no encontrará esas bibliotecas.  

Puedes [encontrar más información de los comandos aquí](assets/docs/commands.md) o ejecutando `h5p help`. 
