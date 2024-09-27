
Para conectar azure con el entorno destino hardis nos ofrece un comando para automatizar el proceso:

![[Pasted image 20240926122501.png]]

Esto genera 2 variables que son las que debemos incluir como variables en los pipelines:

![[Pasted image 20240926122951.png]]

Luego es necesario bloquear el resto de ramas.

Existen 2 pipelines a dia de hoy:

-CHECK 

Esta pipeline se activa una vez se aprueba un pull request:

![[Pasted image 20240926124413.png]]

En el pipeline que dejo propuesto se pasa un Linter para revisar la calida del deploy, a falta de configurar los criterios es interesante  por ejemplo los escaneos de flujos que detecta elementos harcodeados y malas practicas. Se configura mediante el archivo megalinter.yml


![[Pasted image 20240926124434.png]]

![[Pasted image 20240926124601.png]]

Ademas crear un informe de escaneo de resultados que postea en el work item de azure.

![[Pasted image 20240926124644.png]]

Actualmente el punto de bloqueo viene de  la simulacion de deploy, no consigue autorizarse probar a añadir la flag de -d para umentar detalle del debug:

![[Pasted image 20240926124756.png]]

Para la configuracion de seguridad del pipeline debemos configurarlo de la siguiente forma:

![[Pasted image 20240926125126.png]]

