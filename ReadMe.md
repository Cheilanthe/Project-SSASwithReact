# Resumen

En este repositorio se muestran algunas anotaciones y ejercicios que he realizado para comprender temas relacionados con HTLM, React, CSSS y SSAS

## Estructura de la hoja de estilos

### Top-level statements

son declaraciones globales, se usan en la parte superior de la hoja de estilos

Imports
Definición de Mixin 
Definición de una Función 
Módulos 

##### Universa Stataments 

    se usan en cualquier parte de la hoja de estilos. 
    Incluye a las variables, estructuras de control y las reglas @error, @warn y @debug.
    Declaraciones css: reglas de estilo, ar-rules y mixins. 

##### Tipos de variables
En sasss pueden ser declaradas en cualquier parte de la hoja de estilos. Es importante el uso de $ 

$primary-color: blue;

Variables CSS - pueden tener distintos vales para distintos elementos y son declarativas.
Variables SASS - Tienen un calor único corresponde a un elemento y son imperativas. 

!default flag - Se encarga de asignar un valor a la variable si y solo si esta variable no está definida o su valor es null. 

SELECTORES
Un selector de CSS define sobre qué elementos se aplicará un conjunto de reglas CSS
existen selectores de tipo: 
*Clase
*Id 
*Tipo
*Atributo

También ha SCOPE. Las variables locales están declaradas en {}. Cualquier selector anidado puede acceder a las variables locales declaradas dentro del selector. 
También están las variables globales. 

SHADOWING: Las variables locales y globales pueden tener los mismos nombres, ya que se encuentran en diferente nivel de scope. Esto puede ayudar a que no se llegue a modificar por error el valor de las variables globales.

!global flag - Se usa cuando se quiere modificar el valor global de una variable dentro del scope de una variable local.


Importar compoentes en el sytle.scss principal: @import './components/navbar'; los componentes se nombran con un '_' inicial. 

### Conceptos básicos de CSS - Tipos de SELECTORES:
* De tipo: seleccionamos el nombre de la etiqueta. Se usa para códigos pequeños
    <div>
        <p> Hola Mundo</>
    <div/>
    <style>
        div{
            background: pink;
        }
    </style>
* De clase: .elemento
* De ID: #iddelelemento
* De atributo: a[]

    <a href  = 'www.unapagina.com'></a>
    <style>
        a[href='www.unapagina.com']{  
            color: orange;
        }
    </style>
* universal: *{}

### Selectores combinados 
+ Descendientes: El que esta a la derecha es el padre y el de la izq. es el hijo directo. div p 
+ Hijo directo el elemento tiene que estar directamente dentro del selectos padre. div > p
+ Elemento adyacente:  div + p
+ General de hermanos: selecciona a los que estén en el mismo nivel. div ~ p

### Pseudoclases           Psudoelementos
* : active              :: after
* : focus               :: before
* : hover               :: fist-letter
* : nth-child           :: placeholder
<>
/*selector base*/
        p{
            color: black;
        }
        p:hover{
        color: blue;
        }
        el div:p nth-child(2) indica el numero del hijo al que se le aplicará un estilo. 

        https://css-tricks.com/pseudo-class-selectors/

### Cascada y especificidad 
La especificidad consiste en dar un valor a una regla CSS sobre qué tan específicos es el estilo. Entre mayor especificidad mayor porbabilidad de que se ejecuten correctamente. 
La relevancia es descendiente: El orden de las reglas importan, las instrucciones se ejecutan en orden. Los estilos se pueden sobreescrbir.

#### Arquitecturas de CSS
Las arquitecturas se encargan de manejar una norma de código para que cualquiera pueda añadir o quitar funcionalidad sin mucho trabajo. 
El objetivo de las arquitecturas es que: sean ppredecibles, reutilizables,, Mantenible y Escalable. 

* Orientado a Objetos (Object Oriented CSS) - Consiste en separar la estructura principal y la cascara. Separa al contenerdor del contenido y a los objetos de sus mascaras (diseño). 

* BEM (Block Element Modifier) - define a un bloque con elementos y modificadores.
        Bloques: es la estructura principal contenedora de elementos. 
        Elementos: Es el elemento HTML que vive en el contenedor
        Modificador: Son estilos de cada uno de los elementos. 
* Atomic Design - Maneja los elementos como estructura mínima. A partiir de la union de varios elementos se diseña la página. 
        - Átomos
        - Moléculas
        - Organismos
        - Plantillas
        - Páginas
* Triángulo invertido 
*Escalable y modular (Scalable and Modilar Architecture for CSS, SMACSS).

