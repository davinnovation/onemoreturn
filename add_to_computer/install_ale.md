# How to Install [Arcade Learning Environment](https://github.com/mgbellemare/Arcade-Learning-Environment)

(T)install (T)reinforcement_learning (T)simulation (T)game

[official document](https://github.com/mgbellemare/Arcade-Learning-Environment/blob/master/doc/manual/manual.pdf)

## On Ubuntu
1. Get Ubuntu
    - Recommend [vmware player](https://www.vmware.com/products/workstation-player.html), or [virtual box](https://www.virtualbox.org/wiki/Downloads) for virtual machine
    - Get Ubuntu iso ( > 16.4 ) and make ubuntu virtual machine

2. Ubuntu Virtual machine에서 [Anaconda](https://www.anaconda.com/download/) 설치
    - (optional) 설치 이후 ```conda create -n rl_py36 python=3.6 anaconda``` 를 통해 파이썬 환경 생성 추천

3. ALC 설치

    | prerequisites
    1. ```sudo apt-get install git vim```
    2. ```sudo apt-get install libsdl1.2-dev libsdl-gfx1.2-dev libsdl-image1.2-dev cmake```
    3. ```git clone https://github.com/mgbellemare/Arcade-Learning-Environment.git```
    4. ```cd Arcade-Learning-Environment```
    
    | build arcade learning environment
    1. ```mkdir build && cd build```
    2. ```cmake -DUSE_SDL=ON -DUSE_RLGLUE=OFF -DBUILD_EXAMPLES=ON ..```
    3. ```make -j 4``` ( take coffee time )
    
    | install arcade learning environment
    1. (optional) ```source activate rl_py36```
    2. ```cd .. && pip install .```

Furthermore
- go to 'dqn_breakout.md` ( working )
