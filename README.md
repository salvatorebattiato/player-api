# Player-Api endpoints description for linux media player.

## Description
This project aims to create a JS UI-UX for a linux music media player running MPD in the backend. <br>
The simple commands user can choose in this minimal UI should be sent over a local HTTP request listener located in the backend under a Flask framework in Python. All the requests return value are sent over JSON format. <br>

## Requirements
The framework where this webapp will run will be a full-screen one-tab web browser and displayed over two HDMI outputs at the same time: a TV and a 5" TFT display on the front of the device which will be always on. Both will be 16:9 landscape monitors.<br>
Inputs are taken from a remote that will behave like a legacy keyboard so all the hover effects and control commands of the webapp should be done taking in account the fact that there won't be any mouse input but just a keyboard input sending ">", "p", spacebar and so on.<br>
