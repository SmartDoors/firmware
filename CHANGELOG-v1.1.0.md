# Release v1.1.0

## 변경 사항 (2025-01-15)

### OTA 업데이트 시스템
- 커스텀 OTA 업데이트 페이지 추가
- GitHub Release 자동 체크 및 다운로드 기능
- 펌웨어 버전 비교 및 자동 업데이트
- 파일시스템(SPIFFS) 자동 업데이트 지원
- Hardware ID 및 Firmware Version 표시
- 실시간 업로드 진행률 표시

### 시스템 개선
- ElegantOTA 제거 및 커스텀 OTA 시스템 구현
- WebService API 확장 (`/api/system-info`, `/api/ota/upload`)
- 시스템 정보 실시간 조회 기능

### 이전 변경 사항 (25-05-20)
- platformio.ini 기본 환경 설정 변경
- 도어끝단에서 전류 차단시 발생하는 유도성kickback 개선
- 도어 동작 관련 설정 최적화

### 이전 변경 사항 (25-05-19)
- 도어끝단에서 전류 차단시 발생하는 유도성kickback 개선
- 점진적 감속 구현으로 도어 끝단에서 부드러운 정지 구현
- 소프트 스톱 기능 추가로 전압 제한을 점진적으로 감소시켜 안전한 전류 차단

### 이전 변경 사항 (25-05-17)
- DoorDirection 열거형을 MotionType으로 변경하고 값 업데이트
- CommandInterface, DoorController, MotorManager 파일 삭제하여 코드베이스 간소화
- 사용하지 않는 파일 제거 및 코드 구조 개선
- WebService 클래스와 메모리 관리 최적화
- Door 열림/닫힘 동작 개선

## 기술 정보

- **Hardware:** BOARD_LMC_REV_4
- **Chip:** ESP32-S3
- **Firmware Version:** 1.1.0
- **Build Date:** 2025-01-15

## 설치 방법

1. OTA 업데이트 페이지 접속: `http://<ESP32-IP>/update`
2. GitHub 버전 체크에서 자동 확인
3. "최신 버전 자동 다운로드 및 업데이트" 버튼 클릭
4. 또는 수동으로 firmware-v1.1.0.bin 파일 업로드

## 주의사항

- 업데이트 중 전원을 끄지 마세요
- 도어 작동 중에는 업데이트하지 마세요
- 업데이트 후 자동으로 재시작됩니다

