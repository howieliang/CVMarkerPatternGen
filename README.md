# CV Marker Pattern Generator

CV Marker Pattern Generator is a Python script for generating marker patterns for computer vision applications. 

by Rong-Hao Liang: r.liang@tue.nl

Update (Oct 13, 2023): Tested with opencv-python ver. 4.6.0.66 and Python 3.9

The CV Marker Pattern Generator is a Python script that allows you to generate marker patterns for computer vision applications. These marker patterns can be used for tasks such as camera calibration and object tracking. This script is adapted from code originally written by Jes Fink-Jensen and Loe Feijs. It uses the OpenCV library for computer vision tasks.

## Install Python Environment

1. Install MiniConda
    - [https://docs.conda.io/projects/miniconda/en/latest/miniconda-other-installer-links.html](https://docs.conda.io/projects/miniconda/en/latest/miniconda-other-installer-links.html)
2. Open MiniConda Prompt / PowerShell (Windows) or Terminal (Mac)
   
```bash
conda create --name p39 python=3.9
conda activate p39
pip install opencv-contrib-python==4.6.0.66
```

## Usage Example

Here's an example command to generate a marker pattern:

```bash
python cv_marker_gen_pattern.py -o "output_pattern.png" -i 0 -t "DICT_ARUCO_ORIGINAL" -d 72 -s 50 -m 5 -x 3 -y 4 --write-id -p "ful"
```

This command generates a marker pattern with the specified parameters and saves it as "output_pattern.png".

## Command Line Arguments

The script accepts various command line arguments to customize the generated marker pattern. Here is a brief description of each argument:

- `o`, `-output`: Path to the output image containing the ArUCo tag.
- `i`, `-id`: ID of the first ArUCo tag to generate.
- `t`, `-type`: Type of ArUCo tag to generate (default: DICT_ARUCO_ORIGINAL).
- `d`, `-dpi`: DPI (dots per inch) of the output print (default: 72).
- `s`, `-size`: Size in millimeters of the ArUco tag (default: 50).
- `m`, `-margin`: Size in millimeters of the margins between the ArUco tags (default: 5).
- `x`, `-x`: Number of ArUco tags in the X direction (default: 3).
- `y`, `-y`: Number of ArUco tags in the Y direction (default: 4).
- `-write-id`: Write the ID of the tag on the pattern (default: True).
- `p`, `-pattern`: Type of pattern (default: ful).

## Supported Patterns
The CV Marker Pattern Generator supports various types of patterns, each designed for specific use cases. You can specify the pattern type using the -p or --pattern command line argument. Here are the supported patterns:

- ful: FULL Pattern. This pattern generates a full pattern matrix.
- chk: CHECKERS_2X2 Pattern. Generates a checkerboard pattern with a 2x2 grid.
- pt4: PUPPY_TOOTH_4X4 Pattern. Creates a 4x4 puppy tooth pattern.
- pdp8: PIED_DE_POULES_8X8 Pattern. Generates an 8x8 pied de poules pattern.
- hb4: HERRING_BONE_4X4 Pattern. Creates a 4x4 herringbone pattern.
- bt4: BROKEN_TWILL_4X4 Pattern. Generates a 4x4 broken twill pattern.
- ge: GOOZE_EYE_6X8 Pattern. Creates a 6x8 gooze eye pattern.
You can choose the pattern best suits your application by specifying the pattern type in the command line arguments.

## Supported ArUCo Types

The following ArUCo types are supported:

- DICT_4X4_50
- DICT_4X4_100
- DICT_4X4_250
- DICT_4X4_1000
- DICT_5X5_50
- DICT_5X5_100
- DICT_5X5_250
- DICT_5X5_1000
- DICT_6X6_50
- DICT_6X6_100
- DICT_6X6_250
- DICT_6X6_1000
- DICT_7X7_50
- DICT_7X7_100
- DICT_7X7_250
- DICT_7X7_1000
- DICT_ARUCO_ORIGINAL
- DICT_APRILTAG_16h5
- DICT_APRILTAG_25h9
- DICT_APRILTAG_36h10
- DICT_APRILTAG_36h11

## Output

The script will generate an image containing the ArUCo tags based on the provided parameters. The output will be saved to the specified path.

## Notes

- Make sure you have the required libraries (Python, OpenCV) installed before running the script.
- Check that the grid dimensions and sizes fit within the specified DPI and A4 paper size.
- If you encounter any issues, contact Rong-Hao Liang via (r.liang@tue.nl)

Enjoy using the CV Marker Pattern Generator for your computer vision projects!
