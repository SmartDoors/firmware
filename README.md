# SmartDoors Firmware Repository

SmartDoors 자동문 제어 시스템 펌웨어 OTA 업데이트용 저장소입니다.

## 📦 Releases

최신 펌웨어는 [Releases](https://github.com/smartdoors/firmware/releases) 페이지에서 다운로드할 수 있습니다.

## 🔄 OTA 업데이트 방법

### 자동 업데이트 (권장)

1. 스마트도어즈 웹 브라우저에서 `http://<도어-IP>/update` 접속
2. 로그인
3. GitHub 버전 체크에서 최신 버전 확인
4. "📥 최신 버전 자동 다운로드 및 업데이트" 버튼 클릭
5. 자동으로 다운로드, 업로드, 재시작 완료

### 수동 업데이트

1. [Releases](https://github.com/smartdoors/firmware/releases) 페이지에서 `.bin` 파일 다운로드
2. OTA 업데이트 페이지에서 파일 선택
3. "🚀 업로드 및 재시작" 버튼 클릭

## 📝 저장소 구조

이 저장소는 **CHANGELOG만 Git으로 관리**합니다:

```
firmware/
├── CHANGELOG-v1.3.0.md       # 변경 사항 (Git에 커밋됨)
└── README.md                 # 이 파일 (Git에 커밋됨)
```

**펌웨어 바이너리 파일(`.bin`)은 Git에 저장되지 않으며**, [GitHub Releases](https://github.com/smartdoors/firmware/releases)의 **Assets로만 제공**됩니다:

- `firmware-v{version}.bin` - 펌웨어 바이너리
- `filesystem-v{version}.bin` - 파일시스템 이미지

## 🔧 버전 관리

- **Semantic Versioning** 사용 (Major.Minor.Patch)
- CHANGELOG는 Git 저장소에 커밋
- 바이너리 파일은 GitHub Release Assets에만 업로드
- 새 버전 릴리즈 시 `firmware-v{version}.bin` 형식 사용

## ⚠️ 주의사항

- ⚠️ **소스 코드는 이 저장소에 포함하지 않습니다**
- ⚠️ **바이너리 파일(.bin)은 Git에 커밋하지 않습니다** (Release Assets만)
- ⚠️ 업데이트 중 전원을 끄지 마세요
- ⚠️ 도어 작동 중에는 업데이트하지 마세요

## 📞 지원

문제가 발생하면 이슈를 등록하거나 개발팀에 문의하세요.

---

**Repository:** [smartdoors/firmware](https://github.com/smartdoors/firmware)  
**Organization:** [SmartDoors](https://github.com/smartdoors)

