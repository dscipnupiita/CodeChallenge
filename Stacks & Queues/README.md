<p align="center">
  <img src="../images/Stack & Queues.png" width="920">
</p>

# Stacks & Queues

## Reto 1: Paréntesis balanceados

Dado una cadena de texto `A` que consiste sólo en paréntesis `(` y `)`
Se requiere conocer si la combinación de paréntesis en `A` está balanceada, si lo está se devuelve un 1, en caso contrario devuelve un 0

### Entradas de ejemplo :
Entrada 1:
```
A = "(()())"
```
Entrada 2:
```
A = "(()"
```
### Salidas de ejemplo:
Salida 1:
```
1
```
Salida 2:
```
0
```

🔗👉Enlace del problema completo https://www.interviewbit.com/problems/balanced-parantheses/

## Reto 2: Cola usando dos pilas

Una cola es un tipo de datos abstracto que mantiene el orden en el que los elementos fueron agregados, esto permite eliminar primero los elementos más antiguos del frente y agregar nuevos elementos al final. Esto se denomina estructura de datos _First In First Out (FIFO)_ porque el primer elemento que se ha agregado a la cola es siempre el primero en ser eliminado.
Una cola básica tiene las siguientes operaciones:
- Enqueue: Añadir un nuevo elemento al final de la cola
- Dequeue: Remover el elemento del frente de la cola y devolverlo

En este reto, deberás implementar una cola utilizando dos pilas. Luego procesar `q` consultas en donde cada petición es de alguno de los 3 siguientes tipos:
1. `1`Enqueue un elemento `x` al final de la cola.
2. `2`Dequeue el elemento del frente de la cola.
3. `3`Imprimit el elemento del frente de la cola.

### Formato de entrada

La primera línea contiene un numero entero `q` el cual denota el número de consultas. Cada línea siguiente `i` contiene una sola consulta descrita como en el reto. Las tres consultas comienzan con un numero entero denotando el tipo de consulta. Pero solo la consulta `1` es seguida de un valor `x` separado por un espacio, el cual representa el valor a poner en cola (Enqueue)

### Ejemplo de entrada

```
STDIN   Function
-----   --------
10      q = 10 (number of queries)
1 42    1st query, enqueue 42
2       dequeue front element
1 14    enqueue 42
3       print the front element
1 28    enqueue 28
3       print the front element
1 60    enqueue 60
1 78    enqueue 78
2       dequeue front element
2       dequeue front element
```

### Ejemplo de salida

```
14
14
```
