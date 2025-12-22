

 Insertion Sort Visualization with Pygame

This project visualizes the **Insertion Sort** algorithm using the `Pygame` library. It provides a graphical representation of how the sorting algorithm works by highlighting the current element being compared and the key element during the sorting process. The program also integrates sound effects using the `winsound` library to enhance the visual experience.

## Features

- **Graphical Visualization**: Each bar represents an element in the array. As the algorithm progresses, bars are highlighted in different colors to show which elements are being compared.
  - **Red**: The current element being compared.
  - **Green**: The key element being inserted in the sorted portion.
- **Sound Effects**: A beep sound is played each time an element is moved, providing auditory feedback during sorting.

## Prerequisites

Before running the program, ensure you have the following:

- Python 3.x installed on your machine.
- The following Python libraries installed:
  - `pygame`: Install via `pip`:
    ```bash
    pip install pygame
    ```

- **Windows OS**: This script uses the `winsound` library, which is available only on Windows. For other operating systems, the sound functionality will need to be modified or removed.

## How It Works

The project displays an array of 50 randomly generated elements, visualized as vertical bars of varying heights. As the Insertion Sort algorithm sorts the array, bars representing the elements are dynamically redrawn to show their movement and sorting process. Each step of the algorithm is accompanied by a short delay to allow users to see the changes in real time.

### Color Key:

- **Blue**: Bars that are not currently being sorted or compared.
- **Red**: The current bar being compared.
- **Green**: The key element being inserted into its correct position.

## Installation

1. Clone the repository or download the Python script.
2. Install the required dependencies:
   ```bash
   pip install pygame
   ```

3. Run the script:
   ```bash
   python insertion_sort_visualization.py
   ```

## Usage

1. Upon running the script, a window will open, displaying 50 vertical bars, each representing a randomly generated integer.
2. The sorting will start automatically, and you will see the bars rearranged as the Insertion Sort algorithm progresses.
3. The algorithm will be visualized with highlighted bars and sound effects indicating element movements.
4. Once the sorting is complete, the sorted bars will remain on the screen for 3 seconds before the program exits.

## Code Overview

### `draw_bars(window, arr, current=None, key_pos=None)`
This function is responsible for drawing the bars on the screen. It takes the `window` surface, the array `arr` to be visualized, and two optional parameters: `current`, which is the index of the currently highlighted bar, and `key_pos`, which is the index of the key element.

### `insertion_sort(arr)`
This function implements the Insertion Sort algorithm. It updates the array while calling `draw_bars()` to visualize each step of the sorting process. Sound effects are also played for each comparison and movement of elements.

### `main()`
The main function initializes the `pygame` window, generates a random array, and calls the `insertion_sort()` function to start the sorting visualization. It handles the event loop to close the window when the sorting is complete or when the user quits the program.

## Customization

- **Array Size**: You can modify the number of elements in the array by changing the value of `_ in range(50)` in the `main()` function to a different number.
- **Speed**: The delay between each step of sorting can be adjusted by modifying the `pygame.time.delay(100)` value inside the `insertion_sort()` function.
- **Sound**: You can change the frequency or duration of the beep sound by adjusting the arguments in `winsound.Beep(440, 100)`.

## Troubleshooting

- **No Sound**: If you’re using a non-Windows operating system, the `winsound` library will not work. Consider removing the `winsound.Beep()` calls or replacing them with a cross-platform alternative.
- **Performance Issues**: If the visualization runs too slowly, try reducing the number of bars or increasing the sorting speed by lowering the delay value.

## License

This project is licensed under the MIT License. You are free to modify and distribute the code as needed.

---

This **README** file provides the necessary details for installing, configuring, and running your **Insertion Sort Visualization** project.
