This directory includes a few sample datasets to get you started.

*   `california_housing_data*.csv` is California housing data from the 1990 US
    Census; more information is available at:
    https://docs.google.com/document/d/e/2PACX-1vRhYtsvc5eOR2FWNCwaBiKL6suIOrxJig8LcSBbmCbyYsayia_DvPOOBlXZ4CAlQ5nlDD8kTaIDRwrN/pub

*   `mnist_*.csv` is a small sample of the
    [MNIST database](https://en.wikipedia.org/wiki/MNIST_database), which is
    described at: http://yann.lecun.com/exdb/mnist/

*   `anscombe.json` contains a copy of
    [Anscombe's quartet](https://en.wikipedia.org/wiki/Anscombe%27s_quartet); it
    was originally described in

    Anscombe, F. J. (1973). 'Graphs in Statistical Analysis'. American
    Statistician. 27 (1): 17-21. JSTOR 2682899.

    and our copy was prepared by the
    [vega_datasets library](https://github.com/altair-viz/vega_datasets/blob/4f67bdaad10f45e3549984e17e1b3088c731503d/vega_datasets/_data/anscombe.json).

[분석 요약 보고서]
본 분석은 항체 고생산 및 저생산 CHO 세포주의 유전자 발현 데이터를 비교하여 중요한 차이를 보이는 유전자를 식별하는 것을 목표로 합니다.

1. 데이터 개요
데이터셋: GSE57023 (항체 고생산/저생산 CHO 세포주 비교)
총 샘플 수: 15개 (고생산 샘플 6개, 저생산 샘플 6개)
정규화 후 유전자 수: 226개 (저발현 유전자 필터링 완료)
2. 차등 발현 유전자 (DEG) 분석 결과
분석 기준:
Fold Change (log2) 절대값 > 0.3
p-value < 0.05
유의미한 차등 발현 유전자 수: sig DataFrame에서 총 {{len(sig)}}개의 유전자가 확인되었습니다.
3. 주요 차등 발현 유전자
고생산군에서 발현 증가 (Up-regulated) 유전자 (상위 3개):

{{sig.head(3).to_string(index=False)}}
고생산군에서 발현 감소 (Down-regulated) 유전자 (상위 3개):

{{sig.tail(3).to_string(index=False)}}
4. 시각화 요약
히트맵: 상위 30개 차등 발현 유전자의 샘플별 발현 패턴을 시각화하여 두 그룹 간의 명확한 차이를 보여줍니다.
화산 그래프: 모든 유전자의 Fold Change와 p-value 관계를 한눈에 보여주며, 유의미한 차등 발현 유전자들을 시각적으로 강조합니다.
5. 결론
이번 분석을 통해 항체 생산 능력에 따라 CHO 세포주에서 유의미한 발현 차이를 보이는 유전자들을 식별했습니다. 이들 유전자는 항체 생산성 향상을 위한 추가 연구의 잠재적 타겟이 될 수 있습니다.
