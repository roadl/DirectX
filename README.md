## Project Overview
> 게임개발 기능대회 준비작

DirectX, C++로 개발한 캐쥬얼한 게임들 모음입니다.

https://drive.google.com/drive/u/3/folders/1ObF9PwqzzH-GRdHc3VastbHBgJu4-c8F

## Features
- DirectX 기반 엔진
  - Entity - asd asdf asf as
  - World, Scene 개별 클래스
  - 구조 사진 한장
- 2.5D Graphic
  - Top View, Quarter View
  - 3D Images to 2D game

## Controls
- 각 게임 설명 참고

## Build & Run
- Realease 폴더 안의 .exe 파일 실행
- Docker
  - 추가 예정
- Visual Studio에서 실행할 경우 (Visual Studio 18 기준)
  - [DirectX SDK June 2010 Download](https://www.microsoft.com/en-us/download/details.aspx?id=6812)
  - Engine/Define.h 수정

    - 추가
    ```
    #include <filesystem>
    #include <string>
    ```
 
    - 수정
      
    `using namespace std::expermental::filesystem::v1; -> using namespace std::filesystem`

    - 속성 변경
      - 프로젝트 속성 / 구성 속성 / C/C++
        - 일반 / 추가 포함 디렉터리 -> DirectX SDK June 폴더 안의 Include 파일 추가 (Default: C:/Program Files (x86)\Microsoft DirectX SDK (June 2010)/Include)
        - 언어 / C++ 언어 표준 -> /std:c++ 17 이상
      - 프로젝트 속성 / 구성 속성 / 링커
        - 일반 / 추가 라이브러리 디렉터리 -> DirectX SDK June 폴더 안의 Include 파일 추가 (Default: C:/Program Files (x86)\Microsoft DirectX SDK (June 2010)/Lib)
        - 입력 / 추가 종속성 -> 아래 항목들 추가
          ```
          d3d10.lib
          d3dx10.lib
          dxgi.lib
          dsound.lib
          dxguid.lib
          winmm.lib
          ```

## Development Enviroment
- OS: Microsoft Windows 10 Home (10.0.19045)
- Architecture: x64
- Language: C++ (std:c++ 17)
- Compiler: MSVC 14.50.35717
- Graphic Library: DirectX SDK June 2010

## Team Members
Developer - [roadl](https://github.com/roadl) 
Designer - 유진
