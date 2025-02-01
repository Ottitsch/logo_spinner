# ASCII Logo Spinner

This project consists of a C-based ASCII art rendering system, inspired by "donut.c", that converts images into ASCII representations and renders them dynamically in the terminal. The system consists of two key components:

- `convert.py`: Converts an image into a header file containing ASCII representation data.
- `logo.c`: C program that renders the ASCII image with shading and rotation effects.

## Features
- Converts an image into an ASCII representation using Python.
- Dynamically renders ASCII art in a terminal with rotation and shading effects.

## Dependencies
This project requires:
- Python 3
- Pillow (Python Imaging Library)
- A C compiler (e.g., `gcc`)

## Usage
### Step 1: Convert an Image
Convert an image (e.g., `logo.png`) into ASCII format:
```sh
python convert.py logo.png
```
This generates a `data.h` file that will be used by `logo.c`.

### Step 2: Compile the Renderer
Compile the C program:
```sh
gcc logo.c -o logo -lm
```

### Step 3: Run the Renderer
Run the compiled program:
```sh
./logo
```

## How It Works
1. **Image Processing** (`convert.py`):
   - Resizes the image to 128x128 pixels.
   - Extracts brightness values and converts them into ASCII characters.
   - Saves the data into `data.h`.
2. **Rendering** (`logo.c`):
   - Reads the `data.h` ASCII data.
   - Applies rotation, shading, and perspective projection.
   - Continuously updates and displays the ASCII image in the terminal.

## Contributions
Contributions, issues, and feature requests are welcome!

## Author
Developed by Ottitsch. Feel free to reach out or contribute to this project!

