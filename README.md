# Yolov5 custom model

## Purpose 
AI pet의 행동에 대한 보상 모델 
- Ai pet의 행동에 대한 반응을 손동작으로 준다. 보상 손동작을 detection 하기 위해 자체적으로 custom 한 yolov5 모델 제작 

240개의 자체 데이터 셋에 대해 labelImg를 사용해 labeling을 진행 

labelImg Github : https://github.com/HumanSignal/labelImg

### Dataset example 

label : ["stop", "nothing", "positive", "negative"]


<img src="https://github.com/gachon-graduation-project/Yolov5-custom-model/assets/105128163/32deabec-9c61-4238-93ce-856e0a592de0" width="400" height="400"/>

Stop 손동작 


<img src="https://github.com/gachon-graduation-project/Yolov5-custom-model/assets/105128163/440a00e5-5b29-4ec5-96eb-af9523bdeadf" width="400" height="400"/>

Nothing 손동작 


<img src="https://github.com/gachon-graduation-project/Yolov5-custom-model/assets/105128163/8cf31579-b3f8-4803-85b6-047e21f4814c" width="400" height="400"/>

Positive 손동작


<img src="https://github.com/gachon-graduation-project/Yolov5-custom-model/assets/105128163/e141f123-d6f8-416b-beed-a096cf17b4f9" width="400" height="400"/>

Negative 손동작


#### training code
```ruby
!python train.py --img 240 --batch 16 --epochs 50 --data /content/YOLO/data.yaml --cfg ./models/yolov5s.yaml --weights yolov5s.pt --name yolo_hand
```
240개 이미지 사용 

Batch size : 16 

Epochs : 50

Weights : yolov5s.pt 
