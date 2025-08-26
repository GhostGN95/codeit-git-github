# Cancle 시리즈

## reset
- git reset --soft HEAD~1: 브랜치의 범위만 축소된다
- git reset --mixed HEAD~1: 브랜치의 범위 축소, 스테이징 에어리어 리셋
- git reset --hard HEAD~1: 브랜치 범위 축소, 스테이징 에어리어 리셋, 워킹 디렉토리 Tracked 리셋

- 기타
  - git reset --hard HEAD~1 = git reset --hard HEAD^
  - git reset --hard HEAD~2 = git reset --hard HEAD^^
  - git reset --hard [커밋아이디]
