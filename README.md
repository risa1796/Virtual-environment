# 가상환경 
# virtual-environment

파이썬 가상환경의 중요성과 만드는 방법을 알려드리겠습니다.
I will explain the reason why virtual environment is important and how to set it up. 



파이썬을 처음으로 배우는 기초 단계이거나 단순 코딩 연습을 하는 경우에는 가상환경의 중요성이 크게 없습니다. 그러나 실제로 크고 작은 프로젝트들을 할 경우, 프로젝트 마다 각각 가상환경을 만들어서 진행을 하면 프로젝트 관리가 훨씬 수월합니다. 그 이유를 알아보겠습니다.
If you are in the beginning stage of learning Python or simply want to improve your coding skill, it is not a must to set up a virtual environment in Python. However,it is very helpful to mange different projects when you set up a virtual environment for each of your projects. Let me explain the reasons.


### - 프로젝트 마다 필요한 패키지들을 구분할 수 있습니다. 
###   You can sort packages installed for each project. 

 기존 아나콘다 배포판 (base)에서 여러 프로젝트를 만들게 되면, 패키지들이 한 곳에 다 모여 있기 때문에 어느 프로젝트에 어떤 패키지들이 필요한지를 추후에 구분하기가 어렵습니다. 
 프로젝트를 배포할 경우 원격 서버에 패키지들을 새로 설치해야하는데, 구분이 안되있는 상태에서는 불필요한 패키지까지 설치해야한다는 단점이 생깁니다. 
 더불어서 프로젝트에 쓰였던 패키지 버전이 어떤 것이였는지 일일이 확인하기 어려운 점도 있습니다.
If you are doing multiple projects on the Anaconda default environment (base), all installed packages are placed in one folder. This will make it difficult to find out which packages are need for which project. In case you need to distribute a certain project in a new server, unneeded packages will be installed as well. Moreover, it is a unnecessary to check each version of packages one by one. 
 
 
 
 
### - "파이썬 가상환경이란 의존성(dependency)를 관리하기 위한 독립 실행환경입니다." 
###   "Python virtual environment is an independent processing environment to manage dependency."

 파이썬 패키들에서도 서로 의존적인 패키지들이 있습니다. 
 예를 들어, 두가지 프로젝트가 같은 패키지를 사용하더라도 프로젝트 A 에서는 그 패키지의 이전 버전이 필요하고 프로젝트 B에서는 이번에 출시된 새 버전이 필요하는 경우가 발생하기도 합니다.
 기존 아나콘다 배포반 (base) 일 경우, 매번 프로젝트를 실행할 때마다 버전을 downgrade/upgrade 을 해야하는 불필요한 일이 생기게 됩니다. 
 가상환경을 이용하여 프로젝트를 독립적으로 진행할 경우 이런 호환성 문제를 해결할 수 있습니다.
 In python, there are packages that depend on one another. For example, you have two projects and both of them use a certain package. In contrast to project A which uses the older version of the package, project B needs its current version. In this case when using the Anaconda base environment, you have to downgrade/upgrade every time when you execute two projects. Using the virtual environment for each of the projects, you can solve various compatibility issues. 
 
 ## ------------------
 
이제 파이썬 가상환경을 만드는 법을 알려드리도록 하겠습니다.
Now I will explan how to set up a virtual environment in Python. 

1. 제일 처음으로 아나콘다를 설치해야 합니다.
   First and foremost, you need to install Anaconda.
   설치 링크 : URL(https://www.anaconda.com/products/individual)
  
2. 윈도우 경우, 윈도우 시작버튼을 눌러 확인하고 내PC 고급시스템 설정에서 Path(경로)를 지정합니다. 저는 명령어를 사용하여 가상환경을 설치할 경로를 지정해 주었습니다.
   If you have Window, click the Window start button and go to myPC Settings to set the path. I use CMD command to set the path for my virtual environment. 
   
   <img width="702" alt="Bildschirmfoto 2022-07-02 um 13 48 16" src="https://user-images.githubusercontent.com/70292353/176986935-2b3c50d0-f488-4266-a839-606eacb06ae6.png">

   OR 
   
   command line >
  
   (base) chungasmac:~ jincheong-a$ cd ./anaconda3/envs
   
   
3.   

