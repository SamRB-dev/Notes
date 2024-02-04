# Gradient & Tangent
Let, f(x) = $x^2$
- Gradient / Slope 
- $\text{Gradient m} = \frac{\text{Rate of change in y}}{\text{Rate of change in x}}$
- Tangent is a line that intersects only on point of a function graph.
- Tangent for x = a,
		$f(a) + f'(a)(x - a)$
		or, 
		$y - y1 = m(x - x1)$
# Secant Line
A **secant line** is a straight line that intersects a curve at two or more points. In the context of a function, it's a line that connects two points on the graph of the function. The slope of the secant line between two points on a function provides an average rate of change of the function between those points.

To calculate the secant line of the function $\( f(x) = -\frac{1}{2}x^2 + 2x + 1 \)$ between two points, let's choose two specific values of \( x \), say $\( x_1 \)$ and $\( x_2 \)$. For this example, we can pick $\( x_1 = 2 \) and \( x_2 = 4 \)$. The slope of the secant line between these two points is given by the formula:

$$
\text{slope} = \frac{f(x_2) - f(x_1)}{x_2 - x_1}
$$

1. Calculate $\( f(x_1) \)$ and $\( f(x_2) \)$:
   - $\( f(2) = -\frac{1}{2}(2)^2 + 2(2) + 1 \)$
   - $\( f(4) = -\frac{1}{2}(4)^2 + 2(4) + 1 \)$

2. Substitute these values into the slope formula:
   - $\( f(2) = -2 + 4 + 1 = 3 \)$
   - $\( f(4) = -8 + 8 + 1 = 1 \)$
   - $Slope = \( \frac{1 - 3}{4 - 2} = \frac{-2}{2} = -1 \)$

The slope of the secant line between the points (2, f(2)) and (4, f(4)) on the graph of \( f(x) \) is -1. 

With this slope and one of the points, you can write the equation of the secant line. Using point-slope form:

$$
y - y_1 = m(x - x_1)
$$

where \( m \) is the slope (-1) and \( $(x_1, y_1)$ \) is one of the points (let's use (2, 3)):

$$
y - 3 = -1(x - 2)
$$

This is the equation of the secant line that intersects the curve at \( x = 2 \) and \( x = 4 \).