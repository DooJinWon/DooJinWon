# Jinwon Doo

### Electrical Engineering · FPGA / RTL · Embedded Systems · Sensor Interfaces

Fourth-year Electrical Engineering undergraduate, currently studying at the University of Illinois Urbana-Champaign as an exchange student. I’m interested in firmware, sensor systems, and tools that connect hardware to software. I’m also interested in FPGA-based high-frequency trading (HFT), particularly low-latency market-data processing, reliable streaming architectures, and hardware design and verification.

## Current FPGA projects

**SystemVerilog · Vivado · RTL design · Testbenches**

### ILLIT · FPGA Streaming Market-Data Receiver

*Ingress Low-Latency Information Transport*

An FPGA ingress frontend for receiving and normalizing high-rate market-data streams. The design includes FIFO buffering, flow control, and overflow handling, with a testbench for synthetic market-data inputs.

**Status:** RTL design and testbench implementation completed; preparing for physical FPGA board bring-up.

### RESCENE · FPGA Market-Data Consistency and Recovery Engine

*Reliable Exchange Stream Consistency and Network-recovery Engine*

An FPGA engine for parsing CME-inspired market-data payloads, arbitrating redundant A/B feeds, removing duplicates, and detecting sequence gaps. Snapshot-based recovery, buffered incremental-event replay, and atomic order-book switching are designed to preserve Top-N order-book consistency after packet loss.

**Status:** RTL design and testbench implementation completed; preparing for physical FPGA board bring-up.

```text
ILLIT: stream reception → buffering / flow control → normalized events
                                                        ↓
RESCENE: A/B arbitration → sequence checking → order-book updates / recovery
```

The projects can be demonstrated independently; ILLIT can later serve as an input frontend for RESCENE. RESCENE uses a simplified CME-inspired payload format. Actual exchange connectivity and full production CME MDP 3.0 support are outside the current scope.

## Selected projects

### 01 · ESP8266 Sensor Data Logger

**C++ / Arduino · I²C · Wi-Fi / HTTP · Python / Flask**

An embedded temperature-logging prototype connecting an MLX90614 infrared sensor to a server. Firmware reads ambient and object temperatures, sends JSON over HTTP, provides a short local debugging window, and enters timed deep sleep.

```text
MLX90614 → I²C → ESP8266 → Wi-Fi / HTTP → Flask → CSV
                     └── 60-second deep sleep cycle
```

[View project](https://github.com/DooJinWon/ESP8266_Low_Power_Sensor_Data_Logger) · [Read firmware](https://github.com/DooJinWon/ESP8266_Low_Power_Sensor_Data_Logger/blob/main/day-02-ir-temperature-logger/IRdevice_uploaded_on_esp8266.ino) · [See server](https://github.com/DooJinWon/ESP8266_Low_Power_Sensor_Data_Logger/blob/main/day-02-ir-temperature-logger/server.py)

### 02 · On-Device PPG Blood Pressure Estimation

**nRF52840 · MAX30102 · Zephyr · Edge Impulse · 1D CNN**

POSTECH capstone team project. I implemented the sensing and inference pipeline, from PPG acquisition and preprocessing to MCU deployment and subject-specific calibration. The final report records MAE of **8.15 → 2.67 mmHg** across three raw/calibrated comparison rows and a **9.56-second** average inference time over ten repetitions. This is a small research-prototype evaluation; power values are estimates.

[View implementation and results](https://github.com/DooJinWon/TinyML-Based-Low-Energy-Device-for-Blood-Pressure-Estimation-Using-PPG-Signal-Analysis) · [Browse scripts](https://github.com/DooJinWon/TinyML-Based-Low-Energy-Device-for-Blood-Pressure-Estimation-Using-PPG-Signal-Analysis/tree/main/src)

### 03 · KiCad MCP Server

**Python · MCP · KiCad · PCB workflow automation**

A tooling project exposing schematic and PCB operations through an MCP server. Source modules cover schematic editing, board placement, routing integration, and KiCad CLI operations for design checks and manufacturing outputs.

[View project](https://github.com/DooJinWon/kicad-mcp-server) · [Read tool documentation](https://github.com/DooJinWon/kicad-mcp-server/blob/main/docs/setup.md) · [Browse implementation](https://github.com/DooJinWon/kicad-mcp-server/tree/main/tools)

## Additional work

- [MATLAB PPG experiments](https://github.com/DooJinWon/Matlab_PPG): signal preprocessing and LSTM / GRU modeling experiments.

## Technical focus

| Area | Technologies represented in my projects |
| :--- | :--- |
| FPGA / digital design | SystemVerilog, Vivado, streaming RTL, FIFOs, testbenches, market-data recovery |\n| Embedded firmware | C++, Arduino, ESP8266, I²C, sensor acquisition, deep sleep |
| Device-to-server integration | Wi-Fi, HTTP / JSON, Python, Flask, CSV logging |
| Signal processing and ML | MATLAB, Python, PyTorch, PPG preprocessing, CNN, LSTM / GRU |
| Engineering tools | KiCad, Python automation, MCP, ONNX, model-to-C conversion |

## Contact

**Jinwon Doo** · [jinwond2@illinois.edu](mailto:jinwond2@illinois.edu)
