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
## Exercise Part
- Practiced drawing a handle.
- Complex loft feature using guides.
## Helix
- Spiral curve in 3D space.
- A helix is a spiral curve in 3D space that can be defined with a conical face, cylindrical face, sketch circle, or circular edge.
- Height, pitch and rotations are three parameters.
## Composite Curves
- The Composite curve feature adds curves together to form a single wireframe entity. Sketch entities, edges, and other curves may be added together, as long as they share a common endpoint.
- Please note, you may select entities that do not meet, and create multiple curves with a single feature. However, if the underlying curves overlap or cross at edges and not endpoints, the feature will fail to create the composite curve.
- Curves that make up a composite must connect end to end and may not overlap.
- Why is it needed? Well, if you have to delete a part of the solid but you need the boundaries, you can use composite curves.
## Exercise : Spring
- Mix of helix, composite curves and rest.
- Creating a plane from a point and an adjacent line or a plane and a point.

## Bridging Curves
- A Bridging curve is a 2-point spline in 3D space bridging any two points or vertices together.
- The continuity on either side of the curve may be defined to maintain the needed constraints to other geometry.
- The shape of the curve may be refined by adjusting the magnitude and bias of the tangency or curvature, or through the use of control points.
- In addition to a vertex or a point, bridging curves can be created from an edge. Enabling Edit edge positions allows an edge to be selected as the start or end reference. A virtual point is created along that edge at the position specified in Start edge position. The Start edge position is defined as a percentage of distance along the edge.
- When matching tangency or curvature, there are two methods to provide finer control of the bridging curve. Using the Magnitude/bias method, a magnitude is applied to define a scaling factor for the calculation. The closer to zero, the closer the curve is to the straight line connecting the endpoints.
- The Bias defines the weight of the tangency or curvature matching calculation between each side of the curve. A 0.5 bias equally weighs each side of the curve. The magnitude and bias may also be manipulated by dragging the associated handles in the graphics area.
- The other method to define the shape of the bridging curve utilizes control points. When match tangent is selected, these control points control the start and end magnitude of the tangency. When match curvature is selected, the control points define not only the start and end magnitude, but also the start and end curvature offset.

## 3D Fit Splines
- A 3D fit spline fits a curvature continuous spline between selected sketch points, endpoints of other curves, vertices of parts, or a selection of tangential edges or curves. A fit spline may be used to create paths for routing, bridging entities together, paths or guides for sweep or loft features, or complex profile creation.
- Remember to use Shift+Enter shortcut!
## Split Curves
- The split tool splits curves in the same way it splits parts, faces or surfaces.
- Curves can be trimmed or split into multiple curves with the split tool.
- Split curves are combined with other curves or sketch entities to create the final composite curve.
- If a curve doesn't quite have the shape that you want, you can trim it. After trimming draw extended new curves and add it to a composite curve.
## Intersection Curves
- Intersection curve provides a robust way to create a curve or curves of the cross section where two or more surfaces or faces intersect.
- An intersection curve can result in the creation of multiple curves depending on the selections made.
- Intersection curve selections can be surfaces, faces, planes, or even an entire part from the parts list.
- Make selections into groups carefully. Group 2 doesn't automatically activate.
