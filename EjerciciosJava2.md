# Ejercicio 2 (Java Stdin y Stdoun II)

En este desafío, debes leer un entero, a doble, y a Cadena desde stdin, luego imprima los valores de acuerdo con las instrucciones del Formato de Salida.

## Descripción

-Formato de entrada

Hay tres líneas de entrada:

La primera línea contiene un entero.
La segunda línea contiene un doble.
La tercera línea contiene un Cadena.

-Formato de salida

Hay tres líneas de salida:

En la primera línea, imprimir String: seguido por el inalterado Cadena leído desde stdin.
En la segunda línea, imprimir Double: seguido por el inalterado doble leído desde stdin.
En la tercera línea, imprimir Int: seguido por el inalterado entero leído desde stdin.


## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 42 <br> 3.1415 <br> Welcome to HackerRank's Java tutorials! | String: Welcome to HackerRank's Java tutorials! <br> Double: 3.1415 <br> Int: 42 |


## Código Fuente

```
//Julián Merino
import java.util.Scanner;

public class Solucion {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        
        int i = scan.nextInt();
        double d = scan.nextDouble();
        scan.nextLine(); // Limpiar el búfer
        String s = scan.nextLine();

        System.out.println("String: " + s);
        System.out.println("Double: " + d);
        System.out.println("Int: " + i);
        
        scan.close();
    }
}

```
Este código es fundamental para principiantes porque enseña la gestión polivalente de datos y resuelve el error crítico del "salto de línea" en el búfer al combinar entradas numéricas y de texto.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498079191579754556/image.png?ex=69efda78&is=69ee88f8&hm=35272c3e9707bd1dc513400a8d2136c8df95fec91dbdda85a3166000cad7fc58&" alt="Ejercicio 2">
</div>

<p align="right">
  <a href="PortadaEjercicios.md">Volver a la página principal</a>
</p>
