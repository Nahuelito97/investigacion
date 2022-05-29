# Diseño y Aplicaciones en la web 2022



## Trabajo de investigación Temas:

<img src="./img/angular.svg" class="rounded-circle" alt="Cinque Terre" width="200"/> 


   

## Grupo 3

- Cristaldo Yonathan Ariel 
- Wagner Nahuel


## Tema a investigar
    El tema propuesto para el trabajo de invesigación fue algún frameworck de javascript, el tema que vamos a investigar es Angular




### Que es angular?
    Es un marco de diseño de aplicaciones y una plataforma de desarrollo para crear aplciaciones eficientes y sofistificadas de una sola pagina.

    Es una plataforma de desarrollo, como plataforma incluye:

    - Un marco basado en componentes para crear aplicaciones webs escalabes.
    - Coleccion de bibliotecas integradas que cubren una amplia variedad de funciones, como ser enrrutamiento, gestion de formularios, comunicación cliente-servidor.
    - Herramientas de desarrollo para ayudar al desarrollo, compilación, pruebas y actualziaciones de código. 


### Componentes
Los componentes son los bloques de construcción que componen una aplicación, en un componente se incluye una clase de TypeScript '@Component()' con un decorador, plantilla HTML y estilos.


```html
import { Component } from '@angular/core';

    @Component({
    selector: 'hello-world',
    template: `
        <h2>Hello World</h2>
        <p>This is my first component!</p>
    `
    })
    export class HelloWorldComponent {
    // The code in this class drives the component's behavior.
    }
```

Para usar este componente, escribe lo siguiente en una plantilla:
```html
    <hello-world></hello-world>
```

Cuando Angular representa este componente, el DOM resultante se ve así:

```html
    <hello-world>
        <h2>Hello World</h2>
        <p>This is my first component!</p>
    </hello-world>
```
El modelo de componentes de Angular ofrece una fuerte encapsulación y una estructura de aplicación intuitiva. Los componentes también hacen que su aplicación sea fácil de probar y pueden mejorar la legibilidad general de su código.


### Plantillas

Cada componente tiene una plantilla HTML que declara como se represeta ese componente, la plantilla se define cen la linea o por ruta de archivo.
Angular actualiza automáticamente el DOM renderizado cuando cambia el estado de su componente.

```html
   <p>{{ message }}</p>
```
## Caracteristicas

caracteristica, ventajas, desventajas, instalacion, demo
comparacion con otros fm de js, cuando se creo, por que, con que objetivos.

    
---
## Tecnologías 



---
## Analisis de dominio.



---

## Acerca de este Proyecto


--- 

## Configuración.
A continuacion se estara indicando como usar y que se debe de hacer para poder usar y correr esta web de manera local en Windows o en Linux.

**Paso 1:** Tener descargado un servidor, como ser xampp, lamp, Descargar esta versión 7.3.28 / PHP 7.3.28

Link de descarga:
    
- https://www.apachefriends.org/download.html

**Paso 2:** Tener desacargado composer el cual es un manejador de dependencias para php, descargarlo e instalaro de manera global para todos los usuarios. 

Link de descarga: 

- https://getcomposer.org/download/

**Paso 3:** Descargar postgresql-9.4.26 el cual ya viene incluido con PgAdmin en su versión III, es un gestor de bases de datos.
Descargar la version postgresql-9.4.26-1-windows-x64.

Link de descarga:
- https://www.postgresql.org/download/windows/



Despues de haber descargado e instalado las tecnologías mencionadas en los pasos anteriores, debemos de realizar estos pasos.

**Paso 4:** Dirijirse a este link para descargar o clonar el proyecto desde el repositorio el cual está en GitHub:

Enlace:
- https://github.com/Nahuelito97/blog

**Paso 5:** Una ves descargado el proyecto, debemos de colocarlo en nuestro servidor, en este caso xammp, dirijirse a la siguiente ruta:
    
    c/xampp/htdocs/

**Paso 6:** Crear una base de datos en postgres.

**Paso 7:** 
- Abrir la carpeta del proyecto con un editor de código.
- Cambiar el nombre del archivo ".env.example" por ".env".
- En el archivo .env modificar los siguiente:
  
    ![](figuras/MYS.jpg)

    por esto

    ![](figuras/env.jpg)

    para poder correr este proyecto.
    
- Abrir una consola en el editror de código y ejecutar los siguientes comandos:
    ```bash
    #instala las dependencias de composer
    composer install

    # comentar esto en AppServiceProvider.php
    // $categories = Category::take(5)->get();
    // View::share('categories', $categories);
    
    #actualizar composer
    composer update
    composer dump-autoload

    #generar la clave de la aplicación
    php artisan key:generate

    #migrar las tablas a la base de datos y genera los seeders
    php artisan migrate --seed

    # abiliatar en AppServiceProvider.php 
    $categories = Category::take(5)->get();
    View::share('categories', $categories);

    #para ejecutar la aplicación 
    php artisan serve
    ``` 
- Luego de haber ejecutdo todos estos comandos, ingresar desde el navegador a http://127.0.0.1:8000/


---
# Investigación para poder usar postgreSQL como base de datos para poder crear un blog, usando bootstap


**Paso 1:** En el editor de código lo primero que debemos de hacer luego de haber creado un nuevo proyecto es lo siguiente, ir al archivo .env ubicado en la raíz de nuestro proyecto.

![](figuras/example.jpg)

Ya en el archivo se deben de cambiar los parámetros de la base de datos a la cual deseamos tener la conexión.

Al crear un nuevo proyecto viene por defecto la configuración para conectarse a MYSQL, como muestra la siguiente imagen.


![](figuras/MYS.jpg)

debemos de cambiar los parametros de conexión por lo que nos muestra la siguiente imagen.

![](figuras/env.jpg)

Despues de haber cambiado nuestra configuración debemos de dirigirnos al siguiente Archivo "database.php" ubicado en la siguiente Ruta: "Config > database.php" en ese archivo debemos de buscar y reemplazar los siguientes parametros.
```bash
   #Debemos de cambiar la conexón por defecto 
   'default' => env('DB_CONNECTION', 'mysql'),

   #a

   #Esta conexión para poder conectarlo a postgres.
    'default'=>env('BD_CONNECTION','pgsql'),

``` 
  
una ves finalizado el cambio, en nuestro php.ini debemos de habilitar los drivers de conexión de php para Postgres.

![](figuras/habilitar.jpg)

debemos de habilitar los siguientes:            

- php_pdo_pgsql
- php_pgsql

Luego en la consola finalizamos limpiando la cache:
```bash
    composer dump-autoload

    php artisan view:clear

    php artisan cache:clear

    php artisan migrate
```

Para poder utilizar bootstrap debemos de dirijirnos a la web en el siguiente enlace:

- https://getbootstrap.com/docs/4.6/getting-started/introduction/


Dirijirse a la pagina de bootstrap y copiar los CDNS de los archivos css y js.

## Laravel

El marco PHP para artesanos web
Laravel es un marco de aplicación web con una sintaxis elegante y expresiva. Ya hemos sentado las bases, permitiéndole crear sin preocuparse por las pequeñas cosas.

## Esta captura muestra una parte del sitio desarrollado con Bootstrap.



![](figuras/posts.jpg)




**Este blog seguira en constante desarrollo y con actualizaciones a nivel Front-End y Back-End ya que el mismo sera utilizado para comartir información y conocimientos que vaya adquiriendo a medida que vaya desarrollando mas sitios webs.**

**Este blog sera anexado a mi portafolio el cual se encuentra en desarrollo.**

<img src="./public/img/brand.png" class="rounded-circle" alt="Cinque Terre" width="100" height="100"> 

<span class="badge badge-warning text-uppercase">Nahuel Wagner</span>