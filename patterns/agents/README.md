# 효과적인 에이전트 구축 쿡북

Erik Schluntz와 Barry Zhang의 [효과적인 에이전트 구축](https://anthropic.com/research/building-effective-agents)을 위한 참조 구현입니다.

이 저장소에는 블로그에서 논의된 일반적인 에이전트 워크플로우의 최소한의 예제 구현이 포함되어 있습니다:

- 기본 구성 요소
  - 프롬프트 체이닝
  - 라우팅
  - 다중 LLM 병렬화
- 고급 워크플로우
  - 오케스트레이터-하위 에이전트
  - 평가자-최적화기

## 시작하기
자세한 예제는 Jupyter 노트북을 참조하세요:

- [기본 워크플로우](basic_workflows.ipynb)
- [평가자-최적화기 워크플로우](evaluator_optimizer.ipynb)
- [오케스트레이터-작업자 워크플로우](orchestrator_workers.ipynb)