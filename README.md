# SPORRTS-ACTIVITY-RECOGNITION-USING-SENSORS-AND-RASPBERRYPI

Overview
This project aims to build a system that recognizes different sports activities using various sensors connected to a Raspberry Pi. The sensor data is collected, processed, and classified using machine learning models to identify specific sports activities such as running, jumping, walking, etc.

Features
Real-time Activity Recognition: Detects and recognizes various sports activities in real-time.
Sensor Integration: Utilizes multiple sensors, including accelerometers, gyroscopes, and IMUs (Inertial Measurement Units), to collect motion data.
Machine Learning: Trained machine learning model to classify different sports activities.
Raspberry Pi: Serves as the central hub for processing sensor data and running the machine learning model.
Hardware Requirements
Raspberry Pi (Model 3B/4 recommended)
Accelerometer and Gyroscope Sensors (e.g., MPU-6050 or similar IMU sensors)
Power Supply for Raspberry Pi
MicroSD Card (32GB recommended)
Jumper Wires and Breadboard
Optional: External power bank for mobility
Software Requirements
Python 3.x
Libraries:
numpy
pandas
scikit-learn
tensorflow or pytorch
smbus (for I2C communication with sensors)
matplotlib (for data visualization)
Raspberry Pi OS (Raspbian)
SSH (for remote access to Raspberry Pi)
Setup Instructions
1. Install Raspberry Pi OS
Flash the Raspberry Pi OS onto the MicroSD card.
Boot the Raspberry Pi and connect it to your local network.
Install Dependencies
SSH into the Raspberry Pi and install the required Python libraries
sudo apt update
sudo apt install python3-pip
pip3 install numpy pandas scikit-learn tensorflow smbus matplotlib
3. Connect the Sensors
Connect the accelerometer and gyroscope sensors to the Raspberry Pi via I2C protocol. Ensure the connections are secure and check the I2C address using:
sudo i2cdetect -y 1
4. Data Collection
Run the data collection script to record sensor data while performing various sports activities.
python3 collect_data.py
This will save the sensor data in CSV format for further analysis.
5. Model Training
Use the pre-recorded dataset to train the machine learning model. The dataset should consist of labeled activities (e.g., running, walking, jumping). A sample training script is provided:
bash
python3 train_model.py
6. Real-Time Activity Recognition
Once the model is trained, you can run the real-time recognition script to classify sports activities based on incoming sensor data.
bash
