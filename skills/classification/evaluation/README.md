# Promptfoo를 사용한 평가



### 사전 필요 조건
Promptfoo를 사용하려면 시스템에 node.js와 npm이 설치되어 있어야 합니다. 자세한 내용은 [이 가이드](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)를 따르십시오.

npm을 사용하여 promptfoo를 설치하거나 npx를 사용하여 직접 실행할 수 있습니다. 이 가이드에서는 npx를 사용합니다.

*참고: 이 예제에서는 `npx promptfoo@latest init`을 실행할 필요가 없습니다. 이 디렉토리에 이미 초기화된 `promptfooconfig.yaml` 파일이 있습니다.*

공식 문서는 [여기](https://www.promptfoo.dev/docs/getting-started)에서 확인하십시오.



### 시작하기
평가는 `promptfooconfig.yaml` 파일에 의해 조정됩니다. 이 파일에서 다음 섹션을 정의합니다:

- 프롬프트
    - Promptfoo를 사용하면 다양한 형식으로 프롬프트를 가져올 수 있습니다. 자세한 내용은 [여기](https://www.promptfoo.dev/docs/configuration/parameters)에서 확인할 수 있습니다.
    - 이 예제에서는 `prompts.py` 파일에서 `guide.ipynb`에 사용된 것과 동일한 3개의 프롬프트를 로드합니다:
        - 함수는 Anthropic API를 호출하는 대신 프롬프트만 반환한다는 점을 제외하고 `guide.ipynb`에 사용된 함수와 동일합니다. 그런 다음 Promptfoo는 API 호출 조정 및 결과 저장을 처리합니다.
        - 프롬프트 함수에 대한 자세한 내용은 [여기](https://www.promptfoo.dev/docs/configuration/parameters#prompt-functions)에서 확인할 수 있습니다. 파이썬을 사용하면 RAG에 필요한 VectorDB 클래스를 재사용할 수 있으며, 이는 `vectordb.py`에 정의되어 있습니다.
- 공급자
    - Promptfoo를 사용하면 다양한 플랫폼의 다양한 LLM에 연결할 수 있습니다. 자세한 내용은 [여기](https://www.promptfoo.dev/docs/providers)를 참조하십시오. `guide.ipynb`에서는 기본 온도 0.0으로 Haiku를 사용했습니다. Promptfoo를 사용하여 다양한 온도 설정 배열로 실험하여 사용 사례에 가장 적합한 선택을 식별합니다.
- 테스트
    - `guide.ipynb`에 사용된 것과 동일한 데이터를 사용하며, 이 [Google 시트](https://docs.google.com/spreadsheets/d/1UwbrWCWsTFGVshyOfY2ywtf5BEt7pUcJEGYZDkfkufU/edit#gid=0)에서 찾을 수 있습니다.
    - Promptfoo에는 [여기](https://www.promptfoo.dev/docs/configuration/expected-outputs/deterministic)에서 찾을 수 있는 다양한 내장 테스트가 있습니다.
    - 이 예제에서는 평가 조건이 각 행마다 변경되므로 `dataset.csv`에 테스트를 정의하고 모든 테스트 사례에서 일관된 조건에 대해 `promptfooconfig.yaml`에 테스트를 정의합니다. 자세한 내용은 [여기](https://www.promptfoo.dev/docs/configuration/parameters/#import-from-csv)에서 확인할 수 있습니다.
- 변환
    - `defaultTest` 섹션에서 변환 함수를 정의합니다. 이것은 LLM 응답에서 테스트하려는 특정 출력을 추출하는 파이썬 함수입니다.
- 출력
    - 출력 파일의 경로를 정의합니다. Promptfoo는 다양한 형식으로 결과를 출력할 수 있습니다. [여기](https://www.promptfoo.dev/docs/configuration/parameters/#output-file)를 참조하십시오. 또는 Promptfoo의 웹 UI를 사용할 수 있습니다. [여기](https://www.promptfoo.dev/docs/usage/web-ui)를 참조하십시오.


### 평가 실행

Promptfoo를 시작하려면 터미널을 열고 이 디렉토리(`./evaluation`)로 이동하십시오.

평가를 실행하기 전에 다음 환경 변수를 정의해야 합니다:

`export ANTHROPIC_API_KEY=YOUR_API_KEY`  
`export VOYAGE_API_KEY=YOUR_API_KEY`

`evaluation` 디렉토리에서 다음 명령을 실행하십시오.

`npx promptfoo@latest eval`

요청의 동시성을 높이려면(기본값 = 4) 다음 명령을 실행하십시오.

`npx promptfoo@latest eval -j 25`  

평가가 완료되면 터미널에 데이터 세트의 각 행에 대한 결과가 인쇄됩니다.

이제 `guide.ipynb`로 돌아가서 결과를 분석할 수 있습니다!


