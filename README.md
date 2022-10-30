# 코드 설명
### movenet.js, angle_extraction.js
데이터셋 추출 때 사용한 코드

### angle_extract.js
skeleton 값을 넣으면 중요 각도를 list로 도출하는 코드<br>
실질적으로 front_end에 사용할 때 해당 js파일을 import 해서 함수 사용하여 각도 계산하면 됨<br>

#### 1. getAngle 함수 
파라미터 3개 <br>
idx = 몇번째 skeleton 데이터인지 인덱싱. 데이터셋의 경우는 구별을 위해 썼음. 화면 부에서는 프레임 구별시 해당 값 사용하면 될듯. <br>
array = movenet 내 skeleton 데이터 <br>
pose_idx = 해당 포즈가 어떤 자세인지 label 정보 <br>
<br>
output<br>
list 형태로 제공 <br>

index 0 : idx 데이터 <br>
index 1 ~ 8 : angle 1부터 8까지 값 <br>
index 9 : 자세 label 정보 <br>

<br><br>


#### 2. ComputeAngle 함수
세 개의 x,y 좌표값을 넣으면 세 점 간 각도를 계산하는 함수 <br>
getAngle 함수에서 사용함 <br>

