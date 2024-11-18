*한양대학교 BIS LAB 구성원들과 함께 2021년 한국IT서비스학회 추계학술대회를 위해 진행한 연구입니다.

### 5G와 관련된 기사 분석으로 대중의 인식 파악을 통한 이용률 부진 원인 파악 및 관련 서비스 활성화 전략 수립

5G가 급속도로 활성화 될 것이라는 예상과는 달리 5G의 가입자 수는 왜 늘지 않을까?

전 세계적으로 디지털 전환기에 들어서며 5G의 중요성이 대두되면서 한국이 최초로 5G 상용화에 성공하면서 세계의 주목을 받았지만 한국 5G 가입자는 예상보다 훨씬 더딘 추세를 보이고 있습니다.

이렇게 이용률이 낮은 것에 대한 원인으로 코로나19 확산으로 인한 경기 침체 등의 상황적 요인을 들 수 있지만, 이러한 표면적 원인을 넘어 대중의 인식 분석을 통해 이용률 부진의 근본적 원인을 파악하고자 하는 연구가 부족한 실정입니다.

따라서 본 연구에서는 텍스트 마이닝을 활용하여 5G와 관련된 네이버 기사 분석으로 대중의 인식 파악을 통한 이용률 부진에 대한 원인을 파악하고 5G 관련 서비스를 활성화 하기 위한 전략을 제시하고자 하였습니다.

1. 연구 기획(문제점 수립 및 분석 방법론 선정)
2. 데이터 수집 및 분석
    1. 파이썬의 BeautifulSoup을 활용하여 5G의 상용화 시점인 2018년 12월부터 2021년 7월까지 네이버 기사 126,266건 수집
    (단, 신문이라는 미디어의 보도는 어떤 이슈나 현상에 대해 의미를 부여하는 핵심 프레임을 제공할 수 있다는 점에서 분석 데이터로 활용하고자 하였음)
    2. Konlpy의 Okt를 활용하여 토큰화 및 불용어 제거(해당 도메인에 맞는 사전 수립) 등의 전처리
    3. TF-IDF 및 Wordcloud를 통해 자주 등장하는 단어들의 흐름을 파악하여 단어들이 구분되는(바뀌는) 주요 시기를 이슈가 바뀌는 시기로 정의하고 총 8개로 구분
    4. 구분된 8개의 시기를 LDA를 통해 주요 토픽을 통해 시기별 이슈를 파악
    5. LDA와 더불어 SNA 분석을 통해 해당 시기의 중심 단어(주요 토픽)를 도출하고 단어들 간 연결성을 통해 중심단어의 영향 정도를 파악
 
3. 분석 결과 해석
    - 기간별로 도출된 대중의 인식 흐름을 파악
        - 5G가 상용화된 후 2018년 12월부터 2019년 9월까지는 5G에 대해 대중의 인식이 긍정적
        - 2019년 10월 부터 가격 문제로 부정적 인식이 생김. 이에  2020년 3월 가격을 인하하였지만 부정적 인식이 지속됨
        - 정부가 수도권 편중 현상을 해결하고자 5G 콘텐츠 개발을 본격적으로 진행하면서 긍정적 인식으로 전환됨
        - 하지만 2020년 11월 불법 보조금과 속도 저하 및 연결 지연의 문제로 5G에 대한 대중의 부정적 인식 지속
    - 기사 분석 결과 크게 2가지 문제점을 파악
        - 4가지 5G의 실질적 문제와 3가지 대중의 오인으로 인한 부정적 인식이 있음을 파악
        - 이를 기반으로 활성화 방안을 모색
     
