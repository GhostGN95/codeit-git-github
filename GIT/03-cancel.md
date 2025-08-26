# Cancle 시리즈

## reset
- git reset --soft HEAD~1: 브랜치의 범위만 축소된다
- git reset --mixed HEAD~1: 브랜치의 범위 축소, 스테이징 에어리어 리셋
- git reset --hard HEAD~1: 브랜치 범위 축소, 스테이징 에어리어 리셋, 워킹 디렉토리 Tracked 리셋

- 기타
  - git reset --hard HEAD~1 = git reset --hard HEAD^
  - git reset --hard HEAD~2 = git reset --hard HEAD^^
  - git reset --hard [커밋아이디]




cancel 시리즈 


Reset (이미 완료된 커밋을 취소할때) = 뒤로 돌아갈때(최신부터 순차적으로 취소할때)
커맨드
git reset --soft HEAD~1 
브랜치의 범위만 축소
커밋하기 직전으로 회귀
git reset --mixed HEAD~1 
브랜치의 범위 축소, 스테이징 에어리어 리셋
커밋하고 add하기 직전으로 회귀
git reset --hard HEAD~1 
브랜치 범위 축소, 스테이징 에어리어 리셋, 워킹 디렉토리 Tracked 리셋
커밋하고 add하고 작업하기 직전으로 회귀


revert (이미 완료된 커밋을 취소할 때) = 중간에서 작업중인 것을 (위험성 높음)
커맨드 
git revert HEAD
git revert [커밋아이디]
해당 커밋의 역변환이 되는 새로운 커밋을 생성한다.

    
충돌
git revert --continue
직접 '수동으로' 충돌을 해결한다. 
직접 '수동으로' 스테이징 에어리어에 add한다.



Stash (스테이징 에어리어에서 진행된 작업을 잠시 취소할때)
git stash : 현재 스테이징 에어리어에 상태를 잠시 옆에 치워놨다.
git stash drop : 옆에 잠시 치워둔 상태를 제거해버린다. (완전히 지움)
git stsh pop : 옆에 잠시 치워둔 상태를 다시 스테이징 에어리어에 덮어쓴다.
GitHub
인증
인증 등록 
보안에 취약한 방법 
git config --global credential.helper store
토큰을 암호화하지 않고 평문으로 저장됨
Mac: ~/.git-credentials 파일에 저장됩니다.
보안에 좋지만 귀찮은 방법
git config --global credential.helper cache --timeout=3600
토큰이 메모리에 저장됩니다.
보안에 좋은 방법
git config --global credential.helper osxkeychain

로컬과 원격의 연결
git remote add [원격리포지토리 주소의 별명] [원격리포지토리 주소]
git remote add origin [원격리포지토리 주소]
git


업로드
git push [원력리포별명] [업로드하고싶은 브랜치이름]
git push origin dev
Stash 

git stash : 현재 스테이징 에어리어에 상태를 잠시 옆에 치워놨다.
git stash drop : 옆에 잠시 치워둔 상태를 제거해버린다. (완전히 지움)
git stsh pop : 옆에 잠시 치워둔 상태를 다시 스테이징 에어리어에 덮어쓴다.