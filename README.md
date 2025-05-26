# Wake Word Detection System for Arduino Nano 33 BLE Sense

This project implements a wake word detection system on the Arduino Nano 33 BLE Sense board using Edge Impulse and TensorFlow Lite Micro. The system uses MFCC (Mel-frequency cepstral coefficients) preprocessing and a 1D CNN architecture for efficient wake word detection.

## Hardware Requirements

- Arduino Nano 33 BLE Sense
- USB Type-C cable
- Computer with Arduino IDE installed

## Software Requirements

- Arduino IDE 2.0 or later
- Edge Impulse CLI
- TensorFlow Lite Micro library
- Arduino_MKRMEM library
- Arduino_LSM9DS1 library
- PDM library

## Installation Steps

1. **Install Arduino IDE**
   - Download and install Arduino IDE from [arduino.cc](https://www.arduino.cc/en/software)
   - Open Arduino IDE and go to Tools > Board > Boards Manager
   - Search for "Arduino Mbed OS Nano Boards" and install it

2. **Install Required Libraries**
   - Open Arduino IDE
   - Go to Tools > Manage Libraries
   - Search and install the following libraries:
     - Arduino_MKRMEM
     - Arduino_LSM9DS1
     - PDM

3. **Setup Edge Impulse**
   - Install Edge Impulse CLI:
     ```bash
     npm install -g edge-impulse-cli
     ```
   - Login to Edge Impulse:
     ```bash
     edge-impulse-daemon
     ```

4. **Upload the Code**
   - Clone this repository:
     ```bash
     git clone https://github.com/dtdat0194/Wake-Word-Detection-System-for-IoT-Devices.git
     ```
   - Open the project in Arduino IDE
   - Select the correct board:
     - Tools > Board > Arduino Mbed OS Nano Boards > Arduino Nano 33 BLE Sense
   - Select the correct port
   - Click Upload

## Usage

1. **Power On**
   - Connect the Arduino Nano 33 BLE Sense to your computer using a USB Type-C cable
   - The board will automatically start listening for the wake word

2. **Testing the Wake Word**
   - Speak the wake word clearly into the microphone
   - The built-in LED will light up when the wake word is detected
   - The detection results will be printed to the Serial Monitor

3. **Monitoring Output**
   - Open Serial Monitor in Arduino IDE (Tools > Serial Monitor)
   - Set baud rate to 115200
   - You will see detection results and confidence scores

## Project Structure

```
Wake_Word_Detection_inferencing/
├── src/
│   ├── edge-impulse-sdk/    # Edge Impulse SDK files
│   ├── model-parameters/    # Model configuration
│   └── tflite-model/       # TFLite model files
├── README.md
└── Wake_Word_Detection_inferencing.ino
```

## Troubleshooting

1. **Board Not Detected**
   - Ensure proper USB connection
   - Try a different USB cable
   - Check if the board is properly powered

2. **Upload Failures**
   - Make sure the correct board is selected
   - Check if the correct port is selected
   - Try pressing the reset button on the board before uploading

3. **Poor Detection Accuracy**
   - Ensure quiet environment
   - Speak clearly and at appropriate volume
   - Check microphone connections

## Contributing

Feel free to submit issues and enhancement requests!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Edge Impulse for the development platform
- TensorFlow Lite Micro for the inference engine
- Arduino team for the hardware platform