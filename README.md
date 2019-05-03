# tutorial_typescript
Tutorial de TypeScript

**Índice**
1. [Comandos](#id1)
2. [Ficheros](#id2)
3. [Variables](#id3)
4. [Constantes](#id4)
5. [Operadores](#id5)
6. [Control de flujo](#id6)
7. [Tipos primitivos](#id6)


## Comandos <a name="id1"></a>
1. Instalat ts desde npm --> npm install -g typescript
2. Compilar archivo -->  tsc *.ts (genera el archivo *.js)


## Ficheros <a name="id2"></a>


## Variables <a name="id3"></a>

* let --> Restringe su uso al ambito de un bloque de texto. 
* var --> Solo accesible en su función
* Podemos declarar variables en 1 linea separadas por comas. let var1, var2, ar3;
* NaN --> La variable no está inicializada


## Constantes <a name="id4"></a>

* const VARIABLE

## Operadores <a name="id5"></a>
 * ++, --> Solo para los tipos any, number y enum La diferancia entre --num y num-- es el orden en el que se ejecuta el operador
 * +,- --> Sólo para los tipos number, string, any y enum. Convierten un valor de tipo anu a string
* ! --> Negación. También puede convertir un String a boolean 
* ~  --> Cambia todos los bits de 0 a 1 y viceversa
* delete --> Borra propiedades de objetos o elementos de un array. Si se borra la posición de un array, éste no se redimensiona, sino que convierte esa posición en undefined. Devuelve true o false dependiento de si ha podido eliminar o no el elemento.
* void Evalua una expresión y siempre devuelve undefined
... --> Expande un array u objeto
~~~
let numbers = [1, 2];
let moreNumbers = [4, 5, 9, ...numbers, 10]; // 4,5,9,1,2,10
~~~
También sirve como parámetro de una función para indicar que admite un número infinito de argumentos, además de usarse como argumento en sí mismo: 
~~~
function sum (x: number, ...more: number[]) { } // infinitos números
let numbers: number[] = [4,5,9,10];
sum(1, ...numbers); // pasamos el array expandido
~~~
* = Asignación
* Lógicos:
 1. AND
 2. OR
* Aritmeticos ( +, - , * , /, %, x y (potencia y de x)
* Relacionales <, >, <=, >=, ==, !=, ===, !== (comprueban valor y tipo)
* + concatenación. Sólo para any y string
* in --> Busca el valor del operando de la izquierda, que debe ser any, string o number, en el operando de la derecha, que debe ser any, object o array devolviendo true si lo encuentra y false en caso contrario.
* Operador terciario -->  La variable x vale 10. A la variable z se le asigna un valor dependiendo de una condición que en este caso comprueba si la variable x vale 10. Si es cierto, a z se le asigna 1, en caso contrario se le asigna 100;
~~~
let x:number = 10;
let z:number = x == 10 ? 1 : 100; // 1
~~~

## Control de flujo <a name="id6"></a>

### Selectivas
* if
* switch
### Iterativas
* while
* do-while
* for
* for in
* for-of (Esta forma de for es casi idéntica al for-in, con la salvedad de que en cada iteracción lo que se vuelca en la variable temporal es el valor de la posición y no el índice.
### Para bucles
* break
* comtinue 
* return


## Tipos <a name="id6"></a>

let variable: tipo;
Todos los tipos provienen de uno superior llamado Any. El tipo Any se refiere a cualquier cosa. Si declaramos una variable sin tipar sería lo mismo que hacerlo con Any.

~~~
let variable: any; == let variable
~~~

### Tipos primitivos <a name="id7"></a>

|Primitivo | Objeto | Uso |
| -- | -- | -- | 
| number | Number | Numeros |
| string | String | Carácteres y cadenas |
| boolean | Bolean |  trus/false|
| undefined | Undefined | Sin valor |
| null | Null | Valor nulo |
| void | Void | Ausencia de valor|
|never |  | Valores que no pueden ocurrir |
|symbol | Symbol | Valores únicos usados como token |

En TS los tipos primitivos y los objetos poseen el mismo nombre pero con la diferencia de que estos últimos se escriben con la primera letra en mayúsculas.

Template String `Esto es un template String` --> Permite escribir tesxto en diferentes lineas y además incluir expresions
`Esto es un Template String que permite expresiones mediante $[espresion]





