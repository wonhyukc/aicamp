# 인공지능 닭장 캠프
![alt text](https://github.com/joyinstech/aicamp/blob/main/ai_chicken_coop_photo_night.jpg)

# 주최

# Joy Institute of Technology, 
   적정기술 연구소, 경주시, 한국

함께하는 사람들

손문탁, JIT, 대표

최혁, JIT

조대연 교수 (한동대)

서용운 교수 (포항대)

박영자 강사 


 ![alt text](https://github.com/joyinstech/aicamp/blob/main/jit_people.png)


# 취지
     
   닭의 일일 평균 행동량을 자동으로 계산해서  농부들에게 전송해주자!

   인공지능 닭장으로 빈곤국 청년들이 인공지능을 재미있게 배울 수 있게 하자!
   
 
# 캠프 내용 

시간: 1:30분씩 이틀간

대상: 고등학생

내용: 닭사진에 주석달기->신경망훈련시키기->닭의 동영상을 신경망에 넣어 닭을 검출

# 캠프 일정
1일차:

닭사진: 100장, 90장은 train, 10장은 평가용

주석달기: makesense.ai 이용

2일차:

신경망훈련: colab.research.google.com 이용

검출시험용 동영상으로 신경망 평가: mychicken.mp4  


![alt text](https://github.com/joyinstech/aicamp/blob/main/flowchart_1.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/dataset_structure.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/anotation_file_inside.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/yolov5s_pt.png)

# YOLO는 무엇인가

https://www.youtube.com/watch?v=Cgxsv1riJhI


# YOLO는 무서우리만큼 빠르고 정확하게 이미지 속의 객체를 검출한다

https://www.youtube.com/watch?v=XS2UWYuh5u0


# YOLO를 사용하면 인공지능 닭장을 만들 수 있다

https://www.youtube.com/watch?v=GRtgLlwxpc4

# 음베일 마을 '나지리니'의 옥수수 해충 검출기 

![alt text](https://github.com/joyinstech/aicamp/blob/main/nanzirini.png)

http://www.sciengineer.or.kr/board_Tqqc07/24029


# 주석달기 작업
1. 조를 편성.
2. 각조에 100장의 사진을 나누어준다
3. 90장과 10장으로 분류
4. 90장을 images폴더 아래 train폴더에 넣어줌
5. 10장을 images폴더 밑에 val폴더에 넣어줌
6. makesense.ai 사이트로 가서 시작하기 버튼
7. 90장의 사진을 모두 선택하여 makesense.ai의 드롭박스에 던져주라
8. 라벨을 새로 만들어 chicken이라고 이름을 붙이고
9. 90장의 사진에 대해 바운딩박스를 그려서 주석작업을 하라
10. actions메뉴를 클릭하고 export 를 선택. 
11. 주석화일 포맷은 YOLO로 지정
12. export를 마치면 90장개으 주석화일(화일이름.txt)가 압축되어 내려온다
13. 이 압축파일을 labels 폴더 밑에 train폴더에 풀어라
14. 7,8,9,10,11,12 단계를 10장의 사진에 대해 반복하라
15. 이 화일을 labels 폴더밑에 val폴더에 풀어라
16. images와 labels를 한데 묶어 압축화일로 만들어라
17. 이 압축화일의 이름을 chicken_dataset.zip이라고 변경하라

# 신경망 훈련

1. 각 조마다 colab.research.google.com 에 로그인하라
2. 이 깃헙의 aicamp의 콜랩노트북 을 클릭하여 노트북을 열어라

4. 파일메뉴에가서 내드라이브에 사본만들기를 하라
5. 그 사본을 열고 원본노트북은 닫아라
6. 1단계 YOLO다운로드 버튼을 클릭
7. 전단계에서 만든 chicken_dataset.zip을 PC에서 콜랩으로 업로드하라 (드랙앤드롭으로)
8. 2단계 압축풀기 버튼을 클릭
9. aicamp의 chicken.yaml을 yolov5 폴더의 data폴더에 업로드 하라(드랙앤드롭)
10. 3단계  신경망 훈련 버튼을 클릭
11. 신경망이 자동으로 훈련되기 시작한다
12. 10분정도 시간이 흐르면 훈련이 완료된다 (mAP값이 얼마인지 확인 0.9이상이 되어야 함)
13. runs폴더에 가서 훈련 결과를 확인
14. 평가용사진을 클릭하면 신경망이 원본사진에 닭의 위치에 바운딩박스를 그려준것이 확인됨 
# 신경망 추론
1. mychicken.mp4화일을 콜랩의 업로드 (드랙앤드롭)
2.4단계 추론버튼을 누른다
3. 신경망이 닭의 동영상 화일을 열어 매 프레임마다 닭을 검출하여 바운딩 박스를 그려준다
4. 이 결과화일을 PC로 다운로드
5. PC에서 이 화일을 플레이해본다
# 토론 및 종료
1. 다음주제에 대해 토론해본다
2. 신경망이 정확하게 추론하려면 어떤점을 보완해야 할까?
3. 신경망이 생성한 정보를 일상생활에성 용하게 사용하려면 어떤 기술이 더 추가되어야 할까?
4. 캠프에서 배운 지식을 응용하여 발명하고 싶은 장치나 서비스는 무엇인가?


# 사진폴더, 주석폴더 만들때 주의할점
   닭사진화일과 주석화일은 은  다음과 같이 배치하라
   작업폴더에 images와 labels폴더를 만들고
     
     images 폴더 아래 train과 val폴더를 만들라
        train폴더에 90장의 닭사진 화일
        val 폴더 밑에 10장의 닭사진화일을 넣어라
      labels 폴더 아래 train과 val폴더를 만들라
        train폴더에 90장의 주석화일
        val 폴더 밑에 10장의 주석화일을 넣어라

![alt text](https://github.com/joyinstech/aicamp/blob/main/chicken_coop_sideview.png)


![alt text](https://github.com/joyinstech/aicamp/blob/main/ai_chicken_coop_photo_ceiling.jpg)


![alt text](https://github.com/joyinstech/aicamp/blob/main/mychicken_boundingbox.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/chicken_activity_board.png)



# [주석작업 절차]

![alt text](https://github.com/joyinstech/aicamp/blob/main/1000_chicken_image.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/image_separation.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/labeling.png)






![alt text](https://github.com/joyinstech/aicamp/blob/main/90-10_images.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/makesensor_click.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/drag_n_drop_90_photos.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/click_label_list.png)


![alt text](https://github.com/joyinstech/aicamp/blob/main/create_chicken_label.png)



![alt text](https://github.com/joyinstech/aicamp/blob/main/labeling_multi_chicken.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/export_annotation.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/select_yolo_format.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/download_annotation.png)

# [신경망 훈련 절차]
구글에서 만든 콜랩(Colab)을 활용해서 신경망 훈련시키는 과정을 화면 중심으로 프로세스를 설명하겠습니다.


# 콜랩으로 가서 주피터노트북 열기

![alt text](https://github.com/joyinstech/aicamp/blob/main/open_nb.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/from_githun_to_colab.png)


# 파일매니저 열기

![alt text](https://github.com/joyinstech/aicamp/blob/main/open_file_manager.png)


# 데이터셋 업로드

![alt text](https://github.com/joyinstech/aicamp/blob/main/drag_n_drop.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/dataset_upload.png)


# 1단계 YOLO 다운로드 받기


# 2단계 데이터셋 압축 풀기
![alt text](https://github.com/joyinstech/aicamp/blob/main/unzip.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/refresh.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/check_images_labeles.png)


# 데이터셋의 경로 화일을 수정하고 이름 바꾸기

![alt text](https://github.com/joyinstech/aicamp/blob/main/open_coco218.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/erase_coco128.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/edit_coco128.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/change_name.png)



# 드디어 신경망을 훈련시키자

![alt text](https://github.com/joyinstech/aicamp/blob/main/train.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/check_train.png)



# 닭을 잘 검출 하는지 알아보라 

![alt text](https://github.com/joyinstech/aicamp/blob/main/down_prediction_video.png)


# 훈련된 신경망을 닭장의 동영상으로 시험해보자



# 닭장에 가서 동영상을 찍어오라



# 동영상을 콜랩에 업로드 하라

![alt text](https://github.com/joyinstech/aicamp/blob/main/upload_chicken_video.png)



# 동영상의 경로를 클립보드로 복사

![alt text](https://github.com/joyinstech/aicamp/blob/main/copy_chicken_video_path.png)


# 신경망의 경로를 클립보드로 복사

![alt text](https://github.com/joyinstech/aicamp/blob/main/copy_model_path.png)


# 신경망의 경로, 동영상의 경로를 붙여 넣어라

![alt text](https://github.com/joyinstech/aicamp/blob/main/paste_model_and_video.png)



# 두둥,, 진실의 순간 ... 동영상속의 닭이 잘  검출되었는가?

![alt text](https://github.com/joyinstech/aicamp/blob/main/prediction.png)

![alt text](https://github.com/joyinstech/aicamp/blob/main/prediction_result.png)

# 바운딩박스가 붙은 동영상을 다운받자

![alt text](https://github.com/joyinstech/aicamp/blob/main/down_prediction_video.png)

# 닭 검출기의 성능을 확인하라

https://youtu.be/JMpAo1GysWc





