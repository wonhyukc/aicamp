# aicamp

2021년 인공지능 닭장 캠프
 주최: Joy Institute of Technology, Gyeongju City, Korea
시간: 1:30분씩 이틀간
대상: 고등학생
내용: 닭사진에 주석달기->신경망훈련시키기->닭의 동영상을 신경망에 넣어 닭을 검출

닭사진: 100장, 90장은 train, 10장은 평가용
주석달기: makesense.ai 이용
신경망훈련: colab.research.google.com 이용
검출시험용 동영상: mychicken.mp4  


# 사진폴더, 주석폴더 만들때 주의할점
   닭사진화일과 주석화일은 은  다음과 같이 배치하라
   작업폴더에 images와 labels폴더를 만들고
     
     images 폴더 아래 train과 val폴더를 만들라
        train폴더에 90장의 닭사진 화일
        val 폴더 밑에 10장의 닭사진화일을 넣어라
      labels 폴더 아래 train과 val폴더를 만들라
        train폴더에 90장의 주석화일
        val 폴더 밑에 10장의 주석화일을 넣어라
