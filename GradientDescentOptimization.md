<h3>Coursera Gradient Descent 요약</h3><br>

cost function J(theta)를 최소화하기 위해 기울기(gradient) dJ/d(theta)를 이용하는 방법.<br>
Gradient Descent에서는 theta에 대해 gradient의 반대방향으로 일정크기만큼 이동하는 것을 반복해 J의 값을 최소화하는<br>
theta의 값을 찾는다.<br>
<img width="409" alt="gd2" src="https://user-images.githubusercontent.com/67510613/106354046-575a9180-6332-11eb-8b15-17def693f8b5.PNG"><br>
alpha는 미리 정해진 걸음의 크기로써 '적당한 값'을 선택한다.<br>
cost function을 계산할 때 전체 training set을 사용하는 것을 Batch Gradient Descent라고 한다. <strong> 이때 문제가 발생한다 </strong><br>
이런 계산법이라면 한번 step할때마다 전체 데이터에 대해 cost function을 계산하므로 계산량이 너무 많다. <br>
이를 위한 해결법으로 SGD를 이용한다.<br>

<hr>
<h3>Stochastic Gradient Descent(SGD)</h3><br>
이 방법은 전체 데이터(batch)를 사용하는 대신 랜덤하게 추출한 일부데이터(mini-batch)를 사용한다.<br>
일부 데이터만을 이용하니까 좀 더 부정확할 수는 있는데 계산속도가 훨씬 빠르고 같은 시간에 더 많은 step을 가며,<br>
여러번 반복하면 batch와 유사한 결과로 수렴한다. 또 Batch Descent에서 빠질 local minima에 빠지지 않고 더 좋은 방향으로 수렴할 가능성도 있다.<br>
<img src="http://i.imgur.com/pD0hWu5.gif?1">
