# Behavioral Mouse Dynamics Pilot Test 🖱️📊

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)]()
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)]()

## 📌 Overview
This repository contains a standalone, client-side web application designed to conduct human-computer interaction (HCI) pilot tests. The tool captures high-frequency mouse telemetry data—specifically coordinate tracking (X, Y), velocity, and click patterns—while users perform designated cognitive tasks. 

## 🎓 Research Context
This tool was developed as **Work Package 2: Technical Pilot & Feasibility Phase** for the undergraduate software engineering research project: *"Emotion-Adaptive Focus Mode Browser Extension"*. 

The primary goal of this pilot is to gather empirical behavioral data to mathematically determine the thresholds for "Jitter" and "Velocity" in relation to cognitive load. It also serves to calibrate "Rage Click" detection logic to prevent false positives in the final machine-learning fusion engine.

## ✨ Key Features
* **Zero-Setup Execution:** Runs entirely in the browser using standard HTML/CSS/JS. No local server or backend required.
* **Controlled Task Environments:**
    * **Task A (Low Stress):** A baseline reading comprehension task without time constraints.
    * **Task B (High Stress):** A timed logic and mathematics section designed to induce mild cognitive load and urgency[cite: 424].
* **High-Frequency Telemetry:** Captures mouse movements throttled to ~60Hz to calculate real-time movement velocity.
* **Automated CSV Export:** Compiles captured data into a structured CSV file for immediate statistical analysis.

## 🚀 How to Use

1. **Clone or Download** this repository to your local machine.
2. Open `pilot_test.html` directly in any modern web browser (Chrome, Firefox, Edge).
3. **Setup:** Enter a Participant ID (or leave blank for an anonymous ID) and click **Start Recording**.
4. **Execution:** * Have the participant complete Task A at their natural pace.
    * Have the participant complete Task B within the 30-second implied limit.
5. **Export:** Click the **Download Raw Data (CSV)** button at the bottom of the page to save the session logs.

## 🗄️ Data Output Format
The exported CSV file contains the following structured data:

| Column | Description |
| :--- | :--- |
| `Timestamp` | Standard UNIX epoch timestamp (ms). |
| `Participant` | Unique identifier for the test subject. |
| `EventType` | Type of interaction (e.g., `MOVE`, `GLOBAL_CLICK`, `SELECTED: [Option]`, `MARKER`). |
| `X` | Mouse X-coordinate on the viewport. |
| `Y` | Mouse Y-coordinate on the viewport. |
| `Velocity` | Calculated speed between the current and previous coordinate (px/ms). |

## 🛠️ UI/UX Design
The interface utilizes a modern, calm, light-themed aesthetic to ensure the UI itself does not induce baseline stress prior to the tasks. It features soft shadows, intuitive active states, and clear typography to maintain a highly controlled testing environment.

## 👤 Author
**Baddewaththe Laalitha Niroshan Gunarathna** 
* BSc (Hons) Software Engineering Undergraduate
* CINEC Campus

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
