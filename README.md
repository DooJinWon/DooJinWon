# Jinwon Doo

### Electrical Engineering · Embedded Systems · Sensor Interfaces

Fourth-year Electrical Engineering undergraduate, currently studying at the University of Illinois Urbana-Champaign as an exchange student. I’m interested in firmware, sensor systems, and tools that connect hardware to software.

## Selected projects

### 01 · ESP8266 Sensor Data Logger

**C++ / Arduino · I²C · Wi-Fi / HTTP · Python / Flask**

An embedded temperature-logging prototype connecting an MLX90614 infrared sensor to a server. Firmware reads ambient and object temperatures, sends JSON over HTTP, provides a short local debugging window, and enters timed deep sleep.

```text
MLX90614 → I²C → ESP8266 → Wi-Fi / HTTP → Flask → CSV
                     └── 60-second deep sleep cycle
```

[View project](https://github.com/DooJinWon/ESP8266_Low_Power_Sensor_Data_Logger) · [Read firmware](https://github.com/DooJinWon/ESP8266_Low_Power_Sensor_Data_Logger/blob/main/2nd%20day_Temp%20device%20with%20IR/IRdevice_uploaded_on_esp8266.ino) · [See server](https://github.com/DooJinWon/ESP8266_Low_Power_Sensor_Data_Logger/blob/main/2nd%20day_Temp%20device%20with%20IR/server.py)

### 02 · PPG Blood Pressure Estimation / TinyML Preparation

**Python · PyTorch · 1D CNN · ONNX · C model data**

A signal-processing and model-development project exploring blood pressure estimation from PPG. Published code includes preprocessing, CNN training, ONNX export, and conversion of model bytes into a C header for embedded integration.

```text
PPG / ABP data → Preprocessing → CNN training → ONNX export
TFLite model bytes → C header → Embedded integration
```

The public repository documents the model-development workflow; MCU firmware and reproducible hardware benchmarks are not included in the published source.

[View project and report](https://github.com/DooJinWon/TinyML-Based-Low-Energy-Device-for-Blood-Pressure-Estimation-Using-PPG-Signal-Analysis) · [Browse code](https://github.com/DooJinWon/TinyML-Based-Low-Energy-Device-for-Blood-Pressure-Estimation-Using-PPG-Signal-Analysis/tree/main/code)

### 03 · KiCad MCP Server

**Python · MCP · KiCad · PCB workflow automation**

A tooling project exposing schematic and PCB operations through an MCP server. Source modules cover schematic editing, board placement, routing integration, and KiCad CLI operations for design checks and manufacturing outputs.

[View project](https://github.com/DooJinWon/kicad-mcp-server) · [Read tool documentation](https://github.com/DooJinWon/kicad-mcp-server/tree/main/kicad-mcp) · [Browse implementation](https://github.com/DooJinWon/kicad-mcp-server/tree/main/kicad-mcp/tools)

## Additional work

- [MATLAB PPG experiments](https://github.com/DooJinWon/Matlab_PPG): signal preprocessing and LSTM / GRU modeling experiments.

## Technical focus

| Area | Technologies represented in my projects |
| :--- | :--- |
| Embedded firmware | C++, Arduino, ESP8266, I²C, sensor acquisition, deep sleep |
| Device-to-server integration | Wi-Fi, HTTP / JSON, Python, Flask, CSV logging |
| Signal processing and ML | MATLAB, Python, PyTorch, PPG preprocessing, CNN, LSTM / GRU |
| Engineering tools | KiCad, Python automation, MCP, ONNX, model-to-C conversion |

## Contact

**Jinwon Doo** · [jinwond2@illinois.edu](mailto:jinwond2@illinois.edu)
