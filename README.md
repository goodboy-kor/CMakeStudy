# CMake Study
- docs : https://cmake.org/cmake/help/latest/guide/tutorial/index.html   

- example download : https://cmake.org/cmake/help/latest/_downloads/b8a65b498d06de3ba4a7dc1199af2298/cmake-3.26.3-tutorial-source.zip   

- 노션 정리 : https://www.notion.so/CMake-f5842650dd414e1ba5850c4150d25ad3?pvs=4   

# Step1   
https://cmake.org/cmake/help/latest/guide/tutorial/A%20Basic%20Starting%20Point.html
## Exercise 1
- cmake_minimum_required(VERSION 버전명) - 최소 cmake 버전 설정
    - cmake_minimum_required(VERSION 3.10)   
- add_executable(실행파일이름 소스코드) - 소스코드로 실행파일 만듬   
    - add_executable(Tutorial tutorial.cxx)
- project(프로젝트 이름) - 프로젝트 이름 정의    
    -> project(Tutorial)


## Exercise 2
- set(CMAKE_CXX_STANDARD 버전) - cpp 버전 설정   
    - set(CMAKE_CXX_STANDARD 11)
- set(CMAKE_CXX_STANDARD_REQUIRED True) - 이전 c++버전으로 컴파일을 막음
    - set(CMAKE_CXX_STANDARD_REQUIRED True)
    

## Exercise 3
- project(Tutorial VERSION 버전숫자) - project 버전 설정   
    - project(Tutorial VERSION 1.0)
- configure_file(입력파일 출력파일) - 입력파일(.h.in 파일)로 출력파일(.h 파일)을 만듬
    - configure_file(TutorialConfig.h.in TutorialConfig.h)       
        - .h.in 파일에서   
        #define 헤더파일 변수명 @CMakeLists.txt 변수명@ 로 변수를 선언

- target_include_directrories()