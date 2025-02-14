# Valores y Vectores Propios
Dentro del siguiente repositorio se encontrarán bases y conceptos clave para entender Microeconomía. El primer tema a abordarse es entender que son los Valores y Vectores Propios.
"Un vector propio de una matriz A de n × n es un vector x diferente de cero tal que Ax = λx para algún escalar λ. Un escalar λ se llama valor propio de A si existe una solución no trivial x de Ax = λx; una x como ésta se denomina vector propio correspondiente a λ" (Lay, 2007)

Los valores propios de una matriz pueden clasificarse en diferentes tipos, en donde cada uno tendra su forma de resolver
1.- Reales y desiguales
2.- Reales e iguales
3.- Reales y Complejos

Para encontrar los valores propios de una matriz 𝐴 se sigue este procedimiento:
1.- Se calcula el polinomio característico de la matriz, que se obtiene al resolver el determinante de 
A-𝜆I:
    det(A-𝜆I)=0

2.-Se resuelve la ecuación resultante para encontrar los valores de 𝜆 que corresponden a los valores propios de A (Strang, 2016).

3.- Para cada λ, se encuentra el vector propio resolviendo el sistema homogéneo:
(𝐴−𝜆𝐼)𝑥=0

##Valores propios reales y desiguales
Para este caso en que los valores propio son desiguales, se procede a realizar una diagonalización

"Se dice que una matriz cuadrada A es diagonalizable si A es semejante a una matriz diagonal, esto es, si A = PDP^−1 para alguna matriz P invertible y alguna matriz diagonal D. 
Una matriz A de n × n es diagonalizable si, y sólo si, A tiene n vectores propios linealmente independientes. De hecho, A = PDP−1, con D como una matriz diagonal, si, y sólo si, las columnas de P son n vectores propios de A linealmente independientes. En este caso, las entradas diagonales de D son valores propios de A que corresponden, respectivamente, a los vectores propios de P" (Lay, 2007)

##Valores propios reales e iguales
Cuando los valores propios de una matriz son reales e iguales, la matriz puede no ser diagonalizable, pero todavía se puede reducir a una forma de Jordan.

