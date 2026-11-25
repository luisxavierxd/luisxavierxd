<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,100:F5A623&height=140&section=header&text=Luis%20Xavier&fontSize=42&fontColor=FFFFFF&fontAlignY=38" alt="Luis Xavier" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=3200&pause=900&color=F5A623&center=true&vCenter=true&width=640&lines=turning+sensors+into+decisions;making+a+car+drive+itself;sensorless+FOC+at+10+kHz;ROS+2+%C2%B7+digital+twins+%C2%B7+edge+AI" alt="turning sensors into decisions" />
</p>

<p align="center">
  Robotics Engineering @ Tec de Monterrey, Campus Guadalajara<br/>
  Lead of motor control and the Autonomous Driving Challenge at <b>ELYOS Racing</b> (Shell Eco-marathon)
</p>

<p align="center">
  <a href="https://luisxavierxd.github.io/Portfolio/"><img src="https://img.shields.io/badge/Portfolio-live-F5A623?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio"/></a>
  <a href="https://elyos-racing.github.io/team-portfolio/members/luisxavierxd.html"><img src="https://img.shields.io/badge/ELYOS-team%20page-0D1117?style=for-the-badge&logo=githubpages&logoColor=F5A623" alt="ELYOS team page"/></a>
  <a href="https://github.com/ELYOS-Racing"><img src="https://img.shields.io/badge/GitHub-ELYOS--Racing-181717?style=for-the-badge&logo=github&logoColor=white" alt="ELYOS-Racing org"/></a>
  <a href="https://www.linkedin.com/in/luisxaviergpa/"><img src="https://img.shields.io/badge/LinkedIn-connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://calendly.com/luisxaviergpa-proton"><img src="https://img.shields.io/badge/Book%20a%20call-Calendly-006BFF?style=for-the-badge&logo=calendly&logoColor=white" alt="Calendly"/></a>
</p>

---

## 🏁 Now building · ELYOS Racing 2027

<table>
<tr>
<td width="50%" valign="top">

### 🤖 Autonomous Driving Challenge

Shell Eco-marathon ADC · Silesia Ring, Poland · June 2027

A three-wheeled efficiency car that has to drive a lap on its own: dodge cones, stop at the line and finish on as little energy as possible. Everything runs **on board** a Jetson Orin; telemetry flows one way, car → cloud → twin.

- ROS 2 Jazzy stack: EKF localization, LiDAR tracking, Frenet planning with quintics, pure pursuit, safety supervisor
- Software-in-the-loop in **Gazebo Harmonic**, plus a **digital twin** on a second Orin
- OpenUSD track scene built in CI and driven live in **NVIDIA Isaac Sim**
- Energy-optimal speed profiles: CasADi optimal control and pymoo genetic algorithms
- Cloud: Mosquitto, TimescaleDB, Foxglove/MCAP dashboards

**Status:** full pipeline running in SIL and on both Orins; car hardware tests next

</td>
<td width="50%" valign="top">

### ⚡ FOC motor driver

Teensy 4.1 (Cortex-M7 @ 600 MHz) · 48 V BLDC hub motor

Field-oriented control in a 10 kHz hardware ISR, with FreeRTOS handling throttle, telemetry and SD logging so nothing slow can delay the loop.

| Control loop | Before | Now |
|---|---:|---:|
| Compute time | 68 µs | **5.4 µs** |
| Jitter | 27 µs | **0.6 µs** |

<sub>PWM-synchronized current sampling, measured on the bench.</sub>

- **Sensorless FOC (in progress):** Luenberger + PLL angle observer, sliding-mode as fallback
- State machine: start on Halls, shadow the observer, then hand over, with a rollback path to Hall-only firmware
- 2027 motor sized from the Indianapolis energy and loss budget

</td>
</tr>
</table>

<p align="center">
  <sub>🏗️ I also run the team's GitHub org: 13 repos with CI, a versioned protocol shared by every board, per-competition release manifests and PMBOK 8 project management.<br/>
  The code is private to the team; the results are public on the <a href="https://elyos-racing.github.io/team-portfolio/">team portfolio</a>.</sub>
</p>

---

## 🔧 More projects

| Project | What it is | Stack |
|---|---|---|
| [**TelemetryStack**](https://github.com/luisxavierxd/TelemetryStack) | Reusable telemetry base I built from scratch, used by 2 SAE teams so far (MadRams Baja, Quantum Speed Racing) | ESP32 · FreeRTOS · LoRa 915 MHz · MQTT · InfluxDB · Grafana |
| **MadRams Baja car** | Vehicle comms and telemetry. The team placed 4th in Endurance at Baja SAE Oregon | ESP32 · MQTT/Mosquitto · LTE/WiFi · u-blox GPS · SX1262 |
| [**OmniSim Nav2**](https://github.com/omnilink-tech/omnisim/releases/tag/v8.1.17) | Packaged Nav2 stack for Husky diff-drive. PR #12 merged and headlined in release v8.1.17 | ROS 2 · Nav2 · MuJoCo · CycloneDDS |
| [**JTCS**](https://github.com/luisxavierxd/JTCS) · [demo](https://luisxavierxd.github.io/JTCS/) | Edge-AI adaptive traffic signals. Guadalahacks 2026 | YOLOv11 · Python CV · React · Node WS · RPi |
| [**Banky**](https://github.com/luisxavierxd/HackMTY-2026_Banorte) · [demo](https://www.banky.mx) | Finalist, Banorte challenge at HackMTY 2026. Agent-built financial UI; I built the whole backend and harness | LLM · MCP · A2UI · Anthropic / Gemini |
| [**NeuroBeat**](https://github.com/luisxavierxd/NeuroBeat) | EEG signal-processing project | EEG · Python |
| [**Campus Map**](https://github.com/luisxavierxd/MapaInteractivoTEC_GDL) · [demo](https://luisxavierxd.github.io/MapaInteractivoTEC_GDL) | Pedestrian routing map for Tec GDL | GeoJSON · JS |
| [**MadRams Course Library**](https://github.com/luisxavierxd/MadRamsBibliotecaCursos) · [demo](https://luisxavierxd.github.io/MadRamsBibliotecaCursos) | Telemetry and CAD onboarding courses for the Baja team, with sessions mapped to the real car's subsystems | Web · SolidWorks · Three.js |

<details>
<summary><b>🧠 AI orchestration and Claude Code skills</b></summary>

- [**LaTeX Studio**](https://github.com/luisxavierxd/LaTeX-Studio): local IDE that turns PDFs into APA-7 LaTeX. I built the pipeline (FastAPI, PyMuPDF extraction, Monaco, pdflatex); an LLM generates the `.tex`
- **claude-unlimited**: multi-agent orchestrator with per-role fallback over a self-hosted LLM gateway
- [**websight**](https://github.com/luisxavierxd/websight): headless-browser visual QA skill
- [**exploded-view**](https://github.com/luisxavierxd/exploded-view): web-native 3D presentation skill (model-viewer, Three.js, glTF/Draco)
- [**watermarks-remover**](https://github.com/luisxavierxd/watermarks-remover): Claude Code plugin integration for [guillaumemeyer/watermarks-remover](https://github.com/guillaumemeyer/watermarks-remover). The engine is upstream's work

</details>

<details>
<summary><b>🦾 Earlier robotics (high school)</b></summary>

- [**Robot Interprepas**](https://github.com/luisxavierxd/articubot_one): ROS 2 Humble diff-drive robot with Nav2, LiDAR and Arduino
- **AgroBot** · [site](https://agrobot.devops.torroca.com/): raspberry-harvesting prototype with a 6-DOF arm, YOLOv8n and inverse kinematics

</details>

---

## 🛠️ Toolbox

<p align="center">
  <img src="https://img.shields.io/badge/ROS_2-22314E?style=flat-square&logo=ros&logoColor=white" alt="ROS 2"/>
  <img src="https://img.shields.io/badge/Gazebo-F58113?style=flat-square&logo=ros&logoColor=white" alt="Gazebo"/>
  <img src="https://img.shields.io/badge/Isaac_Sim-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="Isaac Sim"/>
  <img src="https://img.shields.io/badge/Jetson_Orin-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="Jetson Orin"/>
  <img src="https://img.shields.io/badge/Teensy_4.1-2E7D32?style=flat-square&logo=arduino&logoColor=white" alt="Teensy 4.1"/>
  <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"/>
  <img src="https://img.shields.io/badge/FreeRTOS-5DB34A?style=flat-square" alt="FreeRTOS"/>
  <img src="https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white" alt="Raspberry Pi"/>
  <br/>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/JS%2FTS-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="JS/TS"/>
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
  <br/>
  <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="MQTT"/>
  <img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white" alt="InfluxDB"/>
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/KiCad-314CB0?style=flat-square&logo=kicad&logoColor=white" alt="KiCad"/>
  <img src="https://img.shields.io/badge/SolidWorks-E2231A?style=flat-square&logo=dassaultsystemes&logoColor=white" alt="SolidWorks"/>
  <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white" alt="Three.js"/>
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white" alt="MATLAB"/>
</p>

<p align="center"><sub><b>Also:</b> FOC/BLDC and sensorless observers (PLL, SMO) · CAN/TWAI · LoRa/SX1262 · GPS NMEA · OpenUSD · CasADi · pymoo · LVGL · BLE reverse-engineering (bleak) · YOLO · local LLMs · MCP</sub></p>

---

## 📊 Where I actually go deep

| Language | Depth | Used for |
|---|---|---|
| **C++** | Core | Embedded control and firmware: FOC/BLDC, FreeRTOS on Teensy and ESP32, sensor drivers |
| **Python** | Strong | ROS 2 nodes, optimal control and simulation, computer vision, data pipelines, FastAPI backends |
| **TypeScript / JS** | Practical, AI-assisted | Web demos, dashboards and course sites that present the engineering |

<sub>GitHub's language stats count lines, so the web demos outweigh the firmware. This table is the honest version.</sub>

<p align="center"><sub>I like controlling tools below their intended abstraction: BLE protocols, file formats, CLIs as engines.</sub></p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:F5A623,100:0D1117&height=90&section=footer" width="100%" alt=""/>
</p>
