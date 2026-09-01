# 현대그린푸드 발주시스템 2.41

Release 2.39 실행파일에서 웹 UI 자산을 복구해 재구성한 PC 버전 계열입니다.

## 2.41 변경 범위
- 어플 설치 버튼이 열리지 않던 문제 수정
- 어플 · 프로그램 연동 버튼 모달 표시 오류 수정
- 휴대폰 APK 설치 QR / 직접 설치 주소 / PC 저장 기능 보강
- 연동 QR, PC 주소, 인증키 표시 및 오류검사 동작 보강
- 도움말에 어플 설치 및 QR 연동 사용법 추가
- 프로그램 패치내용에 Android 앱 패치 이력 추가
- 기존 발주 / 편집 / 메모 / PDF / 자동저장 / 백업 기능은 변경하지 않음

## 앱 연동
- 내장 앱 버전: 1.3.0
- 페어링: `HGFORDER://pair?endpoint=<LAN URL>&token=<TOKEN>`
- 최신 발주: `GET {endpoint}/api/v1/orders/latest`
- 인증: `Authorization: Bearer {token}`
- PC 연결 실패 시 앱은 마지막 성공 연동 기록을 사용

## 앱 설치
- PC와 휴대폰을 같은 Wi-Fi에 연결
- 시작화면 > 어플 설치 > QR 스캔
- QR 사용이 어려우면 표시되는 설치 주소를 휴대폰 브라우저에서 직접 열기
- Windows에 APK 파일만 저장하는 기능도 제공

## 참고
Windows 실행파일에는 Android APK와 브랜드 자산이 내장됩니다. 배포 EXE의 SHA256은 `652ec6e1dbc0524111f8e198a16badcd0dc0f1a0d45dfb7dda6b2ad217b16470` 입니다.
