<h3>Gradient Descent</h3><br>

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
위는 SGD와 그 변형들이다. Momentum만 추가적으로 살펴볼것임.<br>
<br>
<h3>Momentum</h3><br>
경사 하강법과 마찬가지로 매번 기울기를 구하지만, 이를 통해 오차를 수정하기 전에<br>
바로 앞 수정 값과 방향(+, -)을 참고하여 같은 방향으로 일정한 비율만 수정되게 하는 방법이다.<br>
현재 Gradient를 통해 이동하는 방향과 별개로 과거에 이동했던 방식을 기억하면서 그 방향으로 일정정도를 추가적으로 이동한다고 보면 될듯.<br>
<img width="263" alt="momentum" src="https://user-images.githubusercontent.com/67510613/106354990-c4712580-6338-11eb-8e90-46199462d06b.PNG">
vt는 time step t에서의 이동벡터, gamma는 얼마나 momentum을 줄건지에 대한 term으로 보통 0.9정도 줌, <br><br>
둘의 차이를 한번 보자.
<img width="314" alt="sgdshit" src="https://user-images.githubusercontent.com/67510613/106355121-685ad100-6339-11eb-8530-a4c862ff5c39.PNG">
<img width="314" alt="momentumcool" src="https://user-images.githubusercontent.com/67510613/106355124-6abd2b00-6339-11eb-891b-52dc07ab22fb.PNG">
<img width="335" alt="momentumlomin" src="https://user-images.githubusercontent.com/67510613/106355229-ff278d80-6339-11eb-94d8-af37e8c6ffbe.PNG">
<br>진동을 하더라도 중앙으로 가는 방향으로 관성이 걸려 더 빠르게 갈 수있다.<br><br>local minima를 빠져나오는 효과도 있다.<br>
<img width="335" alt="momentumlomin" src="https://user-images.githubusercontent.com/67510613/106355229-ff278d80-6339-11eb-94d8-af37e8c6ffbe.PNG">



