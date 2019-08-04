# To draw arcs or circles, we use the arc() or arcTo() methods.

- arc(x, y, radius, startAngle, endAngle, anticlockwise) : Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).
- x and y are the coordinates of the center of the circle on which the arc should be drawn
- The startAngle and endAngle parameters define the start and end points of the arc in radians,
- anticlockwise parameter is a Boolean value which, when true, draws the arc anticlockwise; otherwise, the arc is drawn clockwise.
- Angles in the arc function are measured in radians, not degrees. To convert degrees to radians you can use the following JavaScript expression: radians = (Math.PI/180)\*degrees.

---

- arcTo(x1, y1, x2, y2, radius) : Draws an arc with the given control points and radius, connected to the previous point by a straight line.

---

# Curve

- quadraticCurveTo(cp1x, cp1y, x, y) : Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.

- bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y) : Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).

---