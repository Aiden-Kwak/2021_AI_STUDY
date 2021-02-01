<strong>1. 머신러닝을 어떻게 정의할 수 있는가?</strong><br>
머신러닝은 데이터로부터 학습할 수 있는 시스템을 만드는 것. 학습이란 어떤 작업에서 주어진 성능지표가 더 나아지는 것을 의미함.<br>
<strong>2. 머신러닝이 도움을 줄 수 있는 문제유형 네 가지</strong><br>
명확한 해결책이 없는 복잡한 문제, 수작업으로 만든 긴 규칙 리스트를 대체하는 경우, 변화하는 환경에 적응하는 시스템을 만드는 경우, 사람에게 통찰을 제공하는 경우(데이터마이닝)
<strong>3. 레이블 된 훈련세트란?</strong><br>
각 샘플에 대해 원하는 정답(레이블)을 담고있는 훈련세트<br>
<strong>4. 가장 널리 사용되는 지도학습 작업 두가지</strong><br>
regression, classification<br>
<strong>5. 보편적인 비지도학습 작업 네가지</strong><br>
clustering, visualization, dimensionality reduction, Association rule learning<br>
<strong>6. 사전정보가 없는 여러 지형에서 로봇을 걸어가게 하려면 어떤 종류의 머신러닝 알고리즘을 사용할수 있는가</strong><br>
강화학습. <br>
<strong>7. 고객을 여러그룹으로 분할하려면 어떤 알고리즘을 사용해야하는가</strong><br>
그룹을 어떻게 정의할지 모를경우엔: clustering algorithm(Unsupervised learning <br>
아는 경우엔: classification(Supervised learning)<br>
<strong>8. 스팸감지의 문제는 지도학습과 비지도학습 중 어떤 문제로 볼 수 있는가</strong><br>
Supervised learning. 많은 이메일과 그에 상응하는 레이블(spam or not)이 제공된다.<br>
<strong>9. 온라인 학습시스템이 무엇인가요</strong><br>
batch 학습시스템과 달리 점진적으로 학습할 수 있다. 변화하는 데이터와 자율시스템에 빠르게 적응하고 매우 많은 양의 데이터를 훈련할 수 있다.
<strong>10. 외부 메모리 학습이 무엇인가요(out-of-core learning)</strong><br>
CPU에 들어갈 수 없는 대용량의 데이터를 다룰 수 있다. 데이터를 mini-batch로 나누고 온라인학습기법을 사용해 학습한다.<br>
<strong>11. 예측을 하기위해 유사도 측정에 의존하는 학습알고리즘은 무엇인가요</strong><br>
사례기반학습 시스템. 훈련데이터를 기억한다. 새로운 샘플이 주어지면 유사도측정을 사용해 학습된 샘플중에서 가장 비슷한 것을 찾아 예측으로 사용한다.<br>
<strong>12. 모델 파라미터와 학습 알고리즘의 하이퍼파라미터 사이에는 어떤 차이가 있는가</strong><br>
모델파라미터(파라미터)는 모델 내부에서 결정되는 변수이다. 정규분포를 그리면 평균과 표준편차값이 구해진다. 이건 파라미터다<br>
파라미터는 데이터를 통해 구해지며 모델 내부적으로 결정되는 값이다. <br>
하이퍼 파라미터는 모델링할때 사용자가 직접 세팅해주는 값. <br>

<strong>13. 모델기반 알고리즘이 찾는 것은 무엇인가. 성공을 위해 이 알고리즘이 사용하는 가장 일반적인 전략은 무엇인가. 예측은 어떻게 만드는가</strong><br>
<strong>14. 머신러닝의 주요도전과제는 무엇인가</strong><br>
<strong>15. 모델이 훈련 데이터에서의 성능은 좋지만 새로운 샘플에서의 일반화 성능이 나쁘다면 어떤 문제가 있는 건가요. 가능한 해결책 세가지.</strong><br>
<strong>16. 테스트 세트가 무엇이고 왜 사용해야하는가.</strong><br>
<strong>17. 검증세트의 목적은 무엇인가.</strong><br>
<strong>18. 훈련-개발세트가 무엇인가. 언제필요하고 어떻게 사용해야하는가</strong><br>
<strong>19. 테스트세트를 사용해 하이퍼파라미터를 튜닝하면 어떤 문제가 생기는가</strong><br>
