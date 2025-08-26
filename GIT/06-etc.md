# 기타

## clone
- git clone [리모트리포지토리주소]
  - 해당 명령어는 다음 명령어를 차례대로 실행한 결과와 같다.
    - 상황: 내가 처음 팀에 합류한 상황
    - 작업
      - 프로젝트 폴더를 생성한다
      - git init
      - git remote add origin [리모트리포지토리주소]
      - git fetch: 리모트 리포지토리에 있는 모든 브랜치의 트래킹 브랜치를 생성합니다.
        - 현재 시점의 브랜치 상태: origin/master, origin/develop
      - git checkout -t origin/develop
        - origin/develop과 동일한 범위를 갖는 develop 브랜치를 생성하고 체크아웃
      - 작업을 진행한다.

## pull
- git pull origin develop --revase
  - git fetch origin develop
  - git rebase origin/develop: 충돌이 날 수 있다

- git pull origin develop --no-rebase
  - git fetch origin develop
  - git merge origin/develop
    - 3-way-merge가 되거나: 충돌이 날 수 있다
    - fast-forward-merge가 되거나: 충돌이 날 수 없다

- git pull origin develop --ff-only
  - git fetch origin develop
  - git merge origin/develop: 반드시 fast-forward-merge

- 결론
  - git config pull.rebase true 1회 설정
  - git pull origin develop
  - 만약 충돌이 발생한 경우, 충돌을 해결한 후에 add를 진행하고
    - git rebase --continue

  - git config pull.rebase flase 1회 설정
  - git pull origin develop
  - 만약 충돌이 발생한 경우, 충돌을 해결한 후에 add를 진행하고
    - git rebase --continue
    -수동으로 커밋을 추가로 진행해야 합니다.

## gitignore
