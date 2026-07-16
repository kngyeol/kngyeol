# 김동열 (Dongyeol Kim)

ROS2와 C++ 기반 자율주행 및 로보틱스 시스템에서 센서와 인지부터 CAN과 액추에이터까지 연결하고, HILS/SILS와 실측 디버깅으로 문제를 검증하는 엔지니어입니다.

`Robotics | Autonomous Driving | Embedded Systems | Verification`

[![Portfolio](https://img.shields.io/badge/Portfolio-View-0A66C2?style=flat-square)](https://kngyeol-portfolio.vercel.app)
[![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)](https://isocpp.org/)
[![ROS2](https://img.shields.io/badge/ROS2-Humble-22314E?style=flat-square&logo=ros)](https://docs.ros.org/en/humble/)
[![Nav2](https://img.shields.io/badge/Nav2-Navigation-22314E?style=flat-square)](https://navigation.ros.org/)
[![SocketCAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)](https://docs.kernel.org/networking/can.html)
[![HILS](https://img.shields.io/badge/Verification-HILS-4A4A4A?style=flat-square)](#experience)

## Profile

- **학력:** 건국대학교 전기전자공학부 학사
- **관심 분야:** 로봇 주행 런타임, 자율주행 SW, 임베디드/차량 인터페이스
- **포트폴리오:** [kngyeol-portfolio.vercel.app](https://kngyeol-portfolio.vercel.app)

## Experience

### Skyautonet | 자율주행SW개발부 인턴

`2024.09 - 2024.12` · `ROS2 Humble` · `Autoware Universe` · `C++` · `SocketCAN` · `Lanelet2`

Autoware 기반 FODRo와 Level 4+ 자율주행 플랫폼에서 Planning, CAN/HILS, HMI 연동을 개발하고 검증했습니다.

- Lanelet2 기반 target lanelet 탐색, 거리 제한 경로, 잔여거리 reroute와 외부 차선변경 흐름을 구현했습니다.
- ROS2 제어 및 위치 토픽과 차량 CAN frame 사이의 변환, vcan 기반 actuator/state HILS를 구성했습니다.
- FOD 접근 시 heading 반대 정렬 문제와 지도 데이터 QoS 불일치를 원인별로 수정하고 HILS에서 동작을 확인했습니다.
- 차선변경 후 이전 차선을 따르던 문제를 상태 구독, 방향별 서비스, flag 초기화와 route reset 순서로 해결했습니다.

## Education & Training

### SSAFY 14기 | 임베디드 특화트랙

`2025.07 - 2026.06` · `1,628시간` · `수료`

삼성청년SW·AI아카데미에서 C/C++, MCU, RTOS, ROS2 기반 임베디드 및 모빌리티 SW 교육을 이수했습니다.

- Balemale, Divery, SCV 팀 프로젝트를 수행했습니다.
- ROS2 시스템 통합, AI 파이프라인, Docker/Jenkins 기반 배포 환경을 프로젝트에서 경험했습니다.

## Selected Projects

### SCV | Smart Companion Vehicle

`2026.03 - 2026.06` · `ROS2 Humble` · `Nav2` · `Python` · `RealSense` · `BNO085`

- 자연어 명령을 ROS2/Nav2 주행, 비전 정렬, 로봇팔 조작으로 연결하고 주행 명령 중재 계층과 LLM drive bridge를 통합했습니다.
- 실제 주행 기록을 반영한 real2sim과 rosbag 기반 SILS로 메카넘 주행을 튜닝했습니다.
- 저장소 비공개 · [Portfolio](https://kngyeol-portfolio.vercel.app)

### TeamKAI | 자율주행 자작차

`2023.11 - 2024.11` · `ROS` · `C++` · `PCL` · `OpenCV` · `SocketCAN`

- 인지 파트장으로 LiDAR pointcloud 전처리, 좌우 콘 분류, 경로 생성과 차량 제어 인터페이스가 연결되는 자율주행 파이프라인을 다뤘습니다.
- 1랩에서 트랙맵을 작성하고 2랩에서 맵 기반으로 주행하는 전략을 수립했습니다.
- [Public repository snapshot](https://github.com/kngyeol/TeamKAI)

### Balemale | AI 스마트 자율주차 로봇

`2026.01 - 2026.02` · `ROS2 Humble` · `Jetson Orin Nano` · `ArUco` · `MQTT`

- 팀 프로젝트에서 ROS2 로봇 런타임, AI 인식과 MQTT 서버 사이의 통합 흐름을 다뤘습니다.
- ArUco 기반 주행과 주차 정렬, 18개 상태의 입출고 미션 흐름을 구성했습니다.
- 저장소 비공개 · [Portfolio](https://kngyeol-portfolio.vercel.app)

### Divary | 다이빙 로그북 AI

`2026.02 - 2026.03` · `Python` · `AWS SQS` · `Docker` · `Jenkins`

- 다이빙 영상에서 하이라이트와 어류를 탐지 및 분류해 AI 로그북을 생성하는 팀 프로젝트를 수행했습니다.
- 영상 분석을 SQS 작업과 GPU worker로 분리하고 Redis, S3와 callback으로 상태와 결과를 연결했습니다.
- Docker Compose와 Jenkins로 통합 실행환경과 배포 흐름을 구성했습니다.
- 저장소 비공개 · [Portfolio](https://kngyeol-portfolio.vercel.app)

### Fire & Smoke Detection Drone

`2024.01 - 2024.06` · `YOLOv9` · `Lite-Mono` · `TensorRT` · `Jetson Orin`

- 화재와 연기 탐지에 단안 depth를 결합해 객체 크기와 상대 거리 기반 위험도를 계산했습니다.
- 저장소 README 기준 validation 759장에서 all-class `mAP50 0.867`을 기록했습니다.
- [Public repository](https://github.com/kngyeol/pjt-fire-detect-drone)

## Additional Projects

- **ResNet50 MAC Accelerator** — 건국대학교 SoC Design Lab 공동 프로젝트에서 Zynq-7000 기반 MAC 가속 구조와 AXI-Stream/DMA 연동을 다뤘습니다. [Repository](https://github.com/kngyeol/resnet50-mac-accelerator)
- **TeamPathfinders** — ROS 자율주행 교육 프로젝트에서 Bezier 주차 경로, Pure Pursuit 추적, 카메라 신호 인식과 IMU 기반 주행 과제를 수행했습니다. [Repository](https://github.com/kngyeol/TeamPathfinders)
- **ATmega128 Coursework** — AVR Assembly로 UART, timer interrupt, ADC, TWI와 7-segment 제어 코드를 작성했습니다. [Repository](https://github.com/kngyeol/pjt_microprocessor)

## Skills

- **Robotics / Autonomous Driving:** ROS2 Humble, Nav2, Autoware Universe, Lanelet2, PCL, OpenCV
- **Embedded / Vehicle:** C/C++, Linux, SocketCAN/vcan, CAN integration, ESP32, Raspberry Pi, HILS/SILS
- **AI / Deployment:** Python, YOLO, TensorRT, Docker, Jenkins, AWS SQS, MQTT
- **FPGA / Acceleration:** Verilog, Vivado, AXI-Stream, AXI DMA

## Award

- **창의설계경진대회 장려상** — 건국대학교 공학교육혁신센터, 2024.09.27
  - 차량의 주변상황과 차량상태 인지시스템
