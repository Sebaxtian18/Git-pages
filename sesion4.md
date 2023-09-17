<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4

# Actividad 4: Ejercicios de control de flujo con expresiones compuestas
## Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.

2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.

3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.

5. Mostrar toda la información del estudiante si está matriculado en el Cesde.

6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.

7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
0.0 - 3.4: El estudiante no recibe beca.
3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
4.5 - 5.0: El estudiante recibe una beca completa.

## Datos
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args){ 
        System.out.println("Actividad 4 if, else, else if.");
        System.out.println("------------------------------");
        // Variables de tipo String
        String nombre = "Juan Pérez";
        String apellido = "González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
// Variable de tipo int
        int edad = 20;
// Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
// Variable de tipo char
        char género = 'M';
// Variable de tipo double
        double promedio = 4.5;
// Variable de tipo int
        int semestre = 2;
    }
}
```
## Primer punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {

        System.out.println("------------------------------");
        System.out.println("Primer punto.");
        if (edad >= 18 && esActivo == true) {
            System.out.println("El estudiante esta activo y es mayor de edad");
        } else if (edad < 18) {
            System.out.println("El estudiante es menor de edad");
        }
        if (esActivo == false) {
            System.out.println("El estudiante no esta activo");
        }
    }
}    
```
## Segundo punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Segundo punto.");
        if (becado == true || carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante esta becado o estudia Desarrollo de software");
        } else if (becado == false) {
            System.out.println("El estudiante no es becado");
        }
        if (carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante estudia Desarrollo de Software");
        }
    }
}    
```
## Tercer punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Tercer punto.");
        if (semestre >= 9 && esActivo == true) {
            System.out.println("El estudiante esta en el ultimo semestre y tiene matricula activa");
        } else if (semestre < 9) {
            System.out.println("El estudinate no esta en el ultimo semestre");
        }
        if (esActivo == true) {
            System.out.println("El estudiante tiene matricula activa");
        }
    }
}   
```
## Cuarto punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Cuarto punto.");
        if (carrera.equals("Desarrollo de Software") && promedio > 4.0) {
            System.out.println("El estudiante estudia Desarrollo de software y tiene un promedio superior a 4.0");
        } else if (carrera.equals("Desarrollo de software")) {
            System.out.println("El estudinate estudia desarrollo de software");
        }
        if (promedio < 4.0) {
            System.out.println("El estudiante tiene un promedio menor a 4");
        }
    }
}        
```
## Quinto punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Quinto punto.");
        Scanner sc = new Scanner(System.in);
        System.out.println("Ingrese el documento del estudiante");
        String documento = sc.nextLine();
        System.out.println("Juan");
        System.out.println("Pérez González");
        System.out.println("juan.perez@ejemplo.com");
        System.out.println("Desarrollo de Software");
        System.out.println("Cesde");
        System.out.println("Genero " + género);
        System.out.println("20 Años");
        System.out.println("Estado " + "Activo");
        System.out.println("Promedio " + promedio);
        System.out.println("Becado " + "No");
        System.out.println("Semestre  " + semestre);
    }
}        
```
## Sexto punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Sexto punto.");
        if (universidad == "Cesde" && promedio > 4.0 && esActivo == true) {
            System.out.println("Hola, por serparte de Cesde y tu buen desempeño academico queremos otorgarte una beca del 50%.");
        } else {
            System.out.println("Hola, sigue esforzandote por eso que tanto deseas. Nunca pares de aprender");
        }
    }
}        
```
## Septimo punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Septimo punto.");
        if (promedio < 3.4) {
            System.out.println("El estudiante no tiene beca");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante tiene una beca del 25%");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante tiene una beca del 50%");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante tiene una beca del 100%");
        }
    }
}        
```
## Octavo punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Octavo punto.");
        if (carrera == "Desarrollo de Software") {
            System.out.println("Cesde quiere invitarte a la charla sobre las nuevas tecnologias el 15/09/2023 en el auditorio de la sede Bello, con la participacion Jhon Freddy Vega que nos va a hablar de la inteligencia artificial en nuestra era.");
        }
    }
}        
```
## Noveno punto
```java
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Noveno punto.");
        if (esActivo == true) {
            System.out.println("Cesde se sinete orgulloso de tenerte y por eso te seguimos alentando en tus metas. Esta semana tendremos jornada recreativa en las sedes Centro y Bello en la que podras disfrutar de diferentes actividades... ");
        } else {
            System.out.println("Cesde te anima a que vuelvas y continues tu camino al exito con nosotros. Matriculate ya y obten 10% de descuento en " + carrera);
        }
    }
}        
```
## Decimo punto
```java        
/**
 *
 * @author zseba
 */
public class Ifelse {

    public static void main(String[] args) {
        System.out.println("------------------------------");
        System.out.println("Decimo punto.");
        if (edad <= 18) {
            System.out.println("Charla vocacional y proyectos futuros");
        } else if (edad >= 18 && edad <= 25) {
            System.out.println("Emprendimiento y camino laboral efectivo");
        }else{
            System.out.println("Cambios de profecion y busqueda de nuevos conocimientos.");
        }
    }
}        
```






