# Ecuaciones Diferenciales Ordinarias (EDOs)?
Las Ecuaciones Diferenciales Ordinarias (EDOs) son ecuaciones que relacionan una función desconocida con sus derivadas. Se llaman ordinarias porque involucran derivadas respecto a una sola variable independiente.

Una **Ecuación Diferencial Ordinaria (EDO) lineal de primer orden** se expresa como:

$$ \frac{d\mathbf{x}}{dt} = A\mathbf{x} $$

donde:
- X es el vector incógnita con dos funciones de t.
- A es una matriz $2 \times 2$ de coeficientes constantes.
- $\frac{d\mathbf{x}}{dt}$ representa la derivada de cada función con respecto a t.

Este sistema de ecuaciones diferenciales se puede resolver usando **valores propios y vectores propios** de $A$.

# Valores y Vectores Propios
Dentro del siguiente repositorio se encontrarán bases y conceptos clave para entender Microeconomía. El primer tema a abordarse es entender que son los Valores y Vectores Propios.
"Un vector propio de una matriz A de n × n es un vector x diferente de cero tal que Ax = λx para algún escalar λ. Un escalar λ se llama valor propio de A si existe una solución no trivial x de Ax = λx; una x como ésta se denomina vector propio correspondiente a λ" (Lay, 2007)

## Características de los valores propios
Cada valor propio tiene infinitos vectores propios dado que existen infinitos números reales que pueden formar parte de cada vector propio. 
Son escalares, pueden ser números complejos (no reales) y pueden ser idénticos (más de un valor propio iguales). 
Existen tantos valores propios como número de filas (m) o columnas (n) tiene la matriz original. 

Los valores propios de una matriz pueden clasificarse en diferentes tipos, en donde cada uno tendra su forma de resolver
1. Reales y desiguales
2. Reales e iguales
3. Reales y Complejos

**Para encontrar los valores propios de una matriz 𝐴 se sigue este procedimiento:**
1. Se calcula el polinomio característico de la matriz, que se obtiene al resolver el determinante de 
A-𝜆I:
    det(A-𝜆I)=0

2. Se resuelve la ecuación resultante para encontrar los valores de 𝜆 que corresponden a los valores propios de A (Strang, 2016).

3. Para cada λ, se encuentra el vector propio resolviendo el sistema homogéneo:
(𝐴−𝜆𝐼)𝑥=0

## Valores propios reales y desiguales
Para este caso en que los valores propio son desiguales, se procede a realizar una diagonalización

"Se dice que una matriz cuadrada A es diagonalizable si A es semejante a una matriz diagonal, esto es, si A = PDP^−1 para alguna matriz P invertible y alguna matriz diagonal D. 

Una matriz A de n × n es diagonalizable si, y sólo si, A tiene n vectores propios linealmente independientes. De hecho, A = PDP−1, con D como una matriz diagonal, si, y sólo si, las columnas de P son n vectores propios de A linealmente independientes. En este caso, las entradas diagonales de D son valores propios de A que corresponden, respectivamente, a los vectores propios de P" (Lay, 2007)

## Valores propios reales e iguales
Cuando los valores propios de una matriz son reales e iguales, la matriz puede no ser diagonalizable, pero todavía se puede reducir a una forma de Jordan.
Si la matriz no es diagonalizable se calculan los vectores propios resolviendo (A-𝜆I)x=0 
Si no hay suficientes, se buscan vectores propios generalizados, resolviendo (𝐴−𝜆𝐼)^𝑘*𝑥=0 para 𝑘>1

## Valores propios reales y complejos
Si la matriz 𝐴 tiene coeficientes reales pero los valores propios son complejos, estos siempre aparecen en pares conjugados de la forma 𝜆=𝑎±𝑏𝑖

**Pasos a seguir**
1. Se calculan los valores propios resolviendo det(A−λI)=0.
2. Se encuentran los vectores propios complejos resolviendo (A−λI)x=0.
3. Como la matriz tiene coeficientes reales, en lugar de vectores propios complejos se usan pares de bases reales, formadas por la parte real e imaginaria de los vectores propios complejos.
4. La matriz no es diagonalizable en el espacio real, pero se puede escribir en forma canónica de Jordan o en una forma de bloques de rotación. Donde cada bloque de  2×2 representa la acción de una transformación con valores propios a±bi (Lay, 2015).

## Referencias
- Strang, G. (2016). Introduction to Linear Algebra (5th ed.). Wellesley-Cambridge Press.
- Lay, D. C. (2007). Linear Algebra and Its Applications (3rd ed.). Pearson.
- Horn, R. A., & Johnson, C. R. (2012). Matrix Analysis (2nd ed.). Cambridge University Press.
- Axler, S. (2015). Linear Algebra Done Right (3rd ed.). Springer.
- Strang, G. (2016). Introduction to Linear Algebra.
- Boyce, W. E., & DiPrima, R. C. (2017). Elementary Differential Equations.

# Resolución de Ecuaciones Diferenciales Ordinarias (EDOs) Lineales con Matrices 2x2

## 1. Definición de una EDO Lineal

Una **Ecuación Diferencial Ordinaria (EDO) lineal de primer orden** en forma matricial se expresa como:

```
    dx/dt = A * x
```

donde:
- `x` es un vector columna con funciones dependientes del tiempo.
- `A` es una matriz `2x2` de coeficientes constantes.

## 2. Pasos para Resolver el Sistema `x' = A*x`

### **Paso 1: Calcular los Valores Propios de A**
Los valores propios `λ` de `A` se obtienen resolviendo el **polinomio característico**:

```
    det(A - λI) = 0
```

donde `I` es la matriz identidad `2x2`. Expandiendo el determinante:

```
    | a11 - λ   a12 |  =  0
    | a21      a22 - λ |
```

### **Paso 2: Encontrar los Vectores Propios**
Para cada `λ_i`, resolvemos:

```
    (A - λI) * v = 0
```

donde `v` es el vector propio correspondiente a `λ_i`.

### **Paso 3: Construir la Solución General**
La solución general del sistema es:

```
    x(t) = C1 * e^(λ1 * t) * v1 + C2 * e^(λ2 * t) * v2
```

donde `C1` y `C2` son constantes determinadas por las condiciones iniciales.

## 3. Casos según los Valores Propios

### **Caso 1: Valores Propios Reales y Distintos (`λ1 ≠ λ2`)**
Si `A` es diagonalizable, la solución toma la forma:

```
    x(t) = C1 * e^(λ1 * t) * v1 + C2 * e^(λ2 * t) * v2
```

### **Caso 2: Valores Propios Reales e Iguales (`λ1 = λ2`)**
Si `A` no es diagonalizable, se necesita un vector generalizado `v_g`:

```
    x(t) = C1 * e^(λ t) * v1 + C2 * t * e^(λ t) * v_g
```

### **Caso 3: Valores Propios Complejos (`λ = a ± bi`)**
Cuando los valores propios son complejos:

```
    x(t) = e^(a t) * (C1 * cos(bt) + C2 * sin(bt))
```



