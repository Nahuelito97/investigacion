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
El valor de mensaje proviene de la clase de componente.

```html
   import { Component } from '@angular/core';

    @Component ({
        selector: 'hello-world-interpolation',
        templateUrl: './hello-world-interpolation.component.html'
    })
    export class HelloWorldInterpolationComponent {
        message = 'Hello, World!';
    }
```
Cuando la aplciacion carga el componente y la plantilla se vera lo siguiente:

```html
   <p>Hello, World!</p>
```


o Ventajas y desventajas
o Comparación entre los otros frameworks
o Pequeño desarrollo
o Proyección a futuro

## Historia

Angular se ha convertido en el framework mas popular para crear aplicaciones de una sola pagína(Single Page Aplciations) 

Angular es mantenido en gran parte por google, asi como por desarrolladores a lo largo del mundo que reportan y ayudan a la mejora del frameworck.

Angular forma parte del Stack *MEAN* el cual es una integración de:
- MongoDB: Como gestor de Bases de Datos.
- ExpressJS: Como aplication web server.
- AngularJS: Encargado del Front-Ende de la aplciación.
- NodeJS: Encargado del Back-End de la aplciación.
  
Los 4 manejasn JavaScript como lenguaje de desarrollo.

## Caracteristicas

caracteristica, ventajas, desventajas, instalacion, demo
comparacion con otros fm de js, cuando se creo, por que, con que objetivos.

    

```bash
   #Debemos de cambiar la conexón por defecto 
   'default' => env('DB_CONNECTION', 'mysql'),

   #a

   #Esta conexión para poder conectarlo a postgres.
    'default'=>env('BD_CONNECTION','pgsql'),

``` 
  


<span class="badge badge-warning text-uppercase">Nahuel Wagner</span>