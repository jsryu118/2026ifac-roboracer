---
title: 자주 묻는 질문 (대면 경쟁)
short_title: FAQ
layout: page
section: race
language: ko-KR
base_url: faq-physical.html
---

<style>
.post li p {
  margin: 0;
}
.post > ul > li > p:first-child {
    font-weight: bold;
}
.post ul ul  {
    list-style-type: '–';
}
</style>

**목 차**
- ToC
{:toc}


# Mechanics

- 차에 기본 제공해주는 타이어와 다른 타이어를 사용할 수 있나요?

  네, 사용할 수 있습니다. 규정에 따르면 타이어에 제한이 없습니다 (스폰지와 고무 모두 허용). 
  단, 화학 첨가제는 엄격히 금지됩니다.



- ”차량 클래스”에 제한된 무게가 있나요?

  없습니다.

- 차량이 가벼워 차량의 트랙션이 동작하지 않습니다. 그래서 중량(예: 소형강판)을 추가할 수 있나요?
  
  자동차 바퀴의 균형을 균등하게 맞춰주는 중량만 허용합니다. 이 중량은 정지한 상태로 장착해야 합니다.

- 차량의 변속기 기어비를 변경할 수 있나요?

  네. 
  변속기 기어비를 포함한 하드웨어 변경은 규정을 준수하는 한 허용됩니다. ROBORACER 자율주행 경주 대회는 알고리즘 성능을 강조합니다. 팀들은 소프트웨어 최적화에 집중하는 것이 권장됩니다.

# Sensors

- 차량에 장착 가능한 카메라는 무엇이 있나요?

  규정에 따르면 단일 카메라와 스테레오 카메라 모두 허용됩니다. 단, **카메라 내부 처리에서 검출이나 VIO 결과와 같은 추가 정보를 제공하는 카메라는 허용되지 않습니다**. (깊이 정보는 허용됨)
  
  **불가능한 카메라:**
  - [Intel Realsense T265](https://www.intelrealsense.com/tracking-camera-t265/): 내장 VIO/SLAM 알고리즘이 6DoF 위치 추적 결과를 직접 제공
  
  **가능한 카메라:**
  - [Intel Realsense L515](https://www.intelrealsense.com/lidar-camera-l515/)
  - [Intel Realsense D455](https://www.intelrealsense.com/depth-camera-d455/)
  - [Stereolabs ZED 2i](https://www.stereolabs.com/zed-2i/)


# Rules

- 어떻게 경주 시작을 알릴 것인가요?

  타임 트라이얼의 경우 준비가 되는 대로 시작할 수 있습니다. 
  시작 선을 넘으면 측정이 시작됩니다.

  1대1 경주에서는 심판이 "ready-set-go"이라고 외칠 것입니다.


[slack]: https://f1tenth-teams.slack.com/archives/C027T45B477
