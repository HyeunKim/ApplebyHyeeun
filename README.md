# ApplebyHyeeun

한동대학교 2022년도 하계 SW 아카데미의 웹서비스프로젝트(Spring) 캠프에서 진행한 1인 개발 프로젝트입니다.

Apple 사이트의 일부 파트를 클론코딩하였습니다.

개발에 앞서, 1주차 개발 환경설정을 기록합니다.

## 닷홉(dothome)

1. 닷홈 가입
2. 무료 호스팅 신청
3. 호스팅 완료

## vscode 및 확장자 설치

- sftp
- html snippets
- vscode 한글 설정 : utf-8
  1. vscode 에디터 창 새 파일에서 html 입력
  2. html:5 선택
  3. 이후 입력한 한글들은 깨짐 없이 잘 나타난다.
- 로컬에 작업 폴더 생성 및 vscode 작업 영역에 생성한 폴더 추가
- ftp 연결
  - 키보드 command + shift + p 해서 SFTP: Config 선택
    - name은 dothome
    - host는 아까 닷홉 호스팅 신청하면서 기입해서 만들어진 주소
    - protocol ftp로 변경
    - port 21로 변경
    - username은 host의 앞부분
  - 구름모양 아이콘 클릭
  - 폴더 클릭
  - 비밀번호 입력
  - 연결 완료
    - local에서 작업하고 싶을 경우 우클릭-Edit in Local을 누른다.
    - local에서 작업한 후 우클릭-Upload.

## FileZilla

- 이미지 이동 쉽게
- 원격 - 로컬 간 파일 이동

1. 설치
2. 빠른 연결
   - 호스트
   - 사용자명
   - 비밀번호
   - port는 x
   - 이후 빠른 연결 클릭
3. 로컬에 있는 파일(로컬에 저장해둔 원하는 이미지 파일) 원격 img 폴더 생성 후 드래그앤드롭.
4. html 폴더도 생성 후 간단한 index.html 파일을 만들어 이미지 태그 삽입해서 이미지 폴더에 잘 들어가 있는지 체크

## vscode github 연동, git 사용

1. github 사이트에서 새로운 레포지토리 생성
2. url 복사
3. vscode 공유(?) 아이콘 클릭
4. 새로운 레포 연결 선택
   1. 나는 실패해서 터미널에 명령어를 입력했다
5. git init
6. git remote add origin 복사한 레포 주소
7. 만약 브랜치 생성해서 작업한다면
   1. git checkout -b hyeeun : 브랜치 생성 후 해당 브랜치로 바로 이동
   2. git branch : 작업하고 있는 브랜치 확인
   3. git pull origin main(아니면 원하는 브랜치)
      - pull은 fetch + merge
   4. git add .
      1. '+' 눌러서 스
   5. git commit -m "커밋 메시지 ~~.."
   6. git push -u origin main
   7. git checkout main
   8. git merge hyeeun : hyeeun 브랜치에서 push 한 내용 main 부분이랑 merge(합치기)
   9. github에서 commit 내역 및 변동 사항 적용됐는지 확인
   10. git branch -d hyeeun : 브랜치 삭제
8. 브랜치 다 삭제되고 main만 있는 상황이라면,
   1. git add .
   2. git commit -m "commit message"
   3. git push -u origin : 바로 main에 푸쉬 및 업데이트
   4. github에서 확인
