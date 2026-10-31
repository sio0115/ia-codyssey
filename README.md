개발자 작업실 구축 프로젝트
1. 프로젝트 소개

개발자로서 필요한 기본 개발 환경을 직접 구축하고 관리하는 것을 목표로 한다.

Windows 환경에서 터미널, 파일 및 디렉토리 관리, 권한 설정 등을 실습하고, 이후 Docker와 Git/GitHub를 활용한 개발 환경 구축을 진행한다.

2. 개발 환경
OS: Windows
터미널: PowerShell
작업 디렉토리: developer-workstation
Docker: 실습 예정
Git: 설치 완료
3. 폴더 구조
text
developer-workstation/
├── app/
├── docs/
└── evidence/

app: 웹 서버 소스코드 저장 공간
docs: 기술 문서 저장 공간
evidence: 실습 결과 스크린샷 저장 공간
4. 실습 진행 내용
4-1. 터미널 기본 조작
현재 위치 확인: Get-Location
폴더 이동: cd
폴더 및 파일 목록 확인: Get-ChildItem
폴더 생성: New-Item
파일 존재 여부 확인: Test-Path
4-2. 파일 및 디렉토리 관리

작업실 내부에 app, docs, evidence 폴더를 생성하고 폴더 이동 및 상위 폴더 복귀를 실습했다.

4-3. 파일 권한 실습

Windows의 icacls 명령어를 이용해 파일과 디렉토리의 권한을 확인하고 수정 권한을 설정했다.

사용한 명령어:

powershell
icacls.exe ".\docs\permission-test.txt"

powershell
icacls.exe ".\docs\permission-test.txt" /grant:r "$($env:USERDOMAIN)\$($env:USERNAME):(M)"

powershell
icacls.exe ".\docs"


실습 결과:

파일 권한 확인 성공
파일 수정 권한 설정 성공
디렉토리 권한 확인 성공
디렉토리 수정 권한 설정 성공
4-4. Git 설치

Git for Windows 설치 완료.

버전 확인 명령어:

powershell
git --version

5. 향후 실습 계획
Linux 권한 실습 (755, 644)
Docker 설치 및 기본 점검
hello-world 컨테이너 실행
Ubuntu 컨테이너 실행
Dockerfile 작성 및 커스텀 이미지 제작
포트 매핑 및 웹 서버 접속
바인드 마운트 실습
Docker 볼륨 영속성 검증
Git 설정 및 GitHub 연동
최종 결과물 및 증거 자료 정리
6. 학습 목표

명령어를 단순히 따라 입력하는 것에 그치지 않고, 각 명령어의 목적과 실행 결과를 이해하며 개발 환경을 구축하는 것을 목표로 한다.
