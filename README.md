# Data_Pipeline
![image](https://github.com/seanshlee/Data_Pipeline/assets/61730984/25c2a986-eb41-417b-a8f1-999de36fd7e0)

유튜브 영상을 올린 후 반응을 모니터링하는 서비스를 만들기 위한 더미 파이프라인입니다. 
- Youtube API를 사용하여 댓글 내용, 작성자, 작성 시간, 좋아요 수를 수집하여 로컬 PC에 저장(csv or excel)
- 수집 데이터를 aws s3에 저장
- hdfs로 데이터 전송
- hive에서 2가지 작업 병렬 처리 
(1. 댓글 키워드분석, 딥러닝 모델 활용 댓글 감성 분류 등 NLP 작업 / 2. 좋아요 수 순으로 정렬하여 Top100 comments 추출)
- 작업한 파일을 다시 hdfs 로 전송
