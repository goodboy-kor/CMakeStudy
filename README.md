# CMake Study
- docs : https://cmake.org/cmake/help/latest/guide/tutorial/index.html   

- example download : https://cmake.org/cmake/help/latest/_downloads/b8a65b498d06de3ba4a7dc1199af2298/cmake-3.26.3-tutorial-source.zip   

- 노션 정리 : https://www.notion.so/CMake-f5842650dd414e1ba5850c4150d25ad3?pvs=4   

# Step1   
## Exercise 1
https://cmake.org/cmake/help/latest/guide/tutorial/A%20Basic%20Starting%20Point.html
- cmake_minum_required() 명령어 작성
    - cmake_minimum_required(VERSION 버전명)   
    -> cmake_minimum_required(VERSION 3.10)
- add_executable() 명령어 작성
    - add_executable(실행파일이름 소스코드)   
    -> add_executable(Tutorial tutorial.cxx)
- cmake_minum_required() 명령어 작성
    - project(프로젝트 이름)   
    -> project(Tutorial)

## 작성 코드
1. CmakeLists.txt 
```bash
cmake_minimum_required(VERSION 3.10)
project(Tutorial)
add_executable(Tutorial tutorial.cxx)
```

## 실행
build 폴더 생성 및 이동
```bash
cmake ../../Step1 # cmakeLists.txt로 make file 생성
cmake --build . # build, makefile로 진행됨
./Tutorial 144 # 144의 루트 출력
```


---