# SRI_Bosco
Aqui se documentará y se expondran las evidencias del trabajo de la UT1

## Apartado 1 
![](</SRI_Bosco/ut1/evidencias/Crear VPC.png>)
crearemos la vpc con las especificaciones necesarias

![](</SRI_Bosco/ut1/evidencias/Crear Subred.png>)
creamos la subred en base a la vpc que hemos creado anteriormente

![](</SRI_Bosco/ut1/evidencias/IPV4.png>)
habilitaremos la opcion de asignacion automática de IPV4

![](</SRI_Bosco/ut1/evidencias/igw.png>)
creamos la puerta de enlace a internet

![](</SRI_Bosco/ut1/evidencias/asignarigw.png>)
una vez creada la añadimos a la VPC que creamos anteriormente

![](</SRI_Bosco/ut1/evidencias/rt.png>)
crearemos una tabla de rutas para la VPC

![](</SRI_Bosco/ut1/evidencias/asignarrt.png>)
ya creada la tabla de rutas interconectaremos nuestra puerta de enlace con internet

![](</SRI_Bosco/ut1/evidencias/sg2.png>)
configuraremos el grupo de seguridad para nuestra red, y lo creamos

configuramos la instancia de la siguiente manera:
![](</SRI_Bosco/ut1/evidencias/nombre.png>)
![](</SRI_Bosco/ut1/evidencias/sistema.png>)
![](</SRI_Bosco/ut1/evidencias/tipo.png>)
![](</SRI_Bosco/ut1/evidencias/claves.png>)
![](</SRI_Bosco/ut1/evidencias/red.png>)
y lanzamos la instancia

![](</SRI_Bosco/ut1/evidencias/hora.png>)
una vez hayamos iniciando la instancia entraremos en la maquina para actualizar los paquetes necesarios y ponerla en horario de "Madrid"

## Apartado 2
![](</SRI_Bosco/ut1/evidencias/nginx.png>)
primer paso de todos instalamos el servicio nginx

![](</SRI_Bosco/ut1/evidencias/oculto.png>)
entramos al archivo de configuracion de nginx con 'sudo nano /etc/nginx/nginx.conf, y debido a que en el archivo el apartado no aparece añadimos el comando server_token off en el apartado http

![](</SRI_Bosco/ut1/evidencias/carpeta.png>)
ya que no tenemos una carpeta propia la crearemos y trabajaremos desde ahi

![](</SRI_Bosco/ut1/evidencias/paginaweb.png>)
![](</SRI_Bosco/ut1/evidencias/archivo.png>)
una vez creada la web iremos a los archivos de nginx para configurarlo

![](</SRI_Bosco/ut1/evidencias/validar.png>)
validamos el nginx para comprobar que no haya ningun fallo

![](</SRI_Bosco/ut1/evidencias/comprobacion.png>)
comprobamos que entre al servidor como es debido