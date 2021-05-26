# 2021년 인공지능 닭장 캠프
![alt text](https://github.com/joyinstech/aicamp/blob/main/ai_chicken_coop_photo_night.jpg)

# 주최

Joy Institute of Technology, Gyeongju City, Korea

함꼐하는 사람들

   손문탁 (Ph.D. JIT President)
   
   최혁 (JIT coordinator), 
   
   조대연(Professor, AI & Coding)
   
   장수영(Professor, master planner)


# 취지
   인공지능기술로  닭의 행동을 관찰하는 방법을 청소년들에게 가르치자!
   
 
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

1. 각 조마다 colab.google.research.com에 로그인하라
2. 이 깃헙의 aicamp의 콜랩노트북 을 클릭하여 노트북을 열어라
3. 파일메뉴에가서 내드라이브에 사본만들기를 하라
4. 그 사본을 열고 원본노트북은 닫아라
5. 1단계 YOLO다운로드 버튼을 클릭
6. 전단계에서 만든 chicken_dataset.zip을 PC에서 콜랩으로 업로드하라 (드랙앤드롭으로)
7. 2단계 압축풀기 버튼을 클릭
8. aicamp의 chicken.yaml을 yolov5 폴더의 data폴더에 업로드 하라(드랙앤드롭)
9. 3단계  신경망 훈련 버튼을 클릭
10. 신경망이 자동으로 훈련되기 시작한다
11. 10분정도 시간이 흐르면 훈련이 완료된다 (mAP값이 얼마인지 확인 0.9이상이 되어야 함)
12. runs폴더에 가서 훈련 결과를 확인
13. 평가용사진을 클릭하면 신경망이 원본사진에 닭의 위치에 바운딩박스를 그려준것이 확인됨 
# 신경망 추론
1. mychicken.mp4화일을 콜랩의 업로드 (드랙앤드롭)
2.4단계 추론버튼을 누른다
3. 신경망이 닰의 동영상 화일을 열어 매 프레임마다 닭을 검출하여 바운딩 박스를 그려준다
4. 이 결과화일을 PC로 다운로드
5. PC에서 이 화일을 플레이해본다
# 토론 및 종료
1. 다음주제에 대해 토론해본다
2. 신경망이 정확하게 추론하려면 어떤점을 보완해야 할까?
3. 신경망이 생성한 정보를 일상생활에성 ㅠ용하게 사용하려면 어떤 기술이 더 추가되어야 할까?
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
