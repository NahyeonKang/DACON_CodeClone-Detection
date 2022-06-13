# DACON_CodeClone-Detection
![image](https://user-images.githubusercontent.com/24906028/173266030-480a2b5b-8ecc-4e5f-a638-9a0452b60818.png)

데이콘 코드 유사성 판단 AI 경진대회 제출 모델입니다.
https://dacon.io/competitions/official/235900/overview/description

## CodeSimilarityDetection_CreateDataSet
학습 데이터 전처리 파일  
각 코드를 전처리하고 코드 Pair를 생성하는 코드입니다.  
유사도가 낮지만 같은 기능을 수행하는 코드 Pair와 유사도가 높지만 다른 기능을 수행하는 코드 Pair, 즉 높은 난이도의 Positive Pair와 Negative Pair를 학습시키는 것이 좋을 것이라고 예상하였으나  
랜덤으로 구성한 Code Pair의 성능이 더 좋아 해당 방법으로 Code Pair를 구성했습니다.  

## graphcodebert1fold3epochs
Inference에서 보팅 시 여섯번째 모델로 사용된 모델입니다.  
장비 성능과 시간의 한계로 5 fold 중 1 fold만 수행하고 학습을 중단하였습니다.

## graphcodebert5folds1epoch
5 folds 학습과 Inference 및 voting 파일.  
Google Colab 런타임 문제로 Fold 및 Epoch를 cell 단위로 나누어 진행하였습니다.  
시간의 한계로 1 epoch만 진행했습니다.
