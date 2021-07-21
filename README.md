# vehicle_damage_detection

1-1. annotation for Mask R-CNN (poly)

![image](https://user-images.githubusercontent.com/74915359/126510683-d3cf76d7-31fd-4210-afc7-7ee8e59c344f.png)

1-2. Train & validation

![image](https://user-images.githubusercontent.com/74915359/126510949-df1333b0-44f6-4577-bef3-3e9b46099478.png) ![image](https://user-images.githubusercontent.com/74915359/126510964-494421d3-b67e-4581-b72a-1183695c76c1.png)


1-3. Prediction (Mask R-CNN)

![image](https://user-images.githubusercontent.com/74915359/126511163-df214aec-61cb-4203-9a00-869cee258cb1.png)

2-1. annotation for YOLOv3(box)

![image](https://user-images.githubusercontent.com/74915359/126511515-fde39220-4d6d-45af-8889-782bb5671a2c.png)


2-2. Train & Prediction (YOLOv3)

![image](https://user-images.githubusercontent.com/74915359/126511251-296f89ad-0121-4393-9d65-db1e1f10d1eb.png)


# 평가 및 개선사항
(2021.04.29)
Mask R-CNN으로 학습 및 예측했을 때, 잘 찾아내는 경우도 있었지만 완전히 틀리게 찾아내는 경우도 많았다(특히 scratch와 spacing). 

참조한 글에서 annotation을 poly형태로 했다. 이 때 scratch와 spacing, dent를 내 기준으로 나눴기 때문에 조금 기준이 뚜렷하지 않게 됐을 수도 있다. Annotation 할 때 scratch와 spacing이 헷갈리게 되었기 때문에 성능이 좋지 않았을 것이라는 생각을 했다.

(2021.07.20)
Annotation 방법을 바꿔보고 YOLOv3 모델을 통해 학습시킨 결과 이전에 잘못 예측한 모델에서 정확한 위치에 정확한 class를 예측했다. 하지만 그 아래에 작은 scratch들은 여전히 잡아내지 못했다.

이번 모델은 잘못 예측하는 경우는 적었으나, 아예 찾아내지 못하는 경우는 여전히 있었다.

쏘카는 자체 업로드 받은 사진을 이용했지만 나는 인터넷에 돌아다니는 여러 이미지를 합쳐서 이용했기 때문에 통일성 부분도 문제가 된 것 같다.
