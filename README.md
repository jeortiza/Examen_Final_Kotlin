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


