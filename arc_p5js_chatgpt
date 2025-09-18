## How do I use the arc command in p5.js?

In **p5.js**, the `arc()` function is used to draw a portion of an ellipse (a curved line). You can think of it as drawing a "slice" or "wedge" of a circle/ellipse.

### Syntax

```javascript
arc(x, y, w, h, start, stop, [mode])
```

### Parameters

* **`x, y`** → The coordinates of the arc's center.
* **`w, h`** → The width and height of the ellipse from which the arc is taken.
* **`start`** → The starting angle, in **radians**.
* **`stop`** → The stopping angle, in **radians**.
* **`mode`** *(optional)* → Defines how the arc is drawn:

  * `OPEN` (default): Just the curved line.
  * `CHORD`: Connects the endpoints of the arc with a straight line.
  * `PIE`: Connects the endpoints to the center, like a pie slice.

### Example

```javascript
function setup() {
  createCanvas(400, 400);
  noFill(); // so we can see just the arc outline
}

function draw() {
  background(220);

  // A semicircle (PI radians = 180°)
  arc(200, 200, 150, 150, 0, PI);

  // A quarter circle
  arc(200, 200, 150, 150, 0, HALF_PI);

  // A "pie slice"
  fill(100, 150, 255);
  arc(200, 200, 150, 150, PI, TWO_PI, PIE);
}
```

### Important notes

* **Angles in p5.js are in radians**, not degrees.

  * `PI` = 180°
  * `HALF_PI` = 90°
  * `TWO_PI` = 360°
* If you want to use degrees instead, call `angleMode(DEGREES);`.

👉 Would you like me to make you a **visual demo sketch** showing different arc modes (`OPEN`, `CHORD`, `PIE`) side by side so you can see the difference?

## Help me visualize the angles

Got it — angles can feel a bit abstract in p5.js since they’re in radians by default. Let’s make it visual.

### How angles work in `arc()`

* The **center** of the arc is your `(x, y)`.
* Angles are measured starting from the **3 o’clock direction** (to the right of the center).
* Positive angles go **counterclockwise**.

So:

* `0` → points right (east)
* `HALF_PI` → points down (south)
* `PI` → points left (west)
* `3*HALF_PI` → points up (north)
* `TWO_PI` → full circle

---

### Visualization Sketch

Here’s a small sketch that shows the reference directions:

```javascript
function setup() {
  createCanvas(400, 400);
  angleMode(RADIANS); // default, but explicit
  noFill();
}

function draw() {
  background(240);

  // Draw guide circle
  ellipse(width/2, height/2, 200, 200);

  // Draw arcs for each quadrant
  strokeWeight(3);
  stroke(255, 0, 0);
  arc(width/2, height/2, 200, 200, 0, HALF_PI); // 0 → HALF_PI (right to down)

  stroke(0, 255, 0);
  arc(width/2, height/2, 200, 200, HALF_PI, PI); // down to left

  stroke(0, 0, 255);
  arc(width/2, height/2, 200, 200, PI, PI+HALF_PI); // left to up

  stroke(200, 100, 255);
  arc(width/2, height/2, 200, 200, PI+HALF_PI, TWO_PI); // up to right

  // Draw angle labels
  fill(0);
  noStroke();
  textAlign(CENTER, CENTER);
  text("0 / TWO_PI", width/2 + 120, height/2); // right
  text("HALF_PI", width/2, height/2 + 120);   // bottom
  text("PI", width/2 - 120, height/2);        // left
  text("3/2 PI", width/2, height/2 - 120);    // top
}
```

This will show:

* A full circle broken into 4 arcs (each a different color).
* Labels for the key angles (`0`, `HALF_PI`, `PI`, `3/2 PI`, `TWO_PI`).

---

👉 Do you want me to also make a **degrees version** (`angleMode(DEGREES)`) so you can compare `0°, 90°, 180°, 270°, 360°` with the radians version?


## Yes

Perfect 👍 Let’s do a **side-by-side visualization**: one circle labeled in radians and one in degrees. That way you can compare how the angles map.

```javascript
function setup() {
  createCanvas(800, 400);
  noFill();
  textAlign(CENTER, CENTER);
  textSize(14);
}

function draw() {
  background(240);

  // -------- Left: Radians --------
  push();
  translate(200, 200);
  angleMode(RADIANS);

  // guide circle
  ellipse(0, 0, 200, 200);

  // arcs
  strokeWeight(3);
  stroke(255, 0, 0);
  arc(0, 0, 200, 200, 0, HALF_PI);

  stroke(0, 255, 0);
  arc(0, 0, 200, 200, HALF_PI, PI);

  stroke(0, 0, 255);
  arc(0, 0, 200, 200, PI, PI + HALF_PI);

  stroke(200, 100, 255);
  arc(0, 0, 200, 200, PI + HALF_PI, TWO_PI);

  // labels
  noStroke();
  fill(0);
  text("0 / TWO_PI", 120, 0);
  text("HALF_PI", 0, 120);
  text("PI", -120, 0);
  text("3/2 PI", 0, -120);
  text("Radians", 0, 150);
  pop();

  // -------- Right: Degrees --------
  push();
  translate(600, 200);
  angleMode(DEGREES);

  // guide circle
  ellipse(0, 0, 200, 200);

  // arcs
  strokeWeight(3);
  stroke(255, 0, 0);
  arc(0, 0, 200, 200, 0, 90);

  stroke(0, 255, 0);
  arc(0, 0, 200, 200, 90, 180);

  stroke(0, 0, 255);
  arc(0, 0, 200, 200, 180, 270);

  stroke(200, 100, 255);
  arc(0, 0, 200, 200, 270, 360);

  // labels
  noStroke();
  fill(0);
  text("0° / 360°", 120, 0);
  text("90°", 0, 120);
  text("180°", -120, 0);
  text("270°", 0, -120);
  text("Degrees", 0, 150);
  pop();
}
```

### What you’ll see

* On the **left**, a circle labeled with **radians** (`0`, `HALF_PI`, `PI`, `3/2 PI`, `TWO_PI`).
* On the **right**, the same circle but labeled in **degrees** (`0°`, `90°`, `180°`, `270°`, `360°`).
* Both show arcs in the same order/colors so you can see that radians and degrees map to the same positions.

---

👉 Would you like me to also overlay **little arrows from the center pointing at each angle** (like a compass) to make the directions clearer?
