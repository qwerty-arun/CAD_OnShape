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
- Exercise stuff: A symmetry constraint requires a line and two other geometries of the same type. Some of the geometry intersects itself or is degenerate.
- Pressing `s` brings out a menu of tools you can pick from.
- Holding shift while using the spline tool avoids unnecessary constraints.
## Curvature 
- The Curvature sketch constraint matches G2 continuity between two curves, making them match in position, tangency, and curvature at the point of intersection. Results in smoother transitions between the curves.
- Automatic conincidency of two endpoints (nearest) is possible.
## Bezier Curve
- A Bezier curve is defined by its control polygon; segments and vertices of this polygon can be constrained with sketch constraints and dimensions.
- Polygonal Bezier curves are parametric curves defined by their control points. A 3rd degree Bezier curve is similar to a two-point spline curve, coordinates of both curves are 3rd degree polynomials.
- A bezier curve cannot create a closed loop.
- Once a Bezier curve is placed, the control polygon can be modified. N control points define a Bezier curve of degree N-1. The degree can be lowered by deleting control points or elevated by adding additional control points.
- The Bezier curve allows for a higher degree of polynomials and can be used for smoother transitions with control of tangency at the ends of the curve.
- Here too, least amount of control points is best.
## 3D Curves
- 3D curves are 1-dimensional wireframe entities that are defined in 3D space, and cannot be defined in a 2D sketch plane.
- Curves such as helices, projected curves, bridging curves, and 3D fit splines may be defined in 3D space.
-  When defining the underlying framework of a complex part by creating curves, it is very common to need curves that are not limited to a 2D sketch plane, but are defined in 3D space, and are non-planar.
## Projected Curves
- A Projected curve is the intersection between two non-parallel sketches, or a projection of a selection of sketch entities, curves or edges onto a face or multiple faces.
- Also allows curves to be projected onto faces.
- These projected curves can later act a sweep path etc.
## Isoparametric Curves
- Isoparametric curves are smooth curves that run along a face or surface in the U or V direction. The Isoparametric curve feature adds selectable curve entities to the Part Studio for reference in other features.
- Equal spacing or location of the curves can be set.
## Offset Curves
- Offset curve creates a new curve by offsetting the edges of surrounding faces, allowing you to create and control a profile without additional sketches or features.
- An Offset curve may be created by selecting a single or multiple edges.
- Offset curves may be placed on a face or used to split a face automatically.
- Choose from two methods to calculate curve length: Geodesic or Euclidean.
- You can't offset a curve which branches from same edge.
- Geodesic calculates the offset using Geodesic distance in the 2D space of the target faces.
- Euclidean calculates the offset using Euclidean distance in the 3D space.
- Splitting faces is possible.
- Target faces is also possible to constrain the curve to those faces.

