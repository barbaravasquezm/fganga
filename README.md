# nelson.ganga-inacapmail.cl
Sección 70 Fundamentos de programación 
 
 /* La finalidad de este programana es pedir al usuario dos numeros enteros y 
realizar operaciones matemáticas básicas sobre ellos.*/

package programa;
import java.io.IOException;
import java.util.Scanner;

public class Programa  {
 
    public static void main(String[] args) throws IOException
  {
    //El programa esta diseñado con una estructura secuencial.
    //declaración de variables con diferentes tipos de dato.
    int Numero1, Numero2, Resultado = 0;
    char TipoOperador;
    String Mensaje = "";

    //se crea objeto de clase Scanner (paquete java.util), para realizar entrada estándar de lectura datos por teclado. 
    Scanner sc = new Scanner(System.in);
    //Lectura primer número ingresado por teclado
    System.out.println("Por favor introduzca primer número: "); 
    //Procede a leer el primer numero ingresado
    Numero1 = sc.nextInt(); 
    //Lectura segundo número ingresado por teclado
    System.out.println("Por favor introduzca segundo número: "); 
    Numero2 = sc.nextInt(); 
    //Lectura de tipo de operacion, mediante estructura de Repetición Do While
    do{
      System.out.println("Por favor introduzca el tipo de operación (+,-,*,/): ");
      TipoOperador = (char)System.in.read(); 
    } while((TipoOperador != '+') && (TipoOperador != '-') && (TipoOperador != '*') && (TipoOperador != '/'));
    
    //múltiples alternativas mediante Case (switch)
    switch(TipoOperador) 
    {
      case '-' : Resultado = Numero1 - Numero2;
                 break;
      case '+' : Resultado = Numero1 + Numero2;
                 break;
      case '*' : Resultado = Numero1 * Numero2;
                 break;
      case '/' : if(Numero2 != 0)
                   Resultado = Numero1 / Numero2;
                 else
                   System.out.print("No se puede dividir por cero: ");
                 break;
      default  : System.out.print("Tipo de operador invalido: ");
    }
    
    //Estructura de decisión doble y salida estándar del programa.
     
          if("".equals(Mensaje))
      System.out.print("El resultado es: " + Resultado);
    else
      System.out.println(Mensaje);
  
  } 
    
}

/* Gemima Hernández, Bárbara Vásquez */
