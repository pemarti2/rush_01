# Rush 01:

> Hola chicos he creado esta documentación para ir añadiendo cosas que querais desde codigo a pseudocodigo. 
> Ideas locas, enlaces relacionados o lo que sea. Debajo de vuestro ## nombre. 
> Si quereis podeis crear otro readme y añadir el link. 
> Tambien podeis usar el siguiente repositorio git https://github.com/pemarti2/rush_01 
> Para comentar cosas de otros: https://hackmd.io/c/tutorials/%2Fs%2Fhow-to-use-comments 

## pemarti2:

El flow de programa que he pensado en pseudocodigo:

(0.1)
comprobacion limitaciones basicas formato input n < 4 , recorrer string y que cumpla la norma. 

(1)
funcion buscar permutaciones de n en este caso 1234
1234, 1243 [...] hasta 24
almacenarlas en un array
[["1","2","3","4"],["4","3","2","1"]...]

(2)
funcion evaluar array permutaciones y añadir un elemento a izquierda y derecha de los visibles ejemplo:
[["4","1","2","3","4","1"],["3","2","3","4","1","2"]...]

(3)
funcion comprobar las diferentes permutaciones con las parejas de suma:
dado input "4 3 2 1 1 2 2 2 4 3 2 1 1 2 2 2"
primero transformar a array:
> puede ser una funcion a parte
[[colup],[coldown],[rowleft],[rowright]]
[["4","3","2","1"],["1","2","2","2"],["4","3","2","1"],["1","2","2","2"]]

empezemos por encajar o rowleft -> rowright o colup ->coldown

para simplificar voy a empezar con rows:
el primer caracter de cada permutacion {la array(2)} tendra que encajar con rowleft y el ultimo con rowright.
["4","3","2","1"],["1","2","2","2"]

recorrer el array de permutaciones y añadir la primera de cada permutacion que cumpla con 4/1, 3/4, 2/2, 1/2.

una vez hecho esto 
1r comprobacion no repiten numeros entre columnas.
si se repiten fijar el primer elemento de la array y variar otro (las permutaciones no se pueden repetir)
comprobar que no se repiten y repetir has que no haya incompatibilidades si se comprueban todas las variaciones de permutaciones posibles y hay incompatibilidades el input es erroneo.

si no es erroneo no encontrara incompatibilidades.

2da comprobacion encaja con [colup],[coldown] ?

si -> imprimir solucioón

no -> repetir variacion de permutaciones y ver si hay otra combinacion que no sea incompatible

si depues de todas las repeticiones llegamos alfinal de permutaciones compatibles el input es erroneo
