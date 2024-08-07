# Estructura de carpetas

La ejecución de los comandos listados en [comandos.md](comandos.md) resulta en la creación de 4 carpetas. Las carpetas se crean en el directorio de trabajo actual (la carpeta donde ejecutó el comando). 
- `content` contiene los tipos de contenido reales y sus activos.  
- `libraries` ontiene las bibliotecas que se han configurado.  
- `temp` contiene copias locales de los repositorios git que se utilizan para calcular las dependencias.  
- `uploads` es una ubicación temporal utilizada por los comandos de importación y exportación.

> [!IMPORTANT]
> Asegúrate de borrar la carpeta `temp` cuando actualices a la última versión de una librería que tenga dependencias nuevas o actualizadas para que se clonen copias nuevas de los repositorios git.  

# Configurar una librería local

1 - Crea una carpeta para ella en el directorio `libraries`.  
    1.1 - Recuerde ejecutar `npm install` y `npm run build` desde dentro de la carpeta de la libnrería si su librería tiene un flujo de construcción.  
2 - Las dependencias de la biblioteca deben estar presentes en la carpeta `libraries`. De lo contrario, deben configurarse por separado. 

# Configurar una librería desde github

Las librerías que se pueden instalar automáticamente se almacenan en el registro local de bibliotecas. El registro es un archivo json  `registro-librerías.json`. 
Finally, run `h5p setup h5p-portfolio` to install the library and its dependencies.  
Puede utilizar el formato de url `git@github.com:Crompuverso/h5p-repo.git` cuando se trate de repositorios privados.  

# GIT y tu AGENTE-SSH

Si tienes que configurar librerías desde repositorios privados o si te encuentras con el error `Permission denied (publickey)` asegúrate de añadir tu clave ssh pública a tu agente ssh local.  
Es tan fácil como ejecutar los dos comandos siguientes.  
```
eval `ssh-agent -t 8h`
ssh-add
```
odos los comandos relacionados con git deberían funcionar ahora en la sesión actual durante al menos 8h. Siéntete libre de cambiar la duración para adaptarla mejor a tus necesidades.
Aquí tienes algunas guías sobre cómo añadir una clave ssh al agente ssh en [Linux](https://docs.github.com/en/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent), [Mac](https://docs.github.com/en/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=mac#adding-your-ssh-key-to-the-ssh-agent), [Windows](https://docs.github.com/en/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows#adding-your-ssh-key-to-the-ssh-agent).  
