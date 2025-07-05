# 스타일

이 프로젝트는 리포지토리 루트의 스타일 파일을 사용하여 [clang-format][fmt]으로 포맷됩니다. 풀 리퀘스트를 보내기 전에 clang-format을 실행하십시오.

일반적으로 주변 코드의 스타일을 따르십시오. 저희는 대부분 [Google C++ 스타일 가이드][cpp-style]를 따릅니다.

커밋 메시지는 [Git 기여 파일][git-contrib]에 설명된 대로 명령형으로 작성해야 합니다.

> 변경 사항을 명령형으로 설명하십시오. 예를 들어 "[이 패치]는 xyzzy가 frotz를 하도록 만듭니다" 또는 "[나]는 xyzzy가 frotz를 하도록 변경했습니다" 대신 "xyzzy가 frotz를 하도록 만드십시오"와 같이 코드베이스에 동작 변경을 명령하는 것처럼 작성하십시오.

[fmt]: http://clang.llvm.org/docs/ClangFormat.html
[cpp-style]: https://google.github.io/styleguide/cppguide.html
[git-contrib]: http://git.kernel.org/cgit/git/git.git/tree/Documentation/SubmittingPatches?id=HEAD

# 테스트

`tests/run_tests` 대상을 실행하여 테스트가 통과하는지 확인하십시오.

기능을 추가하는 경우 그에 따라 테스트를 추가하십시오.

# 풀 리퀘스트 프로세스

모든 풀 리퀘스트는 코드 검토를 거칩니다. 안타깝게도 github의 코드 검토 프로세스는 훌륭하지 않지만 저희는 관리할 것입니다. 코드 검토 중에 변경 사항이 있으면 각 변경 사항에 대해 풀 리퀘스트에 새 커밋을 추가하십시오. 코드 검토가 완료되면 마스터 브랜치에 대해 리베이스하고 단일 커밋으로 스쿼시하십시오.
