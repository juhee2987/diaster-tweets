# diaster-tweets

사전학습 언어모델에 따른 트위터 재난 예측 성능 비교했습니다.

BERT, RoBERTa, ALBERT, OpenAI GPT2 모델을 이용했습니다.

데이터 세트  https://www.kaggle.com/c/nlp-getting-started/data

## 코드 수행 과정

### 설치
* transformers

### 필요한 모듈

* numpy
* torch
* time
* pandas
* matplotlib
* seaborn

### tokenizer

from transformers import AutoTokenizer

from transformers.models.auto import AutoModelForSequenceClassification

각 모델의 tokenizer로 전처리를 진행하고 각 모델 성능 결과를 출력했습니다.


## 주요 실험 결과

### 성능 비교 결과

평가 기준은 정확도(accuracy)입니다.

실험 결과, roberta-base가 86.33%으로 높은 성능을 보였습니다. 그 다음은 bert-base-uncased(84.36%)이며, albert-base-v2(84.23%)가 뒤를 이었습니다.

**<표> 모델별 성능 비교**
|Model|Acc(%)|
|:-------------:|:-----:|
|bert-base-uncased|84.36|
|roberta-base|**86.33**|
|roberta-large|83.44|
|albert-base-v2|84.23|
|gpt2|83.7|

### 단어별 재해 확률

추가로 데이터를 통해 어떤 단어가 재해를 가리키는 확률이 높은지 반대로 어떤 단어가 재해를 가리키는 확률이 낮은지 조사했습니다.


* Suggest a Disaster Tweet

![Suggest a Disaster Tweet](https://user-images.githubusercontent.com/96714121/147572294-55fe4390-2d80-4272-8164-980c4bae0124.png)

* Suggest not a Disaster Tweet

![Suggest not a Disaster Tweet](https://user-images.githubusercontent.com/96714121/147572358-d3b9afd8-6be5-4e38-8197-53b89a69a175.png)


