# 3D Rotating Torus Projection

Variables and Parameters:
- R1: Major radius of the torus.
- R2: Minor radius of the torus.
- u, v: Parametric angles ranging from 0 to 2π.
- A: Rotation angle around the x-axis.
- B: Rotation angle around the y-axis.
- k: Constant representing the viewer's distance from the screen.

Final Equations:

X(u, v, A, B) = (cos(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * sin(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * sin(B) * R2 * sin(v)) / (-sin(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * cos(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * cos(B) * R2 * sin(v) + k)

Y(u, v, A, B) = (cos(A) * (R1 + R2 * cos(v)) * sin(u) - sin(A) * R2 * sin(v)) / (-sin(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * cos(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * cos(B) * R2 * sin(v) + k)

Parametric Surface Equation:

The torus is defined by two radii, R1 (major radius) and R2 (minor radius), and two parametric angles, u and v, ranging from 0 to 2π.

x(u, v) = (R1 + R2 * cos(v)) * cos(u)
y(u, v) = (R1 + R2 * cos(v)) * sin(u)
z(u, v) = R2 * sin(v)

Rotation Matrices:

Rotation around the x-axis by angle A:

Rx(A) = [[1, 0, 0], [0, cos(A), -sin(A)], [0, sin(A), cos(A)]]

Rotation around the y-axis by angle B:

Ry(B) = [[cos(B), 0, sin(B)], [0, 1, 0], [-sin(B), 0, cos(B)]]

Composite Rotation Matrix:

R(A, B) = Ry(B) * Rx(A) = [[cos(B), sin(A) * sin(B), cos(A) * sin(B)], [0, cos(A), -sin(A)], [-sin(B), sin(A) * cos(B), cos(A) * cos(B)]]

Transformed Coordinates:

The transformed coordinates (x', y', z') after applying the rotation matrix are:

x' = cos(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * sin(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * sin(B) * R2 * sin(v)

y' = cos(A) * (R1 + R2 * cos(v)) * sin(u) - sin(A) * R2 * sin(v)

z' = -sin(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * cos(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * cos(B) * R2 * sin(v)

Perspective Projection:

Projecting these coordinates onto a 2D plane:

X = x' / (z' + k)
Y = y' / (z' + k)

Comprehensive Equation:

Combining all elements, the final equation for the 2D projection of the 3D rotating torus is:

X(u, v, A, B) = (cos(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * sin(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * sin(B) * R2 * sin(v)) / (-sin(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * cos(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * cos(B) * R2 * sin(v) + k)

Y(u, v, A, B) = (cos(A) * (R1 + R2 * cos(v)) * sin(u) - sin(A) * R2 * sin(v)) / (-sin(B) * (R1 + R2 * cos(v)) * cos(u) + sin(A) * cos(B) * (R1 + R2 * cos(v)) * sin(u) + cos(A) * cos(B) * R2 * sin(v) + k)





# installing and Running
## Installing
To get this to run on ypour machine do these:
### Prerequisites
GCC:
Linux or MacOS: <br>
If you are any distribution of Linux or MacOS, you can skip this step.
Download and install  ```GCC``` by following <a href="https://code.visualstudio.com/docs/cpp/config-mingw">this page.</a>


Check your installation like this:<br>
1. Open your terminal (Command Prompt or CMD on Windows). <br>
2. Run this command:<br>
```sh
gcc --version
```
<br>
3. Install GIT: <br>
  Follow this page according to your operationg system. <br>

## Installation
1. Clone the repository
     1.1. Open a terminal in a folder. <br>
     1.2. Run this command: <br>
```sh
git clone https://github.com/meetshah1205/3-D-Donut-Terminal.git
```

2. ```cd``` into the folder:
```sh
cd 3-D-Donut-Terminal-main
```

3. ```cd``` into main folder:
```sh
cd Why-You-Need-Maths-For-Programming
```

## Compilition and Execution

1. Compiling: <br>
  1.1. Open terminal in the project folder.
  1.2. Check if you are in the correct folder: <br>
    Run this on Windows:
```sh
dir
```

  And this on Mac/Linux
```sh
ls
```

  It should show ```proof.c``` file.
  
  
  1.3. Compile the code with this command:
  <br>
  Windows:
```sh
gcc proof.c -o proof.exe
```
  Linux/MacOS:
```sh
gcc proof.c -0 proof.out
```

2. Executing the code.
Run this on Windows:
```sh
.\a.exe
```

Run this on Linux/MacOS:
```sh
./a.out
```
