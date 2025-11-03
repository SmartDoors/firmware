# SmartDoors Firmware Repository

ESP32 기반 자동문 제어 시스템 펌웨어 OTA 업데이트용 저장소입니다.

## 📦 Releases

최신 펌웨어는 [Releases](https://github.com/smartdoors/firmware/releases) 페이지에서 다운로드할 수 있습니다.

## 🔄 OTA 업데이트 방법

### 자동 업데이트 (권장)

1. ESP32 웹 브라우저에서 `http://<ESP32-IP>/update` 접속
2. 로그인 (admin/admin123)
3. GitHub 버전 체크에서 최신 버전 확인
4. "📥 최신 버전 자동 다운로드 및 업데이트" 버튼 클릭
5. 자동으로 다운로드, 업로드, 재시작 완료

### 수동 업데이트

1. [Releases](https://github.com/smartdoors/firmware/releases) 페이지에서 `.bin` 파일 다운로드
2. OTA 업데이트 페이지에서 파일 선택
3. "🚀 업로드 및 재시작" 버튼 클릭

## 📝 파일 구조

```
firmware/
├── firmware-v1.1.0.bin       # 펌웨어 파일
├── filesystem-v1.1.0.bin     # 파일시스템 이미지
├── CHANGELOG-v1.1.0.md       # 변경 사항
└── README.md                 # 이 파일
```

## 🔧 버전 관리

- **Semantic Versioning** 사용 (Major.Minor.Patch)
- 현재 버전: v1.1.0
- 새 버전 릴리즈 시 `firmware-v{version}.bin` 형식으로 파일명 지정

## ⚠️ 주의사항

- ⚠️ 소스 코드는 이 저장소에 포함하지 않습니다
- ⚠️ 바이너리 파일(.bin)만 업로드합니다
- ⚠️ 업데이트 중 전원을 끄지 마세요
- ⚠️ 도어 작동 중에는 업데이트하지 마세요

## 📞 지원

문제가 발생하면 이슈를 등록하거나 개발팀에 문의하세요.

---

**Repository:** [smartdoors/firmware](https://github.com/smartdoors/firmware)  
**Organization:** [SmartDoors](https://github.com/smartdoors)

