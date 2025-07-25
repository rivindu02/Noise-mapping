# Smart Noise Mapping System 🔊

A real-time noise monitoring system using ESP32 sensors, Python backend, and React web interface. The system collects environmental noise data from multiple sensors and displays it on an interactive map with real-time interpolation.

## 🆕 What's New (Python Migration)

✅ **Complete Python Backend** - Replaced Node.js with robust Python services  
✅ **WebSocket Integration** - Fast, reliable real-time communication  
✅ **Auto-System Management** - Single-command startup with monitoring  
✅ **Enhanced Documentation** - Comprehensive guides and technical specs  
✅ **Cleaner Codebase** - Removed legacy files and dependencies  
✅ **Standard MQTT Port** - Now using port 1883 (industry standard)  
✅ **UTF-8 Support** - Full emoji and Unicode logging support  

## System Overview

```
ESP32 Sensors → MQTT → Python Backend → WebSocket → React UI
     📡            🔌        🐍            ⚡        ⚛️
   Noise Data    Pub/Sub   Processing   Real-time   Dashboard
```

## Quick Start

### 1. Start the Python Backend
```bash
cd Server
python start_noise_system.py
```

### 2. Start the React UI
```bash
cd mqtt-noise-map-ui
npm start
```

### 3. Access the Application
- **Web Interface:** http://localhost:3000
- **WebSocket Connection:** ws://localhost:9001
- **MQTT Broker:** localhost:1883

### 4. Test with Simulated Sensors
```bash
python fake_esp32.py
```

## Features

✅ **Real-time Monitoring** - Live noise level updates from ESP32 sensors  
✅ **Interactive Maps** - Geographic visualization with sensor locations  
✅ **Noise Interpolation** - IDW algorithm for smooth noise contours  
✅ **WebSocket Integration** - Fast, real-time data streaming  
✅ **Auto-reconnection** - Robust connection handling  
✅ **Cross-platform** - Works on Raspberry Pi, Windows, macOS  
✅ **Easy Deployment** - Single command startup  

## Architecture

### Hardware
- **ESP32 microcontrollers** with noise sensors
- **Raspberry Pi** as central data hub
- **WiFi network** for sensor connectivity

### Software Stack
- **Python Backend** - MQTT client, WebSocket server, data processing
- **React Frontend** - Interactive maps, real-time visualization
- **Mosquitto MQTT** - Message broker for sensor data
- **WebSocket API** - Real-time communication with UI

## Documentation

- **[Python Backend Setup](Server/README.md)** - Complete backend documentation
- **[React UI Guide](mqtt-noise-map-ui/README.md)** - Frontend setup and usage
- **[ESP32 Configuration](ESP32_Noise_Sensor/)** - Sensor programming guide
- **[System Architecture](docs/protocol.md)** - Technical specifications

## Project Structure

```
Noise-mapping/
├── Server/                     # Python backend system
│   ├── mqtt_broker_server.py   # Main WebSocket server
│   ├── simple_noise_processor.py # Data processing
│   ├── start_noise_system.py   # System orchestrator
│   └── requirements.txt        # Python dependencies
├── mqtt-noise-map-ui/          # React web interface
├── ESP32_Noise_Sensor/         # Arduino sensor code
├── fake_esp32.py               # Sensor simulator
└── docs/                       # Technical documentation
```

## System Requirements

- **Python 3.8+** with required packages
- **Node.js 16+** for React development
- **Mosquitto MQTT broker**
- **Modern web browser** with WebSocket support

## SPARK Project

This noise mapping system is part of the SPARK initiative for environmental monitoring and smart city applications.
