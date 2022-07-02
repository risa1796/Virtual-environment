# 가상환경 
# virtual-environment

파이썬 가상환경의 중요성과 만드는 방법을 알려드리겠습니다.<br />
I will explain the reason why virtual environment is important and how to set it up. 




파이썬을 처음으로 배우는 기초 단계이거나 단순 코딩 연습을 하는 경우에는 가상환경의 중요성이 크게 없습니다. 그러나 실제로 크고 작은 프로젝트들을 할 경우, 프로젝트 마다 각각 가상환경을 만들어서 진행을 하면 프로젝트 관리가 훨씬 수월합니다. 그 이유를 알아보겠습니다.<br />
If you are in the beginning stage of learning Python or simply want to improve your coding skill, it is not a must to set up a virtual environment in Python. However,it is very helpful to mange different projects when you set up a virtual environment for each of your projects. Let me explain the reasons.



### - 프로젝트 마다 필요한 패키지들을 구분할 수 있습니다. 
###   You can sort packages installed for each project. 

 기존 아나콘다 배포판 (base)에서 여러 프로젝트를 만들게 되면, 패키지들이 한 곳에 다 모여 있기 때문에 어느 프로젝트에 어떤 패키지들이 필요한지를 추후에 구분하기가 어렵습니다. 
 프로젝트를 배포할 경우 원격 서버에 패키지들을 새로 설치해야하는데, 구분이 안되있는 상태에서는 불필요한 패키지까지 설치해야한다는 단점이 생깁니다. 
 더불어서 프로젝트에 쓰였던 패키지 버전이 어떤 것이였는지 일일이 확인하기 어려운 점도 있습니다.<br />
If you are doing multiple projects on the Anaconda default environment (base), all installed packages are placed in one folder. This will make it difficult to find out which packages are need for which project. In case you need to distribute a certain project in a new server, unneeded packages will be installed as well. Moreover, it is a unnecessary to check each version of packages one by one. 
 
 
 
 
### - "파이썬 가상환경이란 의존성(dependency)를 관리하기 위한 독립 실행환경입니다." <br />
###   "Python virtual environment is an independent processing environment to manage dependency." 

 파이썬 패키들에서도 서로 의존적인 패키지들이 있습니다. 
 예를 들어, 두가지 프로젝트가 같은 패키지를 사용하더라도 프로젝트 A 에서는 그 패키지의 이전 버전이 필요하고 프로젝트 B에서는 이번에 출시된 새 버전이 필요하는 경우가 발생하기도 합니다.
 기존 아나콘다 배포반 (base) 일 경우, 매번 프로젝트를 실행할 때마다 버전을 downgrade/upgrade 을 해야하는 불필요한 일이 생기게 됩니다. 
 가상환경을 이용하여 프로젝트를 독립적으로 진행할 경우 이런 호환성 문제를 해결할 수 있습니다.<br />
 In python, there are packages that depend on one another. For example, you have two projects and both of them use a certain package. In contrast to project A which uses the older version of the package, project B needs its current version. In this case when using the Anaconda base environment, you have to downgrade/upgrade every time when you execute two projects. Using the virtual environment for each of the projects, you can solve various compatibility issues. <br />
 
	
	

	
 
### 이제 파이썬 가상환경을 만드는 법을 알려드리도록 하겠습니다.<br />
### Now I will explan how to set up a virtual environment in Python. 




1. 제일 처음으로 아나콘다를 설치해야 합니다.<br />
   First and foremost, you need to install Anaconda.<br />
   설치 링크 : URL(https://www.anaconda.com/products/individual) <br />
  
		
		
		
2. 윈도우 경우, 윈도우 시작버튼을 눌러 확인하고 내PC 고급시스템 설정에서 Path(경로)를 지정합니다. 저는 명령어를 사용하여 가상환경을 설치할 경로를 지정해 주었습니다. 
   제가 실제로 가상환경을 설치한 방법을 아래와 같습니다. <br />
   If you have Window, click the Window start button and go to myPC Settings to set the path. I used CMD command to set the path for my virtual
   environment. <br />
 
 
   (base) chungasmac:~ jincheong-a$ cd /Users/jincheong-a/anaconda3/envs
   
			
   
3.  다음으로 아래와 같은 command 를 실행하여 cadk7 가상환경을 만듭니다. 파이썬 버전은 3.7을 사용하였습니다.<br />
    Next, I have used the following commands to set up a virtual environment 'cadk7' with the Python version 3.7.<br />

   (base) chungasmac:envs jincheong-a$ conda create -n cadk7 python=3.7
   
			
			
			
4.  명령어에 Proceed ([y]/n)? 이 뜨면 y 을 입력하여 설치를 진행시켜 주세요.<br />
    If you see 'Proceed ([y]/n)?' on cmd, enter y to proceed the setup.<br />
    
    
				
				
5.  설치가 완료되면 아래와 같이 뜹니다.<br />
    After a successful intallation, you will see the following lines. <br />

  To activate this environment, use  
 
      $ conda activate cadk7
 
  To deactivate an active environment, use
 
      $ conda deactivate
				
				
				
6. 위에 설명을 덧붙이자면, 설치된 가상환경을 열고 싶으면 coda activate cadk7 을 입력하시고, 종료는 conda deactivate 을 입력하세요.<br />
   To activate the virtual environment write: 'coda activate cadk7', to close :  'conda deactivate'.<br />




7. 가상환경을 열게되면 경로가 (base) 에서 (cadk7) 으로 변경된 것을 확인하실 수 있습니다. <br />
   When you successfully open the virtual environment, you will see that it has changed from '(base)' to '(cadk7)'<br />




8. 이제 평소처럼 아나콘다 내비게이터를 열면 상단 Applications on 목록에서 base(root) 이외에 cadk7 가상환경을 찾아보실 수 있습니다. 지정해서 가상환경에서 프로젝트를 시작하면 됩니다!<br />
   Now open the Anaconda Navigator as usual and you will see base(root) and cadk7 in the upper 'Applications on' list. Click cadk7 to start your project!<br />





가상환경 관련 코드들:<br />
More codes for the virtual environement<br />

• 버전 명시 설치 : conda create –n 가상환경명 python=3.7<br />

• 가상환경 시작 :activate 가상환경명<br />

• Jupyter notebook 설치 : conda install jupyter notebook<br />

• 패키지 설치 예): conda install numpy pandas matplotlib seaborn scipy scikit-learn tensorflow keras<br />

              기본채널에 패키지 부재시 : conda install –c conda-forge<br />
	   
• 가상환경 종료 : conda deactivate<br />

• 가상환경 저장 : conda env export –n 가상환경명 > 파일명.yml<br />

• 새로운 가상환경 생성 : conda env create –n 가상환경명 –f ./파일명.yml<br />

• 가상환경 복사 : conda create -n 생성할가상환경명 --clone 원본가상환경명<br />

• 가상환경 제거 :conda env remove –n 가상환경명<br />

