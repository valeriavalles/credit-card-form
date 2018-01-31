# Function-scope-js

## OBJETIVO

Reconocer o identificar los siguientes puntos dentro del app.js .


* Funciones globales
* Funciones locales
* funciones de callback
* expresions
* statement,
* clousure, 
* scope,
* contextos de ejecucion, 
* funciones forman parte de la pila de ejecucion (stack execution)
* Funcion de la cola de eventos

## FUNCIONES GLOBALES

Como funcion global tenemos a

> $(document).ready(function() { }

que viene a ser padre de las demas funciones .

## FUNCIONES LOCALES 

Como funciones locales respecto al object window tenemos a :

> function activeButton() { 
    $buttonNext.attr('disabled', false);
  } 

> function desactiveButton() {  
    $buttonNext.attr('disabled', true);
  } 

> function longitud(input) { 
  } 
  
> function soloNumeros(input) {
  } 

> function isValidCreditCard(number){
  }

## FUNCIONES CALBACK

En resumen Las funciones calback  es pasar una función como parámetro para que dicha función se encargue de ejecutar nuestro parámetro.

En el caso del codigo al unico que podria considerar como funcion calback es 

> $inputCard.on('input', function() {
    isValidCreditCard($(this).val().trim());
  });

 que contiene otra funcion llamda isValidCreditCard();
 que  luego vuelve ha ser llamada o invocada.

 ## FUNCIONES EXPRESIONS 

 Las funciones expresions o tambien llamadas funciones como expresión con nombre por ejemplo:

 > var factorial = function fact(number) {
  }

 En el codigo app.js no contamos con ninguna function expresions.

 ## CLOUSURE 

 Un closure es una función que es libre de variables, esto quiere decir que las variables de la función padre funcionan, pero el closure no tiene variables propias.

 ## SCOPE
 
 El scope es el campo de alcance y  determina la accesibilidad (visibilidad) de las variables. 
 en el codigo.

 >  function soloNumeros(input) {
    var regex = /^[0-9]+$/;
    if (regex.test(input)) {
      return input;
    }
  }
  
  El scope  local es local var regrex que es referida dentro de una misma funcion.
  A las siguientes variables podemos considerar variables globales respecto a las funciones pero no respecto a la funcion anonima padre, a esta podriamos referirnos scope global respecto a las funciones hijas.

  > var $inputCard = $('#card-number');

  > var $inputMonth = $('.input-month');

  > var $inputYear = $('.input-year');

  > var $buttonNext = $('#next');

  > var regexOnlyNumbers = /^[0-9]+$/;

  > var labelErrorOrSuccessMessages = $('label[for="card-number"]');












