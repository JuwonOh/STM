# STM

## Introduction

- 본 자료는 R에서 제공하는 Topic modeling 기법인 STM(Structural Topic Model)을 이용하여, 미국의 씽크탱크들의 글들을 살펴본 것이다. Topic modeling을 통해 각 씽크탱크들이 작성한 글의 주제와 핵심 어휘, 주제들 사이의 관계, 그리고 시간의 흐름에 따라 글의 주제들이 어떻게 변화하는지를 살펴보기 위해 작성되었다.
- STM은 문서 단위의 covariate information를 이용한 topic modeling이다. LDA(Latent Dirichlet Allocation)와 유사하게, STM 역시 주어진 문서에 대해서 각 문서에 어떤 주제들이 존재하는지 확률적으로 제시하여 토픽별 단어의 분포와 문서별 토픽의 분포를 보여준다. STM은 기존의 LDA에 문서의 추가적인 meta 정보들 사이의 관계를 예측하게 만든다. 이 과정에서 STM은 topical prevalence와 topical content의 covariate를 사용한다. topical prevalence covariant는 한 문서가 한 토픽과 어떤 관련성을 가지고 있는가를 의미한다. topical content의 covariant는 메타데이터가 특정 토픽내의 단어 사용비율에 영향을 미친다. STM은 이 두가지 메카데이터의 covariate를 통해서 토픽을 예측한다.(Roberts, M. E., Stewart, B. M., & Tingley, D. 2014)

## Data

- 사용된 데이터들은 미국의 주요 씽크탱크들의 blog, article, news를 crawling 한 것이다. crawling 기간은 1차 북미정상회담과 2차 북미정상회담 사이인 2018년 7월 1일부터 2019년 3월 10일까지이다. 
- 선택된 씽크탱크는 38 North, Stimson Center, Center for Strategic and International Studies, Cato Institute, Brookings Institution, RAND Corporation, Human Rights Watch, Freedom House, Bipartisan Policy Center, Center for a New American Security, Heritage Foundation, Woodrow Wilson International Center for Scholar로 총 12개이다. 
- 씽크탱크를 크롤링한 코드와 예시는 전부 github(https://github.com/JuwonOh)에 올라와 있다. 
- 실제 Rmarkdown을 사용한 결과는 rpubs에서 보실 수 있습니다.
