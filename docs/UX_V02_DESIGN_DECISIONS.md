# CareBridge EDU v0.2 — UX/UI 의사결정과 과제 업데이트

**프로젝트:** 2026-2 첨단기술과 간호 · B반 3조  
**날짜:** 2026-11-12  
**기준 자료:** 3조 문제정의 워크시트 · 3단계 아이디어 내기  
**대상:** 통원수술센터·외과병동·혈액종양내과 등 입·퇴원 빈번 부서 간호사와 입·퇴원 환자

## 1. 유지된 핵심 기능
- 가상 환자/부서·입원·퇴원 시점에 따른 교육 모듈 선택
- 환자용 단계별 카드, 읽어주기/일시정지/정지, 음성 속도 설정
- 글자 3단계·고대비 전환
- 이해 여부 자기 점검 및 환자 질문 작성
- 간호사 Teach-back 구두 확인·추가 설명 상태 표시
- 대시보드와 설계 근거/미검증 기대효과 표기

## 2. 역할별 정보 위계
### 간호사 (PC·태블릿)
1. 지금 교육/확인이 필요한 환자를 쉽게 찾는다.
2. 해당 환자에게 필요한 교육 주제 목록을 확인·선택한다.
3. 하나의 대표 CTA(“환자 교육 시작하기”)를 눌러 시작한다.
4. 교육 후 질문·재설명 요청·구두 확인 체크리스트를 확인한다.

### 환자 (태블릿·모바일)
1. “지금 읽을 내용”과 “다음에 할 일”이 가장 먼저 보인다.
2. 글씨 크기, 음성 속도, 고대비는 교육 내용 가까이에 배치한다.
3. 한 화면에 한 주제. 이전/다음 CTA와 음성 버튼을 구분한다.
4. 완료 전 이해/재설명 요청을 표시하고, 간호사에게 질문한다.

### 홈 (진입과 설명)
- 핵심 목적, 1차 행동, 3단계 체험 진입, 가상 상태 요약
- 안내 모달에서 간단한 사용법을 3단계로 제공
- 의료적 검증 전이라는 한계는 상단에서 항상 인식 가능

## 3. 디자인 아틀라스 참조와 적용
아틀라스의 아이디어를 참고한 독립 구현이며 외부 원본 코드를 복사하지 않았음.

| 참조 | 실제 적용 | 주의 |
|---|---|---|
| Fade-through / Easing | 화면 전환과 모달 진입 시 짧은 페이드·이동 | 콘텐츠 입력·판독을 지연시키지 않음 |
| Stagger | 홈 진입 카드의 짧은 순차 등장 | 모든 카드가 바로 조작 가능 |
| Segmented control | 글씨 크기·음성 속도·아티클 탭 활성 상태 표시 | 선택/비선택 대비 유지 |
| Microinteraction/Hover | 선택 환자 행·CTA에 반응, 선택 상태 명확히 표시 | 핵심 기능은 hover 없이도 접근 |
| Toast feedback | 초기화·구두 확인·교육 전달 결과 안내 | 중복/실제 병원 처리 완료로 오인 방지 |
| Disclosure/Sidebar | 사이드바 접기, 툴팁, 모바일 아이콘+짧은 레이블 | 접혀도 기능을 인식 가능 |
| Reduced motion | CSS prefers-reduced-motion: reduce 지원 | 시각·전정계 민감도 고려 |

참고 디자인 아틀라스:
- https://design.solhun.com/
- https://design.solhun.com/transitions/
- https://design.solhun.com/interaction/
- https://design.solhun.com/ux/call-to-action/

## 4. 기능 우선순위 (수정)
- **P0 (구현):** 교육 모듈, 환자별 시연, 조절형 환자 화면, 음성 안내, 이해/재설명 응답, 간호사 최종 확인, 모바일 정보 위계, 접이식 사이드바·사용 안내.
- **P1 (후속·미구현):** 교육자료의 기관 검토·승인 및 수정 이력, 인쇄·보호자 안내, 다국어, 교육 진행시간 측정/평가, 실제 사용자 테스트.
- **P2 (기관 도입 전 필수 별도 설계):** EMR·환자 인증·권한·접근기록, 개인정보 보호·보안, 의료기관의 실제 지침 검증, 임상 평가/도입 절차.

## 5. 과제의 AI 대화 및 초안 구성 6요소
1. **사용자:** 반복적인 입·퇴원 교육을 하는 간호사, 해당 교육을 받는 환자.
2. **문제:** 반복 구두 안내 업무 부담, 교육 누락 위험, 환자별 이해 차이와 실제 이해 확인 어려움.
3. **사용환경:** 환자 입원 또는 퇴원 직전·직후 병동의 간호사 PC/태블릿과 환자 교육용 기기.
4. **해결 아이디어:** 표준화한 승인 교육자료를 환자 특성에 맞게 단계별 전달하고 간호사가 Teach-back 확인.
5. **핵심기능:** P0 기능 목록 참조. 실제 처방 등은 아직 연동하지 않음.
6. **결과물:** 홈 / 의료진 대시보드 / 환자 교육 / 구두 이해 확인 / 아이디어 및 근거 화면.

## 6. 기대효과 vs. 검증된 사실
- **문헌 지침에 의해 뒷받침되는 설계 원칙:** 쉬운 환자교육자료, 건강정보 이해능력 고려, Teach-back 이해 확인.
- **프로그램에 대한 기대효과(미검증):** 간호사 교육시간 및 피로도 감소, 반복 설명·정보 누락 감소, 환자 이해도 증가.
- **현재 확인한 기술적 사항:** 정적 웹 코드 JS 문법 검사 PASS, DOM 모의 테스트에서 5개 화면 렌더링·교육 시작·이해 응답·구두 확인 완료·탭 전환·상태 초기화 흐름 PASS. GitHub Actions/Pages 배포 결과는 저장소 Actions 기록으로 별도 확인해야 함.
- **미확인:** 실제 PC·모바일 시각적 사용성, 브라우저별 한국어 음성 품질, 환자 만족도, 실제 병원 정보와 정책 부합.
- **데이터 제한:** 가상 환자 외 데이터 저장·전송 기능 없음. 실제 환자정보 입력 금지.

## 7. 참고문헌 (APA 7판)
Agency for Healthcare Research and Quality. (2024). *Health literacy universal precautions toolkit* (3rd ed.). https://www.ahrq.gov/health-literacy/improve/precautions/toolkit.html

Agency for Healthcare Research and Quality. (2024). *Use the teach-back method: Tool 5*. https://www.ahrq.gov/health-literacy/improve/precautions/tool5.html

Centers for Disease Control and Prevention. (n.d.). *The CDC clear communication index*. https://www.cdc.gov/ccindex/

Design Atlas. (n.d.). *Design Atlas: A living dictionary of motion, effects, components and UX terms*. https://design.solhun.com/
