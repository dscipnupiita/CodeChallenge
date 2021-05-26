<p align="center">
  <img src="../images/Stack & Queues.png" width="920">
</p>

# Stacks & Queues

Bienvenido a la segunda serie de retos del #CodeChallenge🤖 traído a ti por el DSC IPN-UPIITA, en esta ocasión te retamos a resolver 3 problemas de dificultad variada sobre pilas y colas.

Te compartimos a continuación una breve descripción de los retos y el enlace donde puedes verlo más detallado y probar tu código!

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

🔗👉Enlace del problema completo https://www.hackerrank.com/challenges/queue-using-two-stacks/problem

## Reto 3: Task Scheduler

Dado un array de caracteres `tasks`, representa las tareas que una CPU necesita hacer, donde cada letra representa una diferente tarea. Las tareas podrán ser completadas en cualquier orden.
Cada tarea es completada en una unidad de tiempo. Para cada unidad de tiempo, la CPU podría completar una tarea o simplemente estar inactiva.

Sin embargo, hay un número entero no negativo `n` que representa el periodo de recuperación entre dos tareas iguales (la misma letra en el arreglo), es decir, debe haber al menos `n` unidades de tiempo entre dos tareas iguales.

Devuelve el menor numero de unidades de tiempo que la CPU tomará para finalizar todas las tareas dadas.

### Ejemplo de entradas y salidas 1:

```
Entrada: tasks = ["A","A","A","B","B","B"], n = 2
Salida: 8
Explicación:
A -> B -> inactivo -> A -> B -> inactivo -> A -> B
Hay al menos 2 unidades de tiempo entre dos tareas iguales
```

### Ejemplo de entradas y salidas 2:

```
Entrada: tasks = ["A","A","A","B","B","B"], n = 0
Salida: 6
Explicación: En este caso, cualquier permutación de tamaño 6 funcionaría ya que n = 0
["A","A","A","B","B","B"]
["A","B","A","B","A","B"]
["B","B","B","A","A","A"]
...
y así, sucesivamente
```

### Ejemplo de entradas y salidas 3:

```
Entrada: tasks = ["A","A","A","A","A","A","B","C","D","E","F","G"], n = 2
Salida: 16
Explicación:
Una posible solución es:
A -> B -> C -> A -> D -> E -> A -> F -> G -> A -> inactivo -> inactivo -> A -> inactivo -> inactivo -> A
```

🔗👉Enlace del problema completo https://leetcode.com/problems/task-scheduler/