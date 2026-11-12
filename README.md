# CareBridge EDU · 입·퇴원 맞춤형 교육지원 MVP

> 2026-2 첨단기술과 간호 · B반 3조 · 수업용 시연 프로젝트

## 무엇을 하는 프로그램인가?

통원수술센터, 외과병동, 혈액종양내과 등 입·퇴원이 잦은 부서의 간호사가 **교육 항목을 선택**하면, 환자가 **큰 글씨·음성 안내·속도 조절·반복 설명**으로 주요 내용을 확인하고, 간호사가 **Teach-back(환자 자신의 말로 설명)** 방식으로 최종 이해 여부를 확인하도록 지원하는 웹 MVP입니다.

**중요:** 퇴원 후 건강상태 추적관리 플랫폼이 아닙니다. 병원에서 입·퇴원 절차를 진행하는 시점의 교육을 돕는 개념 시연입니다.

## 데모

- 예상 GitHub Pages 주소: https://pchjesus.github.io/carebridge-edu/
- [교육 아이디어 상세 문서](docs/STEP3_IDEATION.md)
- [과제용 AI 활용 보고 초안](docs/AI_USE_REPORT.md)

### 사용 흐름

1. 의료진 대시보드 → 환자 A/B/C 선택
2. 입원·퇴원 교육 모듈 체크 → 교육 시작
3. 환자 화면 → 글씨 크기/고대비/한국어 음성 속도 설정 → 카드별 교육
4. 이해 확인 → 이해/재설명 요청 및 질문 선택
5. 최종 이해 확인 → 간호사가 대면으로 질문 및 보충설명 후 확인 처리

## 기능

- 세 가지 가상 시나리오: 통원수술센터 입원, 외과병동 퇴원, 혈액종양내과 입원
- 병동/시점별 교육 모듈 조합, 안내 진행 상태
- 글씨 크기 3단계, 고대비, 브라우저 음성 읽기 및 음성 속도 3단계
- 환자별 자체 이해 표시 및 간호사에게 전달할 질문
- 간호사의 Teach-back 체크리스트와 재설명 처리
- 설계의 근거와 아직 검증되지 않은 기대효과를 구분하여 표시
- 모바일·태블릿·PC 대응, 외부 프레임워크 없이 동작

## GitHub Pages 설정

관리 권한 계정에서 **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main → Folder: /(root) → Save**.

정적 HTML 파일 `index.html`만 있으므로 빌드가 필요하지 않습니다. 배포 상태는 GitHub의 Pages / Actions에서 확인해 주세요.

## 보안 및 의료 안전

- **실제 환자정보 입력 금지**: 저장·전송·인증·접근제어·법적 의료정보 보호에 대응하지 않은 시연용 MVP입니다.
- 환자 A/B/C는 가상 사례입니다. 입력한 시연 내용은 메모리에서만 관리되며 새로고침하면 초기화됩니다.
- 모든 교육 문구는 원리 설명용이며 기관 승인을 받은 교육자료나 실제 처방이 아닙니다.
- 수술동의, 환자별 약물·금식 지시, 고위험 지침, 법정 설명의무, 간호사의 판단과 공식 기록을 대체하지 않습니다.
- 음성 안내는 브라우저 SpeechSynthesis 지원 및 기기의 한국어 음성 지원에 따라 달라질 수 있습니다.
- 실제 임상 적용에는 자료 승인 절차·권한관리·안전성 검증·보안성 검토·접근성/사용성 평가 등이 필요합니다.

## 근거와 기대효과 구분

**근거가 있는 설계 원칙:** 쉬운 표현과 정보 구조화, 환자 자신의 말로 이해 내용을 확인하는 Teach-back, 교육자료 활용 후 대화.

**기대효과(미검증):** 간호사 반복 교육 시간 및 업무 부담 감소, 교육 누락 감소, 환자의 이해도 향상. 본 MVP에서 이를 증명하는 실제 평가 결과는 없습니다.

## 참고문헌 (APA 7판)

- Agency for Healthcare Research and Quality. (2024). *Health literacy universal precautions toolkit* (3rd ed.). https://www.ahrq.gov/health-literacy/improve/precautions/toolkit.html
- Agency for Healthcare Research and Quality. (2024). *Use the teach-back method: Tool 5*. https://www.ahrq.gov/health-literacy/improve/precautions/tool5.html
- Agency for Healthcare Research and Quality. (2024). *Use health education material effectively: Tool 12*. https://www.ahrq.gov/health-literacy/improve/precautions/tool12.html
- Centers for Disease Control and Prevention. (n.d.). *The CDC clear communication index*. https://www.cdc.gov/ccindex/


## v0.2 UI/UX 업데이트 (2026-11-12)

- **간호사 중심 정보 위계:** 지금 선택할 환자 → 필요한 교육 모듈 → “환자 교육 시작하기” CTA
- **환자 중심 정보 위계:** 큰 안내문 → 듣기/글씨·속도 조절 → 다음 안내/이해 여부
- **화면 간 3단계 안내:** 설정 → 교육 → 간호사 Teach-back 확인
- **접이식 사이드바:** PC 확장/축소, 태블릿 아이콘 레일, 모바일 아이콘+텍스트 상단 내비게이션
- **사용 안내:** 언제든 열 수 있는 1분 안내 팝업
- **짧은 모션:** fade-through, stagger, 버튼 피드백, 토스트; 모션 감소 사용자 설정 존중
- **아이디어/근거 탭 분리:** 스크롤을 줄이고 필요한 정보만 표시
- **새로고침 시 데이터 초기화:** 가상 환자만 사용, 서버·EMR 저장 없음

**[UX 설계 근거·우선순위·기능/안전성 설명](docs/UX_V02_DESIGN_DECISIONS.md)**

참고한 디자인 패턴: [Design Atlas](https://design.solhun.com/). 모든 소스는 자체 작성한 시연용 구현입니다.

GitHub Pages는 저장소의 **main /(root)** 배포 설정을 통해 자동 게시됩니다. [배포된 시연 사이트](https://pchjesus.github.io/carebridge-edu/). 최종 배포 결과는 [Actions](https://github.com/pchjesus/carebridge-edu/actions)에서 확인합니다.


## v0.3 — 제품 소개형 홈 및 문헌 기반 환자교육 시연 (2026-11-12)

- **홈 정보 위계:** 서비스 목적 → 환자교육 체험 CTA → 간호사/환자/최종 확인 3단계 → 출처·검증상태.
- **메인 시연:** 홈에서 “환자교육 실제 체험하기”를 누르면 가상 환자 D(58세, 외과병동, 복강경 담낭절제술 퇴원 전 안내)의 교육 카드가 즉시 실행됨.
- **실제 내용:** 미국 NLM MedlinePlus·NHS 공개 자료를 참고해 재구성한 5개 교육 주제(회복·활동, 상처관리, 식사·배변, 약물·외래 확인, 경고 증상).
- **가상 데이터:** 환자 D의 인적 특성과 진료 상황은 합성 사례이며 실제 의료정보·처방·진료일은 포함되지 않음.
- **교육자료 파일:** [전체 환자교육 자료](materials/laparoscopic-cholecystectomy-discharge.html) — 별도 탭에서 확인하고 브라우저 인쇄/PDF로 저장 가능.
- **출처·가상 구분:** 홈, 의료진 화면, 환자 화면, 교육문서에서 명시함.
- **기존 기능 유지:** 환자 A/B/C, 교육 선택, 글씨·음성·고대비, 이해 확인, 간호사 구두 확인 및 상태표시.
- **검증:** JS 문법 검사 및 DOM 기반 전체 교육 흐름 모의 검사. 실제 환자 대상 검증·전체 브라우저 시각 검사는 미수행.

[환자교육 근거와 합성데이터 구분 문서](docs/EDUCATION_SOURCE_AND_SYNTHETIC_CASE.md)

추가 근거문헌:
- U.S. National Library of Medicine. (n.d.). *Gallbladder removal – laparoscopic – discharge*. MedlinePlus. https://medlineplus.gov/ency/patientinstructions/000117.htm
- National Health Service. (n.d.). *Recovering from gallbladder removal*. https://www.nhs.uk/tests-and-treatments/gallbladder-removal/recovery/
