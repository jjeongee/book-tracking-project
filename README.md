# book-tracking
이 리포지토리는 **순수 텍스트**(`book_list.txt`)와  
**Markdown**(`README.md`)만으로  
GitHub 협업 워크플로우(이슈 → PR → 태그)를 연습하기 위해 만들어졌습니다.

## 5조 역할편성
- 팀 리더 : 이희정
- 기획자 : 이원석
- 개발자 A : 조성하
  
## 파일 수정 워크플로우
1. book_list.txt 수정 → 커밋  
2. PR 생성 → 리뷰 → 머지  
3. milestone, label 확인  
4. 완료되면 book_list.txt 변경(마일스톤 및 이슈 참고)

## Milestone
- 마일스톤1 : 도서 구매
    - 구매 도서 목록을 작성합니다.
- 마일스톤2 : 도서 배송
    - 구매 완료한 도서들은 도서 배송 목록으로 옮깁니다.
- 마일스톤3 : 배송 완료
    - 프로젝트의 최종 목표로, 
    도서 구매 목록과 도서 배송 목록에 있는 책들을 모두 이곳으로 옮기는것이 목표입니다.
    최종적으로는 도서 도착 날짜도 함께 표기됩니다.

## 브랜치 명명 규칙
``PR작업종류/구현기능이름``
형식으로 작성합니다.
- 커밋 하나당 하나의 브랜치를 생성하는것을 목표로 합니다.

## PR 규칙
PR작업 종류(라벨 이름) : 커밋내용 작성으로 통일한다.

``chore``: 문서작업 관련 커밋입니다.
- 보통 README파일을 수정합니다.
  
``feat``: 새로운 구현 기능 커밋입니다.
- 도서의 상태가 변화할경우(구매, 배송, 배송완료)
  
``bug``: 충돌 발생했을경우의 커밋입니다.
- 충돌의 원인을 분석하고 이를 해결합니다.
  
## 팀원별 회고록 작성
** 기획자 : 이원석 **
프로젝트 개요
- book_list.txt 파일을 수정하고 새로운 브랜치를 만들고 병합하는 과정을 깃과 깃허브를 통해 관리했다.
- 프로젝트 내용은 책을 구입, 배송, 배송완료 목록을 나눠서 txt파일 안에 정리하는 과정을 나타냈고, 전반적인 과정과 파일을 깃과 깃허브를 통해 모니터링하고 관리했다.

역할
- 기획자 역할을 맡아서 시나리오를 팀원들과 함께 구성하고, 마일스톤을 정의하고, 마일스톤에 들어갈 이슈, 이슈에 붙일 라벨을 정의했고, 프로젝트 수행 중 나타나는 변경사항을 확인하고, 깃허브에 반영하고 처리했다.

문제 점 
- 개발자 인원이 1명으로 정해져서 텍스트 파일을 수정하고 branch를 병합하는 과정에서 의도적으로 충돌을 일으키는 것이 쉽지 않았다. 테스팅 레포지토리에서는 confilct라는 브랜치를 생성해서 처리하려고 했지만 실패했다. 실제 레포지토리에서는 첫번째 마일스톤의 첫번째 이슈에서 브랜치를 2개 생성하고 각각 다른 내용을 입력한 후에 병합시 발생하는 충돌 과정을 확인하고 서브 이슈를 정의하여 처리했다. 
- 적절한 라벨을 정의하고 이슈에 붙이는 것 또한 쉽지 않았던 것 같다.
- README.md 파일의 수정을 가상 머신에서 할때 한글 지원이 안되서 웹에서 진행 해야하는 문제가 있었다.

배운 점 및 느낀 점:
- 협업 시에 발생할 수 있는 다양한 코드의 변경 사항을 추적하는데 이슈와 PR을 적절히 잘 사용하는 것이 굉장히 효율적이고 체계적인 것을 체감했다.
- 이슈마다 브랜치를 생성해서 PR을 통해서 main에 병합하도록 하여 더 안정적으로 프로젝트를 관리할 수 있었다.
- 댓글 기능을 사용해서 합의를 통해 병합하여 변경 사항을 한번에 확인하고 병합을 안전하게 진행할 수 있었다.

이후 프로젝트에 반영할 점:
- 마일스톤과 이슈를 좀 더 명확하게 구성하고 시나리오 구성에 시간을 더 많이 할애하여 수정 사항을 줄인다.
- 변경 요구 사항을 댓글에 포함해서 더 유동적으로 문제를 처리할 수 있도록 한다.
--------------
** 팀 리더 : 이희정 **
1. 프로젝트 메인 시나리오 구축
- 팀원들과 함께 시나리오를 구체화하며 프로젝트 전체 흐름을 설계하였다  
- 마일스톤과 이슈, 그리고 각 이슈에 붙일 라벨을 기획자 포지션의 팀원과 함께 논의하였다.  
- 작업 중 발생한 변경사항을 즉시 파악하고 merge 규칙을 생성했다.

2. 도전 과제 및 문제점
- 단독 개발자 환경
  - 의도적인 충돌 유도가 어려워, 테스트 레포지토리에서 여러 번 시도하게 되었다.
- 환경 제약
  - 가상 머신에서 `README.md` 한글 편집이 지원되지 않아, GitHub 웹 UI에서만 수정이 가능했다.

3. 배운 점
- 이슈&PR 기반 워크플로우가 변경 이력을 체계적으로 관리하는 데 효율적임을 알 수 있었다. 
- 브랜치별로 PR을 생성 및 병합함으로써 프로젝트 안정성을 크게 높일 수 있었다.
- 댓글을 통한 팀원 간 상호 확인 과정을 거치면, 병합 후 변경사항을 한눈에 확인 가능

4. 개선할 점 및 향후 계획  
- 라벨 가이드라인을 문서화하여 일관성 확보할 계획이다. 
- 가상 머신 환경에서의 한글 편집 문제를 해결하고 싶다.
- 변경 요구사항을 이슈 코멘트로 관리하여 더 유연하게 대응하고 싶다.
----------
**개발자 A : 조성하 **
각 브랜치의 병합으로 일어난 충돌을 해결하는 방법을 익히고 커밋, push한 뒤 PR을 남기는 협업 방식에도 점차 익숙해졌다. 팀원들의 도움으로 프로젝트를 잘 마무리할 수 있었다.
프로그램 개요:
-GitHub 기반 협업 실습 프로젝트로, 브랜치 생성, 커밋, PR(Pull Request), 충돌 해결, 이슈 및 마일스톤 관리 등 Git과 Github의 핵심 기능을 실습했다. 실습은 코드가 아닌 book_list.txt와 같은 텍스트 파일을 중심으로 진행되었다.

맡은 역할: 
-개발자 A 역할을 맡아 book_list.txt 파일을 생성하고 수정했다.
-README파일에 따른 팀 협업 방식에 따라 브랜치를 생성한 뒤 commit, push, PR을 생성했다.
-의도적으로 브랜치 간 충돌 상황을 만들었다.

문제점:
-개발자 인원이 제한적인 이유로 의도적으로 브랜치 간의 충돌을 발생시키는 방안이 쉽게 떠오르지 않았다.
- 이전에 book_list.txt파일을 수정한 부분이 반영되지 않았었다.

해결방안:
-개발자 A local 환경에서 2개의 브랜치를 생성해 같은 파일 내의 같은 줄을 다르게 수정하여 병합해 충돌을 일으켰다.
-merge과정에 오타가 있음을 확인하고 다시 merge를 진행하였다.

향후계획 및 느낀 점:
-실습 경험을 바탕으로 다른 프로젝트에서도 GitHub와 Git을적극 활용하고, 팀 내 협업을 위한 PR 작성, 이슈 관리, 커밋 메시지 전략 등을 더 체계화할 계획이다.
-텍스트 파일이 아닌 코드 기반 프로젝트에서도 병합과 충돌 해결 능력을 더 발전시키고 싶다.
