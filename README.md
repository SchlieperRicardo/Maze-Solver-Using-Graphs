# Maze-Solver-Using-Graphs
# 🧩 Maze Solver Using Graphs (BFS) - C ANSI

## 📖 About the Project

This project was developed for the **Data Structures** course at **Universidade Católica de Santa Catarina**.

The objective is to solve a maze by applying **Graph Theory** concepts and the **Breadth-First Search (BFS)** algorithm to find the shortest path between the entrance and the exit.

The program reads a maze from a `.txt` file, automatically identifies the entrance and exit, finds the shortest path, and displays the solved maze directly in the console.

---

# 🎯 Objectives

* Represent a maze using a character matrix.
* Model the maze as a graph.
* Automatically locate the entrance (`E`) and exit (`S`).
* Find the shortest path using BFS.
* Display the solved maze.
* Show the total number of steps.
* Allow different maze files to be tested without modifying the source code.

---

# 🧠 Concepts Applied

* Data Structures
* Graph Theory
* Breadth-First Search (BFS)
* Character Matrices
* Structures (`struct`)
* Queue (FIFO)
* Path Reconstruction
* File Handling

---

# 📂 Project Structure

```text
Project/
│
├── MazeSolver.c
├── Maze1.txt
├── Maze2.txt
├── Maze3.txt
├── Maze4.txt
├── Maze5.txt
├── RandomMaze.txt
└── README.md
```

---

# 📄 Maze Format

Each `.txt` file represents a maze.

| Symbol | Meaning             |
| ------ | ------------------- |
| `#`    | Wall                |
| `.`    | Free path           |
| `E`    | Entrance            |
| `S`    | Exit                |
| `*`    | Shortest path found |

Example:

```text
####################
#E.....#..........S#
#.###..#..#####....#
#..................#
####################
```

---

# ⚙️ How It Works

The program performs the following steps:

1. Requests the maze file name.
2. Reads the `.txt` file.
3. Stores the maze in a character matrix.
4. Locates the entrance (`E`).
5. Locates the exit (`S`).
6. Executes the BFS algorithm.
7. Reconstructs the shortest path.
8. Marks the path using `*`.
9. Displays the solved maze.
10. Prints the total number of steps.

---

# 📊 Graph Representation

Although the maze is stored as a matrix, it is internally treated as a graph.

* Every free cell is considered a **vertex**.
* Every valid movement between adjacent cells is an **edge**.
* Only four directions are allowed:

  * Up
  * Down
  * Left
  * Right
* Walls (`#`) are not part of the graph.

---

# 🔍 Algorithm

The project uses the **Breadth-First Search (BFS)** algorithm.

BFS was chosen because every movement has the same cost (1 step). Therefore, BFS guarantees the shortest path between the entrance and the exit.

---

# 🧱 Data Structures Used

* Character Matrix
* `struct Position`
* Queue (FIFO)
* Visited Matrix
* Parent Matrix (Path Reconstruction)

---

# 📈 Time Complexity

### Finding the Entrance

**O(R × C)**

### Finding the Exit

**O(R × C)**

### Breadth-First Search

**O(V + E)**

For a maze represented as a matrix, it can be approximated as:

**O(R × C)**

Where:

* **R** = Number of rows
* **C** = Number of columns

---

# 💻 Compilation

Compile using any ANSI C compatible compiler.

Example (GCC):

```bash
gcc MazeSolver.c -o MazeSolver
```

Run the program:

```bash
./MazeSolver
```

Enter the maze file name:

```text
Maze1.txt
```

---

# 📸 Example Output

```text
=====================================
ORIGINAL MAZE
=====================================

####################
#E....#..........S#
#.###.#.######....#
#..................#
####################

=====================================
BFS RESULT
=====================================

Shortest path found!
Total steps: 42

=====================================
SOLVED MAZE
=====================================

####################
#E****#..........S#
#.###*#.######....#
#....*************#
####################
```

---

# ✨ Features

* Automatic maze loading from `.txt` files.
* Shortest path calculation using BFS.
* Automatic path reconstruction.
* Blue-colored shortest path (Windows Console).
* Supports mazes up to **100 × 100**.
* Compatible with multiple maze files without changing the source code.

---

# 👨‍💻 Author

**Ricardo Falcão Schlieper**

Software Engineering Student
Universidade Católica de Santa Catarina

---

# 📚 License

This project was developed exclusively for academic purposes as part of the **Data Structures** course.
