![image alt](*https://github.com/Lucifer1406/OpenCV_Based_Projects-Using-Pyhton/issues/3#issue-2767755392)

# Lane Detection with OpenCV

This project demonstrates lane detection in images and videos using OpenCV. It processes frames to identify and highlight lane lines using techniques like edge detection, Hough transforms, and region masking.

## Features
- Lane detection on static images.
- Real-time lane detection on video files.
- Flexible parameters for edge detection, line detection, and region of interest masking.

## Prerequisites
To run this project, ensure you have the following installed:
- Python (3.x)
- OpenCV (`cv2`)
- NumPy
- Matplotlib (optional, for visualizations)

## Installation
1. Clone the repository or download the script.
2. Install the required Python libraries:
   ```bash
   pip install opencv-python-headless numpy matplotlib
   ```

## File Structure
- **main.py**: The primary script containing all functions and execution logic.
- **test_image.jpg**: (Optional) A sample image for static lane detection (commented in the script).
- **test2.mp4**: A sample video file for real-time lane detection.

## Functions Overview
### `make_coordinates(image, line_parameters)`
Calculates the coordinates of a line based on its slope and intercept to overlay on the image.

### `average_slope_intercept(image, lines)`
Separates lines into left and right lane markers, averages their parameters, and creates a single line for each lane.

### `canny(image)`
Applies grayscale conversion, Gaussian blur, and Canny edge detection to an image.

### `display_lines(image, lines)`
Draws the detected lane lines on a blank image.

### `region_of_interest(image)`
Masks the image to focus on the region of interest (triangular region where lanes are expected).

## Usage
### Image Processing
1. Uncomment the **Image Processing** section in the script.
2. Replace `'test_image.jpg'` with the path to your image file.
3. Run the script:
   ```bash
   python main.py
   ```
4. The resulting image with detected lanes will be displayed.

### Video Processing
1. Ensure a video file (e.g., `test2.mp4`) is in the same directory as the script.
2. Run the script:
   ```bash
   python main.py
   ```
3. The video will play with lane lines overlaid. Press `q` to quit.

## Output
- For images, the script overlays lane lines and displays the processed image.
- For videos, the script processes each frame and overlays lane lines in real-time.

## Customization
- **Edge Detection**:
  Adjust parameters in `cv2.Canny()` inside the `canny()` function.
- **Hough Transform**:
  Modify the parameters of `cv2.HoughLinesP()` (e.g., `minLineLength`, `maxLineGap`) to fine-tune line detection.
- **Region Masking**:
  Update the `polygons` array in `region_of_interest()` to redefine the region of interest.

## Limitations
- Designed for straight roads with clear lane markings.
- Performance may degrade in low-light or complex environments.

## Acknowledgments
- This project uses OpenCV, an open-source library for computer vision tasks.
- Inspired by standard lane detection techniques in self-driving car research.

## License
This project is open-source and available under the MIT License.

