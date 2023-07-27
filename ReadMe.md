# Resumen

En este repositorio se muestran algunas anotaciones y ejercicios que he realizado para comprender temas relacionados con HTLM, React, CSSS y SSAS

## Estructura de la hoja de estilos

### Top-level statements

son declaraciones globales, se usan en la parte superior de la hoja de estilos

Imports
Definición de Mixin 
Definición de una Función 
Módulos 

Universa Stataments 

    se usan en cualquier parte de la hoja de estilos. 
    Incluye a las variables, estructuras de control y las reglas @error, @warn y @debug.
    Declaraciones css: reglas de estilo, ar-rules y mixins. 

Tipos de variables
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


Importar compoentes en el sytle.scss principal: @import './components/navbar'; los componentes se nombran con un '_' inicial 



Conceptos básicos de CSS - Tipos de SELECTORES:
* De tipo: seleccionamos el nombre de la etiqueta. Se usa para códigos pequeños
    <div>
        <p> Hola Mundo</>
    <div/>
    <style>
        div{
            background: pink;
        }
    </style>
[*] De clase: .elemento
[*]De ID: #iddelelemento
[*]De atributo: a[]

    <a href  = 'www.unapagina.com'></a>
    <style>
        a[href='www.unapagina.com']{
            color: orange;
        }
    </style>
* universal: *{}

