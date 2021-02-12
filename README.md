# coursera-machine-learning-Andrew-Ng-
coursera machine learning(Andrew Ng)<br>
https://www.coursera.org/learn/machine-learning#syllabus


<h3>1 week</h3><br>
Machine learning algorithm: Supervised learning, Unsupervised learning<br>
-Supervised learning: 작업을 수행할 수 있는 방법을 컴퓨터에게 가르치는 것이 핵심<br>
-Unsupervised learing: 컴퓨터가 스스로 학습하도록 유도<br>
<br>
<h3>What is Supervised learning?</h3><br>
Supervised learning은 우리가 알고리즘에 데이터셋을 주는데 각 데이터에 '정답'이 포함되어 있는것이다.<br>
알고리즘의 역할은 그 '정답'을 더 많이 만들어 내는것. 이것은 regression problem(회귀문제)이라고도함.
<br>회귀문제: 연속된 값을 가진 결과를 예측하려 하는것<br><br>
Breast Cancer (malignant, benign) -> Classification : Discrete valued output (0 or 1)<br>
Tumor size에 따른 양성, 악성 판별문제.
<img src="https://user-images.githubusercontent.com/67510613/105625656-03513800-5e6e-11eb-8c6b-490fbd461fbc.JPG">
Tumor size, age에 따른 양성, 악성 판별문제.
<img src="https://user-images.githubusercontent.com/67510613/105625741-8c686f00-5e6e-11eb-9020-b89b6efd85ed.JPG">
<br><br>
이렇게 1,2개 특성이 아니라 무한대의 특성을 다루려면 어떻게해야하는가? <br>
-> Support Vector Machine Algorithm<br><br>
<hr>
<h3>Supervised Learning</h3><br>
In supervised learning, we are given a data set and already know what our correct output should look like, <br>
having the idea that there is a relationship between the input and the output.<br><br>

Supervised learning problems are categorized into "regression" and "classification" problems. In a regression<br> problem, we are trying to predict results within a continuous output, meaning that we are trying to map input <br>
variables to some continuous function. In a classification problem, we are instead trying to predict results <br>
in a discrete output. In other words, we are trying to map input variables into discrete categories. <br>
<hr><br>


<h3>What is Unsupervised learning?</h3><br>
데이터 레이블이 주어지지않는다. 이것으로 뭘할지 또 각 데이터가 무엇인지 알 수 없다.<br>
1. clustering algorithm
<img src="https://user-images.githubusercontent.com/67510613/105629761-3b657480-5e88-11eb-95f4-b2bd4782a045.JPG">
스스로 그룹화하는 것?<br><br>


2. Cocktail party problem<br>
여러 잡음이 존재하고 다양한 오디오를 각각 분리한다.<br>
[W,s,v]=svd((repmat(sum(x.*x,1),size(x,1),1).*x)*x');<br>
*수업에서 Octave programming environment를 사용할 것임.<br>
svd함수는 특이값분해(singular value decomposition)의 약자_octave내장함수임
<hr>
<h3>Unsupervised Learning</h3><br>
Unsupervised learning allows us to approach problems with little or no idea what our results should look like. <br>
We can derive structure from data where we don't necessarily know the effect of the variables.<br>

We can derive this structure by clustering the data based on relationships among the variables in the data.<br>

With unsupervised learning there is no feedback based on the prediction results.<br>
<br>
<strong>Example:</strong><br>
<br>
Clustering: Take a collection of 1,000,000 different genes, and find a way to automatically group these genes <br>
into groups that are somehow similar or related by different variables, such as lifespan, location, roles, <br>
and so on.<br><br>

Non-clustering: The "Cocktail Party Algorithm", allows you to find structure in a chaotic environment. <br>
(i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).<br>
<hr><br>
<h3>Supervised learning Model Representation</h3><br>

<img src="https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/H6qTdZmYEeaagxL7xdFKxA_2f0f671110e8f7446bb2b5b2f75a8874_Screenshot-2016-10-23-20.14.58.png?expiry=1611792000000&hmac=cqtMQlTK9mMvVbM28xf7tYYXMG44sEC1AnpGz-eTrhk">
<br>Function h is called htpothesis.
<hr>
<h3>Cost function</h3><br>
<img src="https://user-images.githubusercontent.com/67510613/105865886-b5d3f700-6036-11eb-84e7-fb705c826a50.JPG">
<img width="415" alt="goal" src="https://user-images.githubusercontent.com/67510613/106297264-da79da00-6295-11eb-9d84-e6bc59eb2c1b.PNG">
<img width="525" alt="min" src="https://user-images.githubusercontent.com/67510613/106292445-2cb7fc80-6290-11eb-89d8-c56956e31306.PNG">
MSE같은 손실함수는 정담에 대한 오류를 숫자로 나타내는 것으로 오답이 가까울 수록 큰 값이 나오고 반대로 정답에 가까울수록 작은 값이 나온다.<br>

<hr>
<h3>Gradient decent</h3><br>
<img width="407" alt="gd" src="https://user-images.githubusercontent.com/67510613/106299400-71479600-6298-11eb-8f24-21f37a1473eb.PNG">
<br> 초기화는 일반적으로 theta1과 theta2를 모두 0으로 한다. 그리고 기울기하강법을 통해 thata1,2를 조금씩 바꾸면서 J값을 조금이라도 줄이는 것을 목표로한다.

<img width="409" alt="gd2" src="https://user-images.githubusercontent.com/67510613/106301114-a94fd880-629a-11eb-9e10-21b851626909.PNG">
<br> alpha는 훈련비율(learning rate)로 얼마나 많은 값이 변하는가에 대한 변수이다. 
<br> <strong>gradient decent 수식의 이해</strong><br>
<br>
<img width="415" alt="gd3" src="https://user-images.githubusercontent.com/67510613/106308004-74944f00-62a3-11eb-87cd-152e6ead8202.PNG">
식에서 alpha를 감소시킬 이유가 없는 이유가 무엇인가? : local min값에 가까워질수록 기울기(미분계수)는 0에 가까워지고(작아지고) 따라서 <br>
이동거리는 alpha를 fix했더라도 알아서 자연스럽게 감소한다.
<hr>
<h3>Cost function & Gradient decent</h3><br>
기울기 하강을 이용해서 cost function을 최소화시켜보자<br>
<img width="351" alt="cofunc,gd" src="https://user-images.githubusercontent.com/67510613/106310895-9ee80b80-62a7-11eb-8129-45a9af806716.PNG">
<img width="274" alt="cogd" src="https://user-images.githubusercontent.com/67510613/106311330-52510000-62a8-11eb-9f0e-7c7de18628b9.PNG">
<br>batch gradient decent? 전체 데이터셋에 대해 에러를 구하고 기울기를 한번만 계산하는 방식인거같음. 
<hr><br>
<h2>2nd week</h2><br>
하나 이상의 변수나 feature를 다루기 위한 강력한 선형회귀를 다룬다

<img width="281" alt="multifeat" src="https://user-images.githubusercontent.com/67510613/106318623-8978de80-62b3-11eb-8b45-46e7abf36b3d.PNG">
아래와 같은 식으로도 표현가능하다.
<img width="289" alt="multifea2" src="https://user-images.githubusercontent.com/67510613/106318779-c0e78b00-62b3-11eb-816d-d6b2b2353617.PNG"><br>
Gradient Descent for multuple variables<br>
<img width="470" alt="multi3" src="https://user-images.githubusercontent.com/67510613/106319752-43bd1580-62b5-11eb-9b83-f9de8b9b248c.PNG">
<hr>
<strong>Feature Scaling</strong>
<br>여러개의 feature가 있고 그 단위와 크기가 비슷하다면 다른 feature더라도 gradient descent는 더 빠르게 수렴할 수 있다.
<img width="413" alt="scaling" src="https://user-images.githubusercontent.com/67510613/106347683-e9977100-6303-11eb-940f-90609bf7a990.PNG">
왼쪽 그림에서는 범위의 차이가 크기 때문에 J를 그렸을때 굉장히 뾰족한 등고선이 나오며 이는 경사하강법을 적용했을때 구불구불한 조정때문에 오랜시간이 걸리게된다.<br>
오른쪽 그림에서와 같이 feature scaling은 범위를 비슷하게 맞춰줌으로써 J의 등고선이 거의 완전한 원을 그리도록 하고 경사하강법이 더 빨리 수렴하도록한다.<br>
every feature는 -1에서 1 즈음에 근사하게한다. 0~3 ok. -2~0.5 ok. -100~100은 not ok. -0.0001~0.0001 not ok <br>
<strong> Mean normalization</strong><br>
<img width="91" alt="mn" src="https://user-images.githubusercontent.com/67510613/106348026-51e75200-6306-11eb-8a71-98e54b0e0ba2.PNG">
ui는 average of all the value for features(i)이고 si는 (max-min) 또는 standard deviation이다.
<img width="671" alt="mn2" src="https://user-images.githubusercontent.com/67510613/106348072-b0143500-6306-11eb-91df-ee686f1e2031.PNG">
<hr>
1. Debugging <br>
2. How to choose learning rate 'alpha'<br>
<img width="419" alt="debug" src="https://user-images.githubusercontent.com/67510613/106348374-2154e780-6309-11eb-811e-b9726be6c18a.PNG">
alpha가 너무 크면 위에처럼 된다. 직접 반복횟수당 J(cost func)을 그려봐서 경사하강이 제대로 되는지를 체크할 수 있다. <br>
제대로라면 매 반복마다 J는 감소하게 된다.

<hr>
<strong>Polynomial Regression</strong><br>
hypothesis function은 straight 할 필요없다. quadratic, cubic or square root function이어도 된다. 
<hr>
<h3>Normal equation</h3><br>
:Method to solve for theata analytically
<img width="129" alt="theta" src="https://user-images.githubusercontent.com/67510613/106352100-f1ffa400-6323-11eb-9085-43976f84b850.PNG">
Octave: pinv(X'*X)*X'*y<br>

<img width="457" alt="theta1" src="https://user-images.githubusercontent.com/67510613/106352101-f5932b00-6323-11eb-8889-8bd03a05ec90.PNG">
<img width="592" alt="gdnm" src="https://user-images.githubusercontent.com/67510613/106352108-fa57df00-6323-11eb-9d7a-cb689a770124.PNG">
n의 값. 즉 feature의 개수가 너무클때는 (1000정도는 괜찮은데 10000부터는 힘들다) normal equation의 경우 inverse를 계산해야하기때문에 <br>
시간이 매우 오래걸린다. 그럴경우엔 경사하강법이 더 적합한 방법이다.
logistic regression 같은거 배울때 보면 노말이퀘이션은 쓰기힘들것. 주로 gradient descent 사용한다.<br>
<hr>
X'는 X의 transpose임. <br>
X'X의 역행렬이 없으면 어떻게 되는가? octave에선 pinv(pseudo-inverse) 쓰면 그런경우에도 theta를 잘 구해준다.<br>
X'X의 역행렬이 없게되는 경우는 무엇인가?(non-invertible)<br>
쓸데없는 feature를 가지고 있는 경우이다. x1=size in feet^2이고 x2=size in m^2이면 x1=(3.28)^2*x2로 둘이 연관되어버린다. <br>

다음은 너무 많은 feature를 가지고 있는 경우이다. (e.g. m<=n). 해결을 위해선 feature를 좀 지우거나 regularization을 이용한다.
<hr>
<h3>Vectorization</h3><br>
<img src="https://user-images.githubusercontent.com/67510613/107059245-e9720680-6818-11eb-9b48-47813a8bcb73.JPG">
벡터화된 표현이 훨씬 간단하다.
<hr>
<h3>Classification</h3><br>
ex) spam 분류기, 종양 양/음성 분류. <br>
0-> negative Class, 1-> Positive Class 
<img src="https://user-images.githubusercontent.com/67510613/107066700-a6686100-6821-11eb-9702-76d8e7c3105e.JPG">
Binary-classification 문제이다. h=(theta)'x를 그리고 이걸로 예측.<br>
<strong>선형회귀는 합리적인가? 위의 문제만 보면 그렇게 보인다.</strong><br>
<img src="https://user-images.githubusercontent.com/67510613/107067278-68b80800-6822-11eb-9556-053753266015.JPG">
x축 range를 늘려 뒤쪽에 데이터를 추가했더니 hypothesis는 새롭게 그려진다. 1,0을 나누는 지점도 새롭게 만들어진다. 결국 선형회귀를 이용해 더 안좋은 결과를 얻게 된것이다. <strong>선형회귀를 분류문제에 적용하는건 좋은생각이 아니다!</strong><br>
logistic Regression을 이용하자! : 0 <= h <= 1
<hr>
<h3>Hypothesis Representation</h3><br>
원래 선형회귀에선 hypothesis=(theta)'x를 썼음. logistic회귀를 위해 g(theta)'x를 사용.<br>
g=1/(1+exp(-z))로 이를 sigmoid function 혹은 Logistic function이라 함.  
<img src="https://user-images.githubusercontent.com/67510613/107112328-229e8b00-689a-11eb-8324-ffd79288e96e.JPG">
<img src="https://user-images.githubusercontent.com/67510613/107112342-3d70ff80-689a-11eb-962d-a4908e492e3a.JPG">
<hr>
<h3>Decision Boundary</h3><br>

<img src="https://user-images.githubusercontent.com/67510613/107113060-b0c94000-689f-11eb-945e-a12cbde2d3b6.JPG">
<br>
Non-linear Boundary<br>
<img src="https://user-images.githubusercontent.com/67510613/107113062-b32b9a00-689f-11eb-87b0-c0638f24dd31.JPG">
바운더리를 이런식으로 줄수도 있을것임. 이를 응용해 다양한 형태의 바운더리 만들 수 있을 것
<hr>
<h3>Cost Function</h3><br>
어떻게 parameter(theta)를 찾을 것인가?<br>
linear regression에서 했듯이 똑같은 cost function을 logistic function에서 쓰는 건 좋지 않은 선택이다. 왜냐면 convex하지 않은 output을 낼것이기 때문이다. convex하지 않으면 local optima가 많이 생겨서 도달점이 global optima라고 장담할 수 없다. <br>
logistic regression에서 사용할 cost function은 다음과 같다. <br>
<img src="https://user-images.githubusercontent.com/67510613/107114744-b9c00e80-68ab-11eb-88bf-a646807c979d.JPG">
<br>
<img src="https://user-images.githubusercontent.com/67510613/107114787-fee44080-68ab-11eb-8822-e565125e5301.JPG">
y=1 일때와 y=0일때의 그래프다. <br>
y=1일때 h가 1로 간다면 cost function은 0에 수렴할 것이고, h가 0으로 간다면 cost function은 infinite하게 갈것이다. <br>
y=0일때 h가 0으로가면 J=0, 1로가면 infinite.  
<hr>
<h3>Simplified Cost function and Gradient Descent</h3><br>
어떻게 cost function을 간단하게 쓸것인가, 경사하강법을 이용해 로지스틱 회귀의 매개변수(theta)를 피팅하는 방법<br>
앞서 아래의 y=0일때와 1일때로 구분된 식을 이야기했었는데 이걸 하나의 식으로 합칠 수가 있다. <br>
<img src="https://user-images.githubusercontent.com/67510613/107115447-23dab280-68b0-11eb-95b3-4ef8a6649bdc.JPG">
왜그런지는 y에 0,1넣어보면 납득이간다. <br>
식을 완전히 쓰면 다음과 같다.<br>
<img src="https://user-images.githubusercontent.com/67510613/107115451-2806d000-68b0-11eb-8e51-8c13f5e7418d.JPG">
경사하강법의 적용은 다음과 같다. linear regression과 같은 식인걸 볼수 있는데 그렇다 해도 hypothesis를 sigmoid로 바꿨기때문에<br>
다른식이다.<br>
<img src="https://user-images.githubusercontent.com/67510613/107115452-29d09380-68b0-11eb-825b-c529857ecdd8.JPG">
<hr>
<h3>Advanced Optimization</h3><br>
-Gradient descent<br>
-Conjugate gradient<br>
-BFGS<br>
-L-BFGS<br>
어떤 이점들이 있을까?<br>
learning rate alpha를 수동적으로 고를필요가 없고, 보통 경사하강법보다 빠르다. 단점은 더 복잡하다는 것.<br>

'''m<br>
function [jVal, gradient] = costFunction(theta)<br>
&nbsp;&nbsp;&nbsp;jVal = [...code to compute J(theta)...];<br>
&nbsp;&nbsp;&nbsp;gradient = [...code to compute derivative of J(theta)...];<br>
end<br>
'''<br>
<br>
'''<br>
options = optimset('GradObj', 'on', 'MaxIter', 100);<br>
initialTheta = zeros(2,1);<br>
&nbsp;&nbsp;&nbsp;[optTheta, functionVal, exitFlag] = fminunc(@costFunction, initialTheta, options);<br>
'''<br>
<br>
<hr>
<h3>Multiclass Classification: One-vs-all</h3><br>
class가 여러개인 경우는 어떻게 분류하는가? 학습알고리즘을 어떻게 적용할까? <br>
One-vs-all (one-vs-rest) 를 이용한다. <br>
<img src="https://user-images.githubusercontent.com/67510613/107117716-9737f080-68bf-11eb-868b-a626d6bb8886.JPG">
이걸 세가지의 binary-classification 문제로 바꿀것이다. 
<img src="https://user-images.githubusercontent.com/67510613/107117788-07467680-68c0-11eb-8183-2317e57f9d0b.JPG">
<hr>
...........
<hr>
<h3>4 weeks</h3><br>
<h3>Neural Networks: Non-linear Hypothesis</h3>
n이 엄청 큰데 로지스틱 연산을 한다고 생각해보자. 엄청 비효율 적임. (ex. 컴퓨터 비전)<br>
신경망의 배경: 뇌를 모방한 알고리즘이다. 80~90년대 널리 사용되었지만 계산비용이 큰만큼 어느순간 인기가 줄었는데 컴퓨터의 성능이 좋아지기 시작하면서 다시 주목 받게됨.<br>
신경망을 표현할 때 가설이나 모델을 어떻게 표현할 것인가?



























