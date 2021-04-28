윈도우에서 tensorflow를 사용하기 위한 환경설정을 진행해보자! 

나는 파이썬 3 버전과 텐서플로우 1 버전이 익숙하기 때문에 이를 가상환경에 설치해 볼 것이다.

​          

설치 환경

------------------

Windows 10 Home

Intel i5-8600 @3.1GHz, RAM 8GB

NVIDIA GeForce GTX 1060 3GB

​             

Anaconda 3 설치

--------------------------------

Anaconda는 파이썬에서 data science 관련 패키지를 다 모아 배포하는 플랫폼이다.        

아나콘다에서는 윈도우 cmd 처럼 생긴 'Anaconda Prompt' 라는 것을 제공하기 때문에 이를 이용하면 여느 파이썬 패키지나 라이브러리도 아주 쉽게 설치할 수 있다는 장점이 있다!         

또한 아나콘다를 깔면 자동으로 spyder도 깔리고 jupyter notebook도 깔려서 파이썬 코드 빌드 및 실행 또한 할 수 있으므로 파이썬 개발을 할 예정이라면 이것저것 다 깔지말고 그냥 아나콘다만 까는 게 정신건강에 이롭다.       

아나콘다를 설치하는 건 아주 쉽다. 그냥 홈페이지 가서 자기한테 맞는 os 용을 다운받아 설치하면 된다.     

[아나콘다 다운로드 홈페이지](https://www.anaconda.com/products/individual)

​                 

CUDA / cuDNN 설치

---------------------------------

tensorflow를 cpu만 사용해서 돌릴 거라면 이 부분은 스킵해도 된다!         

만약 tensorflow gpu 버전을 사용할거라면 이 부분은 필수!             

두 개 다 그래픽 카드만 있다고 사용할 수 있는 것은 아니고 NVIDIA 홈페이지를 가서 라이브러리를 직접 설치해야 한다. 이 때 주의할 점은 내가 설치할 텐서플로우 버전에 유의해서 그에 맞는 CUDA와 cuDNN 버전을 설치해야한다는 것이다.           

만약 버전이 맞지 않는다면 오랜 시간 기다려서 설치한 보람도 없이 호환이 되지 않기 때문에 다 삭제하고 새로 까는 불상사가 발생한다....... 정신건강을 위해 호환되는 버전을 꼭! 미리 확인하자!!          

호환되는 버전 확인은 여기서 -> [호환 버전 확인](https://www.tensorflow.org/install/source_windows#tested_build_configurations)

여기서는 텐서플로우 1.9 버전을 설치할 것이기 때문에 CUDA 9.0 과 cuDNN 7.1.4 를 설치할 것이다.      





뇌의 구조는 굉장히 복잡하지만 그걸 구성하고 있는 연결체인 뉴런의 구조는 생각보다 단순한 구조인데 이걸 기계로 만들어 보자는 생각에서 출발한 것이 ANN 인 것이다.        
아래는 간단하게 뉴런의 작동방식을 도식화한 그림이다.<br/>
<img src="D:/Github/DeepLearning/Artifical Neural Network/images/1.jpg" title="뉴런 동작방식" alt="뉴런 동작방식"></img><br/>

이 그림을 보면 input으로 들어온 각 x 값에 weight인 w 값이 각각 곱해지고 더해진 뒤 bias 값을 추가로 더하고 나온 값을 Activation function에 통과시키면 최종적으로 output이 나온다는 걸 알 수 있다.    