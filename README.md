# 면접 한 걸음 · CX Interview Lite

스냅컴퍼니 AI 솔루션 AM팀 면접을 준비하는 가벼운 웹앱입니다. 기존 CX Interview Lab과 별도 저장소·저장 키로 운영됩니다.

- 컬처핏 36개 + 직무 30개, 본 질문 66개와 꼬리질문 129개
- 한 화면에 질문 하나, 내 답변 자동 저장, 참고 답변 펼치기
- 이전·다음 이동, 꼬리질문별 답변 유지, 다시 볼 질문 표시
- 전체 질문 목록과 질문·답변 검색
- 전체/컬처핏/직무/중요/다시 보기 범위, 순서대로 또는 중복 없는 무작위 연습
- 모바일 대응, 외부 라이브러리·서버·유료 API 없음

## 사용

`index.html`을 열거나 정적 웹 서버로 실행합니다. 예: `python3 -m http.server 8000` 후 http://localhost:8000 접속.

학습 준비 → 연습 시작 → 내 답변 작성 → 참고 답변 또는 꼬리질문 확인 → 완료·다음. 다음 버튼으로 본 질문을 연습 완료로 기록합니다. 질문을 건너뛰려면 전체 질문 목록에서 원하는 질문을 선택하세요.

기록은 현재 브라우저의 localStorage `cx-interview-lite:snapcompany:v1`에 저장됩니다. 기기 간 동기화되지 않습니다. 브라우저 데이터를 지우면 기록이 사라집니다. 저장 실패 시 안내하며 입력 내용은 화면에 유지됩니다. 중요한 답변은 별도로 복사해 보관하세요.

## 자료

`questions.js`: 사용자 제공 스냅컴퍼니 원문 질문·참고 답변·꼬리질문·주의 문구·부록. 기존 앱의 자료를 그대로 복사했습니다. 실제 출제·합격자 답변이 아니며 개인의 실제 경험을 확인하면서 사용하세요. 일반 학습 화면에 편집·기업 관리 등 복잡한 기능은 두지 않았습니다.

`index.html`: 화면 / `styles.css`: 디자인 / `app.js`: 연습과 저장.

## GitHub Pages

GitHub 저장소에서 Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main, /(root) → Save.

배포 주소: https://mat-ap.github.io/cx-interview-lite/

## 검증

`tests/smoke.cjs`는 Playwright와 Chromium이 설치된 개발 환경에서 `node tests/smoke.cjs`로 실행합니다. 앱 자체에는 Node나 빌드 도구가 필요하지 않습니다.
