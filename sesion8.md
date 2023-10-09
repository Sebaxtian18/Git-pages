<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


# Actividad: Ejecicios de métodos en Java
Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

# Solución
1. 
```java
    import java.util.Scanner;

/**
 *
 * @author zseba
 */
public class Mavenproject4 {

    public static void main(String[] args) {
        Scanner Scanner = new Scanner(System.in);
        System.out.println("Funciones y metodos");
        saludar();
        System.out.println("--------------------------------------------------");
        System.out.println("Ingrese el primer numero a comparar");
        int a = Scanner.nextInt();
        System.out.println("Ingrese el segundo numero a comparar");
        int b = Scanner.nextInt();
        int mayor = numeroMayor(a, b);
        System.out.println("el numero mayor es: " + mayor);
    }

    public static int numeroMayor(int a, int b) {
        int maximo;
        if (a > b) {
            maximo = a;
        } else {
            maximo = b;
        }
        return maximo;
    }
    public static void saludar(){
        System.out.println("Hola bienvenid@");
    }
}
```
2. 
```java
    import java.util.Scanner;

/**
 *
 * @author zseba
 */
public class Mavenproject4 {

    public static void main(String[] args) {
        Scanner Scanner = new Scanner(System.in);
        System.out.println("Funcionnes y metodos");
        saludar();
        System.out.println("---------------------------------------------------");
        System.out.println("Escribe un verso de tu cancion favorita");
        String cancion = Scanner.nextLine();
        int contador = contadorDeVocales(cancion);
        System.out.println("--------------------------------------------------");
        System.out.println("Este verso contiene " + contador+ " vocales" );
    }

    public static void saludar() {
        System.out.println("Hola, Bienvenid@");
    }

    public static int contadorDeVocales(String cancion) {
        int i = 0;
        int contador = 0;
        while (i < cancion.length()) {
            char vocales = cancion.charAt(i);
            if (vocales == 'a' || vocales == 'e' || vocales == 'i' || vocales == 'o' || vocales == 'u'
             || vocales == 'A' || vocales == 'E' || vocales == 'I' || vocales == 'O' || vocales == 'U') {
                contador++;
            }
            i++;
        }
        return contador;
    }
}
```
3. 
```java
    /**
 *
 * @author zseba
 */
public class Mavenproject4 {
    
    public static void main(String[] args) {
        String textoOriginal = "La LoCura NuNca TuVo MaEstro";
        String textoInvertido = invertido(textoOriginal);
        System.out.println("Con la inversion de las letras mayusculas por las minusculas quedaria así: " + textoInvertido);
    }

    public static String invertido(String texto) {
        char[] letras = texto.toCharArray();
        for (int i = 0; i < letras.length; i++) {
            if (Character.isUpperCase(letras[i])) {
                letras[i] = Character.toLowerCase(letras[i]);
            } else if (Character.isLowerCase(letras[i])) {
                letras[i] = Character.toUpperCase(letras[i]);
            }
        }
        return new String(letras);
    }
}
```
4. 
```java
    /**
 *
 * @author zseba
 */
public class Mavenproject4 {

    public static void main(String[] args) {
        String textoOriginal = "La LoCura NuNca TuVo MaEstro";
        int cantidadDePalabras = contadorDePalabras(textoOriginal);
        System.out.println("La cadena de texto contiene: " + cantidadDePalabras + " palabras.");
    }

    public static int contadorDePalabras(String texto) {
        
        if(texto == null || texto.isEmpty()){
            return 0;
        }
        String[] palabras = texto.split("\\s+");
        return palabras.length;
    }

}
```
5. 
```java
    /**
 *
 * @author zseba
 */
public class Mavenproject4 {

    public static void main(String[] args) {
        String textoOriginal = "La locura nunca tuvo mastro";
        String cadenaOrdenada = contadorDePalabras(textoOriginal);
        System.out.println("Esta es la cadena ordenada alfabeticamente: " + cadenaOrdenada);
    }

    public static String contadorDePalabras(String texto) {
        String[] palabras = texto.split(" ");
        Arrays.sort(palabras);
        String cadenaOrdenada = String.join(" ", palabras);
        return cadenaOrdenada;
    }

}

```