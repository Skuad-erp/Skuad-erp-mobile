# 재고 관리 ERP - 모바일 (Android)

현대 파츠(가상 고객사)의 현장 직원을 위한 입출고 관리·재고 조회 앱

## 프로젝트 개요
- 기간: 2026.11.25 ~ 2026.12.28
- 팀 구성: 웹 프론트 1 / 모바일 1 / 백엔드 3
- 담당: 안드로이드 앱 전체 개발 (모바일 파트)

## 주요 기능
- 입고 / 출고 처리
- 재고 조회 및 검색
- 바코드 스캔
- 로그인 (JWT)

## 기술 스택
- Kotlin, Jetpack Compose
- MVVM, Hilt
- Retrofit, OkHttp, Room
- CameraX, ML Kit
- JUnit5, MockK
- GitHub Actions (CI)

## 아키텍처
[//]: # (todo)

## 컨벤션

### 브랜치
- `main`: 배포 가능한 상태 유지
- `feature/기능명`: 기능 개발 (예: `feature/stock-in`)
- `fix/버그명`: 버그 수정
- 작업 후 PR → CI 통과 → main에 merge

### 커밋 메시지
`타입: 내용` 형식으로 작성해요.

| 타입 | 용도 |
|---|---|
| feat | 새 기능 |
| fix | 버그 수정 |
| refactor | 구조 개선 (기능 변화 없음) |
| test | 테스트 추가·수정 |
| docs | 문서 수정 |
| chore | 설정, 빌드, 의존성 |

예: `feat: 입고 화면 수량 입력 추가`

### 코드 스타일
- Kotlin 공식 코딩 컨벤션 준수
- 클래스: PascalCase / 함수·변수: camelCase / 상수: UPPER_SNAKE_CASE
- Composable 함수는 PascalCase (예: `StockListScreen`)
- 화면별 접미사: `Screen`, `ViewModel`, `UiState`

### 패키지 구조
- `data` / `domain` / `ui` / `di` 계층으로 분리
- 화면 단위로 폴더를 나눠요. 예: `ui/stock/`