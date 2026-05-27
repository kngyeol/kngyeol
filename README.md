# 김동열 (Dongyeol Kim)
ROS2/Nav2 기반 로봇 런타임과 임베디드/차량 인터페이스를 연결하는 엔지니어입니다.

`ROS2 Robotics | Autonomous Driving | Embedded Systems | CAN Communication | HILS Verification`

[![GitHub](https://img.shields.io/badge/GitHub-kngyeol-181717?style=flat-square&logo=github)](https://github.com/kngyeol)
[![ROS2](https://img.shields.io/badge/ROS2-Humble-22314E?style=flat-square&logo=ros)](https://www.ros.org/)
[![Nav2](https://img.shields.io/badge/Nav2-Navigation-22314E?style=flat-square)](https://navigation.ros.org/)
[![SocketCAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)](https://www.kernel.org/doc/Documentation/networking/can.txt)
[![FreeRTOS](https://img.shields.io/badge/RTOS-FreeRTOS-87C540?style=flat-square)](https://www.freertos.org/)
[![HILS](https://img.shields.io/badge/Verification-HILS-4A4A4A?style=flat-square)](#)

## Profile
- 이름: 김동열 (Dongyeol Kim)
- 학력: 건국대학교 전기전자공학부 학사
- 교육: 삼성청년SW·AI아카데미(SSAFY) 14기 임베디드 특화트랙
- 관심 분야: 로봇 주행 런타임, 자율주행 SW, 임베디드/차량 인터페이스, AI 에이전트
- 포트폴리오: [kngyeol-portfolio.vercel.app](https://kngyeol-portfolio.vercel.app)

## Experience
### Skyautonet 자율주행SW개발부 인턴 (2024.09 ~ 2024.12)

**1) Autoware 기반 자율주행 플랫폼**
- Autoware Universe와 ROS2 Humble 기반 자율주행 시스템 개발 참여
- 기술: ROS2 Humble, Autoware Universe, C++, SocketCAN, Lanelet2, Qt5
- 담당:
  - Planning Manager: Lanelet2 기반 target lanelet 탐색, 경로 생성/재경로 생성, external lane change 흐름 구현
  - CAN Converter: ROS2 control/localization 토픽을 차량 CAN frame으로 변환, yaw 정규화, WGS84 역투영, CAN log 저장
  - HILS Actuator: AutowareState, DrivingStatus, OperationMode 기반 actuator/state CAN 생성과 enable 분기 구현
  - HMI 통합: Start/Stop, Lane Change, Velocity 등 운영자 제어 흐름 보강

**2) FODRo (Foreign Object Debris Removal Robot)**
- 도로/활주로 이물질 탐지 및 제거 로봇 운영 로직 개발 참여
- 기술: ROS2 Humble, C++, Python, SocketCAN/vcan, Lanelet2
- 담당:
  - FOD 객체 pose 생성, current/next lane 유효성 검증, 2m clustering
  - 청소 장비 제어와 cleaning state 발행
  - 다중 FOD 우선순위 정렬 및 debug client 지원

## Projects
| 프로젝트 | 설명/핵심 기여 | 기술 | 링크 |
|---|---|---|---|
| SCV - Smart Companion Vehicle | 자연어 명령을 ROS2/Nav2 주행, 비전 정렬, 로봇팔 조작으로 연결하는 이동형 AI 홈 어시스턴트. RoboCrew/XLeRobot 기반 조작 런타임과 LLM drive bridge를 프로젝트 요구에 맞게 연결하고 precision alignment, 실물 runtime/smoke test, 시연 시나리오를 통합 | ROS2 Humble, Nav2, SLAM/AMCL, robot_localization, Python, RealSense, BNO085 IMU, RoboCrew, XLeRobot | Private |
| CAN MultiECU HILS | STM32 기반 Sensor ECU/Control ECU 분리 구조, CAN 이중화 fail-over, FreeRTOS task 구조, Python HILS 시나리오 주입/로깅/리플레이를 준비 중인 개인 프로젝트 | STM32, FreeRTOS, CAN, Python, HILS | Private/Local |
| Balemale - AI 스마트 자율주차 시스템 | ROS2 Humble 로봇, Jetson Orin Nano, mecanum base, ArUco localization, MQTT bridge, 18-state mission FSM, Spring/Vue/kiosk/backend 연동 구조 경험 | ROS2 Humble, Jetson Orin Nano, Python, OpenCV, ArUco, MQTT, Spring Boot | Private |
| TeamKAI - 자율주행 자작차 | 인지 파트장으로 LiDAR/camera/GPS/IMU 기반 cone detection, path planning, Stanley/Pure Pursuit control, CAN bridge가 연결되는 자율주행 파이프라인 경험 | ROS, C++, Python, PCL, OpenCV, YOLOv5/v8, LiDAR | [Repo](https://github.com/kngyeol/TeamKAI) |
| ResNet50 MAC Accelerator | Zynq-7000 기반 ResNet50 Conv 연산 가속기. Q10.22 fixed-point MAC datapath, AXI DMA, AXI4-Lite 제어, 1x1/NxN convolution data movement 설계 | Verilog, Vivado, Xilinx Zynq-7000, AXI DMA, C | [Repo](https://github.com/kngyeol/resnet50-mac-accelerator) |
| Fire & Smoke Detection Drone | YOLOv9 기반 화재/연기 탐지와 Lite-Mono 단안 거리 추정을 결합해 거리 기반 위험도를 산정한 Edge AI 프로젝트 | YOLOv9, Lite-Mono, TensorRT, Python, Gradio | [Repo](https://github.com/kngyeol/pjt-fire-detect-drone) |
| TeamPathfinders - Xycar 자율주행 | Lane detection, traffic signal recognition, Bezier/Pure Pursuit 기반 주차 경로, IMU 기반 주행 과제를 수행한 ROS 자율주행 교육 프로젝트 | ROS, Python, OpenCV, Pure Pursuit, IMU | [Repo](https://github.com/kngyeol/TeamPathfinders) |

## Tech Stack
### Core
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat-square&logo=ros&logoColor=white)
![Nav2](https://img.shields.io/badge/Nav2-22314E?style=flat-square)
![CAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-87C540?style=flat-square)
![HILS](https://img.shields.io/badge/HILS-4A4A4A?style=flat-square)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Jetson](https://img.shields.io/badge/Jetson-Orin%20Nano-76B900?style=flat-square&logo=nvidia&logoColor=white)

### Supporting
![Autoware](https://img.shields.io/badge/Autoware-00A3E0?style=flat-square)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=eclipsemosquitto&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Verilog](https://img.shields.io/badge/Verilog-FPGA-8A2BE2?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-v8%2Fv9-111111?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-Ubuntu%2022.04-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Qt5](https://img.shields.io/badge/Qt-5-41CD52?style=flat-square&logo=qt&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

## Award
- 건국대 공학교육혁신센터 장려상 (2024.09.27)
  - 차량의 주변상황과 차량상태 인지시스템
