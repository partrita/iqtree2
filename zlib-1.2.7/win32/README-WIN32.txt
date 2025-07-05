ZLIB 데이터 압축 라이브러리

zlib 1.2.7은 범용 데이터 압축 라이브러리입니다. 모든 코드는 스레드로부터 안전합니다. zlib 라이브러리에서 사용하는 데이터 형식은 RFC(Request for Comments) 1950부터 1952까지의 문서에 설명되어 있으며, 해당 파일은 http://www.ietf.org/rfc/rfc1950.txt (zlib 형식), rfc1951.txt (deflate 형식) 및 rfc1952.txt (gzip 형식)에서 확인할 수 있습니다.

압축 라이브러리의 모든 함수는 zlib.h 파일에 문서화되어 있습니다 (man 페이지 작성 자원봉사자는 zlib@gzip.org로 연락 바랍니다). 이 패키지에는 컴파일된 예제 두 개(example 및 minigzip)가 배포됩니다. example_d 및 minigzip_d 버전은 zlib1.dll 파일이 올바르게 작동하는지 확인합니다.

zlib에 대한 질문은 <zlib@gzip.org>로 보내주십시오. zlib 홈페이지는 http://zlib.net/ 입니다. 문제를 보고하기 전에 이 사이트를 확인하여 최신 버전의 zlib를 사용하고 있는지 확인하십시오. 그렇지 않으면 최신 버전을 받고 문제가 여전히 존재하는지 확인하십시오.

도움을 요청하기 전에 DLL_FAQ.txt와 zlib FAQ http://zlib.net/zlib_faq.html을 읽어보십시오.


목록:

zlib-1.2.7-win32-x86.zip 패키지에는 다음 파일이 포함됩니다.

  README-WIN32.txt 이 문서
  ChangeLog        이전 zlib 패키지 이후 변경 사항
  DLL_FAQ.txt      zlib1.dll에 대해 자주 묻는 질문
  zlib.3.pdf       Adobe Acrobat 형식의 이 라이브러리 설명서

  example.exe      정적으로 바인딩된 예제 (dll이 아닌 zlib.lib 사용)
  example.pdb      example.exe 디버깅을 위한 기호 정보

  example_d.exe    zlib1.dll에 바인딩된 예제 (zdll.lib 사용)
  example_d.pdb    example_d.exe 디버깅을 위한 기호 정보

  minigzip.exe     정적으로 바인딩된 테스트 프로그램 (dll이 아닌 zlib.lib 사용)
  minigzip.pdb     minigzip.exe 디버깅을 위한 기호 정보

  minigzip_d.exe   zlib1.dll에 바인딩된 테스트 프로그램 (zdll.lib 사용)
  minigzip_d.pdb   minigzip_d.exe 디버깅을 위한 기호 정보

  zlib.h           zlib.lib 또는 zdll.lib를 사용하는 프로그램을 컴파일하려면
  zconf.h          이 파일들을 컴파일러의 INCLUDE 경로에 설치하십시오.

  zdll.lib         컴파일된 프로그램을 zlib1.dll 바이너리에 링크하는 경우
  zdll.exp         이 파일들을 컴파일러의 LIB 경로에 설치하십시오.

  zlib.lib         zlib1.dll 런타임 종속성 없이 zlib를 컴파일된 프로그램에
  zlib.pdb         링크하려면 이 파일들을 컴파일러의 LIB 경로에 설치하십시오.
                   (zlib.pdb는 컴파일 타임 링커에 디버깅 정보를 제공합니다.)

  zlib1.dll        이 바이너리 공유 라이브러리를 시스템 PATH 또는
                   프로그램의 런타임 디렉토리(.exe가 있는 위치)에 설치하십시오.
  zlib1.pdb        WinDbg 또는 유사한 도구를 사용하여 응용 프로그램 충돌을 디버깅하려면
                   zlib1.dll과 동일한 디렉토리에 설치하십시오.

위의 모든 .pdb 파일은 전적으로 선택 사항이지만 프로그램 오작동이나 충돌을 진단하려는 개발자에게 매우 유용합니다. 개발자를 위한 더 많은 중요한 파일은 http://zlib.net/에서 제공되는 zlib127.zip 소스 패키지에서 찾을 수 있습니다. 자세한 내용은 해당 패키지의 README 파일을 검토하십시오.


감사의 말:

zlib에서 사용하는 deflate 형식은 Phil Katz가 정의했습니다. deflate 및 zlib 사양은 L. Peter Deutsch가 작성했습니다. zlib의 문제점을 보고하고 다양한 개선 사항을 제안해 주신 모든 분들께 감사드립니다. 너무 많아서 여기에 모두 언급할 수 없습니다.


저작권 고지:

  (C) 1995-2012 Jean-loup Gailly and Mark Adler

  이 소프트웨어는 어떠한 명시적 또는 묵시적 보증 없이 '있는 그대로' 제공됩니다. 어떠한 경우에도 저자는 이 소프트웨어의 사용으로 인해 발생하는 모든 손해에 대해 책임을 지지 않습니다.

  상업적 응용 프로그램을 포함하여 모든 목적으로 이 소프트웨어를 사용하고 다음 제한 사항에 따라 자유롭게 변경하고 재배포할 수 있는 권한이 모든 사람에게 부여됩니다.

  1. 이 소프트웨어의 출처를 허위로 표시해서는 안 됩니다. 원본 소프트웨어를 작성했다고 주장해서는 안 됩니다. 제품에 이 소프트웨어를 사용하는 경우 제품 설명서에 감사의 말을 표시하는 것은 좋지만 필수는 아닙니다.
  2. 변경된 소스 버전은 명확하게 표시해야 하며 원본 소프트웨어로 허위 표시해서는 안 됩니다.
  3. 이 고지는 모든 소스 배포에서 제거하거나 변경할 수 없습니다.

  Jean-loup Gailly        Mark Adler
  jloup@gzip.org          madler@alumni.caltech.edu

제품에 zlib 라이브러리를 사용하는 경우 서명해야 할 장황한 법적 문서를 받지 않기를 바랍니다. 소스는 무료로 제공되지만 어떠한 종류의 보증도 없습니다. 이 라이브러리는 Jean-loup Gailly와 Mark Adler가 전적으로 작성했으며 타사 코드를 포함하지 않습니다.

수정된 소스를 재배포하는 경우 변경 사항을 문서화하는 ChangeLog 파일 기록 정보를 포함해 주시면 감사하겠습니다. 수정된 소스 버전 배포에 대한 자세한 내용은 FAQ를 읽어보십시오.
