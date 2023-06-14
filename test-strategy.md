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
