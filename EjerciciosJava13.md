# Ejercicio 13 (Java Stack)

Una cadena que contiene solo paréntesis se equilibra si se cumple lo siguiente: 1. si es una cadena vacía 2. Si A y B son correctos, AB es correcto, 3. Si A es correcto, (A) y {A} y [A] también son correctos.

## Descripción

-Formato de entrada

Habrá varias líneas en el archivo de entrada, cada una con una única cadena no vacía. Debes leer la entrada hasta el final del archivo.

La parte del código que maneja la operación de entrada ya está proporcionada en el editor.

-Formato de salida

Para cada caso, imprima 'verdadero' si la cadena está equilibrada, 'falso' en caso contrario.

## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | {}() <br> ({()}) <br> {}( <br> [] | true <br> true <br> false <br> true |


## Código Fuente

```
// Julián Merino
import java.util.*;

public class Solucion {
    public static void main(String[] argh) {
        Scanner sc = new Scanner(System.in);
        
        while (sc.hasNext()) {
            String entrada = sc.next();
            Stack<Character> pila = new Stack<>();
            boolean estaEquilibrado = true;

            for (int i = 0; i < entrada.length(); i++) {
                char soporteActual = entrada.charAt(i);
                
                if (soporteActual == '{' || soporteActual == '[' || soporteActual == '(') {
                    pila.push(soporteActual);
                } else {
                    if (pila.isEmpty()) {
                        estaEquilibrado = false;
                        break;
                    }
                    char soporteSuperior = pila.pop();
                    if ((soporteActual == '}' && soporteSuperior != '{') ||
                        (soporteActual == ']' && soporteSuperior != '[') ||
                        (soporteActual == ')' && soporteSuperior != '(')) {
                        estaEquilibrado = false;
                        break;
                    }
                }
            }
            if (!pila.isEmpty()) {
                estaEquilibrado = false;
            }
            System.out.println(estaEquilibrado);
        }
        sc.close();
    }
}

```
Este código es fundamental para principiantes porque introduce la estructura de datos Pila (Stack) y el principio LIFO (Last-In, First-Out), permitiendo resolver problemas complejos de anidamiento y simetría de forma eficiente.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498117595801583727/image.png?ex=69effe3c&is=69eeacbc&hm=fea1f6050a9a8410730140a0a00bf96a078b7c611da657d36a139f2151c835fd&" alt="Ejercicio 13">
</div>

<p align="right">
  <a href="PortadaEjercicios.md">Volver a la página principal</a>
</p>
