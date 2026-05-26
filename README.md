# 김동열 (Dongyeol Kim)

ROS2/Nav2 기반 실물 로봇 런타임과 임베디드/차량 SW 인터페이스를 연결하는 엔지니어입니다.

`ROS2 Robotics` `Autonomous Driving` `Embedded Systems` `CAN` `HILS`

[![GitHub](https://img.shields.io/badge/GitHub-kngyeol-181717?style=flat-square&logo=github)](https://github.com/kngyeol)
[![ROS2](https://img.shields.io/badge/ROS2-Humble-22314E?style=flat-square&logo=ros)](https://www.ros.org/)
[![Nav2](https://img.shields.io/badge/Nav2-Navigation-1F6FEB?style=flat-square)](https://navigation.ros.org/)
[![Autoware](https://img.shields.io/badge/Autoware-Autonomous%20Driving-00A3E0?style=flat-square)](https://autoware.org/)
[![SocketCAN](https://img.shields.io/badge/CAN-SocketCAN-00599C?style=flat-square)](https://www.kernel.org/doc/Documentation/networking/can.txt)
[![FreeRTOS](https://img.shields.io/badge/RTOS-FreeRTOS-87C540?style=flat-square)](https://www.freertos.org/)

## Snapshot

| 구분 | 내용 |
|---|---|
| Education | 건국대학교 전기전자공학부 학사, SSAFY 14기 임베디드 특화트랙 |
| Experience | Skyautonet 자율주행SW개발부 인턴 |
| Main Field | 로보틱스 런타임, 자율주행 SW, 임베디드/차량 인터페이스, HILS 검증 |
| Portfolio | [v0-portfolio-indol-chi-29.vercel.app](https://v0-portfolio-indol-chi-29.vercel.app/) |

## Core Strengths

| Robotics Runtime | Vehicle Interface | Verification | Edge AI / Acceleration |
|---|---|---|---|
| ROS2 action/service/topic 기반 로봇 명령 실행 구조 | CAN/UART/STM32/Jetson과 autonomy stack 연결 | timeout, cancel, sensor stale, fail-safe stop 처리 | YOLO/TensorRT, Zynq FPGA 가속기, Jetson 배포 |
| Nav2, localization, map calibration, odometry | SocketCAN, vcan, CAN frame packing, protocol conversion | HILS 시나리오, logging/replay, 실물 하드웨어 디버깅 | Detection + depth, fixed-point MAC, AXI DMA |

## Experience

| 기간 | 조직 | 핵심 업무 |
|---|---|---|
| 2024.09 - 2024.12 | Skyautonet 자율주행SW개발부 인턴 | Autoware 기반 Lv4 자율주행 플랫폼, Lanelet2 경로 생성, external lane change, HMI 제어, ROS2 상태-CAN 변환, vcan 기반 HILS 검증 |
| 2024.09 - 2024.12 | FODRo debris removal robot | ROS2 topic-CAN protocol converter, Multi-FOD clustering, lane validity check, cleaning state, debug client |

## Selected Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>SCV-drive</h3>
      <p><b>LLM 명령 기반 ROS2 서비스 로봇 런타임</b></p>
      <ul>
        <li>자연어/앱 명령을 실제 주행과 조작 행동으로 연결</li>
        <li><code>relative_move</code>, <code>precision_align</code>, <code>navigate_to_pose</code>, stop/cancel/return 흐름 구성</li>
        <li>Nav2 adapter, motion coordinator, drive bridge, field map, task pose, 실행 스크립트 연결</li>
      </ul>
      <p><code>ROS2 Humble</code> <code>Nav2</code> <code>robot_localization</code> <code>Python</code> <code>STM32/CAN</code> <code>Jetson</code></p>
    </td>
    <td width="50%" valign="top">
      <h3>TeamKAI</h3>
      <p><b>자율주행 자작차 인지/주행 파이프라인</b></p>
      <ul>
        <li>자율주행 경진대회 차량 프로젝트 인지 파트장</li>
        <li>LiDAR cone detection, camera/YOLO detection, traffic light recognition</li>
        <li>Bezier path, Stanley/Pure Pursuit, CAN bridge와 연결되는 perception-planning-control 흐름 경험</li>
      </ul>
      <p><a href="https://github.com/kngyeol/TeamKAI">Repository</a></p>
      <p><code>ROS</code> <code>C++</code> <code>Python</code> <code>PCL</code> <code>OpenCV</code> <code>YOLOv5/v8</code></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>Balemale</h3>
      <p><b>AI 스마트 자율주차 로봇</b></p>
      <ul>
        <li>번호판 인식, 키오스크, 백엔드, 로봇 주행이 연결되는 서비스 로봇 프로젝트</li>
        <li>ROS2, Jetson Orin Nano, mecanum base, ArUco marker, MQTT 기반 로봇 흐름 구성</li>
        <li>18-state mission FSM과 backend/kiosk 상태 동기화 경험</li>
      </ul>
      <p><code>ROS2 Humble</code> <code>Jetson Orin Nano</code> <code>Python</code> <code>OpenCV</code> <code>ArUco</code> <code>MQTT</code></p>
    </td>
    <td width="50%" valign="top">
      <h3>ResNet50 MAC Accelerator</h3>
      <p><b>Zynq-7000 기반 CNN 연산 가속기</b></p>
      <ul>
        <li>Conv 연산 병목을 줄이기 위한 PS/PL co-design 프로젝트</li>
        <li>Q10.22 fixed-point MAC datapath, AXI DMA, AXI4-Lite 제어 구현</li>
        <li>1x1 output-stationary와 NxN streaming 구조로 data movement 설계</li>
      </ul>
      <p><a href="https://github.com/kngyeol/resnet50-mac-accelerator">Repository</a></p>
      <p><code>Verilog</code> <code>Vivado</code> <code>Xilinx Zynq-7000</code> <code>AXI DMA</code> <code>C</code></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>Fire & Smoke Detection Drone</h3>
      <p><b>화재/연기 탐지 + 단안 거리 추정 Edge AI</b></p>
      <ul>
        <li>YOLOv9 detection과 Lite-Mono depth를 결합해 거리 기반 위험도 산출</li>
        <li>Structured pruning, TensorRT 최적화, Gradio UI 구성</li>
        <li>모델 결과를 장치 판단 흐름에 연결하는 edge deployment 경험</li>
      </ul>
      <p><a href="https://github.com/kngyeol/pjt-fire-detect-drone">Repository</a></p>
      <p><code>YOLOv9</code> <code>Lite-Mono</code> <code>TensorRT</code> <code>Python</code> <code>Gradio</code></p>
    </td>
    <td width="50%" valign="top">
      <h3>CAN MultiECU HILS</h3>
      <p><b>STM32 기반 멀티 ECU 검증 플랫폼</b></p>
      <ul>
        <li>Sensor ECU / Control ECU 분리 구조 설계</li>
        <li>CAN 이중화, fail-over, FreeRTOS task structure 구성</li>
        <li>Python 기반 scenario logging/replay와 HILS 검증 흐름 준비</li>
      </ul>
      <p><code>STM32</code> <code>FreeRTOS</code> <code>CAN</code> <code>Python</code> <code>HILS</code></p>
    </td>
  </tr>
</table>

## Tech Stack

| Area | Stack |
|---|---|
| Robotics / Autonomous Driving | `ROS2`, `Nav2`, `Autoware`, `robot_localization`, `Lanelet2`, `OpenCV`, `PCL` |
| Embedded / Vehicle Interface | `C`, `C++`, `Python`, `STM32`, `CAN`, `SocketCAN`, `UART`, `I2C`, `SPI`, `FreeRTOS` |
| AI / Edge | `PyTorch`, `YOLOv8/v9`, `TensorRT`, `ONNX`, `Jetson`, `OpenCV` |
| Hardware / Acceleration | `Verilog`, `Vivado`, `Xilinx Zynq`, `AXI DMA`, `Fixed-point arithmetic` |
| Product / Tools | `Linux`, `Docker`, `MQTT`, `Qt5`, `Spring Boot`, `Vue`, `TypeScript` |

## Open Source Plan

| Target Area | Contribution Ideas |
|---|---|
| ROS2 / Nav2 | 문서 보완, launch/config 예제 개선, 작은 test case 추가 |
| Autoware / Vehicle Tooling | 재현 가능한 issue report, HILS/CAN 주변 tooling 탐색 |
| SocketCAN / Robotics Utilities | 예제 정리, bug reproduction, review-friendly small PR |

## Award

| Date | Award |
|---|---|
| 2024.09.27 | 건국대 공학교육혁신센터 장려상 - 차량의 주변상황과 차량상태 인지시스템 |
