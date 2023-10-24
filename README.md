# ESP8266 RFID Access Control System

This project implements an RFID access control system using an ESP8266 and an MFRC522 RFID module. The system is designed to grant access to authorized users based on RFID card authentication. When an authorized RFID card is detected, the system opens a boom gate to allow access.

## Hardware Requirements

- ESP8266 microcontroller.
- MFRC522 RFID module.
- Servo motor.
- RFID cards or key fobs

## Setup

### Hardware Setup

1. Connect the MFRC522 RFID module to the ESP8266 controller. Ensure that the connections are correctly established.

2. Connect the servo motor to the ESP8266, ensuring that it is wired for boom gate operation.

### Software Setup

1. Upload the project code to the ESP8266 controller using the Arduino IDE or your preferred development environment.

2. After uploading the code, open the Arduino IDE Serial Monitor.

## Usage

The system runs in an RFID access mode, continuously monitoring for authorized RFID cards. When an authorized card is detected, the boom gate opens for a predetermined duration (5 seconds) before closing. Unauthorized cards do not trigger the gate to open.

- The `rfidAccessMode` function continuously monitors for authorized RFID cards.
- When an authorized RFID card (e.g., `VISITOR_TAG_1`) is detected, the system opens the boom gate using the `openMode` function.
- The gate remains open for 5 seconds.
- After 5 seconds, the system closes the boom gate using the `closeMode` function.
- The system continues to monitor for new RFID card scans.

## Customization

You can customize this project by modifying the list of authorized RFID card IDs (`VISITOR_TAG_1`, etc.) in the code to match your requirements. 

## Troubleshooting

If the system is not functioning as expected, ensure the following:

- Verify that the RFID module and servo motor are correctly connected to the ESP8266.
- Ensure you have the necessary libraries installed for the MFRC522 module.
- Check the wiring configuration to ensure it matches the code.
