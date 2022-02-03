# 2022 Open Frontier Snorkel

![snorkel deep learning - Cheap Online Shopping -](https://www.snorkel.org/doks-theme/assets/images/layout/SnorkelHeader.png)

## Project에서 참여해 볼 수 있는 점들

1. 논문 읽고, 프로젝트 구조 이해
2. 현재의 Labeling 기능 외의 적용할 수 있는 부분들
3. 기존 코드 실습 및 버그 개선
4. maintainer들과의 소통
5. 데이터 수집 모델과 함께 연동해서 쓰면, 사실 사람에 의한 데이터 라벨링이라는 가장 큰 병목 현상을 해소할 수 있는 것 아닌가?
6. Labeling Function과 Generative model을 조합해 사용하면 학습 성능이 개선 되는가?



## 방향성

- 머신러닝 & 딥러닝 분야의 가장 큰 특징은 연구 결과를 공유하는 부분이다.
- 즉, 버그 리포트나 기능 개선만이 오픈 소스 기여점으로 보는 것이 아니다.
  - 예를 들면, Weak Supervision 개념을 도입하고 있는 Snorkel을 이용해 데이터 라벨링을 했을 경우, 특정 분야의 데이터 라벨링에서는 큰 효과를 발휘하는 것을 볼 수 있는데, 다른 분야에서는 동일한 환경 조건에서 되려 성능이 떨어지는 부분들을 발견할 수 있었다.
  - 이를 토대로 ~한 부분에 대해 AI 비즈니스 솔루션이 스노클을 도입할 경우, 라벨링에 투입되는 비용을 많이 개선할 수 있을 것으로 보인다, 등의 리포트를 낼 수 있는 것
  - 즉, ML에서 `Good data for good model` 이라는 하나의 큰 방향에서 Good data를 위한 task에 집중하는 것
- 크래프트 테크놀로지의 면접 결과를 토대로 추측컨데, 주가를 예측하는데 사용되는 강화 학습 모델도 사실은 perfectly하게 라벨링을 사용하지 않는 것은 아니고, semi-supervision 형태의 라벨링은 포함된다고 언급했었다.
- 아직까진 지도 학습이 머신러닝 & 딥러닝의 하나의 큰 흐름인 이상, 국내에서 Snorkel을 연구하는 것은 특정 필드에 많은 영향을 줄 가능성이 높다.
- 지금 기업에서 머신러닝 프로젝트 수행할 때, 가장 병목 현상이 걸리는 단계가 데이터 라벨링(Data Labeling)이다.
  - 머신 러닝은 닭잡는 칼이 아니라 소잡는 칼이다.
  - 때문에 많은 리소스를 필요로 하고, 큰 문제를 해결할 때 필요로하는 기술이라는 것을 알 수 있다.
  - 전반적으로 아직까지는 지도 학습이 머신러닝의 많은 비중을 차지하고 있다.
    - 즉, 모델 학습하는데 있어 데이터 라벨링을 하는 것에 충분히 많은 관심을 가져야하는 이유이기도 하다.



## 목표

![image](https://user-images.githubusercontent.com/40455392/149875071-bcb95db9-756a-4a97-b991-f560e9c66112.png)

- 이 글을 작성하는 2022년 1월 18일 기준 국내에서 Snorkel Project에 대한 글은 50건이 채 안된다.
- 그 마저도 해양 스포츠 "스노클링" 키워드가 걸리는 것이 대다수라, 아직까지는 해외 내용에 비해 자료가 부족하다.
- Weak Supervision에 대한 개념을 조금 더 전파하자. 아직 ML에서 data에 집중해서 연구하는 사례가 국내에 턱없이 부족하다. 



## 진행 일정

스노클에서 제시하는 Case Study별 데이터 라벨링 정확도를 실제 Open dataset을 이용해 라벨링 정확도 검증에 초점을 두고 있음

해당 일정에 집중하는 이유는 국내 기업들이 라벨링에 충분히 많은 물질적, 시간적 비용을 투입하고 있고, 이러한 부분을 해소하기 위한 방편으로 open-dataset을 사용해 모델을 구성하고 있음

그러나 현실은 open-dataset으로 문제 해결이 안되는 경우가 다반사이기 때문에 크라우드 소싱 등 라벨링 업체를 이용하고 있으며, 대체로 6개월 이상의 라벨링 관리 시간이 필요로 하고 있음

국내에서도 인공지능 학습용 데이터 품질 개선에 여러 노력을 기울이고 있고, 분명 그 해답 중 하나로 Snorkel과 같은 소프트웨어가 될 수 있을 것

따라서, 이러한 오픈소스 데이터 라벨링 툴의 국내 활성화 도입이 유의미한 수치상의 결과를 산업 생태계에 제시할 필요가 있음.

​	(특히 국내 기업들 데이터들, 예를 들어, AI 허브에 개방되어 있는 데이터들을 라벨링해주는 방식으로)

Vision / NLP 중심으로 데이터셋 검증 --> 개인적으로 월별로 데이터셋 하나씩 잡아서 라벨링 성능 & 데이터 품질의 정량적인 측정을 중심으로 오픈 프론티어를 진행하면 좋을 것 같다.

버그리포트나 트러블 슈팅, 성능 개선은 부차적인 이슈가 될 것

###3월
* 2 종류 논문의 꼼꼼한 리뷰 및 연구 개발 계획 수립
* Snorkel: Rapid Training Data Creation with Weak Supervision
* End-to-End Weak Supervision
* Snorkel Use Case Intro Dataset 테스트

###4월
* 1 종류 논문의 꼼꼼한 리뷰 및 Labeling 방향성 분석
  * Data Programming: Creating Large Training Set, Quickly
* Snorkel Hybrid Labeling Use Case 분석
* 국내 AI Hub의 K-Fashion 데이터를 토대로 Labeling 되어 있는 데이터와 Sampling을 통한 일부 Labeling이 되어 있지 않는 데이터로 Snorkel Labeling 성능 검증 (국내 데이터로 Hybrid Labeling 성능 검증)
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###5월
* Snorkel Visual Relationship Labeling Use Case 분석
* COCO Dataset 을 이용한 Visual Relationship Labeling 성능 검증
* Faster R-CNN, YOLO 모델 등 다양한 객체 탐지 모델을 통한 성능 검증 진행
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###6월
* 자율 주행 도로 장애물 / 표면 인지 영상(수도권) 데이터를 이용한 Visual Relationship Labeling 성능 검증
* Faster R-CNN, YOLO 모델 등 다양한 객체 탐지 모델을 통한 성능 검증 진행
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###7월
* 1 종류 논문의 꼼꼼한 리뷰 및 Data Augmentation Labeling 방향성 분석
  * Learning to Compose Domain-Specific Transformations for Data Augmentation
* Snorkel Data Augmentation Use Case 분석
* 국/영문 SNS dataset을 토대로 Data Augmentation 부분 Snorkel 성능 검증
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###8월
* 1 종류 논문의 꼼꼼한 리뷰 및 NLP Labeling 방향성 분석
  * Training Classifiers with Natural Language Explanations
* Snorkel NLP Use Case 분석
* 국문 채용 공고를 기반으로한 데이터 라벨링 수행 (채용 공고 업로드 회사들의 채용 데이터 크롤링을 기반으로 수행)
* Naver Deview, pycon 연사 신청
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###9월
* 1 종류 논문의 꼼꼼한 리뷰 및 Multi-Task Labeling 방향성 분석
  * Training Complex Models with Multi-Task Weak Supervision
* Multi-Task Learning Tutorial 수행
* Snorkel 내에서 단일 모델에 대한 Multi-Task 수행 성능 검증 진행
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###10월 (내용 보충 필요)
* Snorkel RecSys Use Case 분석
* Recommender System Public Dataset 중 선택해 Snorkel Labeling 성능 검증 (국내 추천 시스템 관련 공개 데이터셋 부재)
* 실험 데이터 보고서 작성 (실습 환경, 검증 사항, Snorkel / Human-Labeling 성능 비교 등)

###11월 (내용 보충 필요)
* 실험 데이터 보고서 영문 번역 (총 7편)
* Snorkel Team 과 공유 및 향후 방향성 논의 진행

###12월
* Snorkel 데이터 라벨링 연구 개발 보고서 및 국내 도입 시사점 정리
* 최종 성과 공유


## Reference

- [블로그 글 1](https://hoororyn.tistory.com/26)