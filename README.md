# 깃허브 마스터하기

## 1. 원하는 폴더에서 Git 초기화를 하면 그때부터 사용 가능

    1-1. **[git init]**
    1-2. Git 초기화를 하면 .git이라는 숨겨진 폴더가 만들어진다. 이 곳이 바로 로컬저장소이다.
    1-3. 로컬 저장소에 내가 만든 버전 정보, 원격 저장소 주소 등이 저장된다.
    1-4. 원격 저장소에서 내 컴퓨터로 코드를 받아오면 로컬 저장소가 자동으로 생긴다.
    1-5. 한 폴더에 하나의 로컬 저장소만 유지해야 한다. git init은 한번만

    **[pwd]** 현재 폴더 위치 확인
    **[ls]** 현재 하위 폴더들 확인

2.  **[git add README.md]**
    **[git commit -m "README.md 추가"]**
    **[git log]** git을 커밋했는지 안 했는지 확인

    전체 파일을 추가하고 싶으면 **[git add .]**
    **[git commit -m "메인 페이지 생성"]**

    -   커밋은 의미있는 변동사항을 묶어서 만든다.
        예를 들어 버튼 클릭 버그를 고치는데 5가지 파일을 수정했다면 그 5가지를 묶어 하나의 커밋으로 만든다.(그래야지 동료개발자가 버튼 클릭 버그를 고치는데 어떤 파일을 수정하였는지 손쉽게 파악 가능)

3.  github 사이트에서 프로젝트 저장소 만들기

4) 내 컴퓨터 프로젝트 폴더에 github 저장소 주소 알려주기
   **[git remote add origin https://github.com/hyekyeong123/gitmaster_study.git]**

    원격 저장소 연결을 제거할때에는 git remote remove [저장소 이름] 을 사용

5. 내 컴퓨터에 만들었던 덩어리 github에 올리기
   로컬저장소 -> 원격 저장소
   **[git push origin master]]**
   origin은 remote 이름//master은 브린치 이름

    **failed to push some refs to** 이러한 오류가 뜸
    그래서 **[git pull, git push -f origin master]**을 하였음(커밋 이력을 강제로 덮어 씌우는 것)

---

6. 다른 사람이 만든 것을 가져오기
   6-1. 원격 저장소를 내 컴퓨터에 받아오기(clone)
   클론을 하면 원격 저장소의 코드를 내 컴퓨터에 받아올 수 있음.
   로컬저장소(.git 폴더)도 자동으로 생김
   **[git clone https://github.com/hyekyeong123/gitmaster_study.git .]**
   //저 명령어를 그대로 쓰니 폴더까지 복사해버림
   //일단 삭제 후 뒤에 .을 붙여서 복사


    6-2. 업데이트 된 데이터가져오기(pull)
    **[git pull origin master]**

    6-3. 다른 사용자도 커밋을 만들어서 원격 저장소로 push 할 수 있음
    몰론 원격 저장소에 푸시 권한이 있을 경우

    복싱 사이트 짱
    ## 기능 목록
    1. 스파링 상대 찾기
