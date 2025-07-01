# watchNavi
appleWatch 연동 Navigation

# 🧭 WatchNav – Apple Watch 기반 도보 길안내 인터페이스

## 🔍 개요

기존 길안내 앱은 스마트폰 화면을 지속적으로 주시해야 하며, 이는 보행 중 시야 분산과 안전 문제를 유발함.  
**WatchNav는 Apple Watch를 통해 최소한의 정보를 직관적으로 제공**함으로써,  
**폰을 보지 않고도 길을 안전하게 찾을 수 있는 스마트 길안내 시스템**을 목표로 함.

---

## 🎯 주요 기능 (MVP 기준)

- ⌚ **Apple Watch 기반 UI**
  - 현재 진행 방향을 화살표 형태로 표시 (나침반 방식)
  - 다음 경로 전환까지 남은 거리 표시 (예: “100m 후 좌회전”)
  - ETA(예상 도착 시간) 간단 표기
  - 진동 피드백으로 시각 정보 대체

- 📱 **iPhone 앱 연동 (선택 사항)**
  - 목적지 설정
  - 경로 요청 및 계산
  - 애플워치로 정보 전송

---

## 🧱 기술 스택

- **프로그래밍 언어**: Swift
- **UI 프레임워크**: SwiftUI, WatchKit
- **위치/지도 API**:
  - CoreLocation (현재 위치 및 이동 방향)
  - MapKit (도보 경로 요청 및 거리 계산)
- **기타**
  - Haptic Engine (진동 피드백)
  - Apple Developer 계정 필요 (MapKit 사용 및 배포용)

---

## 🧭 예시 화면 구성 (Apple Watch)



- 방향 화살표: 현재 진행해야 할 방향
- 거리 및 전환 정보: 다음 명령 요약
- 모든 정보는 미니멀하게 표시

---

## 🛠️ 개발 계획

1. **MVP 구현**
   - iPhone에서 목적지 입력 → 경로 요청
   - 애플워치에서 나침반 + 다음 지시사항 + 진동

2. **기능 확장 아이디어**
   - 음성 안내 or AirPods 연동
   - 안전 루트 필터링 (야간/혼잡도 고려)
   - 오프라인 경로 저장
   - 관광객 모드 (랜드마크 음성 안내 등)

---

## 💡 차별성 및 시장성

| 요소 | 기존 앱 | WatchNav |
|------|----------|-----------|
| 지도 시각화 | 복잡함 | 없음 (나침반 + 거리만 표시) |
| 폰 의존도 | 높음 | 낮음 (워치 중심) |
| 진동 피드백 | 제한적 | 핵심 기능 |
| UX 단순성 | 낮음 | ✅ 매우 높음 |

---

## ⚠️ 참고 사항

- Apple MapKit은 turn-by-turn 안내를 제한적으로만 제공하므로, 사용자 커스텀 방향 추론 로직 필요할 수 있음
- Google Directions API 사용 시 상업화 전 유료 요금제 고려 필요
- OpenStreetMap + OSRM으로 완전 오픈소스 대체 가능

---

## 👤 개발자 메모

> "폰을 보지 않고 길을 찾을 수 있다면, 길안내 앱의 본질이 바뀐다."  
> - 목표는 단순히 '경로 안내'가 아닌 '사용자 안전 중심의 UX 설계'

---

## 📂 향후 구조화 방향

WatchNav/
├── WatchApp/
│ ├── CompassView.swift
│ ├── HapticManager.swift
│ └── NavigationHUD.swift
├── iOSApp/
│ ├── DestinationSelector.swift
│ └── RouteManager.swift
├── Shared/
│ └── LocationService.swift
└── README.md


---

## 📌 라이선스

MIT License (예정)

---

## ✉️ Contact

> 개발자: Doyeop Kim  
> University of Exeter – Computer Science  
> 📧 Email: [YourEmailHere@example.com]

