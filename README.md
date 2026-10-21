# SRI_Bosco
Aqui se documentará y se expondran las evidencias del trabajo de la UT1.

## Apartado 1 
![](<ut1/Evidencias/Crear VPC.png>)
Crearemos la vpc con las especificaciones necesarias.

![](<ut1/Evidencias/Crear Subred.png>)
Creamos la subred en base a la vpc que hemos creado anteriormente.

![](<ut1/Evidencias/IPV4.png>)
Habilitaremos la opcion de asignacion automática de IPV4.

![](<ut1/Evidencias/igw.png>)
Creamos la puerta de enlace a internet.

![](<ut1/Evidencias/asignarigw.png>)
Una vez creada la añadimos a la VPC que creamos anteriormente.

![](<ut1/Evidencias/rt.png>)
Crearemos una tabla de rutas para la VPC.

![](<ut1/Evidencias/asignarrt.png>)
Ya creada la tabla de rutas interconectaremos nuestra puerta de enlace con internet.

![](<ut1/Evidencias/sg2.png>)
Configuraremos el grupo de seguridad para nuestra red, y lo creamos.

Configuramos la instancia de la siguiente manera:
![](<ut1/Evidencias/nombre.png>)
![](<ut1/Evidencias/sistema.png>)
![](<ut1/Evidencias/tipo.png>)
![](<ut1/Evidencias/claves.png>)
![](<ut1/Evidencias/red.png>)
Y lanzamos la instancia.

![](<ut1/Evidencias/hora.png>)
Una vez hayamos iniciando la instancia entraremos en la maquina para actualizar los paquetes necesarios y ponerla en horario de "Madrid".

## Apartado 2
![](<ut1/Evidencias/nginx.png>)
Primer paso de todos instalamos el servicio nginx.

![](<ut1/Evidencias/oculto.png>)
Entramos al archivo de configuracion de nginx con 'sudo nano /etc/nginx/nginx.conf, y debido a que en el archivo el apartado no aparece añadimos el comando server_token off en el apartado http.

![](<ut1/Evidencias/carpeta.png>)
Ya que no tenemos una carpeta propia la crearemos y trabajaremos desde ahi.

![](<ut1/Evidencias/paginaweb.png>)
![](<ut1/Evidencias/archivo.png>)
Una vez creada la web iremos a los archivos de nginx para configurarlo.

![](<ut1/Evidencias/validar.png>)
Validamos el nginx para comprobar que no haya ningun fallo.

![](<ut1/Evidencias/comprobacion.png>)
Comprobamos que entre al servidor como es debido.

## Apartado 3

En este apartado alojaremos 3 webs en nuestro servidor, alojaremos una web principal, un blog, y una intranet.

![](<ut1/Evidencias/web principal 1.png>)
![](<ut1/Evidencias/web principal 2.png>)
![](<ut1/Evidencias/web principal 3.png>)
Empezaremos con la creacion de la Web principal paso a paso.

![](<ut1/Evidencias/blog 1.png>)
![](<ut1/Evidencias/blog 2.png>)
![](<ut1/Evidencias/blog 3.png>)
Seguimos creando y configurando la web del blog.

![](<ut1/Evidencias/intranet 1.png>)
![](<ut1/Evidencias/intranet 2.png>)
![](<ut1/Evidencias/intranet 3.png>)
Y por ultimo la intranet.

![](<ut1/Evidencias/encender.png>)
Ahora vamos a encender los sitios.
Para deshabilitar el sitio temporalmente sin borrar su configuracion simplemente se borrara el archivo del apartado en enable con un "rm", de esta forma siempre quedara la configuracion en available.

![](<ut1/Evidencias/validar 2.png>)
Aplicamos los cambios y reiniciamos el servicio.

Cambiamos las opciones del archivo hosts y comprobamos si las paginas web nos funcionan.

Pagina Web:
![](<ut1/Evidencias/prueba 1.png>)

Blog:
![](<ut1/Evidencias/prueba 2.png>)

## Apartado 4

![](<ut1/Evidencias/php.png>)
Primero instalaremos el modulo de php. 

![](<ut1/Evidencias/fancy.png>)
Instalamos el paquete de fancyindex.

![](<ut1/Evidencias/descargas.png>)
Creamos la carpeta de descargas y en ella 3 archivos.

![](<ut1/Evidencias/hora1.png>)
![](<ut1/Evidencias/hora2.png>)
Creamos un archivo para enseñar el dia y la hora.

![](<ut1/Evidencias/index.png>)
Añadimos la location de "descargas" y la "hora".

### Tabla de contenido

| Módulo | Tipo | Descripción y Uso | Bloque de configuración |
| :--- | :--- | :--- | :--- |
| **`ngx_http_core_module`** | De serie | Proporciona las directivas principales de Nginx (`server_tokens`, `autoindex`). Permite ocultar la versión del servidor e inhabilitar el listado de directorios por defecto. | `http { }` / `server { }` |
| **`ngx_http_fastcgi_module`** | De serie | Permite la comunicación por sockets con procesadores FastCGI externos como PHP-FPM para ejecutar archivos dinámicos `.php` (como `hora.php`). | `location ~ \.php$ { }` |
| **`ngx_http_fancyindex_module`** | Instalado (`apt`) | Genera un listado gráfico e interactivo para directorios. Muestra tamaños legibles (KB, MB) y horas en zona local para la carpeta `/descargas/`. | `location /descargas { }` |

## Apartado 5

![](<ut1/Evidencias/apache.png>)
Para hacer este apartado instalaremos el servicio Apache

![](<ut1/Evidencias/usuarios.png>)
Creamos los usuarios bosco con contraseña usuario@1 y el usuario profesor con contraseña usuario1

Las comprobaciones la he echo en base a mi ip publica de mi ordenador personal, entonces en el archivo de configuracion lo unico que he echo ha sido comentar el apartado "allow" con mi ip publica para que nginx conozca o desconozca a mi ordenador.

Allow sin #:
![](<ut1/Evidencias/allow1.png>)
![](<ut1/Evidencias/conexion3.png>)

Allow con #:
![](<ut1/Evidencias/allow2.png>)
![](<ut1/Evidencias/conexion1.png>)
![](<ut1/Evidencias/conexion2.png>)