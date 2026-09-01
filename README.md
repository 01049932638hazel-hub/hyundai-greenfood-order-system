# 현대그린푸드 발주시스템 2.42

Release 2.39 실행파일에서 웹 UI 자산을 복구해 소스 구조를 재구성한 PC 버전입니다.

## 2.42 변경 범위
- 기존 발주/편집/메모/PDF/자동저장/백업 UI와 로직 유지
- 앱 v1.3.1 내장
- Android 로컬 HTTP 통신 허용으로 같은 Wi-Fi PC 접근 차단 문제 수정
- QR 인증 직후 실제 PC 서버 연결 확인
- 앱 불러오기 오류를 인증키/서버/네트워크/데이터 형식으로 구분 안내
- PC 서버는 `0.0.0.0:8765`에 바인딩하고 QR에는 LAN IP를 사용
- PC 오프라인 시 앱의 마지막 성공 동기화 기록 복원 유지
- 어플 설치/QR 연동/오류검사/앱 최신버전 안내 기능 유지

## 연동 규격
- 페어링: `HGFORDER://pair?endpoint=<LAN URL>&token=<TOKEN>`
- 최신 발주: `GET {endpoint}/api/v1/orders/latest`
- 인증: `Authorization: Bearer {token}`
- 응답: `{ "items": [...] }`

## 문제 해결
QR 스캔 후 연결 확인이 실패하면 PC와 휴대폰이 같은 Wi-Fi인지 확인하고, Windows 방화벽에서 현대그린푸드 발주시스템의 사설 네트워크 통신을 허용한 뒤 QR을 다시 스캔합니다.

## 참고
Windows 실행파일에는 Android APK와 브랜드 PNG 자산이 내장됩니다. 텍스트 소스는 유지보수 기준본이며 배포 EXE는 별도 빌드 산출물로 관리합니다.
