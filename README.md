# 🔎 Maze Solver

This repository is part of a **university assignment** from the **first-year, first semester**. It demonstrates a **maze-solving algorithm** using **Java**. The project processes maze images and determines connectivity between different parts of the maze using **Union-Find (Disjoint Set)**.

## 📄 Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Project Overview

The **Maze Solver** processes images of mazes and determines whether there is a solution by checking connectivity between the **start** and **end points**. The program uses **image processing** to analyze the maze structure and applies **Union-Find (Disjoint Set)** to determine connected components. The project supports:

✅ **Loading and displaying maze images**
✅ **Processing images to identify walls and paths**
✅ **Detecting connected components**
✅ **Determining if a maze is solvable**
✅ **Generating a visual representation of the connected components**

## 🛠️ Technologies Used

| Technology | Description |
|------------|------------|
| **Java** | Programming language |
| **Swing** | GUI framework for displaying images |
| **AWT** | Used for image manipulation and color processing |
| **ImageIO** | Handles reading and writing image files |
| **Union-Find (Disjoint Set)** | Data structure for managing connected components |

## 📂 Project Structure

```
MazeSolver/
├── src/
│   ├── DisplayImage.java      # Handles loading and displaying images
│   ├── Maze.java              # Implements the maze processing and connectivity check
│   ├── UnionFind.java         # Implements Union-Find (Disjoint Set) data structure
├── images/                    # Contains sample maze images
├── README.md                  # Project documentation
└── MazeSolver.iml             # IntelliJ IDEA project file
```

## 🚀 Getting Started

### ✅ Prerequisites

Ensure you have the following installed:
- [Java JDK 8+](https://www.oracle.com/java/technologies/javase-downloads.html)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) or any Java IDE

### 🔧 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ronsalomon97/MazeSolver.git
   cd MazeSolver
   ```
2. **Compile the Java files:**
   ```bash
   javac src/*.java
   ```
3. **Run the program with a maze image:**
   ```bash
   java src.Maze images/maze2.PNG
   ```

## 📌 Usage

### Running the Maze Solver

- **Display an image:**
  ```java
  DisplayImage img = new DisplayImage("images/maze2.PNG");
  img.show();
  ```
- **Check if the maze is solvable:**
  ```java
  Maze maze = new Maze("images/maze2.PNG", Color.BLACK);
  System.out.println("Maze has solution: " + maze.mazeHasSolution());
  ```
- **Get number of connected components:**
  ```java
  System.out.println("Number of components: " + maze.getNumComponents());
  ```
- **Generate and display the connected components image:**
  ```java
  DisplayImage compImg = maze.getComponentImage();
  compImg.show();
  ```

## 🧪 Testing

To test maze connectivity and component detection, use the `main` method in `Maze.java`:
```bash
java src.Maze images/maze2.PNG
```
This will:
1. **Check if the maze has a solution**
2. **Print the number of connected components**
3. **Display the maze with distinct colors for each component**

## ⚙️ How It Works

1. **Load the maze image**: Reads an image file and extracts pixel data.
2. **Identify walls and paths**: Uses pixel intensity to determine open paths and walls.
3. **Apply Union-Find**: Groups connected path pixels into components.
4. **Check connectivity**: Determines if the start and end points belong to the same component.
5. **Visualize the components**: Generates an image where each component is colored differently.

## 🤝 Contributing

This repository is part of a **university assignment**, so external contributions are not expected. However, feel free to open an issue if you have suggestions.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

