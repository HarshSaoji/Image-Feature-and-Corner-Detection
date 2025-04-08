🖼️ Image-Feature-and-Corner-Detection

This repository demonstrates key techniques in image feature detection and matching using OpenCV. It includes implementations of the SIFT and SURF algorithms for feature detection and description, as well as RANSAC for outlier removal and estimating geometric transformations between images.

📂 Contents
1. SIFT Keypoint Detection and Matching
File: sift_matching.py

This script implements the SIFT (Scale-Invariant Feature Transform) algorithm to:

Detect keypoints in two images

Compute descriptors

Match the descriptors using a Brute-Force matcher

Apply Lowe’s ratio test to filter good matches

Visualize the keypoint matches

SIFT is scale and rotation invariant, making it suitable for detecting features under varying conditions.

2. SURF Keypoint Detection on Scaled/Rotated Images
File: surf_matching.py

This script uses the SURF (Speeded-Up Robust Features) algorithm to:

Detect keypoints and descriptors in two images, including those with different scales and orientations

Perform descriptor matching using Brute-Force matcher

Apply Lowe’s ratio test for good match filtering

Display the matched features

🔒 Note: SURF is a patented algorithm, so this code requires opencv-contrib-python.

3. RANSAC for Outlier Removal and Transformation Estimation
File: ransac_filtering.py

This script shows how to:

Use SIFT for feature detection and descriptor computation

Match keypoints using the Brute-Force matcher and Lowe's ratio test

Apply RANSAC (Random Sample Consensus) to:

Remove outlier matches

Estimate a homography matrix between the two sets of matched keypoints

Visualize only the inlier matches (matches that conform to the estimated transformation)

This is useful for applications like image stitching, panorama generation, and geometric alignment.

🧰 Requirements
Python 3.x

OpenCV (with contrib module for SURF)

Matplotlib (for plotting)

Install dependencies
bash
Copy
Edit
pip install opencv-contrib-python matplotlib
📸 Example Use
Make sure to replace 'image1.jpg' and 'image2.jpg' in the scripts with the actual image filenames you are using.

📌 License
This repository is for educational and research purposes only.

