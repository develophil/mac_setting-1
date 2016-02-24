# 업무준비 & mac_setting
업무 환경설정 및 맥북 유틸 세팅

##맥환경설정 유틸
shift it : 작업창 자동 화면분할 | http://shift-it.en.softonic.com/mac

Parallels Desktop : 멀티 운영체제 사용 프로그램 | http://www.parallels.com/kr/

Microsoft Remote Desktop : 윈도우 원격 접속 | 앱스토어

karabiner : 키보드 리매퍼(키보드 세팅) | https://pqrs.org/osx/karabiner/
> OS X 10.11 엘 캐피탄부터 입력 소스 단축키가 바뀌었다..( `command`+`space` -> `control`+`space` )
따라서 karabiner 사용자는 다음 소스를 아래 경로에 설정해줘야 쉽게 사용할 수 있음..
```preference > Misc & Uninstall > Custom Setting > Open private.xml``
```xml
<?xml version="1.0"?>
<root>
    <item>
        <name>한영키, 한자키 적용</name>
        <appendix>한영키 -> Ctrl+Space, 한자키 -> Opt+Return</appendix>
        <identifier>private.haneng_and_hanja</identifier>
        <autogen>
            __KeyToKey__
            KeyCode::COMMAND_R,
            KeyCode::SPACE, ModifierFlag::CONTROL_L
        </autogen>
        <autogen>
            __KeyToKey__
            KeyCode::OPTION_R,
            KeyCode::RETURN, ModifierFlag::OPTION_L
        </autogen>
    </item>
</root>
```
`Reroad XML` 눌러서 등록된 설정 체크 하면 오른쪽 `command`키는 한/영키로, 오른쪽 `option`키는 한자키로 매핑된다.

iterm2 : 좀 더 쉬운 터미널 사용을 위한 유틸 - 창분할, 자동완성, 텍스트선택/복사, 단축키설정, 검색 등 | http://www.iterm2.com/#/section/home

Caffeine : 잠자기모드 방지 | https://itunes.apple.com/kr/app/caffeine/id411246225?mt=12


##개발관련 유틸
postman : web api test HTTP 클라이언트 request 생성기 | chrome 확장 프로그램

Filezilla : 무료 FTP 프로그램 | https://filezilla-project.org/

Gas mask : 호스트파일매니저. 여러 호스트 파일 전환 | http://clockwise.ee/

Atom : github가 만든 에디터. | https://atom.io/
> Preferences > Install > git-control 검색 > install


Sublime Text 3	https://www.sublimetext.com/3

macdown : 맥용 마크다운 에디터 | http://macdown.uranusjr.com/

Chrome : 크롬브라우저 | https://www.google.co.kr/chrome/browser/desktop/

homebrew : package manager	| http://brew.sh
HomeBrew를 이용한 git 설치 - 터미널에서 아래의 명령어를 입력.
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
HomeBrew 설치후 아래의 명령어를 입력한다.
```
# brew install git
# brew install curl --with-ssl --with-libssh2
# brew install git-ftp
```


##협업/ 메신저
카카오톡 : 무료 통화/메시지 앱 | http://www.kakao.com/talk/ko

Jandi : 한국형 업무 커뮤니케이션 툴 | https://www.jandi.com/landing/kr

Line : 무료 통화/메시지 앱 | http://line.me/ko/

asana : 업무 일정 관리 | https://app.asana.com/

일정 간트차트 연동 | http://instagantt.com/app
