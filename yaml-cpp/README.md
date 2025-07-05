# yaml-cpp [![빌드 상태](https://travis-ci.org/jbeder/yaml-cpp.svg?branch=master)](https://travis-ci.org/jbeder/yaml-cpp) [![문서](https://codedocs.xyz/jbeder/yaml-cpp.svg)](https://codedocs.xyz/jbeder/yaml-cpp/)

yaml-cpp는 [YAML 1.2 사양](http://www.yaml.org/spec/1.2/spec.html)과 일치하는 C++용 [YAML](http://www.yaml.org/) 파서 및 이미터입니다.

사용 방법에 대한 감을 잡으려면 [튜토리얼](https://github.com/jbeder/yaml-cpp/wiki/Tutorial) 또는 [YAML 방출 방법](https://github.com/jbeder/yaml-cpp/wiki/How-To-Emit-YAML)을 참조하십시오. 이전 API(버전 < 0.5.0)의 경우 [문서 구문 분석 방법 (이전 API)](https://github.com/jbeder/yaml-cpp/wiki/How-To-Parse-A-Document-(Old-API))을 참조하십시오.

# 문제 있나요? #

버그를 발견하면 [이슈](https://github.com/jbeder/yaml-cpp/issues)를 게시하십시오! yaml-cpp 사용 방법에 대한 질문이 있으면 http://stackoverflow.com에 게시하고 [`yaml-cpp`](http://stackoverflow.com/questions/tagged/yaml-cpp) 태그를 지정하십시오.

# 빌드 방법 #

yaml-cpp는 크로스 플랫폼 빌드를 지원하기 위해 [CMake](http://www.cmake.org)를 사용합니다. 기본 빌드 단계는 다음과 같습니다.

1. [CMake](http://www.cmake.org) 다운로드 및 설치 (리소스 -> 다운로드).

**참고:** 플랫폼에 제공된 설치 프로그램을 사용하지 않는 경우 CMake의 bin 폴더를 경로에 추가해야 합니다.

2. 소스 디렉토리로 이동하여 다음을 입력합니다.

```
mkdir build
cd build
```

3. CMake를 실행합니다. 기본 구문은 다음과 같습니다.

```
cmake [-G 생성기] [-DBUILD_SHARED_LIBS=ON|OFF] ..
```

  * `생성기`는 사용하려는 빌드 시스템 유형입니다. 플랫폼의 전체 생성기 목록을 보려면 `cmake` (인수 없음)를 실행하십시오. 예를 들어:
    * Windows에서는 "Visual Studio 12 2013"을 사용하여 Visual Studio 2013 솔루션을 생성하거나 "Visual Studio 14 2015 Win64"를 사용하여 64비트 Visual Studio 2015 솔루션을 생성할 수 있습니다.
    * OS X에서는 "Xcode"를 사용하여 Xcode 프로젝트를 생성할 수 있습니다.
    * UNIX 계열 시스템에서는 옵션을 생략하여 makefile을 생성합니다.

  * yaml-cpp는 기본적으로 정적 라이브러리를 빌드하지만 `-DBUILD_SHARED_LIBS=ON`을 지정하여 공유 라이브러리를 빌드할 수 있습니다.

  * 빌드 사용자 지정에 대한 자세한 옵션은 [CMakeLists.txt](https://github.com/jbeder/yaml-cpp/blob/master/CMakeLists.txt) 파일을 참조하십시오.

4. 빌드하십시오!

5. 정리하려면 `build` 디렉토리를 제거하십시오.

# 최근 릴리스 #

[yaml-cpp 0.6.0](https://github.com/jbeder/yaml-cpp/releases/tag/yaml-cpp-0.6.0)이 릴리스되었습니다! 이 릴리스에는 C++11이 필요하며 더 이상 Boost에 의존하지 않습니다.

이전 API를 원하면 [yaml-cpp 0.3.0](https://github.com/jbeder/yaml-cpp/releases/tag/release-0.3.0)을 계속 사용할 수 있습니다.

**이전 API는 계속 지원되며 버그 수정도 계속 받을 것입니다!** 0.3.x 및 0.4.x 버전은 이전 API 릴리스이고 0.5.x 이상은 모두 새 API 릴리스입니다.
