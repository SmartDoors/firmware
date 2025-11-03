# GitHub Release 생성 가이드

## 🚀 v1.1.0 Release 생성 방법

### 1. GitHub 웹사이트 접속
https://github.com/smartdoors/firmware/releases/new

### 2. Release 정보 입력

**Tag:** `v1.1.0`  
**Release title:** `Release v1.1.0 - SmartDoors OTA Update`

**Release notes (아래 내용 복사):**

```markdown
# Release v1.1.0

## 🎉 주요 기능

### OTA 업데이트 시스템
- ✨ 커스텀 OTA 업데이트 페이지 추가
- 🌐 GitHub Release 자동 체크 및 다운로드 기능
- 📱 펌웨어 버전 비교 및 자동 업데이트
- 💾 파일시스템(SPIFFS) 자동 업데이트 지원
- 🔧 Hardware ID 및 Firmware Version 표시
- 📊 실시간 업로드 진행률 표시

### 시스템 개선
- 🗑️ ElegantOTA 제거 및 커스텀 OTA 시스템 구현
- 🔌 WebService API 확장 (`/api/system-info`, `/api/ota/upload`)
- 📈 시스템 정보 실시간 조회 기능

## 🔄 변경 사항 (25-05-20)
- platformio.ini 기본 환경 설정 변경
- 도어끝단에서 전류 차단시 발생하는 유도성kickback 개선
- 도어 동작 관련 설정 최적화

## 📦 파일 정보

- **firmware-v1.1.0.bin** (1.9MB) - ESP32-S3 펌웨어
- **filesystem-v1.1.0.bin** (7MB) - SPIFFS 파일시스템

## 🛠️ 기술 정보

- **Hardware:** BOARD_LMC_REV_4
- **Chip:** ESP32-S3
- **Firmware Version:** 1.1.0
- **Build Date:** 2025-01-15

## 📥 설치 방법

### 자동 업데이트 (권장)
1. ESP32 웹 브라우저에서 `http://<ESP32-IP>/update` 접속
2. 로그인 (admin/admin123)
3. GitHub 버전 체크에서 최신 버전 확인
4. "📥 최신 버전 자동 다운로드 및 업데이트" 버튼 클릭
5. 자동으로 다운로드, 업로드, 재시작 완료

### 수동 업데이트
1. 아래 파일들을 다운로드
2. OTA 업데이트 페이지에서 파일 선택
3. "🚀 업로드 및 재시작" 버튼 클릭

## ⚠️ 주의사항

- 업데이트 중 전원을 끄지 마세요
- 도어 작동 중에는 업데이트하지 마세요
- 업데이트 후 자동으로 재시작됩니다
```

### 3. 파일 업로드

**Assets 섹션에서 다음 파일들을 업로드:**

1. `firmware-v1.1.0.bin` 
2. `filesystem-v1.1.0.bin` (선택사항)

### 4. Release 생성

- "Publish release" 버튼 클릭

---

## ✅ 완료 후 확인

Release 생성 후 다음 URL에서 확인:
https://github.com/smartdoors/firmware/releases/tag/v1.1.0

OTA 업데이트 페이지에서 자동으로 감지되어야 합니다!

---

## 📝 다음 Release 생성 시

새 버전(v1.2.0 등)을 릴리즈할 때:

1. `config.h`에서 버전 업데이트:
   ```cpp
   #define FW_VERSION "1.2.0"
   #define SW_VERSION "120"
   ```

2. 빌드 및 복사:
   ```bash
   pio run -e esp32-s3-devLMC-v4
   pio run -e esp32-s3-devLMC-v4 -t buildfs
   Copy-Item ".pio\build\esp32-s3-devLMC-v4\firmware.bin" -Destination "firmware\firmware-v1.2.0.bin"
   Copy-Item ".pio\build\esp32-s3-devLMC-v4\spiffs.bin" -Destination "firmware\filesystem-v1.2.0.bin"
   ```

3. Git 커밋 및 푸시:
   ```bash
   cd firmware
   git add firmware-v1.2.0.bin filesystem-v1.2.0.bin
   git commit -m "Release v1.2.0"
   git push
   ```

4. GitHub에서 Release 생성 (위 절차 동일)

