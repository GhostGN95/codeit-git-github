# Github

## 업로드(push)
- git push [원격리포지토리별명] [업로드하고싶은브랜치이름]
  - git push origin master
  - 리모트 리포지토리에 master 브랜치가 업데이트가 됩니다.
  - 로컬 리포지토리에 트래킹 브랜치 origin/master이 리모트 브랜치와 동기화 됩니다.

## 다운로드(fetch)
- git fetch [원격리포지토리별명] [다운로드하고싶은브랜치이름]
  - git fetch origin master
  - 로컬 리포지토리에 origin/master 이름을 가진 트래킹 브랜치가 생성됩니다.
  - 트래킹 브랜치는 그림자 브랜치입니다.(체크앙웃 X, 커밋 X)