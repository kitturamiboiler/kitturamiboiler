# 문재민 · MUN JAEMIN

**Java · Spring 백엔드 개발을 중심으로, 프론트엔드와 UI도 구현합니다.**

OMAGOTCHI에서 출결·보상 기능과 사용자 화면을 만들었습니다.
서버에서는 재시도와 동시 요청을, 화면에서는 로딩·빈 데이터·오류 상태를 구분해 다뤘습니다.

[NHN Academy AIoT 3기](https://github.com/nhnacademy-aiot3) · Java Backend 과정 수료 (2025.12–2026.09)

## 대표 프로젝트 · OMAGOTCHI

출석과 학습 기록을 캐릭터 성장으로 연결한 **8인 팀 프로젝트**입니다.
기수·출결·게이미피케이션 백엔드와 Home·반응형 UI를 담당했습니다.

| 영역 | 다룬 문제 | 구현한 내용 |
| :--- | :--- | :--- |
| Backend | 출결 저장 후 이벤트 발송에 실패하면 보상이 누락될 수 있음 | 출결과 Outbox 이벤트를 같은 트랜잭션에 기록하고 발송 실패 재처리 |
| Backend | 이벤트 재수신·동시 요청으로 XP가 중복 반영될 수 있음 | 수신 영수증·XP 원장·행 잠금·유니크 제약을 조합해 중복 반영 방지 |
| Backend | 정시·지각 판정의 시간 경계 검증 | 출결 정책을 분리하고 Clock 주입으로 테스트 |
| Frontend | 작은 화면에서 HUD가 겹치거나 잘림 | 단일 /home에서 문서 흐름·Grid 기반 반응형 레이아웃 구현 |
| Frontend | 재실 조회 실패가 정상 값인 0명처럼 표시됨 | fallback을 제거하고 loading·empty·error 상태 구분 |

[Frontend 저장소 →](https://github.com/nhnacademy-aiot3-omagotchi/omagotchi-frontend)

### 확인한 기록

| 항목 | 수치와 범위 |
| :--- | :--- |
| UI 자동 테스트 | Vitest **21개 파일 · 80개 테스트 통과** 기록 |
| 반응형 확인 | **5개 화면 크기**에서 정적 통합 fixture의 Home·출석부 가로 넘침 없음 |
| 직접 제작한 캐릭터 | **시로몽 저작권 등록 1건** · 제C-2026-040776호 |

<details>
<summary>테스트 기록의 기준과 범위</summary>

2026.08.14 UI 통합 리팩토링 작업 기록 기준입니다.
테스트 수는 당시 프로젝트의 실행 결과이며, 모두 제가 작성한 테스트라는 의미는 아닙니다.

- 화면 크기: 1440×900, 1024×768, 844×390, 390×844, 320×568
- 정적 통합 fixture에서 화면 넘침, 패널 열기·닫기, 포커스 복귀 등을 확인했습니다.
- 실제 서비스 전체의 E2E 완료나 사용자 대상 사용성 검증을 뜻하지 않습니다.

</details>

## 그 밖의 개발 경험

- **Mini Dooray** · Project·Project Member·Tag·Milestone **4개 영역**의 서비스·Controller와 관련 테스트 구현. Front·Gateway 담당자와 API 계약을 맞춰 연동했습니다.
- **Flip-Bot** · Python·discord.py 경제 시뮬레이션 봇 개발. 사용자 자산·거래 기록을 관리하고 Railway 배포 오류를 로그로 확인했습니다.

## 사용한 기술

| 구분 | 프로젝트에서 사용한 기술·도구 |
| :--- | :--- |
| Backend | Java, Spring Boot, Spring MVC, JPA, PostgreSQL |
| Frontend | HTML, CSS, JavaScript, React, Thymeleaf |
| 확인·협업 | JUnit 5, Vitest, Storybook, Git, GitHub |
| UI·시각 작업 | Figma, Aseprite |

Figma로 화면을 설계하고 Aseprite로 캐릭터·픽셀 애니메이션을 제작했습니다.
시로몽은 직접 제작한 저작물이며, 팀 프로젝트 전체의 저작권을 의미하지 않습니다.
에셋의 재사용·재배포는 사전 문의해 주세요.
