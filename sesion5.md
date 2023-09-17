<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 

# Actividad 5: Ejercicios de bucles
## Resolver los siguientes ejercicios:

### Ejercicios - while
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.
### Ejercicios - do while
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.
### Ejercicios - for
1. Imprimir los números impares del 1 al 50.
2. Imprimir los números primos del 1 al 100.
## Solucion

### Los primeros ejecicios con While y Do while fueron realizados en clase.

```java
package com.repaso.actividad5;

import java.util.Scanner;

/**
 *
 * @author zseba
 */
public class Actividad5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);

        // Solicitar al usuario su peso en kilogramos y estatura en metros
        System.out.print("Ingrese su peso en kilogramos: ");
        double peso = scanner.nextDouble();

        System.out.print("Ingrese su estatura en metros: ");
        double estatura = scanner.nextDouble();

        // Calcular el índice de masa corporal (IMC)
        double imc = peso / (estatura * estatura);

        // Mostrar el IMC
        System.out.printf("Su IMC es: %.2f\n", imc);

        // Calcular el porcentaje de masa muscular basado en el IMC
        double porcentajeMasaMuscular;

        if (imc < 16) {
            porcentajeMasaMuscular = 5.0;
        } else if (imc >= 16 && imc < 17) {
            porcentajeMasaMuscular = 10.0;
        } else if (imc >= 17 && imc < 18.5) {
            porcentajeMasaMuscular = 15.0;
        } else if (imc >= 18.5 && imc < 25) {
            porcentajeMasaMuscular = 20.0;
        } else {
            porcentajeMasaMuscular = 25.0;
        }

        // Mostrar el porcentaje de masa muscular
        System.out.printf("Su porcentaje de masa muscular es: %.2f%%\n", porcentajeMasaMuscular);

    }
}
```