# iot-sensor-project

This project was borne out of a need to monitor the humidity levels within my crawl space, and a realization that I could very easily learn about IoT while gaining insight about the threat growing (or not growing) under my floorboards.

This project seeks to provide a heatmap / sensor array of the temperature and humidity levels in my crawl space & attic, blended with data taken from the living space via Ecobee APIs.

## Tech Stack -- Field Testing
- Prototype boards
-- Evaluation using Heltec Wireless Stick Lite & Espressif ESP32-POE board
-- DHT11 & 3-in-1 CJMCU-8128 (CCS811, SU7021, BMP280)
- ESPHome for firmware, sensor reading, OTA updates and sending back-to-base
- Home Assistant to collect and display data.
-- Displaying temp/humidity history graphs
- Raspberry Pi for hosting Home Assistant (docker)

## Tech Stack -- Prototype
- Espressif ESP32-POE boards, because:
-- No batteries to mess with.  If power is out, I have bigger problems.
-- Once a sensor is installed, no need to crawl on hands and feet to go change the battery for long periods of time (>1-3yr)
- CJMCU-8128 all-in-one sensor pack
-- More reliable than DHT11's, less calibration required

TBD on visualization requirements.
There is a desire to eliminate the RPi and leverage a SPA hosted via S3 & Serverless & IoT from AWS.
