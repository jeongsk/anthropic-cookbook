# Anthropic Cookbook (앤스로픽 쿡북)

앤스로픽 쿡북은 개발자들이 클로드를 사용하여 구축하는 데 도움이 되도록 설계된 코드와 가이드를 제공하며, 복사하여 자신의 프로젝트에 쉽게 통합할 수 있는 코드 스니펫을 제공합니다.

## Prerequisites (사전 필요 조건)

이 쿡북의 예제를 최대한 활용하려면 앤스로픽 API 키가 필요합니다 ([여기](https://www.anthropic.com)에서 무료로 가입하세요).

코드 예제는 주로 파이썬으로 작성되었지만, 개념은 앤스로픽 API와의 상호 작용을 지원하는 모든 프로그래밍 언어에 적용될 수 있습니다.

앤스로픽 API 작업이 처음이라면, 탄탄한 기초를 다지기 위해 [앤스로픽 API 기초 과정](https://github.com/anthropics/courses/tree/master/anthropic_api_fundamentals)부터 시작하는 것이 좋습니다.

## Explore Further (더 살펴보기)

클로드 및 AI 어시스턴트 경험을 향상시키기 위한 더 많은 리소스를 찾고 계신가요? 다음 유용한 링크를 확인하세요:

- [Anthropic developer documentation (앤스로픽 개발자 문서)](https://docs.anthropic.com/claude/docs/guide-to-anthropics-prompt-engineering-resources)
- [Anthropic support docs (앤스로픽 지원 문서)](https://support.anthropic.com)
- [Anthropic Discord community (앤스로픽 디스코드 커뮤니티)](https://www.anthropic.com/discord)

## Contributing (기여하기)

앤스로픽 쿡북은 개발자 커뮤니티의 기여로 번창합니다. 아이디어 제출, 오타 수정, 새 가이드 추가 또는 기존 가이드 개선 등 여러분의 의견을 소중하게 생각합니다. 기여를 통해 이 리소스를 모든 사람에게 더욱 가치 있게 만들 수 있습니다.

중복 작업을 피하기 위해 기여하기 전에 기존 이슈와 풀 리퀘스트를 검토해 주세요.

새로운 예제나 가이드에 대한 아이디어가 있다면 [이슈 페이지](https://github.com/anthropics/anthropic-cookbook/issues)에서 공유해 주세요.

## Table of recipes (레시피 목록)

### Skills (기술)
- [Classification (분류)](https://github.com/anthropics/anthropic-cookbook/tree/main/skills/classification): 클로드를 사용한 텍스트 및 데이터 분류 기술을 살펴보세요.
- [Retrieval Augmented Generation (검색 증강 생성)](https://github.com/anthropics/anthropic-cookbook/tree/main/skills/retrieval_augmented_generation): 외부 지식으로 클로드의 응답을 향상시키는 방법을 알아보세요.
- [Summarization (요약)](https://github.com/anthropics/anthropic-cookbook/tree/main/skills/summarization): 클로드를 사용한 효과적인 텍스트 요약 기술을 알아보세요.

### Tool Use and Integration (도구 사용 및 통합)
- [Tool use (도구 사용)](https://github.com/anthropics/anthropic-cookbook/tree/main/tool_use): 클로드의 기능을 확장하기 위해 외부 도구 및 기능과 통합하는 방법을 알아보세요.
  - [Customer service agent (고객 서비스 에이전트)](https://github.com/anthropics/anthropic-cookbook/blob/main/tool_use/customer_service_agent.ipynb)
  - [Calculator integration (계산기 통합)](https://github.com/anthropics/anthropic-cookbook/blob/main/tool_use/calculator_tool.ipynb)
  - [SQL queries (SQL 쿼리)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/how_to_make_sql_queries.ipynb)

### Third-Party Integrations (타사 통합)
- [Retrieval augmented generation (검색 증강 생성)](https://github.com/anthropics/anthropic-cookbook/tree/main/third_party): 외부 데이터 소스로 클로드의 지식을 보강하세요.
  - [Vector databases (Pinecone) (벡터 데이터베이스 (Pinecone))](https://github.com/anthropics/anthropic-cookbook/blob/main/third_party/Pinecone/rag_using_pinecone.ipynb)
  - [Wikipedia (위키백과)](https://github.com/anthropics/anthropic-cookbook/blob/main/third_party/Wikipedia/wikipedia-search-cookbook.ipynb/)
  - [Web pages (웹 페이지)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/read_web_pages_with_haiku.ipynb)
  - [Internet search (Brave) (인터넷 검색 (Brave))](https://github.com/anthropics/anthropic-cookbook/blob/main/third_party/Brave/web_search_using_brave.ipynb)
- [Embeddings with Voyage AI (Voyage AI를 사용한 임베딩)](https://github.com/anthropics/anthropic-cookbook/blob/main/third_party/VoyageAI/how_to_create_embeddings.md)

### Multimodal Capabilities (멀티모달 기능)
- [Vision with Claude (클로드를 사용한 비전)](https://github.com/anthropics/anthropic-cookbook/tree/main/multimodal):
  - [Getting started with images (이미지 시작하기)](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/getting_started_with_vision.ipynb)
  - [Best practices for vision (비전 모범 사례)](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/best_practices_for_vision.ipynb)
  - [Interpreting charts and graphs (차트 및 그래프 해석)](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/reading_charts_graphs_powerpoints.ipynb)
  - [Extracting content from forms (양식에서 콘텐츠 추출)](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/how_to_transcribe_text.ipynb)
- [Generate images with Claude (클로드를 사용하여 이미지 생성)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/illustrated_responses.ipynb): 이미지 생성을 위해 스테이블 디퓨전과 함께 클로드를 사용하세요.

### Advanced Techniques (고급 기술)
- [Sub-agents (하위 에이전트)](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/using_sub_agents.ipynb): Opus와 함께 Haiku를 하위 에이전트로 사용하는 방법을 알아보세요.
- [Upload PDFs to Claude (클로드에 PDF 업로드)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/pdf_upload_summarization.ipynb): PDF를 파싱하여 텍스트로 클로드에 전달하세요.
- [Automated evaluations (자동 평가)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/building_evals.ipynb): 클로드를 사용하여 프롬프트 평가 프로세스를 자동화하세요.
- [Enable JSON mode (JSON 모드 활성화)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/how_to_enable_json_mode.ipynb): 클로드에서 일관된 JSON 출력을 보장하세요.
- [Create a moderation filter (중재 필터 만들기)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/building_moderation_filter.ipynb): 클로드를 사용하여 애플리케이션용 콘텐츠 중재 필터를 만드세요.
- [Prompt caching (프롬프트 캐싱)](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/prompt_caching.ipynb): 클로드를 사용한 효율적인 프롬프트 캐싱 기술을 알아보세요.

## Additional Resources (추가 리소스)

- [Anthropic on AWS (AWS의 앤스로픽)](https://github.com/aws-samples/anthropic-on-aws): AWS 인프라에서 클로드를 사용하기 위한 예제 및 솔루션을 살펴보세요.
- [AWS Samples (AWS 샘플)](https://github.com/aws-samples/): 클로드와 함께 사용하도록 수정할 수 있는 AWS의 코드 샘플 모음입니다. 일부 샘플은 클로드와 최적으로 작동하도록 수정해야 할 수 있습니다.