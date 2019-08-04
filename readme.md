# canvas grid or coordinate space.

const ctx = canvas.getContext("2d");
ctx.fillStyle = "green";
ctx.fillRect(20, 10, 150, 100);

- Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 100 pixels high
- 1 unit in the grid corresponds to 1 pixel on the canvas.
- Default origin of this grid is positioned in the top left corner at coordinate (0,0).
- All elements are placed relative to this origin.
- 20 is distance from x-axis and 10 is distance from y axis

(0,0)
-------------------- x-axis
|
|
|
|
|
|
y-axis

---

# Drawing Rectangles :

- <canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines).
- using path we can draw possible to compose very complex shapes.
- for rectangle, three functions that draw rectangles on the canvas:

  - fillRect(x, y, width, height) : Draws a filled rectangle.
  - strokeRect(x, y, width, height) : Draws a rectangular outline.
  - clearRect(x, y, width, height) : Clears the specified rectangular area, making it fully transparent.

- Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.

---

# paths:

- A path is a list of points, connected by segments of lines that can form different shapes, curved, of different width and of different color.
- To make shapes using paths, follow these below steps

  - create the path.
  - use drawing commands to draw into the path.
  - onces the path has been created, you can stroke or fill the path to render it.

- beginPath() : Creates a new path.
- closePath() : Adds a straight line to the path
- stroke() : Draws the shape by stroking its outline.
- fill() : Draws a solid shape by filling the path's content area.

- The first step to create a path is to call the beginPath(). Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.
- The second step is calling the methods that actually specify the paths to be drawn.
- The third, and an optional step, is to call closePath(). This method tries to close the shape by drawing a straight line from the current point to the start.

---

- moveTo(x,y) : useful function, which doesn't actually draw anything but becomes part of the path list described above, is the moveTo() function. You can probably best think of this as lifting a pen or pencil from one spot on a piece of paper and placing it on the next.
- Moves the pen to the coordinates specified by x and y.

---

- lineTo(x, y) : For drawing straight lines, use the lineTo() method.
- Draws a line from the current drawing position to the position specified by x and y.
