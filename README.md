# Examen_Final_Kotlin

## 1. EJERCICIO #1 - ERROR EN AL MOMENTO DE REASIGNAR LA VARIABLE

#### 1.1 CODIGO CORREGIDO
fun main() {
    var edad = 20 
    edad = 25
    println(edad)
}

#### 1.2 RESULTADO
<img width="311" height="65" alt="image" src="https://github.com/user-attachments/assets/19f4d35c-8673-4770-919e-8956042efedf" />

#### 1.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: El código intenta reasignar el valor de edad a 25 (edad = 25) , pero la variable fue declarada usando val (val edad = 20). En Kotlin, val se utiliza para declarar variables inmutables (de solo lectura).

#### SOLUCIÓN: Para poder modificar el valor de una variable después de su inicialización, debes declararla usando la palabra clave var



## 2. EJERCICIO #2 - ERROR EN AL MOMENTO DE HACER COMPARACIONES E IGUALDADES

#### 2.1 CODIGO CORREGIDO
fun main() {
    val x = 10
    if (x == 10) {
        println("Correcto")
    }

#### 2.2 RESULTADO
<img width="266" height="69" alt="image" src="https://github.com/user-attachments/assets/2b43c6ab-6902-4880-a42c-9f9797d651be" />

#### 2.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: En la condición del if, se está utilizando un solo signo de igual (x = 10). Un solo = es un operador de asignación, no de comparación.

#### SOLUCIÓN: Para comparar si dos valores son iguales, debes usar el operador de igualdad que consta de dos signos iguales (==)



## 3. EJERCICIO #3 - ERROR EN AL DECLARAR LA VARIABLE NOMBRE

#### 3.1 CODIGO CORREGIDO
fun main() {
    val nombre: String = "Junior"
    println(nombre)
}

#### 3.2 RESULTADO
<img width="242" height="49" alt="image" src="https://github.com/user-attachments/assets/b62dc19b-0bce-4f5e-a240-23d6d75929c1" />

#### 3.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: La variable nombre es declarada indicando que es de tipo String (val nombre: String) , pero se intenta imprimir (println(nombre)) sin haberle asignado nunca un valor.

#### SOLUCIÓN: Kotlin requiere que las variables estén inicializadas (que tengan un valor asignado) antes de ser utilizadas para evitar errores de valores nulos (NullPointerException).



## 4. EJERCICIO #4 - ERROR EN LA CONDICION LOGICA

#### 4.1 CODIGO CORREGIDO
fun main() {
    val nota = 15
    when {
        nota >= 11 -> println("Aprobado")
        else -> println("Desaprobado")
    }
}

#### 4.2 RESULTADO
<img width="254" height="52" alt="image" src="https://github.com/user-attachments/assets/219cc53a-7516-4855-b544-8393736caf8a" />


#### 4.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: La estructura when(nota) recibe la variable nota como argumento , pero dentro de las opciones se están evaluando expresiones booleanas como nota >= 11. Esto no es válido cuando when recibe un argumento directo.

#### SOLUCIÓN: Para usar condiciones lógicas (como mayor o menor que) dentro de un when, debes omitir el argumento en los paréntesis de la declaración del when. De esta forma, actuará como una cadena de sentencias if-else.



## 5. EJERCICIO #5 - ERROR EN EL BUCLE FOR

#### 5.1 CODIGO CORREGIDO
fun main() {
    for (i in 1..5) {
        println(i)
    }
}

#### 5.2 RESULTADO
<img width="256" height="150" alt="image" src="https://github.com/user-attachments/assets/39536896-27b7-4c7a-a909-232fa0160225" />


#### 5.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: Se está intentando usar la sintaxis tradicional de un ciclo for de lenguajes como Java o C (for(i i=1 i <= 5; i++)). Esta sintaxis no existe en Kotlin.

#### SOLUCIÓN: En Kotlin, los bucles for se manejan a través de rangos (ranges) utilizando la palabra clave in.



## 6. EJERCICIO #6 - ERROR EN LA ASIGNACIÓN DE LLAVES

#### 6.1 CODIGO CORREGIDO
fun main() {
    val numero = 5
    if (numero > 10) {
        println("Mayor")
    } else {
        println("Menor")
    }
}

#### 6.2 RESULTADO
<img width="299" height="79" alt="image" src="https://github.com/user-attachments/assets/3e3eee6c-e0b4-48dc-bd7e-994760a67b21" />


#### 6.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: Técnicamente, este código compilará sin problemas porque el bloque else solo tiene una línea de código (println("Menor")). Sin embargo, en evaluaciones de buenas prácticas, se considera un error o una mala práctica omitir las llaves {}.

#### SOLUCIÓN: Siempre es recomendable encerrar los bloques de código if y else entre llaves {} para evitar errores lógicos a futuro si decides agregar más líneas, además de que mejora la legibilidad.





## 7. EJERCICIO #7 - ERROR EN LA EXPRESIÓN WHEN Y CIERRE DE LLAVES

#### 7.1 CODIGO CORREGIDO
fun main() {
    val nota = 18
    when {
        nota >= 18 -> println("Excelente")
        nota >= 11 -> println("Aprobado")
        else -> println("Desaprobado")
    }
} // Llave de cierre que faltaba

#### 7.2 RESULTADO
<img width="323" height="86" alt="image" src="https://github.com/user-attachments/assets/570dd557-219e-4f15-9729-237553318de1" />


#### 7.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: Este fragmento tiene dos errores. Primero, comete el mismo error lógico que el ejercicio 4: usa when(nota) y luego intenta evaluar nota >= 18. Segundo, falta la llave de cierre } del bloque when y del main al final.

#### SOLUCIÓN: Se debe remover el argumento del when para que acepte expresiones booleanas, y se deben cerrar las llaves correctamente para que el código pueda compilar.




## 8. EJERCICIO #8 - ERROR AL MOMENTO EN LA FUNCIÓN

#### 8.1 CODIGO CORREGIDO
fun saludo(): String { 
    return "10" 
}

fun main() {
    println(saludo())
}

#### 8.2 RESULTADO
<img width="288" height="59" alt="image" src="https://github.com/user-attachments/assets/5222c30e-e931-46c2-a680-1867641e6e68" />


#### 8.3 EXPLICACIÓN DE LA CORRECCIÓN
#### ERROR: solo se define la estructura de la función saludo(), pero no se incluye una función main()

#### SOLUCIÓN: se debe agregar la función main() e invocar a tu función dentro de ella.



