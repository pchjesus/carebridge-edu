# CareBridge EDU — 문헌 기반 환자교육 자료 및 합성사례 기록

## 왜 이 교육자료를 선택했나?
**입·퇴원 환자교육 지원**이라는 프로젝트의 핵심 기능을 실제에 가까운 내용으로 시연하기 위해, MedlinePlus의 공개 환자교육 자료 *Gallbladder removal – laparoscopic – discharge*와 NHS의 복강경 담낭절제술 회복 안내를 사용했다.

이는 **퇴원 후 추적관리 서비스가 아니라 병원 퇴원 직전 진행하는 환자교육의 시연**이다.

## 입력 데이터의 출처 구분

| 데이터 | 성격 |
|---|---|
| 복강경 담낭절제술 후 회복·활동·상처·식사·경고 증상 안내 | 공개 환자교육 문헌을 근거로 한국어로 새로 재구성한 교육 콘텐츠 |
| 환자 D, 58세, 외과병동, 퇴원교육 시나리오 | 모델이 작성한 **100% 가상·합성 데이터**. 실제 환자와 관계없음 |
| 약물 이름·용량, 실제 외래 날짜·연락처 | 임의 생성하지 않음. 실제 의료진의 처방·병원 자료로 확인해야 함 |
| 교육 완료·재설명 요청·Teach-back 체크 | UI 동작을 보여주는 **가상 세션 상태**. 의료기록이 아님 |

## 현재 탑재된 5개 교육 주제

1. **회복과 활동**: 회복 상태에 맞춘 가벼운 걷기와 점진적 활동, 무리한 활동의 재개는 의료진과 확인.
2. **상처 관리**: 봉합 방식에 따른 샤워·드레싱 지시 확인, 탕목욕·수영 주의, 발적·열감·농성 분비물 관찰.
3. **식사와 배변**: 회복기 균형 잡힌 식사, 불편감에 따라 소량씩 먹기, 기름진 음식·지속되는 설사 등 상담.
4. **약 복용과 외래 일정**: 실제 처방전과 병원별 안내에 따라 복용·예약·문의처 확인.
5. **경고 증상**: 발열, 악화되는 복통, 상처 이상, 황달, 음식·수분 섭취 불가능 및 호흡곤란·흉통 등 의료기관 확인이 필요한 증상.

이 콘텐츠는 공개 지침의 핵심을 쉬운 언어로 요약·재구성한 **시연용 초안**으로, 원문을 그대로 전재하지 않았다.

## 시연 링크
- 웹앱 홈: https://pchjesus.github.io/carebridge-edu/
- 전체 교육자료(인쇄/PDF 저장 지원): https://pchjesus.github.io/carebridge-edu/materials/laparoscopic-cholecystectomy-discharge.html

홈의 **환자교육 실제 체험하기**를 누르면 합성사례 환자 D의 5개 교육카드를 바로 시작한다. 간호사 화면에서도 같은 자료의 출처와 전체 교육자료 링크를 확인할 수 있다.

## 중요한 한계
- 개인별 의료진 지침, 수술 결과, 상처 상태, 약물 용량·기간, 퇴원 일정 등은 제공하지 않으며 임의로 생성하지 않는다.
- 실제 의료기관의 교육자료로 사용하려면 해당 진료과·간호부의 의료적 정확성 검토와 기관 승인, 콘텐츠 버전 관리, 환자 접근성 및 사용성 검증이 필요하다.
- 교육자료를 읽은 것과 실제 이해는 다르다. 간호사의 Teach-back 확인을 보조할 뿐 대체하지 않는다.
- **검증된 사실:** 문헌에 언급된 교육 영역과 Teach-back 방식은 공개 근거를 갖는다.
- **아직 검증되지 않은 기대효과:** 교육시간 단축, 간호사 업무부담 감소, 환자 이해도 향상. MVP 자체의 임상 효과 데이터는 없음.

## 근거문헌 (APA 7판)

U.S. National Library of Medicine. (n.d.). *Gallbladder removal – laparoscopic – discharge*. MedlinePlus. https://medlineplus.gov/ency/patientinstructions/000117.htm (페이지 검토일: 2026년 7월 6일)

National Health Service. (n.d.). *Recovering from gallbladder removal*. https://www.nhs.uk/tests-and-treatments/gallbladder-removal/recovery/

Agency for Healthcare Research and Quality. (2024). *Health literacy universal precautions toolkit* (3rd ed.). https://www.ahrq.gov/health-literacy/improve/precautions/toolkit.html
