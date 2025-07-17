### Today I Learned 
# GIT

## GIT이란?
*분산 버전 관리 시스템*이다.
여기서 버전 관리란,
변경사항을 기록하고 추적하는 것이다.

분산식
> 버전을 여러개 복제 - 나는 복제본 수정 > 이것을 중앙에 적용

**장점**
- 중앙 서버에 의존하지 않고 동시에 다양한 작업을 수행할 수 있다.
- 중앙 서버 장애에 대비해서 백업과 복구에 용이하다.
- 인터넷에 연결되지 않은 환경에서도 작업을 할 수 있다.
  - 로컬 저장소에 기록하고 나중에 중앙 서버와 동기화 한다.
 

중앙 집중식 
: 버전은 중앙에 저장되고 서버에 저장되어 있는 한개의 파일을 가져와 수정 후 다시 중앙에 업로드 하는 방식이다.

---

버전 관리 단계
1. Working Directory
  : 실제 작업 중인 파일들이 위치하는 영역 (ex. 프로젝트 폴더)
2. Staging Area
   : 디렉토리에서 변경된 파일 중, 다음 버전에 포함시킬 파일들을 선택적으로 추가하거나 제외할 수 있다.
3. Repository
   : 버전 (commit)이력과 파일들이 적용되어 있는 최종적인 저장소이다.
---

### git 활용하기
```
git init #로컬 장소 초기화
git -r .git/ #잘못 만들어진 init 삭제

git status #현재상태를 보여줌
git add [파일명] #staged change로 올라감
git add . #해당 폴더에 있는 내용 전체를 올림

git commit -m "메세지" #커밋하기 / -m은 메세지를 나타냄
git commit --amend #커밋 내용 수정함

git log #여태까지 변경 내역들 확인
```

### github와 local Repository 연결하기
```
git remote add [이름] [레파지토리 링크]
# 이름은 보통 origin 사용

git remote -v #리모트 상태 확인
```

### push : commit 이력이 없으면 push 할 수 없음
```
git push origin master
git push -u origin master
```

### clone / pull
```
git clone [레파지토리 링크]
git pull origin master
```

