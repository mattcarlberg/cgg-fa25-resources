
# 2D Arrays in JavaScript

Note: This primer on 2D arrays was generated via large language model. 

## 1. What Is a 2D Array?

A **2D array** is an array **of arrays**.

Think of it like:

* A **table**
* A **grid**
* A **spreadsheet**
* A **map made of rows and columns**

Example (3 rows, 4 columns):

```js
let grid = [
  [1, 2, 3, 4],
  [5, 6, 7, 8],
  [9, 10, 11, 12]
];
```

Each inner array is a **row**.

---

## 2. Visualizing Indexes

In a 2D array, you usually think in terms of:

```
grid[row][column]
```

Example:

```js
grid[0][0]  // 1
grid[0][3]  // 4
grid[2][1]  // 10
```

* First index → row
* Second index → column

---

## 3. Accessing Values

```js
let grid = [
  ["A", "B", "C"],
  ["D", "E", "F"],
  ["G", "H", "I"]
];

console.log(grid[1][2]); // "F"
```

Breakdown:

* `grid[1]` → `["D", "E", "F"]`
* `grid[1][2]` → `"F"`

---

## 4. Modifying Values

You can change values just like with normal arrays:

```js
grid[0][1] = "X";

console.log(grid);
// [
//   ["A", "X", "C"],
//   ["D", "E", "F"],
//   ["G", "H", "I"]
// ]
```

---

## 5. Looping Through a 2D Array

### Nested Loops (Most Important Pattern)

To visit **every cell**, you need **two loops**:

```js
for (let row = 0; row < grid.length; row++) {
  for (let col = 0; col < grid[row].length; col++) {
    console.log(grid[row][col]);
  }
}
```

Think:

* Outer loop → rows
* Inner loop → columns

---

## 6. Creating a 2D Array Programmatically

Instead of typing everything by hand, you usually **build** a 2D array.

Example: create a 5×5 grid filled with zeros.

```js
let rows = 5;
let cols = 5;
let grid = [];

for (let r = 0; r < rows; r++) {
  let row = [];
  for (let c = 0; c < cols; c++) {
    row.push(0);
  }
  grid.push(row);
}

console.log(grid);
```

Result:

```js
[
  [0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0],
  [0, 0, 0, 0, 0]
]
```

---

## 7. Common Use Cases

2D arrays are great for:

* Game boards (chess, tic-tac-toe, minesweeper)
* Pixel data
* Tile maps
* Grids in simulations
* Cellular automata (Conway’s Game of Life)

---

## 8. Example: Tic-Tac-Toe Board

```js
let board = [
  ["", "", ""],
  ["", "", ""],
  ["", "", ""]
];

// Player X moves in the center
board[1][1] = "X";

console.log(board);
```

---

## 9. Common Mistakes (Watch Out!)

❌ Mixing up row and column order

```js
grid[col][row] // usually wrong
```

❌ Forgetting nested loops

```js
// This only loops rows, not columns
for (let r = 0; r < grid.length; r++) {
  console.log(grid[r]);
}
```

❌ Assuming all rows are the same length

```js
grid[row].length // always check!
```

---

# 10. 2D Arrays in p5.js (Visual Example)

Now let’s use a 2D array to draw a **grid of squares** in p5.js.

### Idea

* Each cell stores a number (0 or 1)
* `0` = white square
* `1` = black square

---

### p5.js Example: Grid Drawing

```js
let grid;
let rows = 10;
let cols = 10;
let cellSize = 40;

function setup() {
  createCanvas(400, 400);
  
  // Create 2D array
  grid = [];
  for (let r = 0; r < rows; r++) {
    let row = [];
    for (let c = 0; c < cols; c++) {
      // Randomly fill with 0 or 1
      row.push(floor(random(2)));
    }
    grid.push(row);
  }
}

function draw() {
  background(220);

  for (let r = 0; r < rows; r++) {
    for (let c = 0; c < cols; c++) {
      if (grid[r][c] === 1) {
        fill(0);
      } else {
        fill(255);
      }

      rect(
        c * cellSize,
        r * cellSize,
        cellSize,
        cellSize
      );
    }
  }
}
```

---

## 11. What’s Happening Here?

* `grid[r][c]` stores the **state** of each square
* Rows control **vertical position**
* Columns control **horizontal position**
* The 2D array acts like a **map** for drawing

---

## Final Mental Model

> A 2D array is just an array where **each element is another array** — perfect for representing **grids, boards, and spaces**.

If you want, I can also:

* Add **mouse interaction** to the p5.js grid
* Turn this into a **game board**
* Create a **worksheet or practice problems** for students
