# 김동열 (Dongyeol Kim)

ROS2/Nav2 기반 실물 로봇 런타임과 임베디드/차량 SW 인터페이스를 연결하는 엔지니어입니다.

`ROS2 Robotics | Autonomous Driving | Embedded Systems | CAN Communication | HILS Verification`

[![GitHub](https://img.shields.io/badge/GitHub-kngyeol-181717?style=flat-square&logo=github)](https://github.com/kngyeol)
[![ROS2](https://img.shields.io/badge/ROS2-Humble-22314E?style=flat-square&logo=ros)](https://www.ros.org/)
[![Nav2](https://img.shields.io/badge/Nav2-Navigation-1F6FEB?style=flat-square)](https://navigation.ros.org/)
[![Autoware](https://img.shields.io/badge/Autoware-Autonomous%20Driving-00A3E0?style=flat-square)](https://autoware.org/)
[![SocketCAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)](https://www.kernel.org/doc/Documentation/networking/can.txt)
[![FreeRTOS](https://img.shields.io/badge/RTOS-FreeRTOS-87C540?style=flat-square)](https://www.freertos.org/)

## About

- 건국대학교 전기전자공학부 학사
- SSAFY 14기 임베디드 특화트랙
- Skyautonet 자율주행SW개발부 인턴
- 관심 분야: 로보틱스 런타임, 자율주행 SW, 임베디드/차량 인터페이스, HILS 검증
- Portfolio: [v0-portfolio-indol-chi-29.vercel.app](https://v0-portfolio-indol-chi-29.vercel.app/)

## What I Build

- LLM/앱 명령을 ROS2 action, service, topic 기반 로봇 동작으로 연결하는 런타임
- Nav2, localization, map calibration, IMU/encoder odometry를 활용한 실물 로봇 주행 흐름
- CAN, UART, STM32, Jetson 장치와 상위 autonomy stack 사이의 검증 가능한 인터페이스
- 실제 하드웨어에서 timeout, cancel, sensor stale, fail-safe stop 같은 실패 모드를 다루는 제어 로직

## Experience

### Skyautonet 자율주행SW개발부 인턴, 2024.09 - 2024.12

**Lv4 autonomous driving platform**

- Autoware Universe 기반 자율주행 트럭 플랫폼 개발에 참여했습니다.
- Lanelet2 맵 기반 경로 생성, external lane change, HMI 제어 버튼, operation mode 기반 제어 분기를 구현했습니다.
- ROS2 상태를 CAN 메시지로 변환하는 HILS actuator 흐름을 다뤘습니다.

**FODRo debris removal robot**

- ROS2 topic을 CAN protocol로 변환하는 converter와 vcan 기반 HILS 검증 환경을 구성했습니다.
- Multi-FOD clustering, lane validity check, cleaning state, debug client 등 로봇 작업 흐름을 보강했습니다.

## Selected Projects

### SCV-drive - LLM 명령 기반 ROS2 서비스 로봇 런타임

실내 서비스 로봇이 자연어/앱 명령을 받아 실제 주행과 조작 행동으로 이어지도록 만든 로봇 런타임 프로젝트입니다.

- LLM drive packet을 `relative_move`, `precision_align`, `navigate_to_pose`, stop/cancel/return 흐름으로 변환했습니다.
- Nav2 adapter, motion coordinator, drive bridge, field map, task pose, 실행 스크립트를 연결했습니다.
- 실물 로봇 주행에서 발생하는 sensor readiness, timeout, cancel, map calibration, home return 문제를 다뤘습니다.

`ROS2 Humble` `Nav2` `robot_localization` `Python` `STM32/CAN` `Jetson` `LLM Bridge`

### TeamKAI - 자율주행 자작차

자율주행 경진대회 차량 프로젝트에서 인지 파트장으로 참여했습니다.

- LiDAR 기반 cone detection, camera/YOLO detection, traffic light recognition을 다뤘습니다.
- Bezier path, Stanley/Pure Pursuit control, CAN bridge와 연결되는 perception-planning-control 흐름을 경험했습니다.

[Repository](https://github.com/kngyeol/TeamKAI)

`ROS` `C++` `Python` `PCL` `OpenCV` `YOLOv5/v8` `LiDAR`

### Balemale - AI 스마트 자율주차 로봇

번호판 인식, 키오스크, 백엔드, 로봇 주행이 연결되는 스마트 주차 서비스 로봇 프로젝트입니다.

- ROS2 Humble, Jetson Orin Nano, mecanum base, ArUco marker, MQTT 기반 로봇 흐름을 구성했습니다.
- 18-state mission FSM과 backend/kiosk 상태 동기화를 통해 서비스형 로봇 제품 구조를 경험했습니다.

`ROS2 Humble` `Jetson Orin Nano` `Python` `OpenCV` `ArUco` `MQTT` `Spring Boot`

### ResNet50 MAC Accelerator

Zynq-7000 PS/PL 환경에서 Conv 연산 병목을 가속하는 FPGA/SoC 프로젝트입니다.

- Q10.22 fixed-point MAC datapath, AXI DMA, AXI4-Lite 제어, SW/HW benchmark 흐름을 구현했습니다.
- 1x1 output-stationary 구조와 NxN streaming 구조를 나눠 convolution 특성에 맞춘 data movement를 설계했습니다.

[Repository](https://github.com/kngyeol/resnet50-mac-accelerator)

`Verilog` `Vivado` `Xilinx Zynq-7000` `AXI DMA` `C`

### Fire & Smoke Detection Drone

드론 탑재 화재/연기 탐지와 단안 거리 추정을 결합한 Edge AI 프로젝트입니다.

- YOLOv9-c detection과 Lite-Mono depth를 결합해 거리 기반 위험도를 산출했습니다.
- Structured pruning, TensorRT 최적화, Gradio UI를 통해 모델을 실제 사용 흐름에 가깝게 구성했습니다.

[Repository](https://github.com/kngyeol/pjt-fire-detect-drone)

`YOLOv9` `Lite-Mono` `TensorRT` `Python` `Gradio`

### CAN MultiECU HILS

STM32 기반 Sensor ECU / Control ECU 분리 구조와 Python HILS 시나리오 주입 환경을 만드는 개인 프로젝트입니다.

- CAN 이중화, fail-over, FreeRTOS task structure, scenario logging/replay 흐름을 구성하고 있습니다.

`STM32` `FreeRTOS` `CAN` `Python` `HILS`

## Tech Stack

**Robotics / Autonomous Driving**

`ROS2` `Nav2` `Autoware` `robot_localization` `Lanelet2` `OpenCV` `PCL`

**Embedded / Vehicle Interface**

`C` `C++` `Python` `STM32` `CAN` `SocketCAN` `UART` `I2C` `SPI` `FreeRTOS`

**AI / Edge**

`PyTorch` `YOLOv8/v9` `TensorRT` `ONNX` `Jetson` `OpenCV`

**Hardware / Acceleration**

`Verilog` `Vivado` `Xilinx Zynq` `AXI DMA` `Fixed-point arithmetic`

**Product / Tools**

`Linux` `Docker` `MQTT` `Qt5` `Spring Boot` `Vue` `TypeScript`

## Open Source

오픈소스 기여를 시작하기 위해 작은 단위의 재현 가능한 PR부터 준비하고 있습니다.

- 관심 영역: ROS2/Nav2 문서와 테스트, Autoware 주변 tooling, SocketCAN/vehicle interface 예제, robotics Python utilities
- 기여 방식: bug reproduction, documentation fix, test case 추가, 작은 refactor, example 개선
- 목표: 공개 프로젝트에서 읽기 쉬운 issue report와 review-friendly PR을 꾸준히 쌓기

## Award

- 건국대 공학교육혁신센터 장려상, 2024.09.27
  - 차량의 주변상황과 차량상태 인지시스템
