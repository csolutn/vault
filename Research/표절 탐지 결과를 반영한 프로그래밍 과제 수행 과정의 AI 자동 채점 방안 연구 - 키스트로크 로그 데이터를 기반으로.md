
# 연구문제
#### RQ1.  패턴 별 표절 사례분석을 통한  표절 탐지 속성(feature)정량화
* 키스트로크 및 붙여넣기 패턴과 대응되는 사례 연구 --> 적합(내적타당도가 높은)한 속성 산출
* 길이 기반 : pasted 된 content의 길이, typed된 content의 길이, 타이핑 수 등
* 내용 기반 : pasted된 content와 final_code 사이의 교집합 비율
#### RQ2. 복사-붙여넣기(Copy Paste) 유형 표절 탐지 및 검정
* 분류모델1 : 속성값 + 과정 재생을 통한 표절 응답의 지도학습 데이터 생성, ML FP최적화
* 분류모델2. 키스트로크 로우데이터 input을 통한 LLM의 표절확률계산 - 임계값 FP최적화
* 두 분류를 통한 Confusion Matrix를 통한 정확도 계산
#### RQ3.보고 타이핑(mimicking) 유형 표절 탐지 검정
* 정답지가 주어진 과제와 주어지지 않은 과제의 Xms미만(최적화) 타이핑간 latency의 표준편차 t or z검정 분석 (임계도 최적화)
#### RQ4.  자동 채점 모델의 개발과 검정
* 외적 타당도 확보를 위해 성적자료와 상관분석
* S_oj = S
* S_copy = A + (1- C)* S
* S_prag = A + (1-M)* (1-C)* S
* (A: 시도점수 lenlog_norm / M: mimic 여부 /  C: CopyPaste여부 /  S:Success-Unsucces)