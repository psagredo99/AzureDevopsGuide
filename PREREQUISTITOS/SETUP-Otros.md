
Necesitamos tener instalado:

-NodeJs (https://nodejs.org/en/)
-Visual Studio Code
-Git
-OpenSSL

Desde visual studio code, isntalamos la extensión:

![[Pasted image 20240925163148.png]]


Una vez instalada desde la terminal de bash de vsc ejecutamos los siguientes comandos:

> sf plugins install sfdx-hardis
> sf plugins install @salesforce/plugin-packaging
> sf plugins install sfdmu
> sf plugins install sfdx-git-delta
> sf plugins install texei-sfdx-plugin

Una vez instalada tiene el siguiente aspecto:

![[Pasted image 20240925163838.png]]

![[Pasted image 20240925164002.png]]

Desde este panel observamos si se han instalado correctamente las dependencias necesarias, las marcadas con warning no es necesario actualizarlas urgentemente. El comando para el update es el siguiente:

> echo y | sf plugins:install sfdx-hardis && echo y|sf plugins:install @salesforce/plugin-packaging && sf hardis:work:ws --event refreshPlugins --websocket localhost:2702

