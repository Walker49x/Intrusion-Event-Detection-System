OpenCV Zone-Based Game Event Detection System
Tech Stack: Python · OpenCV · Video Processing

📌 Overview
This project demonstrates a zone-based computer vision system designed for interactive physical games. Using real-time video processing, the system monitors player movement and triggers game events when predefined rules are violated, such as entering restricted zones or crossing virtual boundaries.

In addition to detecting events, the system records highlight video segments, enabling automated generation of gameplay clips and post-game analysis.

🎯 Why This Project Matters
Modern arcade and physical games increasingly rely on computer vision to automate gameplay logic. This project showcases how traditional surveillance-style vision techniques can be repurposed to build:

Laser-vault style challenges

Motion-based arcade games

Escape-room mechanics

Automated rule enforcement without wearables or sensors

The system demonstrates how the flow of player movement → vision logic → game events can be implemented efficiently using Python and OpenCV.

⚙️ How It Works
The gameplay logic is built using a classical computer vision pipeline:

1. Background Subtraction
Uses createBackgroundSubtractorKNN() to separate moving players from the static environment.

2. Noise Reduction
Applies morphological erosion to eliminate minor noise and ensure stable motion detection.

3. Motion & Contour Analysis
Extracts contours from foreground regions using findContours() to identify significant movement areas.

4. Zone-Based Event Logic
Evaluates the size and spatial location of detected motion to determine whether a game event (zone breach) has occurred.

5. Event Triggering & Video Capture
When a rule is violated:

A visual game alert is displayed.

Relevant gameplay frames are recorded.

Event footage is saved for highlights or analysis.

🛠️ Tech Stack & Prerequisites
Ensure you have Python 3.6+ installed along with the following libraries:

OpenCV (opencv-python)

NumPy

Matplotlib

MoviePy

ImageIO

IPython (for Jupyter/Colab environments)

Installation
Bash

pip install opencv-python matplotlib ipython moviepy numpy imageio
🧪 Getting Started
Follow these steps to run the project locally:

Clone the repository:

Bash

git clone https://github.com/Brandi-Kinard/opencv-intrusion-detection.git
Open the notebook: Open the .ipynb file locally or via Google Colab.

Run cells: Execute the cells sequentially to observe:

Motion detection

Zone breach detection

Event-triggered video output

🎮 Use Cases
Arcade Gaming: Motion-based scoring systems.

Physical Security: Laser-vault challenges.

Automation: Escape room interaction logic.

Analytics: Gameplay highlight generation for sports or esports.

🚀 Potential Enhancements
[ ] Multi-player tracking: Identifying and tracking separate IDs.

[ ] Dynamic Difficulty: Adjusting detection thresholds in real-time.

[ ] Integrations: Connecting events to Unity or web-based dashboards.

[ ] Feedback: Adding real-time audio cues upon breach detection.
