# Image Classification Pipeline Project

![image](https://user-images.githubusercontent.com/59557720/161180827-47c6a0cc-47ab-4877-9788-bebd501f5549.png)

## __[포스터 발표 pdf](https://drive.google.com/file/d/1MXJkpX0EzgkuRKZ0-JHrRKQlKcId01PC/view?usp=sharing)__   
> CNN 분류 모델의 유명한 실습인 개-고양이를 이진 분류하는 매우 간단한 예제만으로는 부족함을 느꼈습니다.
>    
> 따라서 직접 크롤링하여 얻은 위 이미지 dolphin, shark, whale 3가지 동물을 분류하는 프로젝트를 아래 과정대로 진행하였습니다.   
>   
> 개인적인 프로젝트였지만 교수님의 제안으로 학부에서 진행하는 __포스터 발표회에서 발표를 하게 되었습니다.__    

혼자서 이미지 수집부터 모델 설계까지 전체를 경험했기에 몰랐던 기술들이나 지식들을 습득하는 좋은 기회였습니다.   
colab으로 진행하였기 때문에 좀 더 좋은 장비가 있는 곳에서 쾌적한 프로젝트 & 실험을 해보고 싶은 욕심이 생겼습니다.   

--------------------------------------------------------------------------------------------------------------------------------------
## 진행 과정
__[전 과정 블로그 포스팅](https://inhovation97.tistory.com/category/Project/Image%20Classification%20Pipeline%20Project)__   
1. 크롤링을 통한 이미지 수집   
2. 이미지 전처리   
3. Transfer Learning & Fine tuning ResNet50   
4. 안정적인 학습을 위한 more Fine tuning을 적용   

## 얻을 수 있었던 결과들
#### 1. Augmentation의 효과
![image](https://user-images.githubusercontent.com/59557720/161185001-9e1431a0-4f1e-4177-8681-b2270d6ee1ba.png)
+ transfer learning을 진행하기 전, Augmentation의 효과를 직접 느껴보고 싶었습니다.   
+ 아주 간단한 Augmentation을 진행한 데이터셋 A & 강력한 Augmentation을 진행한 데이터셋 B를 만들고 이를 성능 비교한 결과   
+ 학습의 당락 여부를 결정할 정도로 강력한 Augmentation의 영향을 경험하였습니다.   

#### 2. 섬세한 fine tuning
![image](https://user-images.githubusercontent.com/59557720/161186146-ea7e97b7-8397-495e-a1d1-40d8980ccaa9.png)
+ fc layer를 튜닝한 뒤 바로 전체 네트웍을 학습하지 않고, fc layer만을 한 번 학습한 뒤 최종적으로 전체 네트웍을 trainable하게 만들어 학습을 진행. [code](https://github.com/inhovation97/personal_project/blob/main/pytorch/pytorch_project_fine_tuning.ipynb)   
### 최종적으로 92.4%의 분류 모델을 설계할 수 있었습니다.
