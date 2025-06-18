
# Promptfoo를 사용한 평가

### 이 평가 제품군에 대한 참고 사항

1) 아래 지침, 특히 필수 패키지에 대한 사전 필요 조건을 반드시 따르십시오.

2) 전체 평가 제품군을 실행하려면 평소보다 높은 속도 제한이 필요할 수 있습니다. promptfoo에서 테스트의 하위 집합만 실행하는 것을 고려하십시오.

3) 모든 테스트가 즉시 통과하는 것은 아닙니다. 평가는 적당히 어렵게 설계되었습니다.

### 사전 필요 조건
Promptfoo를 사용하려면 시스템에 node.js와 npm이 설치되어 있어야 합니다. 자세한 내용은 [이 가이드](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)를 따르십시오.

npm을 사용하여 promptfoo를 설치하거나 npx를 사용하여 직접 실행할 수 있습니다. 이 가이드에서는 npx를 사용합니다.

*참고: 이 예제에서는 `npx promptfoo@latest init`을 실행할 필요가 없습니다. 이 디렉토리에 이미 초기화된 `promptfooconfig.yaml` 파일이 있습니다.*

공식 문서는 [여기](https://www.promptfoo.dev/docs/getting-started)에서 확인하십시오.

### 시작하기

시작하려면 ANTHROPIC_API_KEY 환경 변수 또는 선택한 공급자에 필요한 기타 키를 설정하십시오. `export ANTHROPIC_API_KEY=YOUR_API_KEY`를 수행할 수 있습니다.

그런 다음 `evaluation` 디렉토리로 `cd`한 후 `npx promptfoo@latest eval -c promptfooconfig.yaml --output ../data/results.csv`를 작성하십시오.

그런 다음 `npx promptfoo@latest view`를 실행하여 결과를 볼 수 있습니다.

### 작동 방식

promptfooconfig.yaml 파일은 평가 설정의 핵심입니다. 몇 가지 중요한 섹션을 정의합니다:

프롬프트:
- 프롬프트는 prompts.py 파일에서 가져옵니다.
- 이러한 프롬프트는 LM 성능의 다양한 측면을 테스트하도록 설계되었습니다.

공급자:
- 여기서 사용 중인 클로드 모델을 구성합니다.

테스트:
- 테스트 사례는 여기에 정의됩니다.
- 이러한 테스트는 평가를 위한 입력 및 예상 출력을 지정합니다.
- Promptfoo는 다양한 기본 제공 테스트 유형을 제공하거나(문서 참조) 직접 정의할 수 있습니다.

출력:
- 평가 결과의 형식과 위치를 지정합니다.
- Promptfoo는 다양한 출력 형식도 지원합니다!

### 파이썬 바이너리 재정의

기본적으로 promptfoo는 셸에서 파이썬을 실행합니다. 파이썬이 적절한 실행 파일을 가리키도록 하십시오.

파이썬 바이너리가 없으면 "python: command not found" 오류가 표시됩니다.

파이썬 바이너리를 재정의하려면 PROMPTFOO_PYTHON 환경 변수를 설정하십시오. 경로(/path/to/python3.11 등) 또는 PATH의 실행 파일(python3.11 등)로 설정할 수 있습니다.