# Monte-Carlo-Simulation-to-calculate-pi

A simple tutorial for doing a Monte Carlo simulation using Python 3.0

From geometry, we know that the ratio of an circle inscribed in a square to that square is pi/4. For our Monte Carlo simulation, we will generate a bunch of points in a square and determine which ones are in the circle and which are not. The ratio of the points inside the circle to the total number of points is pi/4.

Draw a square and a circle
Generate points within a square.
Determine which points are also in the circle
Plot the points to visualize those points
Plot the estimate for pi versus the iteration number to see how quickly we converge on the true value.
Drawing a square and a circle
We want our square within a 2x2 grid centered at the origin. The corners of the square will be at (1,1), (-1,1), (1,-1), (-1,-1). The circle will be a unit circle with radius of 1.

For the square, we can generate a list for X and Y values using the corner points.

The circle we can generate using the knowledge of trigonometry. The X value of a particular point will be cosine of the angle, and the Y value will be its sine. The total angle of circle is 2pi radians, and a for loop will allow a quick caculation of the X and Y values of the circle ever degree.

Generating points in the square
Numpy's random() function will generate a uniform random number between 0 and 1. We want a number between -1 and 1, so we must first transform it. Subtracting 0.5 from random() gives a value between -0.5 and 0.5 and multiplying that by 2 give a number between -1 and 1. We will do this twice. Once for X and once for Y.

Pythagoras tells us the distance from origin (r) of our randomly generated points is the square root of the sum of their squares. If this r value is less than or equal to 1, it is within the circle, otherwise it is not.

Once we're done iterating, we can calculate the final value of pi, and its error versus the true value.

Drawing the plots
We want two plots, one is the points with relation to the square and circle, the other the estimate of pi over a number of iteration.
