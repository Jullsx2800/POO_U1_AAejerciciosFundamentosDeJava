# Ejercicio 11 (Tag Content Extractor)

En un lenguaje basado en etiquetas como XML o HTML, el contenido está encerrado entre a etiqueta de inicio y un etiqueta final como <tag>contents</tag>.

## Descripción

-Formato de entrada

La primera línea de entrada contiene un solo número entero, N (el número de líneas).
El N Las líneas subsiguientes contienen cada una una línea de texto.

-Restricciones

1 <= N <= 100

Cada línea contiene un máximo de 10^4 caracteres imprimibles.

El número total de caracteres en todos los casos de prueba no excederá 10^6

-Formato de salida

Para cada línea, imprima el contenido incluido dentro de etiquetas válidas.

Si una línea contiene varias instancias de contenido válido, imprima cada instancia de contenido válido en una nueva línea; si no se encuentra contenido válido, imprima None.


## Datos de Entrada y Salida

+ Datos de entrada 

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498108972643913828/image.png?ex=69eff634&is=69eea4b4&hm=12e597a7fc87cc275e71d22ff074bc7786d1f6b333e207ce2008ff0be2b11a4b&" alt="DE">
</div>

+ Datos de salida

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498109587851579522/image.png?ex=69eff6c7&is=69eea547&hm=ea2bfd36dc7ba5d420939dc9cebb47e31bd76c8c9b2e05a5c70022c0685b96e2&" alt="DS">
</div>

## Código Fuente

```
//Julian Merino
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int testCases = Integer.parseInt(in.nextLine());
        
        // Expresión regular para encontrar etiquetas y su contenido
        Pattern tagPattern = Pattern.compile("<([^>]+)>([^<]+)</\\1>");
        
        while (testCases > 0) {
            String line = in.nextLine();
            Matcher matcher = tagPattern.matcher(line);
            boolean foundValidContent = false;

            while (matcher.find()) {
                System.out.println(matcher.group(2));
                foundValidContent = true;
            }

            if (!foundValidContent) {
                System.out.println("None");
            }

            testCases--;
        }
    }
}

```
Este código es fundamental para principiantes porque introduce el uso de Expresiones Regulares (Regex) mediante las clases Pattern y Matcher, herramientas esenciales para realizar búsquedas y extracciones de texto complejas de forma automatizada.

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498110142493884496/image.png?ex=69eff74b&is=69eea5cb&hm=4f53b1e39466d6dde46da9bb4463b7c862cb89255aa2e6d05f8049ef59652001&" alt="Ejercicio 11">
</div>
