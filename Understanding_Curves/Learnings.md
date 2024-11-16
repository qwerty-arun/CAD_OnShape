# Course: Understanding Curves
## Introduction to Curves
- Curvature is the inverse of radius.
- `Shift+C` shows the curvature comb of the spline.
- Less is more. While evaluating a spline, you look for smooth transitions between curves. Too many spline points can bring rapid change in curvature and create a lower quality spline.
- Try removing extra spline points on the curve.
- Types of continuity: Discontinuous, G0, G1, G2, and G3.
- Discontinuous curves do not share an endpoint and do not have a G value.
- G0 describes curves that only match in position, basically only sharing one endpoint.
- G1 describes continuity between two curves that share position and tangency. There might be a jump in curvature if curvatures do not match.
- G2 curvature indicate that the curves match in position, tangency and curvature. Curvature combs are parallel and have the same radius at the point where the two curves meet.
- G3: position, tangency, curvature and rate of curvature. Can't be created automatically on OnShape. But manually using constraints, we can.

## Conics
- A conic a curve which results from a plane intersecting a cone.
- Types: Parabola, Hyperbola, Circle and Ellipse.
- Rho: ratio between the distance along the line connecting the virtual sharp and the vertex of the conic.
- Create Selection option. What is the use? Well, we can quickly select stuff.
- Introduction to pierce option. Ex: Piercing endpoint of a line to edge of the part. But this only works if you select the edge of the part which interacts with the sketch plane.
- Introduction to intersection sketch tool.
- Made a Mobile Case Cover.
## Splines
- Are piece wise polynomials between interpolation points that maintain curvature continuity along their length.
- Are used to create paths for sweep, loft etc.
- Double clicking the last point on the spline to complete the spline.
- Are dynamic, their shape can be changed after creation.
- Spline handles have both direction and magnitude. We can use dimension for this.
- What defines a spline fully? Magnitude and direction of end points, location with respect to origin, length of the spline, lengths between intermediate points and end points.
- You can add more points to spline using the same tool.
- Between the spline points, the interpolation is very smooth. At the spline points, there is G2 continuity and rate of change of curvature can change abruptly at the point.
- Inserting photos is quite common. Keep the image in the same sketch. So that hiding and showing images is easier.
- You can insert images on planes which are located at an offset to current sketches.
- Only one dimension is enough to define the constraint for the image. Aspect ratio is maintained.
