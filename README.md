Unidad 2: Graficación 2D

 2.1. Transformación bidimensional
Las transformaciones bidimensionales son procedimientos matemáticos que se aplican a los puntos de un objeto para alterar su posición, tamaño u orientación en un plano XY. En computación gráfica, un punto se representa como un vector columna P =[x/y].

 2.1.1. Traslación
Es el movimiento de un objeto a una nueva posición. Se logra sumando distancias de desplazamiento (dx, dy) a las coordenadas originales:
 x' = x + dx
 y' = y + dy

 2.1.2. Escalamiento
Altera el tamaño de un objeto multiplicando sus coordenadas por factores de escala (sx, sy):
 x' = x* sx
 y' = y * sy
Si sx = sy, el escalamiento es uniforme; de lo contrario, se distorsiona la figura.

 2.1.3. Rotación
Gira un objeto alrededor de un punto (usualmente el origen) con un ángulo \theta. Las fórmulas trigonométricas son:
 x' = x cos(0) - y sin(0)
 y' = x sin(0) + y cos(0)

 2.1.4. Sesgado (Shearing)
Es una transformación que distorsiona la forma de un objeto como si las capas del mismo se deslizaran una sobre otra.
 Sesgo en X: x' = x + sh_x * y
 Sesgo en Y: y' = y + sh_y * x



 2.2. Representación matricial de las transformaciones
Para combinar múltiples transformaciones de manera eficiente, se utilizan coordenadas homogéneas, añadiendo una tercera dimensión (x, y, 1). Esto permite representar todas las operaciones (incluida la traslación) como multiplicaciones de matrices.

La matriz general de transformación T se expresa como:
P' = M * P

Donde las matrices básicas son:
* Traslación
* Escalamiento
* Rotación



 2.3. Trazo de líneas curvas
A diferencia de las líneas rectas, las curvas se definen mediante ecuaciones polinómicas que pasan por puntos de control.

 2.3.1. Bézier
Las curvas de Bézier se definen mediante puntos de control que "atraen" la curva hacia ellos. La forma de la curva es determinada por los Polinomios de Bernstein. Son ampliamente usadas en diseño vectorial (SVG, fuentes de texto).

2.3.2. B-spline
Las Basic Splines ofrecen mayor control local que las de Bézier. Modificar un punto de control solo afecta a una sección cercana de la curva, no a toda la trayectoria, lo que las hace ideales para modelado complejo.



 2.4. Fractales
Un fractal es un objeto geométrico cuya estructura básica, fragmentada o irregular, se repite a diferentes escalas (autosimilitud). En graficación, se generan mediante algoritmos recursivos.
* Ejemplos clásicos: Conjunto de Mandelbrot, Triángulo de Sierpinski, Copo de nieve de Koch.



 2.5. Uso y creación de fuentes de texto
En computación gráfica, el texto se trata de dos formas:
1.  Mapas de bits (Bitmap): Caracteres definidos por una rejilla de píxeles. Son rápidos pero pierden calidad al escalarse.
2.  Fuentes de contorno (Vectoriales): Utilizan curvas de Bézier para definir la silueta de cada letra (ej. TrueType, OpenType). Permiten escalamiento infinito sin pérdida de resolución.



Referencias Bibliografías 
* Hearn, D., & Baker, M. P. (2006). Gráficas por computadora con OpenGL (3ra ed.). Pearson Educación.
* Hughes, J. F., Van Dam, A., McGuire, M., Sklar, D. F., Foley, J. D., Feiner, S. K., & Akeley, K. (2013). Computer Graphics: Principles and Practice. Addison-Wesley Professional.
* Wolfram MathWorld. (2024). Bézier Curve. Recuperado de [https://mathworld.wolfram.com/BezierCurve.html](https://mathworld.wolfram.com/BezierCurve.html)
