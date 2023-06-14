Durante la revision tuve los siguientes hallazgos.

1. al momento de ejecutar en el navegador el codigo, ingresaba un numero, pero al presionar el boton no sucedia ninguna accion. asi que revise el codigo y encontre:
2         a) Faltaba un punto al querer usar la clase lowOrHi en el selector. linea 49
          b) El evento de escucha del boton estaba mal escrito.

Despues de corregir lo anterior, pude ejecutar el boton y se observo lo siguiente:

          a) solo da 5 intentos y no los 5 esperados.
          b) solo genera numeros de 1 al 10
          c) Siempre en el ultimo intento te dice, Felicitaciones adivinaste, aunque en los 5 intentos usaras el mismo numero.
          d) los colores de los mensajes estan incorrectos.
          e) acepta el ingreso de decimales y no despliega ningun mensaje, ya sean en esta forma 1.2 o 1,2.
          
 Soluciones>
 
        a) corregir linea 46, const ATTEMPS = 5  por const ATTEMPS = 10
        b) cambie la funcion en la linea 44 let randomNumber = Math.random() * 10; por la funcion let randomNumber = Math.floor(Math.random() * 100) + 1. ya que la funcion anterior genera numeros aleatorios decimales. en cambio la nueva funcion genera solo enteros.
        c) en la linea 31, cambie el input de tipo text a tipo number para que acepte numeros enteros y no letras.
        d) agregue una validacion para asegurarme que el valor que ingrese el usuario en el input sea un numero entero. ya que con el cambio anterior no se pueden agregar letras y muestra una alerta cuando se agrega un numero con punto decimal o coma, ademas toma el primer valor antes del signo. ejemplo: ingresa 56.5 solo tomara el 56, el resto lo ignora.
        e) Se actualizo el mensaje de felicitanes para que muestre el color correcto si el usuario adivina antes de los 10 intentos. ya que antes lo mostraba en rojo, ahora lo muestra en verde.
        f)se actualizo el mensaje cuando el usuario no adivina el numero despues de los 10 intentos, ahora muestra el mensaje perdiste... el numero correcto era X (x es el numero a adivinar) y el bckg del mensaje es rojo.
        g) se cambio el estilo de los mensajes anteriores para que muestre en blanco sobre fondo negro.
        
