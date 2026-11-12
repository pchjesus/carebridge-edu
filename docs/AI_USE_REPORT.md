# AI 도구 활용 내역 보고 · 2026-2 첨단기술과 간호 3조

> **초안 / 사실과 구별:** 이 문서는 현재 대화에서 실제 수행된 활동을 중심으로 작성했습니다. 이후 조원 수정이나 Codex 활용, 제출 시점 변경은 별도로 반영해야 합니다.

## 1. 사용 도구·모델·사용일
- 도구: ChatGPT (GPT-6), GitHub 연결 도구, 공개 웹 문헌 검색
- 사용일: 2026년 11월 12일 (이번 3단계 아이디어 및 초기 MVP 구성)
- 개발환경: GitHub 리포지토리 `pchjesus/carebridge-edu`, 정적 HTML/CSS/JavaScript
- **Codex 사용 내역:** 본 초기 MVP 작성 시점에는 별도 Codex 실행이 확인되지 않았음. 추후 사용 시 모델·일시·작업 범위를 추가 기록할 것.
- 이전 워크시트 및 공감지도 초안 작성에도 AI를 활용했으므로, 최종 제출 시 대화 내역에 따라 추가 사용일과 실제 사용 모델을 확인해 보완할 것.

## 2. 입력 자료의 범위
- 3조 문제정의 워크시트(5쪽): 문제 상황, 핵심 사용자·사용환경, 공감지도, 현행 방식의 한계, 핵심 필요와 중요성, 최종 요약.
- 3단계 과제 양식 이미지: HMW 아이디어 발상 질문, 브레인라이팅 목록.
- 사용자 지시: 퇴원 후 관리가 아닌 입·퇴원 시 교육 보조, 간호사의 최종 구두 확인, 접근성 조정, GitHub Pages 배포 및 과제 보고 요건.
- 외부 공개 자료: AHRQ 건강정보 이해능력/Teach-back/교육자료 활용 지침, CDC Clear Communication Index, GitHub Pages 안내.
- 실제 환자자료·실제 EMR·개별 처방·병원 내부 지침은 입력하지 않았음.

## 3. 핵심 프롬프트 (요지)
“통원수술센터, 외과병동, 혈액종양내과 등 입·퇴원이 잦은 곳의 간호사가 반복 교육 부담을 줄일 수 있도록, 환자별 주요 주의사항을 음성·문자로 제공하는 프로그램을 구상해 줘. 큰 글씨와 느린 음성 등 고령자를 위한 기능을 포함하고, 환자의 실제 이해 내용은 간호사가 나중에 구두로 확인한다. 이는 퇴원 후 관리가 아니라 입·퇴원 시 교육이다. 3단계 HMW·브레인라이팅 과제를 작성하고 GitHub Pages에서 시연 가능한 MVP를 만들되, 참고문헌과 기대효과/검증 결과를 구분하고 AI 사용 내역을 기록하라.”

위 문장은 일련의 사용자 요구를 **보고서용으로 요약·정리한 핵심 프롬프트**이며, 단일 입력문을 그대로 복사한 원문이 아님.

## 4. 결과물 선정 및 수정 과정
1. 간호사의 반복적인 구두 교육과 환자별 이해도 차이를 핵심 문제로 확정.
2. 퇴원 후 추적관리·임의 의료판단·실제 처방 생성을 범위에서 제외.
3. 아이디어 후보 가운데 모듈 선택, 접근성, 단계별 안내, 환자 자기 점검, 간호사 Teach-back 확인을 MVP 핵심으로 선택.
4. 실제 병원 데이터를 쓰지 않고 가상 환자 3명의 기본 교육 주제로만 프로토타입 구성.
5. 근거문헌에 기반한 설계 원칙과 아직 검증하지 않은 서비스 기대효과를 MVP에 구별하여 표시.
6. 조원별 추가 아이디어와 수정 결과는 아직 반영 전이며, 이후 회의 내용을 기록·수정할 예정.

## 5. 최종 판단 근거 및 한계
- **판단 근거:** 기존 3조 워크시트의 핵심 사용자와 문제정의에 부합, 실제 교육 콘텐츠 보조의 범위 유지, 환자별 차이를 고려한 UX, 간호사의 최종 확인을 통한 책임 경계 유지.
- **내용의 한계:** AHRQ·CDC 문헌은 설계 원칙을 뒷받침하지만 **CareBridge EDU 자체의 안전성·효과를 검증한 문헌이 아님**.
- **기술적 한계:** 정적 웹 시연으로 실제 EMR/병원 인증/개인정보 처리/교육자료 승인·버전관리/의료기관 접근성 인증은 구현하지 않음. 한국어 음성 합성은 브라우저와 음성팩의 영향을 받음.
- **추가 검증:** 임상간호사·환자 의견 수렴, 승인된 지침과 의학적 정확성 검토, 환자용 사용성 및 접근성 테스트, 교육시간·재설명 횟수·Teach-back 결과 등 측정, 개인정보 보호 영향 검토.
- **효과 표기:** 간호사 업무부담 완화와 환자 이해도 향상은 **기대효과(미검증)** 로 표기하고, 실증 결과가 있는 것처럼 표현하지 않음.

## 참고문헌 (APA 7판)
- Agency for Healthcare Research and Quality. (2024). *Health literacy universal precautions toolkit* (3rd ed.). https://www.ahrq.gov/health-literacy/improve/precautions/toolkit.html
- Agency for Healthcare Research and Quality. (2024). *Use the teach-back method: Tool 5*. https://www.ahrq.gov/health-literacy/improve/precautions/tool5.html
- Agency for Healthcare Research and Quality. (2024). *Use health education material effectively: Tool 12*. https://www.ahrq.gov/health-literacy/improve/precautions/tool12.html
- Centers for Disease Control and Prevention. (n.d.). *The CDC clear communication index*. https://www.cdc.gov/ccindex/
