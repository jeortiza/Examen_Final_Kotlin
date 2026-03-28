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
