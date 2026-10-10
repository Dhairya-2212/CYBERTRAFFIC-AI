# CYBERTRAFFIC-AI

🚦 CYBERTRAFFIC AI

Adaptive Signal Control & Vision Nexus

CYBERTRAFFIC AI is a comprehensive, software-driven blueprint for the smart cities of tomorrow. It bridges real-time computer vision analytics with fuzzy logic decision-making to create intelligent, responsive, and autonomous traffic intersections.

By replacing traditional fixed-timer traffic lights with an adaptive system, CYBERTRAFFIC AI aims to reduce intersection delay, save idle fuel, cut carbon emissions, and instantly clear paths for emergency vehicles.

🌟 Features

This project consists of an interactive web simulation platform and standalone Python backend scripts.

Fuzzy Logic Controller: Real-time Mamdani inference engine that calculates crisp green-light durations based on queue length and waiting time.

Live 4-Way Simulator: A 60-FPS Canvas-based physics engine demonstrating the adaptive AI versus a traditional fixed 45-second timer.

AI Video Analyzer (Web & Python): Detects, tracks, and counts vehicles, estimating their speed (km/h) and flagging violations using MobileNet-SSD.

10-Scenario Benchmark Matrix: Validates delay reduction, fuel waste prevention, and emission cuts across diverse traffic regimes.

Emergency Vehicle Priority (EVP): Automatically detects ambulances and forces an immediate 90-second green wave corridor.

🛠️ Technology Stack

Frontend / Web Platform: HTML5, CSS3, Vanilla JavaScript, HTML5 Canvas API

Web AI: TensorFlow.js, COCO-SSD (Browser-side inference)

Python Backend: Python 3.x

Computer Vision: OpenCV (cv2), MobileNet-SSD Caffe Model

Mathematics: NumPy (Membership functions, Center of Gravity defuzzification)

📁 Repository Structure

cybertraffic-ai/
│
├── index.html                    # The main interactive web application
├── ai_video_analyzer.py          # Standalone Python script for video analysis
├── traffic_fuzzy_controller.py   # Standalone Python script for the math/logic
├── requirements.txt              # Python dependencies
├── .gitignore                    # Git ignore rules
└── README.md                     # Project documentation


🚀 Installation & Usage

1. The Web Application

The web app is entirely client-side. No server is required!

Simply double-click index.html to open it in any modern web browser (Chrome, Edge, Firefox, Safari).

The AI Video Analyzer tab includes a built-in demo, or you can upload your own MP4/WebM files to test locally.

2. Python Backend Scripts

To run the standalone Python scripts, you will need Python 3 installed.

Clone the repository:

git clone https://github.com/yourusername/cybertraffic-ai.git
cd cybertraffic-ai


Install dependencies:

pip install -r requirements.txt


Run the AI Video Analyzer:

python ai_video_analyzer.py


(Note: On its first run, this script will automatically download the required ~23MB MobileNet-SSD model files to your directory).

Test the Fuzzy Controller:
You can import the TrafficFuzzyController class into your own Python projects:

from traffic_fuzzy_controller import TrafficFuzzyController

controller = TrafficFuzzyController()
# Calculate green time for 30 queued cars waiting 5 minutes
green_time = controller.compute(queue=30, wait=5.0)
print(f"Recommended Green Phase: {green_time} seconds")


📊 Benchmarks

Tested against a standard 45-second fixed timer across 10 scenarios, CYBERTRAFFIC AI demonstrates:

~43% Average Efficiency Boost

Significant reduction in cross-street idling during low-traffic periods.

Dynamic clearing of multi-block backups during rush hour surges.

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
