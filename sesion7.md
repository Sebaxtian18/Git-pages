<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


# Actividad: Ejecicios Array - ArrayList

1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.
Ejemplo Array
2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.
# Solucion
1.
```java 
import java.util.Arrays;

/**
 *
 * @author zseba
 */
public class Mavenproject1 {

    public static void main(String[] args) {
        //Aqui se crea y se inicializa un array con un tamaño de 5 enteros.
        int[] numeros = {5, 2, 10, 7, 1};

        //imprime en pantalla el array inicializado en la operacion anterior, haciendo uso de la biblioteca de (import java.util.Arrays;)
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Suma todos los elementos que hay dentro del array utilizando un iterador (for) y la propiedad .length (Tamaño del array) y por ultimo lo imprime en pantalla. 
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```
2. 
### Ejemplo de Array. 
```java
/**
 *
 * @author zseba
 */
public class Mavenproject1 {

    public static void main(String[] args) {
        //Primero procedomos a crear el array. (Este array va a ser te tipo String).
        String[] cars = new String[8];
        //Despues procedemos a inicializar nuestro array.
        cars[0] = "Volvo";
        cars[1] = "BMW";
        cars[2] = "Mercedes";
        cars[3] = "Toyota";
        cars[4] = "Cupra";
        cars[5] = "Peugeot";
        cars[6] = "VolksWagen";
        cars[7] = "Pagani";
        //Ahora procedomos a llamar y mostrar el contenido de cada indice. Se puede hacer uno por uno o todos a la vez.
        //Miremos commo se llaman individualmente.
        String valor = cars[5];
        System.out.println("Esta es la muestra del indice individual: " + valor);
        System.out.println("--------------------------------------------------");
        //ahora veamos como hacer para llamar todos los indices al tiempo.
        //En este caso utilice el (for-each) para hacer la iteracion, ya que esta no requiere de un contador para iterar sobre cada elemento del Array lo que lo hace perfecto para manejar este caso, ya que el array es de tipo (String) y no podemos utilizar numeros para el contador. 
        for (String car : cars) {
            System.out.println("Esta es la muestra del indice utilizando el iterador: " + car);
        }
    }
}
```
### Ejemplo de ArrayList

```java
import java.util.ArrayList;

/**
 *
 * @author zseba
 */
public class Mavenproject1 {

    public static void main(String[] args) {
        //Creamos nuestro ArrayList, pero antes tenemos que agregar a las dependencia el (import java.util.ArrayList;) para que nuestro sistema lo rastree.
        ArrayList<String> monedaInternacional = new ArrayList<>();
        //Procedemos a inicializar nuestro ArrayList y agragarle los valores.
        monedaInternacional.add("Dolar");
        monedaInternacional.add("Euro");
        monedaInternacional.add("Dolar Canadience");
        monedaInternacional.add("Yen Japones");
        for (String moneda : monedaInternacional) {
            System.out.println(moneda);
        }
        System.out.println("--------------------------------------------------");
        //Ahora vamos a agregar un par de monedas mas, pero no a la cola del array sino a respectivos puestos ya definidos para darle prioridad a estas nuevas.
        monedaInternacional.add(2, "Libra esterlina");
        monedaInternacional.add(3, "Franco suizo");
        monedaInternacional.add(4, "Dolar hongkonés");
        //Ahora removere el Dolar Canadience. Lo puedo hacer por su nombre o por el indice.
        //por el nombre seria: monedaInternacional.remove("Dolar canadiense");
        //Por el indice seria:
        monedaInternacional.remove(5);
        //Ahora vemos el resultado hasta el momento se deben de haber agregado tres elementos y eliminado uno.
        for (String moneda : monedaInternacional) {
            System.out.println(moneda);
        }
        System.out.println("--------------------------------------------------");
        //Quiero ver que hay en el indice #4 para eso voy a utilizar el siguiente comando.
        String moneda = monedaInternacional.get(4);
        System.out.println(moneda);
        System.out.println("--------------------------------------------------");
        //para ver el tamaño de un arraylist utilizamos la funcion size.
        int size = monedaInternacional.size();
        System.out.println(size);
    }
}        
```
        