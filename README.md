# MATLAB Image Segmentation Project

This repository contains a MATLAB script for segmenting and processing an image of fruits. The script demonstrates how to perform image segmentation in the HSV color space to isolate specific objects based on their color characteristics. The project focuses on identifying apples, bananas, oranges, and kiwis.

## Features

- **Image Reading and Conversion:**
  - Reads an input image and converts it from RGB to HSV color space for effective segmentation.
- **HSV Channel Separation:**
  - Splits the image into individual Hue (H), Saturation (S), and Value (V) channels for precise analysis.
- **Color-based Segmentation:**
  - Uses threshold values to segment specific fruits based on their color ranges in the HSV space.
- **Masked Image Generation:**
  - Creates binary masks for each fruit and applies them to generate separate images highlighting each fruit.
- **Visualization:**
  - Displays intermediate steps and results using MATLAB's `subplot` functionality.

## How It Works

1. **Image Preprocessing:**
   - The script reads an input image (`fruits.jpg`) and converts it from RGB to HSV.
2. **Channel Analysis:**
   - Splits the HSV image into separate channels: H, S, and V.
   - Similarly, splits the original RGB image into R, G, and B channels.
3. **Segmentation:**
   - Defines HSV ranges for each fruit:
     - **Apple and Banana:** Uses specific Hue, Saturation, and Value ranges to create a binary mask.
     - **Orange:** Uses a distinct set of thresholds for segmentation.
     - **Kiwi:** Another unique set of thresholds for identification.
   - Combines binary masks using logical operations to refine the segmentation.
4. **Masked Image Extraction:**
   - Multiplies the original RGB channels by the binary masks to extract each fruit.
5. **Visualization:**
   - Uses `subplot` to display intermediate results, including individual channels, binary masks, and segmented fruit images.

## Requirements

- MATLAB R2018b or later.
- `fruits.jpg`: An input image containing multiple fruits for segmentation.

## Running the Script

1. Clone this repository and navigate to the project directory:
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. Place the input image (`fruits.jpg`) in the same directory as the script.

3. Open MATLAB and run the script:
   ```matlab
   run <script_name>.m
   ```

4. View the results displayed in a 4x4 grid of subplots.

## Output Description

- **HSV Channels:**
  - Displays the HSV image and its individual H, S, and V components.
- **Binary Masks:**
  - Shows binary masks for apples, bananas, oranges, and kiwis.
- **Segmented Fruits:**
  - Displays images of each fruit segmented from the original image.

## Customization

- Modify the HSV threshold ranges in the script to adapt the segmentation for different images or objects.
- Change the input image to test the script with other datasets.


