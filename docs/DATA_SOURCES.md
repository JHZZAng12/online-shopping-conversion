# 사용한 데이터와 출처

이번 실습에서는 UCI의 **Online Shoppers Purchasing Intention Dataset**을 사용했습니다. 쇼핑몰 방문 기록과 구매 여부가 담겨 있으며, `Revenue` 열을 정답으로 사용했습니다.

원문 인용 정보는 다음과 같습니다.

Sakar, C. & Kastro, Y. (2018). *Online Shoppers Purchasing Intention Dataset*. UCI Machine Learning Repository. [DOI: 10.24432/C5F88Q](https://doi.org/10.24432/C5F88Q).

[UCI 데이터 소개 페이지](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset)

입력과 정답이 같은 중복 기록은 정리했습니다. `Revenue=True`를 구매(1)로 바꿨고, 예측 시점에 사용할 수 있는지 확실하지 않은 `PageValues`는 입력에서 뺐습니다.

## 데이터를 다시 받는 방법

원본 CSV는 저장소에 올리지 않았습니다. `python src/train.py`를 실행하면 공식 UCI ZIP 파일에서 필요한 CSV를 내려받아 `data/`에 보관합니다. 그다음 실행부터는 받아 둔 파일을 사용합니다.

## 이용 조건

데이터의 라이선스는 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)입니다. 사용할 때는 원저작자와 출처를 밝히고, 데이터를 바꿨다면 그 사실도 알려야 합니다. 이 프로젝트에서는 위에 적은 정리와 변환을 거쳤으며, 보고서·통계·오답 CSV에도 원본 데이터에서 만든 결과가 들어 있습니다. 원저작자가 이 프로젝트나 모델을 보증한다는 뜻은 아닙니다.

## 구현하면서 참고한 문서

- [scikit-learn: 학습 과정에서 데이터를 다룰 때 주의할 점](https://scikit-learn.org/stable/common_pitfalls.html)
- [scikit-learn: 순열 중요도로 모델 해석하기](https://scikit-learn.org/stable/modules/permutation_importance.html)
