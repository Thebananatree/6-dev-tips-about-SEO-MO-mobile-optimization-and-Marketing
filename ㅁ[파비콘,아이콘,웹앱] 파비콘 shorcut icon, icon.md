#### 파비콘 shortcut icon, icon

#####(0).앞서 알아야 할 내용  
.
	1.파비콘 파일은 루트디렉토리(index파일있는곳)에 있어도되고, 서브 디렉토리에 있어도 된다.
	But, 크로스브라우징을 염두에 둔 가장 좋은 설정방법은 루트 디렉토리에 놓는방법이라 한다. 
	,루트디렉토리에 위치시 link태그도 안적어도 된다고 한다.
	[링크 : https://eyoom.net/bbs/board.php?bo_table=tip&wr_id=14]  
	[링크 : https://myseolabo.com/wordpress/what-is-cms]    
.    
	2.link의 type은 내용 유형을 말할 때 쓰이는 것이다. icon태그의 type=image/x-icon , image/png 속성은 해당 이미지의 형태를 알려준다. (ex. x-icon은 ico파일)
	(더쿠,인스티즈, 기타등 shortcut icon의 파일을 뭐로 하냐에 따라 type이 달라진다. 근데, 적어도 되고 안적어도 상관없나보다. 디시인은 안적었다.)
    [링크 : https://aboooks.tistory.com/147]
    +
    추가로
    type 속성의 값은 IE에서만 ICO 파일에 대한 서버의 MIME 값에 영향을 받고 다른 브라우저는 이 속성을 무시한다.
    즉, type 속성은 있어도되고 없어도된다.
    [링크 : https://webdir.tistory.com/337]
.
    3.link의 sizes를 쓰는곳(더쿠)가 있는데, link태그중 rel 속성값이 icon인경우만 사용할 수 있다한다.(더쿠)
    shortcut icon의 경우는 사용할 수 있는지 안나와있고, 이 외에 인스티즈나 디시인에서는 안쓰니 쓰지않는게 좋겠다.
    [링크 : http://www.tcpschool.com/html-tag-attrs/link-sizes]
.
    4.파비콘의 이미지형식에 ico를 쓰는이유는
        [1].여러크기의 이미지를 한파일에 제공해 준다.(multiple size)(PNG는 multiple size 지원안됨)
        [2].모든 브라우저에서 지원이 잘되기 때문이다.(png는 IE11이상부터 지원됨, 그전은 지원안됨, jpg와 gif는 더 지원이 안되는거로 안다.)
        [링크 : https://aqune.tistory.com/33]
.
    5.배경을 투명하게 한 png를 ico파일로 변형시 ico파일의 배경도 투명해짐.
.
    6.gif,jpeg,png등 ico 변환해주는 사이트마다 지원하는 사진형식에따라 가능하다
    [링크 : https://www.icoconverter.com/]
.
    7.jpeg는 배경투명안되고, png는 배경투명되고, gif형태로는 투명되는것 같으나 ico변환하니 불투명된다.
    [직접해보았다.] 
.      
    8.png,jpeg,gif를 ico파일로 변환시킨다 할때, 멀티사이즈 종류 및 갯수에 따라 파일크기가 차이날뿐, png냐 jpeg냐 gif냐
    같고는 ico파일크기에서 그렇게 큰 차이를 보이지 않았다.(png,jpeg등 파일종류보다는 이미지 자체의 변환으로 ico파일로 변환시키기 떄문인것같다.)
    [직접해보았다.]
.
    9.셀럽마인 왕관로고 PNG24를 PNG8로 배경투명으로 하니, 로고가 깨져서 흰색같은것들이 보이는데,이를 그대로 ico파일로
    만드니, 투명한 배경에 흰색잔여물들이 그대로 남았었다. 즉, ico변환은 그대로 보여지는 이미지파일의 모습을 ico파일대로
    변환시키는것같다. 또한, 이렇게 PNG8로 투명배경을 ico파일로 만들어도 PNG24를 변형한것과 파일크기 차이가 안났다.
    [직접해보았다.]    
.
    10.이미지뷰어로 멀티사이즈 ICO파일을 보면, 한장의 아이콘 파일 안에 사용자가 사용하겠다고 지정한 여러가지 아이콘 파일이 들어있는걸 확인할 수 있다 한다.
    [링크 : https://mastmanban.tistory.com/935]
.
    11.인터넷 익스프롤러 구버전(5~9)의 경우 파비콘을 16 X 16 크기로 표시한다. 반면, 익스프롤러 신버전 등에서는 32x32 크기를 사용한다.
    [링크 : https://aqune.tistory.com/33]
.
    12.파일명 표기법
        -파비콘 파일 이름에 사이즈의 크기를 적어주면 개발자가 알아보기 쉽다.
        [링크 : https://webisfree.com/2017-05-23/%ED%99%88%ED%8E%98%EC%9D%B4%EC%A7%80%EC%97%90-%ED%95%84%EC%9A%94%ED%95%9C-%EC%A0%81%EC%A0%88%ED%95%9C-favicon-%EC%82%AC%EC%9D%B4%EC%A6%88%EB%8A%94]
.  
    13.rel이 shortcut icon 처럼 두가지 값을 모두 입력하면, IE6 ~10까지는 이상없이 작동되고, 그 밖의 다른 브라우저는
    rel="icon"처럼 icon값만 입력해도 작동한다.
    [링크 : https://webdir.tistory.com/337]
.      
    파비콘(shortcut icon, icon) 업데이트 문제
        사전설명 : 크롬, 사파리 등 브라우저에서 캐쉬로 이전의 파비콘이 저장되어있어서 나와, 업데이트 된 것이 나오지 않는 경우가 있다.
        1.파비콘의 href의 경로를 full경로로 (ex) http://www.~/favicon.ico")로 해주면 잘 읽어 온다고 하기도 한다.
        [링크 : https://dreamaz.tistory.com/371]
.        
        2.쿠키,방문기록 삭제하고 다시 접속 및 즐겨찾기 등록
.
    파비콘 변환 사이트
        [-https://icoconvert.com/ - 멀티사이즈 가능]    
        [-https://www.icoconverter.com/ - 멀티사이즈 가능 + GIF가능]
.        
#####(1).전체태그
.
	<link rel="shortcut icon" type="~" href="~">
.    
#####(2).기능
.
    파비콘 기능
.
#####(3).사용법
.
	<link rel="shortcut icon" type="~" href="~">
.
#####(4).위치
.
	< /head>태그 바로 앞에(CSS파일들 보다 뒤에 태그넣기) 넣는게 다른 기타문제없이 안전하다하는데, 디시인같은거보면 괜찮기도 한가보다.
	[링크 : https://eyoom.net/bbs/board.php?bo_table=tip&wr_id=14&sst=wr_datetime&sod=desc&sop=and&page=1]
.











아니, 홈 화면 추가 제목이랑 이미지가 도대체 어디서 따온거지? 더쿠,인스티즈,디시인사이드 가늠을 할 수가 없어.
엥, 구글 즐겨찾기에도 파비콘이 아닌 아이콘이 쓰이는건가. https://yomi-tory.tistory.com/70
정리하자
1.디시인사이드는, m.dcinside.com에 파비콘이랑 아이콘 두개 태그 밖에 없는데,
    모바일버전은 title이 디시인사이드다. 그래서 홈 화면 추가해도, 디시인사이드라뜨고(pc버전 반영x)
    그래서, pc버전은 title저리 길게하고, 모바일은 짧게한거구나.(나도 이렇게 해야 겠다.)
2.인스티즈는, 인스티즈라 뜨는이유가, 따로 설정을 해놨기 때문이다.
3.더쿠는 site.manifest로 따로 설정해놨다.    
아, 스크립트로도 조정할 수 있다. - http://chongmoa.com/mobile/5478


<link rel="shortcut icon" href="https://nstatic.dcinside.com/dc/w/images/logo_icon.ico">
    [이건 m.dcinside.com에만 있다.] <link rel="apple-touch-icon-precomposed" href="https://nstatic.dcinside.com/dc/m/img/dcinside_icon.png">
    보면, 아누엔헨은 shortcut icon 코드 밖에 없어서, 아이폰 즐겨찾기 해놔도 아이콘이 안뜬다.
    근데 dcinside.com도 pc웹에서는 shortcut 코드 밖에 없기때문에, 즐겨찾기 하니 아이콘이 아무것도 안뜬다. 즉,
    아이폰 즐겨찾기에서 아이콘이 뜨려면, apple-touch-icon태그를 해야만 한다.


아니 더쿠는 다른 인스티즈와 디시인의 홈 화면 추가 앱이랑 ui가 달라, 또한 추가 기능도 있어.
또한, 더쿠의 홈 화면 추가시 이름이 다른것도, 저 manifest에서 설정하나보다.


1.아니 근데, 더쿠는 홈 화면 추가 했을때, 사파리 주소창이 안보이고 앱같아 보이는데
이는 meta name="apple-mobile-web-app-capable" content=yes가 그 기능을 한다고 한다.
근데, 문제는 더쿠에서 이 코드가 안보임
https://chaewonkong.github.io/posts/pwa.html
아, manifest 이거로 연결하는거구나
https://www.it-swarm.dev/ko/iis/%EC%9B%B9-%EC%82%AC%EC%9D%B4%ED%8A%B8%EC%97%90%EC%84%9C-iis-webmanifest-%ED%8C%8C%EC%9D%BC%EC%9D%84-%EC%98%AC%EB%B0%94%EB%A5%B4%EA%B2%8C-%EC%A0%9C%EA%B3%B5%ED%95%98%EB%A0%A4%EB%A9%B4-%EC%96%B4%EB%96%BB%EA%B2%8C%ED%95%B4%EC%95%BC%ED%95%A9%EB%8B%88%EA%B9%8C/837357566/
https://joshua1988.github.io/web-development/pwa/webapp-manifest/

아니, 도대체 더쿠는 앱같아보이게 어떻게 하는거야
https://doolyit.tistory.com/152 이게 조금 가까운것같다. script사용
pickk.one도 웹앱이다. 참고하기
https://opens.kr/64
https://developers.google.com/web/fundamentals/native-hardware/fullscreen?hl=ko
음, meta태그 같은게 아니면 script일 확률이 높고 둘중 어느걸 사용하는게 좋을지는 알아서 하기
아니면...
manifest.json파일에서 display:fullscreen한것만으로도 설마 그게 되는건가? 더쿠는 어떤가
더쿠는 browser인데


또, 한가지 신기한게, 사파리 웹으로 되는게 아니라 일종의 앱처럼 개별적으로 차지해(더쿠나, 핔 둘다.)
이게 manifest 파일때문에 이런건가. 그리고 manifest파일에 start_url 부분 안적으면
처음 홈 화면 등록할 당시의 화면이 자꾸 뜬다한다한다.
https://developers.google.com/web/tools/lighthouse/audits/manifest-contains-start_url?hl=ko


link href="manifest", manifest.json 이게 자동으로
아이콘 생성에 영향을 준다.
https://sicrap.tistory.com/3


아니 거기다가,
1.더쿠 pc화면 보기하니 그 후로 계속 껏다켜도 pc화면으로 보임
2.근데 막상 카테고리 누르면 모바일 최적화로 나옴(?이게뭐지)
3.근데 또 맨 아래 모바일 최적화로 보기 버튼이 있다.
4.2번과 3번처럼 한 같은화면의 내용물이 다름. 이게 뭘까 도대체

link태그의 rel속성 manifest에서
site.webmanifest 과 manifest.json이 있는데, 둘의 차이는 
manifest.json은 많이 사용하고 있으나, webmanifest는 wc3에서 명시하고 있다한다.
더쿠는 webmanifest, 핔은 manifest.json,
참고링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs
그리고 고려해야할게, 이 부분이 혹시 네이버 대표사이트에 영향을 주는건 아니겠지(디시인이나 인스티즈는 없다. 사실 얘네는 앱이 있어서 안한걸수도)



아, apple-touch-icon은 모두 인스,더쿠,디시 모두 png로 해놓았네

더쿠는 파비콘,아이콘 되있는건 이게 전부다.
< link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="manifest" href="/site.webmanifest">
[얘는 전부 png로 했네]

디시인은 이게 끝인데?
<link rel="shortcut icon" href="https://nstatic.dcinside.com/dc/w/images/logo_icon.ico">
[이건 m.dcinside.com에만 있다.] <link rel="apple-touch-icon-precomposed" href="https://nstatic.dcinside.com/dc/m/img/dcinside_icon.png">
근데, 이 apple-touch-icon-precomposed같은게 없으면, 그냥 홈페이지 첫화면 캡쳐해서 뜨나본데 -> anuandhenn.com

인스티즈는 이게 끝(+아니 근데, 저 href 아래에 있는거 따라가도 없던데?)
<link href="//static.instiz.net/favicon.ico?1907071" rel="shortcut icon" type="image/x-icon">
<link href="//static.instiz.net/m/images/ico_android_kor.png?1907071" rel="apple-touch-icon-precomposed">
<meta name="google-play-app" content="app-id=net.instiz.www.instiz">
<meta name="apple-itunes-app" content="app-id=1218109903">
<meta name="apple-mobile-web-app-title" content="인스티즈">

플레이송즈는
<link rel="icon" type="image/png" href="/fa_ps.png">

아누엔핸은
<link rel="shortcut icon" href="/web/upload/favicon_20200216214949.ico">

https://cafe.naver.com/hacosa/21686
apple-touch-icon-precomposed은 안드로이드의 홈 추가 아이콘에도 적용된다함


그 패드(안드로이드 크롬)에서 홈 화면 추가하니까, 아누에핸은 title 그대로 이름이 생겨지고, 플레이송즈는
title이 없다보니 그냥 m.playsongs.co.kr이 새겨진다. 그리고 둘다 아이콘이 없어서 각각 아누에핸의 첫글짜 a
플레이송즈의 첫글자 p가 뜨게된다.


네이버는
모바일에는
<link rel="apple-touch-icon-precomposed" href="https://s.pstatic.net/static/www/mobile/edit/2019/0520/mobile_ios_iphone_120120.png">
<link rel="apple-touch-icon-precomposed" sizes="180x180" href="https://s.pstatic.net/static/www/mobile/edit/2019/0520/mobile_ios_iphone_180180.png">
<link rel="shortcut icon" type="image/x-icon" href="/favicon.ico?7"> 이 3개가 있고,
pc버전에는
<link rel="shortcut icon" type="image/x-icon" href="/favicon.ico?7">
이거 하나 밖에 없다.
근데 네이버는 파비콘을 ?가 있긴한데 루트 디렉토리에 놓았네

네이버도 이거 있다. <meta name="apple-mobile-web-app-title" content="NAVER">

네이버도 <link rel="shortcut icon" type="image/x-icon" href="/favicon.ico?1"> 이렇게 물음표쓴다.

https://m.blog.naver.com/PostView.nhn?blogId=bhher&logNo=220788983128&proxyReferer=https:%2F%2Fwww.google.com%2F
https://support.wix.com/ko/article/iphone-ipad-android%EA%B8%B0%EA%B8%B0-%ED%99%88%ED%99%94%EB%A9%B4-%EC%95%84%EC%9D%B4%EC%BD%98-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0

https://aqune.tistory.com/33



경로에 /부터 적는거는, 그냥 표기해주는것같다.



아니 근데, 인스티즈의 저 link href에서 ?는 뭐야, pavicon.ico? , 네이버도.



http://static.instiz.net/m/images/ico_apple_kor.png?1907071
http://static.instiz.net/favicon.ico?1907071
인스티즈보면, 이거 치면 따로 아이콘들이 있는데 아마 아마존 클라우드 서비스로 어떻게연결하나보다.







https://eyoom.net/bbs/board.php?bo_table=tip&wr_id=14 - 엥 여기 파비콘 아이콘 만드는데, manifest 파일도 같이 있는데?