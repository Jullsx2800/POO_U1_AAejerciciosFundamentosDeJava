# Ejercicio 9 (Java Int to String)

Se te da un número entero , tienes que convertirlo en una cadena.

## Descripción

Complete el código parcialmente completado en el editor. Si su código se convierte correctamente n en una cuerda s El código imprimirá "Buen trabajo". De lo contrario imprimirá "Respuesta incorrecta".

n puede variar entre -100 to 100 inclusivo.


## Datos de Entrada y Salida

| N° | Dato de Entrada | Dato de Salida |
| :---: | :---: | :---: |
| 1 | 100 | Buen trabajo |


## Código Fuente

```
import java.util.*;
import java.security.*;

public class Solution {
    public static void main(String[] args) {

        DoNotTerminate.forbidExit();

        try {
            Scanner in = new Scanner(System.in);
            int n = in.nextInt();
            in.close();

            //Julian Merino
            String s = String.valueOf(n);

            if (n == Integer.parseInt(s)) {
                System.out.println("Good job");
            } else {
                System.out.println("Wrong answer.");
            }
        } catch (DoNotTerminate.ExitTrappedException e) {
            System.out.println("Unsuccessful Termination!!");
        }
    }
}

class DoNotTerminate {
    public static class ExitTrappedException extends SecurityException {
        private static final long serialVersionUID = 1;
    }

    public static void forbidExit() {
        final SecurityManager securityManager = new SecurityManager() {
            @Override
            public void checkPermission(Permission permission) {
                if (permission.getName().contains("exitVM")) {
                    throw new ExitTrappedException();
                }
            }
        };
        System.setSecurityManager(securityManager);
    }
}

```
Este código es fundamental para principiantes porque introduce el concepto de conversión de tipos de datos, enseñando la forma estándar y segura de transformar un valor primitivo (int) en un objeto (String) mediante el método String.valueOf().

## Comprobación por HackerRank

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1494512379105509467/1498105570152943807/image.png?ex=69eff309&is=69eea189&hm=6d3137603cdee41cddef2e81ac6d9d0f6aa9b7652264dc744218fb203cbd5d7a&" alt="Ejercicio 9">
</div>
