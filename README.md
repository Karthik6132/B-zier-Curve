# B-zier-Curve
This project implements an interactive cubic Bezier curve that behaves like a flexible rope. The curve responds to mouse movement and updates smoothly in real time using a simple spring and damping model.

The implementation is done using plain HTML, JavaScript, and the Canvas API, with all math and motion logic written manually.

Math:

The curve is implemented as a cubic Bezier curve using four control points. The curve position is computed by evaluating the Bezier equation for values between zero and one at small intervals to generate a smooth path. Tangent vectors are calculated using the derivative of the cubic Bezier equation and are normalized for visualization along the curve.

Physics Model:

The two middle control points follow a simple spring and damping model. Each point moves toward a target position defined by mouse input. The spring force pulls the point toward the target, while damping reduces velocity to prevent instability. This produces smooth, elastic, rope-like motion.

Design Choices:

All Bezier math, tangent computation, and motion logic are implemented manually without using any built in libraries. The endpoints are kept fixed to maintain curve stability, while the middle control points provide flexibility. Rendering and updates are handled in real time using the Canvas API and requestAnimationFrame to maintain smooth performance.

