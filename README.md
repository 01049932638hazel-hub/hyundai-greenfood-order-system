# 현대그린푸드 발주시스템 2.40

Release 2.39 실행파일에서 웹 UI 자산을 복구해 소스 구조를 재구성한 PC 버전입니다.

## 2.40 변경 범위
- 기존 발주/편집/메모/PDF/자동저장/백업 UI와 로직 유지
- 시작화면 `어플 설치` 버튼 추가
- PC ↔ Android 앱 최초 1회 QR 페어링 구조 추가
- Bearer 토큰 기반 `/api/v1/orders/latest` 발주 연동 API 추가
- PC 발주 변경 시 앱용 최신 발주 캐시 자동 갱신
- 오류검사 API 및 화면 추가
- 앱 최신버전 안내용 `app_latest.json` 확인 기능 추가
- 기존 GitHub Release 기반 PC 자동업데이트 기능 유지

## 연동 규격
- 페어링: `HGFORDER://pair?endpoint=<LAN URL>&token=<TOKEN>`
- 최신 발주: `GET {endpoint}/api/v1/orders/latest`
- 인증: `Authorization: Bearer {token}`
- 응답: `{ "items": [...] }`

## 참고
Windows 실행파일에는 Android APK와 브랜드 PNG 자산이 내장됩니다. 텍스트 소스는 유지보수 기준본이며 배포 EXE는 별도 빌드 산출물로 관리합니다.
