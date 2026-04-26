# Ejercicio 6 (Java Datatypes)

Java tiene 8 tipos de datos primitivos; char, booleano, byte, corto, int, largo, flotante y doble. Para este ejercicio, trabajaremos con las primitivas utilizadas para contener valores enteros (byte, corto, int, y largo)

## Descripción

-Formato de entrada

La primera línea contiene un número entero, T , que indica el número de casos de prueba.
Cada caso de prueba, T , se compone de una sola línea con un número entero, n , que puede ser arbitrariamente grande o pequeño.

-Formato de salida

Para cada variable de entrada n y primitivo apropiado dataType, debes determinar si las primitivas dadas son capaces de almacenarlo.

Si hay más de un tipo de datos apropiado, imprima cada uno en su propia línea y ordénelos por tamaño.

Si el número no se puede almacenar en una de las cuatro primitivas mencionadas anteriormente, imprima la línea:

**n can't be fitted anywhere.**

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 5 <br> -150 <br> 150000 <br> 1500000000 <br> 213333333333333333333333333333333333 <br> -100000000000000 | -150 can be fitted in: <br> * short <br> * int <br> * long <br> 150000 can be fitted in: <br> * int <br> * long <br> 1500000000 can be fitted in: <br> * int <br> * long <br> 213333333333333333333333333333333333 can't be fitted anywhere. <br> -100000000000000 can be fitted in: <br> * long |


## Código Fuente

```
//Julian Merino
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh)
    {
        Scanner sc = new Scanner(System.in);
        int t=sc.nextInt();

        for(int i=0;i<t;i++)
        {
            try
            {
                long x=sc.nextLong();
                System.out.println(x+" can be fitted in:");
                if(x>=-128 && x<=127)System.out.println("* byte");
                if(x >= Short.MIN_VALUE && x <= Short.MAX_VALUE) {
                    System.out.println("* short");
                }
                if(x >= Integer.MIN_VALUE && x <= Integer.MAX_VALUE) {
                    System.out.println("* int");
                }
                System.out.println("* long");
            }
            catch(Exception e)
            {
                System.out.println(sc.next()+" can't be fitted anywhere.");
            }
        }
    }
}

```
Este código es fundamental para principiantes porque enseña la gestión de tipos de datos y sus límites de memoria, permitiendo entender qué espacio ocupa cada variable en el sistema.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498095865317949641/image.png?ex=69efe9ff&is=69ee987f&hm=55cd677fcadccf8e6cad6587257303f0d9bbd602cfd021dc92c879d64707b23c&" alt="Ejercicio 6">
</div>
