# EMG-Controlled Game & Data Analysis

<iframe width="560" height="315" src="https://www.youtube.com/embed/R4kmWpyMrCM?si=QD3PrQiske5TVufq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Project Introduction
This ambitious project, a joint venture between the **University of Glasgow**, under the guidance of **[Jonathan Grizou](https://jgrizou.com/)** and **Imperial College London** with **[Xiaoqi Wang](https://www.linkedin.com/in/xiaoqi-wang/)** under **[Cristohpher Salvi](https://www.imperial.ac.uk/people/c.salvi)**, aimed to exploit the potential of off-the-shelf components to use EMG data for control and deep data analysis. 

The cornerstone of this project is a game of 'Breakout', controlled through wrist movements using two EMG sensors interfaced with an Arduino Nano. In parallel, we developed datasets capturing the nuances of EMG signals in relation to strength exertion, specific finger movements, and body tracking.

**[Link to project GitHub repo](https://github.com/FKGSOFTWARE/EMGControl)**

## Features and Deliverables

  Sensor placement:
    ![Sensor placement diagram](https://raw.githubusercontent.com/FKGSOFTWARE/EMGControl/master/Images/arm%20anatomical%20emg%20sensors%20marked.jpeg)
    
  Basic system diagram: 
    ![Basic system diagram](https://raw.githubusercontent.com/FKGSOFTWARE/EMGControl/master/Images/hardware%20diagram.jpeg)
    
- **Breakout Game Control via EMG**: Experience a unique gaming interface controlled through wrist flexion and extension.
  - **Visuals Needed**: Video demonstration showcasing the EMG-based game controls.
- **Datasets**:
  - **Strength vs Signal Strength**: Combining EMG sensors with a load cell to analyze the relationship.
    - [Download Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/official%20recordings/official%20recordings%2010min/1%20load%202%20emg%2010min.csv?download=)
    - **Visuals Needed**: Sensor diagrams and data visualization charts.
  - **Finger Movement Detection**: Integrating EMG sensors with touch sensors to deduce specific finger actions.
    - [Download 2 Finger Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/official%20recordings/official%20recordings%2010min/2%20touch%202%20emg%2010min.csv?download=)
    - [Download 3 Finger Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/official%20recordings/official%20recordings%2010min/3%20touch%202%20emg%2010min.csv?download=)
    - [Download 5 Finger Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/official%20recordings/official%20recordings%2010min/5%20touch%202%20emg%2010min.csv?download=)
    - **Visuals Needed**: Hand sensor placement diagrams and data visualization charts.
  - **Hand and Body Tracking**: Initial hand and digit tracking, later focusing on palm angles in relation to the forearm using MediaPipe.
    
    - [Download Raw Wrist Angle Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/working_scirpts_for_dataset/wrist_angle_dataset/_output/TA_body_and_hand_landmarks_data_TimeVideo_20230908_163442.csv?download=)
   
      
      ![Iterpolated Plot](https://raw.githubusercontent.com/FKGSOFTWARE/EMGControl/8ac7afeaabe2f3f871786fa9da782ee1d069a8b4/output/official%20recordings/official%20recordings%2010min/official%20EMG%20mediapipe%2010%20minute%20-%20interpolation.png)
    - [Download Interpolated Wrist Angle Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/official%20recordings/official%20recordings%2010min/official%20EMG%20mediapipe%2010%20minute%20-%20interpolation.csv?download=)
   
      
      ![No NaN Plot](https://raw.githubusercontent.com/FKGSOFTWARE/EMGControl/8ac7afeaabe2f3f871786fa9da782ee1d069a8b4/output/official%20recordings/official%20recordings%2010min/official%20EMG%20mediapipe%2010%20minute%20-%20no%20NaN.png)
    - [Download No NaN Wrist Angle Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/official%20recordings/official%20recordings%2010min/official%20EMG%20mediapipe%2010%20minute%20-%20no%20NaN.csv?download=)
   
      
    - [Download Full Wrist Angle Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/working_scirpts_for_dataset/wrist_angle_dataset/_output/updated_body_and_hand_landmarks_data_TimeVideo_20230908_163442.csv?download=)
    - **Visuals Needed**: Video demonstration and data visualization charts highlighting angles.

- **Basic EMG for wrist Flexion and Extension**:
  - <iframe width="560" height="315" src="https://www.youtube.com/embed/fjLq5sRPJhM?si=kGab2tkeCibMa3Me" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  - [Basic EMG Dataset](https://github.com/FKGSOFTWARE/EMGControl/raw/master/output/gesture%20recordings/2%20emg%20mediapipe%2010min.csv?download=)

## Challenges and Learnings
- **Challenges**: The task of integrating multiple components and creating bespoke tools tailored to our requirements was a considerable challenge. Further, the project had to be executed within a constrained budget, pushing us to innovate and optimize.
- **Major Takeaways**: The adoption of Large Language Models (LLMs) drastically reduced the time required for code development and refinement. This optimization made it feasible to tackle larger projects in a significantly shorter timeframe.


## Feedback and Public Interaction
We're excited to showcase our project at Glasgow University's **Exploration 2023** event, a grand stage for research displays. This will offer us invaluable feedback from the public and the academic community, which we eagerly anticipate.


## Future Direction
Our vision for the project extends beyond its current state. We aim to refine the game, enhancing its interaction and responsiveness. Moreover, we're eager to uncover the untapped potential of these basic sensors, especially when combined with signature analysis and advanced machine learning techniques.


## Included Files and Scripts
Below is a brief description of some of the main files in the github attached to this project that any interested parties are free to use. Not all files have been mentioned but proper documentation will be coming.
### Arduino Scripts:

#### 1. 2_emg_sensor_default.cpp
- **Description**: Interfacing with up to two EMG sensors.
- **Usage**:
  - Upload to your Arduino board.
  - Connect sensors to specified analog pins.
  - Establish serial connection.

#### 2. 2_emg_1_load_dac.cpp
- **Description**: Interface with two EMG sensors and a load cell.
- **Usage**: 
  - Upload to Arduino.
  - Connect sensors and load cell to specified pins.

#### 3. arduino giga load cell loadout.cpp
- **Description**: Interface specifically with a load cell using the HX711 library.
- **Usage**: 
  - Upload to Arduino.
  - Connect the load cell to specified pins.

#### 4. 2_emg_sensor_game.cpp
- **Description**: Interfacing with two EMG sensors for game-related applications.
- **Usage**: 
  - Upload to Arduino.
  - Connect sensors to specified pins.

### Python Scripts:

#### 5. AEMG_SP default.py
- **Description**: Read and process the serial data from the Arduino and visualize the sensor data.
- **Usage**: 
  - Install necessary libraries.
  - Run the script.

#### 6. hand+body_to_angle_001.py
- **Description**: Calculate angles based on hand and body landmarks.
- **Usage**: 
  - Specify file path containing landmark data.
  - Run the script.

#### 7. mediapipe_handbones.py
- **Description**: Process video data to extract hand landmark information using MediaPipe.
- **Usage**: 
  - Specify video file directory.
  - Run the script.

#### 8. complete_script_with_interpolation.py
- **Description**: Process datasets related to arm angles and EMG readings.
- **Usage**: 
  - Specify dataset paths.
  - Run the script.

#### 9. AEMG_SP filters + toggle + mouse.py
- **Description**: Interface with EMG sensors and apply filters. Provides functionalities for toggling and mouse interactions.
- **Usage**: 
  - Set configurations and file paths.
  - Run the script.

#### 10. plotting_script_MOUSE.py
- **Description**: Visualize data from CSV files.
- **Usage**: 
  - Specify CSV directory.
  - Run the script.

#### 11. AEMG + Filters + Game Q - working.py
- **Description**: Interface with EMG sensors, apply filters, and connect to a gaming module.
- **Usage**: 
  - Set configurations.
  - Run the script.

#### 12. AEMG_SP filters.py
- **Description**: Interface with EMG sensors and apply data filters.
- **Usage**: 
  - Set configurations.
  - Run the script.

#### 13. Breakout_attempt_002.py
- **Description**: Classic Breakout game potentially integrated with other project parts.
- **Usage**: 
  - Run the script.
  - Control the paddle using integrated controls.


## Setting Up & Usage

### Arduino:
1. Upload the desired `.cpp` file to your Arduino board.
2. Ensure the sensors/load cells are connected to the specified pins.
3. Start serial communication with the specified baud rate.

### Python:
1. Install the required libraries:
   ```
   pip install numpy serial pandas PyQt5 pyqtgraph
   ```
2. Navigate to the script's directory and run your desired `.py` file:
   ```
   python [script_name].py
   ```


## Customization & Troubleshooting

## Customization
- Modify constants in Python scripts as required.
- Update `sensor_placement_dict` for additional sensors or change placements.

## Troubleshooting
- Ensure the Arduino is connected and that the correct COM port is selected in the Python script.
- Ensure that the baud rate matches between the Arduino and Python scripts.
- Check Python script logs for errors or anomalies.


## Conclusion and Invitation
This project embodies the fusion of readily available hardware components with innovative software techniques to forge new frontiers in game control and data analytics. We invite academics, enthusiasts, and curious minds alike to dive into our work, leverage the tools we've curated, and take them to unprecedented heights.
