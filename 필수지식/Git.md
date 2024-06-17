# Git

### 빠르고 효율적인 분산형 버전 관리 시스템

버전 관리 → 소스코드의 변경 내역을 추적하고 관리

> 💡 빠르고 효율적인 이유 ?
Linux 커널에서 작동하도록 구축 → 처음부터 대규모 저장소를 효과적으로 처리해야했다 (커널은 작고 복잡하니)
C로 작성되어 고급언어와 관련된 런타임 오버헤드를 줄였다.
최선 버전이 아닌 전체 기록을 다운하는 초기 복제 작업을 제외하면 SVN대비 2배까지 빠르다.

### Github ?

- Git 저장소 관리 서비스

## 구성 요소

- Working Tree (Working Directory)
    - 작업하고 있는 파일이 있는 장소 즉, 폴더
- Staging area
    - commit 전 예비 저장소
- Repository
    - Local
        - local pc에 저장되는 개인 저장소
    - Remote
        - 원격 저장소

### 기본 동작 원리

수정 → snapshot 대기 → 레포 저장

Git에서의 SnapShot
변경 내역을 추적하여 관리 
파일 변동 → 전체 저장 (snapShot) 

> 전체를 저장 후 비교하는 방식이 효율적인 이유 
기존 SVN에서 사용하던 델타형식은 변경사항 관리 → 10000개면 1부터 변경사항 찾아야함              
git은 변경사항이 없으면 같은 blob(파일 저장객체 = 각각의 해시 = 데이터 무결성)처리 → 중복x 
특점 시점시 snapShot만으로 빠른 비교가능
### 자주 사용하는 명령어의 동작

- add
    - 로컬의 변동 사항을 staging
- Commit (각각의 해시값을 가지며, 변경 내역 추적 가능)
    - 특정시점의 snapshot을 찍어 새로운 version을 저장
- branch
    - 독립적인 작업을 위해 코드의 다른 버전 관리
- rebaseT
    - 특정 시점으로 작업환경 변경
- merge
    - 두개 이상의 브랜치를 합치는 작업
- fetch
    - remote repository 의 변경사항 → local repository 복사본 저장 (변화 감지)
- pull (fetch + merge)
    - remote repository 의 변경사항 → local repository 적용
- clone
    - remote repository → local repository 복사
- reset
    - 현재 작업 내용 보관가능 (soft options)
- revert
    - 현재 작업 내용 날라감

### Commit 원리

스냅샷의 최상위 객체
커밋 객체 생성 → 루트 트리 객체 → 파일과 하위 디렉토리 트리 (커밋 메세지, 작성자 정보, 부모커밋에 대한 참조 등 포함)

⇒ tree객체로 이루어진 특정시점 스냅샷(commit) 비교 가능