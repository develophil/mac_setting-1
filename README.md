##맥환경설정 유틸
shift it : 작업창 자동 화면분할 | http://shift-it.en.softonic.com/mac

Parallels Desktop : 멀티 운영체제 사용 프로그램 | http://www.parallels.com/kr/
> parallels tools 설치 - mac과 파일 공유 위해


(*) Microsoft Remote Desktop : 윈도우 원격 접속 | 앱스토어

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

karabiner-elements : 키보드 리매퍼(키보드 세팅) | https://github.com/tekezo/Karabiner-Elements
> OS X 10.12 씨에라부터는 기존 karabiner가 사용이 안된다.... 이게 웬... 그 대안으로 이걸 사용해야지.. 
근데 이건 1 : 1 매핑밖에 되지 않는다....ㅠㅠ

iterm2 : 좀 더 쉽고 기능 많은 터미널 - 창분할, 자동완성, 텍스트선택/복사, 단축키설정, 검색 등 | http://www.iterm2.com/#/section/home

Caffeine : 잠자기모드 방지 | https://itunes.apple.com/kr/app/caffeine/id411246225?mt=12

amphetamine : sierra 버전에선 Caffeine이 안되서 이걸로 사용 : https://itunes.apple.com/kr/app/amphetamine/id937984704?mt=12

##개발관련 유틸
postman : web api test HTTP 클라이언트 request 생성기 | chrome 확장 프로그램

(*) Filezilla : 무료 FTP 프로그램 | https://filezilla-project.org/

Gas mask : 호스트파일매니저. 여러 호스트 파일 전환 | http://clockwise.ee/

(*) Atom : github가 만든 에디터. | https://atom.io/
> 패키지 설치 : Preferences > Install > 패키지 검색
> - git-control
> - convert-to-utf8
> - Remote-FTP
> - language-asp


Sublime Text 3	https://www.sublimetext.com/3

macdown : 맥용 마크다운 에디터 | http://macdown.uranusjr.com/

Chrome : 크롬브라우저 | https://www.google.co.kr/chrome/browser/desktop/

! homebrew : package manager	| http://brew.sh
> HomeBrew 설치 - 터미널에서 아래의 명령어를 입력.
>
	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

> HomeBrew를 이용한 git, git-ftp 설치
> 
	# brew install git
	# brew install curl --with-ssl --with-libssh2
	# brew install git-ftp

> git-ftp 설치 후 세팅
>
	git config git-ftp.user wooripension
    git config git-ftp.password dnfl\!\$%vpstus
     : 비번에 `!$`가 포험되어 `\!\$`로 대체함
    git config git-ftp.syncroot /Users/Leo/Work/wooripension_asp_source/www
    git config git-ftp.deployedsha1file leosha1.log
    git config git-ftp.url ftp://14.0.89.145

    1)로컬에만 파일이있고 아직 FTP에 아무 파일도 업로드 되지 않은 상태라면 다음 명령어를 사용하여 초기화 한다.
        git ftp init --user [ftp사용자] --passwd [ftp비번] - ftp://www.example.com
    2)로컬에 파일이 있으며 이미 동일한 모든 파일이 수동으로 FTP에도 업로드가 되어있는 경우 다음명령어를 통해 초기화 한다.
        git ftp catchup -u [ftp사용자] -p [ftp비번] - ftp://www.example.com
    3)이미 위의 명령어들을 통해 초기화 되어있는 상황에서, 로컬에 수정사항을 서버로 업로드하고싶을경우 다음 명령어를 사용한다.
        git ftp push -u [ftp사용자] -p [ftp비번] - ftp://www.example.com

    깃 설정을 통해 미리 아이디, 패스워드, 소스경로, FTP경로를 설정할 수 있다.
    $ git config git-ftp.user john
    $ git config git-ftp.url ftp.example.com
    $ git config git-ftp.password secr3t
    $ git config git-ftp.syncroot path/dir
    미리 설정한 경우
    git ftp push -A
    git ftp catchup -A 명령어만 입력하면 된다. 

> HomeBrew를 이용한 java 설치
>
	$ brew update
	$ brew tap caskroom/cask
    $ brew install Caskroom/cask/java

(*) sourcetree : GUI 환경의 git 컨트롤러 | https://www.sourcetreeapp.com/
> github와 연동 : LeoDevPhil
> remote github : wooripension_asp_source clone 받을것


##협업/ 메신저
카카오톡 : 무료 통화/메시지 앱 | http://www.kakao.com/talk/ko

(*) Jandi : 한국형 업무 커뮤니케이션 툴 | https://www.jandi.com/landing/kr

Line : 무료 통화/메시지 앱 | http://line.me/ko/

(*) asana : 업무 일정 관리 | https://app.asana.com/

일정 간트차트 연동 | http://instagantt.com/app





##개인환경세팅
LiteIcon : 아이콘 쉬운 교체 |

CandyBar : 쉬운 아이콘 관리 |

Icons8 Lite : 간단한 클립아트 검색 | https://icons8.com/app/#/ios

Automator 세팅
> - finder 실행 액션 추가 : `control` + `shift` + `command` + E
> - 화면보호기 실행 액션 추가 : `control` + `alt` + `command` + L


PhotoScape X : 쉬운 사진 편집기 | http://x.photoscape.org/mac/

Android file transfer : 안드로이드 파일 이동 | https://www.android.com/filetransfer/

Numi : 서술형 계산기 | http://macnews.tistory.com/4181

checkor : 한글 맞춤법/ 문법 체크 | http://blog.mywizz.io/checkor-for-mac

alfred : spotlight 보다 향상된 검색/ 수행기 | https://www.alfredapp.com/
> keyword를 등록하여 이동 액션 커스터마이징하여 사용하기 좋음
> Features - Web Search - Add Custom Search

VLC : 동영상 플레이어 | http://www.videolan.org/vlc/

pocket : 콘텐츠 즐겨찾기 서비스 | https://getpocket.com/mac/?a=mac

evernote : 메모, 콘텐츠 저장/ 공유 | 앱스토어. | https://evernote.com

skitch : 간단한 화면캡쳐 및 이미지 편집툴 | 앱스토어. http://macworld.hjsong.net/44

coconut battery : 배터리 상태 체크 | http://www.coconut-flavour.com/coconutbattery/

quicksilver : 검색/ 실행기. spotlight, alfred의 원조 | https://qsapp.com/

cheatsheet : 활성화면 단축키 보기 | https://www.mediaatelier.com/CheatSheet/

hotkey-eve : 단축키가 등록된 액션을 수행하면 알림으로 단축키 알려줌 | http://www.hotkey-eve.com/

clipmenu : 클립보드/스니펫 매니저 | http://www.clipmenu.com

clipy : clipmenu를 계승 발전시킨 앱. 클립메뉴는 더이상 업데이트가 안된다나... : https://clipy-app.com/

betterTouchTool : 멀티 제스쳐 확장 프로그램 | https://www.boastr.net/
