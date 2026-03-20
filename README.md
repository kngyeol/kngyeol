# 김동열 (Dongyeol Kim)
임베디드 시스템과 CAN 통신 기반 HILS 검증, ROS2 로보틱스 개발을 수행하는 엔지니어입니다.  
`Embedded Systems | CAN Communication | HILS Verification | ROS2 Robotics`

[![GitHub](https://img.shields.io/badge/GitHub-kngyeol-181717?style=flat-square&logo=github)](https://github.com/kngyeol)
[![ROS2](https://img.shields.io/badge/ROS2-Humble-22314E?style=flat-square&logo=ros)](https://www.ros.org/)
[![SocketCAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)](https://www.kernel.org/doc/Documentation/networking/can.txt)
[![FreeRTOS](https://img.shields.io/badge/RTOS-FreeRTOS-87C540?style=flat-square)](https://www.freertos.org/)
[![HILS](https://img.shields.io/badge/Verification-HILS-4A4A4A?style=flat-square)](#)

## Profile
- 이름: 김동열 (Dongyeol Kim)
- 학력: 건국대학교 전기전자공학부 학사 (2019.03 ~ 2025.08), 3.38/4.5
- 교육: 삼성청년SW·AI아카데미(SSAFY) 14기 임베디드 특화트랙 (2025.07 ~ 진행중)
- 병역: 카투사(KATUSA) 만기제대 (2020.06 ~ 2021.12)
- 어학: TOEIC 885, OPIc IM2

## Experience
### Skyautonet 자율주행SW개발부 인턴 (2024.09 ~ 2024.12)

**1) SkyAutonet Lv4 자율주행 플랫폼**
- Autoware Universe 기반 Level 4 자율주행 트럭(Maxen 차량) 개발 참여
- 기술: ROS2 Humble, Autoware Universe, C++, SocketCAN, Lanelet2, Qt5
- 담당:
  - Planning Manager 개발(16 커밋): Lanelet2 맵 기반 자동 경로 생성, External Lane Change 구현, `GetEndOfLaneGoal` 함수 수정
  - HILS Actuator(Lv4): `AutowareState`/`DrivingStatus`를 State CAN 메시지로 변환, Operation Mode 기반 제어 분기
  - HMI(Qt5) 통합: Start/Stop, Lane Change, Velocity 버튼 기능 구현

**2) FODRo (Foreign Object Debris Removal Robot)**
- 활주로/도로 위 이물질 자동 탐지 및 제거 로봇 개발 참여
- 기술: ROS2 Humble, C++, Python, SocketCAN/vcan, Lanelet2
- 담당:
  - CAN Converter 패키지 개발: ROS2 토픽→CAN 프로토콜 변환, Offset/Factor 변환, CAN 프레임 패킹, Quaternion→Yaw 변환, CAN 로그 자동 저장
  - HILS Actuator 구축: vcan 기반 실차 없는 SW 검증 환경 구성
  - FOD Manager 개발: Multi-FOD 클러스터링, 유효 차선 검증, 청소기 자동 제어
  - Cleaning State 구현, Proxy Debug Client 개발

## Projects
| 프로젝트 | 기간 | 설명/핵심 기여 | 기술 | 링크 |
|---|---|---|---|---|
| CAN MultiECU HILS | 진행중 | STM32 F446RE 2대로 Sensor ECU/Control ECU 분리, FreeRTOS 태스크 구조 설계, CAN 이중화 Fail-over, Python HILS 시나리오 주입/로깅 | STM32, FreeRTOS, CAN, Python, HILS | Private/Local |
| Balemale - AI 스마트 자율주차 시스템 | 2026.01 ~ 2026.02 | 4WD 메카넘휠 자율주행/주차, 28개 ArUco 맵+18개 FSM 미션, Dead Reckoning 기반 연속 주행, MQTT 실시간 통신, Backend(Spring Boot) 경로탐색 참여 | ROS2 Humble, Jetson Orin Nano, Python, OpenCV, ArUco, MQTT, YOLOv8, EasyOCR, Spring Boot | [Repo](https://github.com/kngyeol/balemale) |
| TeamKAI - 자율주행 자작차 | 2023.11 ~ 2024.11 | 한국자동차안전학회 경진대회 참가, 인지 파트장(20명), LiDAR 기반 5단계 콘 검출 파이프라인, 신호등 검출, ROS 인터페이스(ICD) 설계 | ROS, C++, Python, PCL, OpenCV, YOLOv5/v8, LiDAR(Ouster) | [Repo](https://github.com/kngyeol/TeamKAI) |
| ResNet50 MAC Accelerator | 학부 | Zynq-7000(PS+PL) 기반 Conv 연산 가속, Q10.22 고정소수점 MAC, AXI DMA x4, Weight 재사용 구조 및 SW/HW 벤치마크 | Verilog, Vivado, Xilinx Zynq-7000, AXI DMA, C | [Repo](https://github.com/kngyeol/resnet50-mac-accelerator) |
| Fire & Smoke Detection Drone | 졸업 프로젝트 | 드론 탑재 산불/연기 탐지 + 단안 거리추정, mAP50 0.867, Structured Pruning + TensorRT 최적화, 인식/거리추정 병렬 처리 | YOLOv9-c, Lite-Mono, TensorRT, Python, Gradio | [Repo](https://github.com/kngyeol/pjt-fire-detect-drone) |
| ARAS - RC Car ADAS 시스템 | SSAFY | Raspberry Pi 5 기반 ADAS 축소 구현, MQTT 기반 노드 통신, MANUAL/AUTO/ACC 모드, 센서 Stale Fail-Safe 정지 | Python, OpenCV, MQTT, UART/Modbus, PCA9685 | Local |

## Tech Stack
### Core
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat-square&logo=ros&logoColor=white)
![CAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-87C540?style=flat-square)
![HILS](https://img.shields.io/badge/HILS-4A4A4A?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Jetson](https://img.shields.io/badge/Jetson-Orin%20Nano-76B900?style=flat-square&logo=nvidia&logoColor=white)

### Supporting
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=eclipsemosquitto&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white)
![Simulink](https://img.shields.io/badge/Simulink-0076A8?style=flat-square&logo=mathworks&logoColor=white)
![Verilog](https://img.shields.io/badge/Verilog-FPGA-8A2BE2?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-v8%2Fv9-111111?style=flat-square)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![Git](https://img.shields.io/badge/Git-GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Ubuntu%2022.04-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Qt5](https://img.shields.io/badge/Qt-5-41CD52?style=flat-square&logo=qt&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)

## Award
- 건국대 공학교육혁신센터 장려상 (2024.09.27)  
  - "차량의 주변상황과 차량상태 인지시스템"

## GitHub Stats
![GitHub stats](https://github-readme-stats.vercel.app/api?username=kngyeol&show_icons=true&hide_border=true&count_private=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=kngyeol&layout=compact&hide_border=true)
