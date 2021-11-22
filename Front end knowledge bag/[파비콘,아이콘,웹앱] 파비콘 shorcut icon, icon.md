#### 파비콘 shortcut icon, icon

#####(0).앞서 알아야 할 내용  
.
	1.파비콘 파일은 루트디렉토리(index파일있는곳)에 있어도되고, 서브 디렉토리에 있어도 된다.
	    But, 크로스브라우징을 염두에 둔 가장 좋은 설정방법은 루트 디렉토리에 놓는방법이라 한다. 
	    ,루트디렉토리에 위치시 link태그도 안적어도 된다고 한다.(더쿠는 png이지만 루트디렉토리에 놓긴했다.)
	    [참조링크 : <https://eyoom.net/bbs/board.php?bo_table=tip&wr_id=14>]  
	    [참조링크 : <https://myseolabo.com/wordpress/what-is-cms>]    
.    
	2.link의 type은 내용 유형을 말할 때 쓰이는 것이다. icon태그의 type="image/x-icon" , "image/png" 속성은 해당 이미지의 형태를 알려준다. (ex. x-icon은 ico파일)
	    (더쿠,인스티즈, 기타등 shortcut icon의 파일을 뭐로 하냐에 따라 type이 달라진다. 근데, 적어도 되고 안적어도 상관없나보다. 디시인은 안적었다.)
        [참조링크 : <https://aboooks.tistory.com/147>]
        +
        추가로
        type 속성의 값은 IE에서만 ICO 파일에 대한 서버의 MIME 값에 영향을 받고 다른 브라우저는 이 속성을 무시한다.
        즉, type 속성은 있어도되고 없어도된다.
        [참조링크 : <https://webdir.tistory.com/337>]
.
    3.link의 sizes를 쓰는곳(더쿠)가 있는데, link태그중 rel 속성값이 icon인경우만 사용할 수 있다한다.(더쿠)
        shortcut icon의 경우는 사용할 수 있는지 안나와있고, 이 외에 인스티즈나 디시인에서는 안쓰니 쓰지않는게 좋겠다.
        [참조링크 : <http://www.tcpschool.com/html-tag-attrs/link-sizes>]
.
    4.파비콘의 이미지형식에 ico를 쓰는이유는
        [1].여러크기의 이미지를 한파일에 제공해 준다.(multiple size)(PNG는 multiple size 지원안됨)
        [2].모든 브라우저에서 지원이 잘되기 때문이다.(png는 IE11이상부터 지원됨, 그전은 지원안됨, jpg와 gif는 더 지원이 안되는거로 안다.)
        [참조링크 : <https://aqune.tistory.com/33>]
.
    5.배경을 투명하게 한 png를 ico파일로 변형시 ico파일의 배경도 투명해짐.
.
    6.gif,jpeg,png등 ico 변환해주는 사이트마다 지원하는 사진형식에따라 가능하다
        [참조링크 : <https://www.icoconverter.com/>]
.
    7.jpeg는 배경투명안되고, png는 배경투명되고, gif형태로는 투명되는것 같으나 ico변환하니 불투명된다.
        [직접해봄] 
.      
    8.png,jpeg,gif를 ico파일로 변환시킨다 할때, 멀티사이즈 종류 및 갯수에 따라 파일크기가 차이날뿐, png냐 jpeg냐 gif냐
        같고는 ico파일크기에서 그렇게 큰 차이를 보이지 않았다.(png,jpeg등 파일종류보다는 이미지 자체의 변환으로 ico파일로 변환시키기 떄문인것같다.)
        [직접해봄]
.
    9.셀럽마인 왕관로고 PNG24를 PNG8로 배경투명으로 하니, 로고가 깨져서 흰색같은것들이 보이는데,이를 그대로 ico파일로
        만드니, 투명한 배경에 흰색잔여물들이 그대로 남았었다. 즉, ico변환은 그대로 보여지는 이미지파일의 모습을 ico파일대로
        변환시키는것같다. 또한, 이렇게 PNG8로 투명배경을 ico파일로 만들어도 PNG24를 변형한것과 파일크기 차이가 안났다.
        [직접해봄]    
.
    10.이미지뷰어로 멀티사이즈 ICO파일을 보면, 한장의 아이콘 파일 안에 사용자가 사용하겠다고 지정한 여러가지 아이콘 파일이 들어있는걸 확인할 수 있다 한다.
        [참조링크 : <https://mastmanban.tistory.com/935>]
.
    11.인터넷 익스프롤러 구버전(5~9)의 경우 파비콘을 16 X 16 크기로 표시한다. 반면, 익스프롤러 신버전 등에서는 32x32 크기를 사용한다.
        [참조링크 : <https://aqune.tistory.com/33>]
.
    12.파일명 표기법
        -파비콘 파일 이름에 사이즈의 크기를 적어주면 개발자가 알아보기 쉽다.
        [참조링크 : <https://webisfree.com/2017-05-23/%ED%99%88%ED%8E%98%EC%9D%B4%EC%A7%80%EC%97%90-%ED%95%84%EC%9A%94%ED%95%9C-%EC%A0%81%EC%A0%88%ED%95%9C-favicon-%EC%82%AC%EC%9D%B4%EC%A6%88%EB%8A%94>]
.  
    13.rel이 shortcut icon 처럼 두가지 값을 모두 입력하면, IE6 ~10까지는 이상없이 작동되고, 그 밖의 다른 브라우저는
        rel="icon"처럼 icon값만 입력해도 작동한다.
        [참조링크 : <https://webdir.tistory.com/337>]
.    
    14.아래 링크에 보면 최신글 타이틀 폰트 사이즈가 작아지는 문제가 있다하니까, 작성자가 CSS파일들을 모두 로딩한 다음에 태그를 적어야
        문제가 발생하지 않는다 한다.
        근데, 이게 바로 픽이나 인스티즈나 맥북 프로 메인즐겨찾기 화면 아이콘이 작게 뜨는거나, 아이폰 사파리 메인즐겨찾기 화면 아이콘이 작게뜨는거랑
        연관지어 생각할 수도 있다. 더쿠는 그런문제가 전혀 없는데, css파일 링크하는 태그가 모두 shortcut icon, apple-touch-icon태그보다 앞에 있다.
        (엣지, 메인 화면 즐겨찾기 아이콘에 인스티즈는 작은 아이콘으로 뜬다. 근데 이건 shortcut icon이 반영되는거다.여기선 아누앤핸도 작게뜨는데, css링크보다 shorcut이 앞에있다.)
        [참조링크 : <https://eyoom.net/bbs/board.php?bo_table=tip&wr_id=14&sst=wr_datetime&sod=desc&sop=and&page=1>]
.    
    파비콘(shortcut icon, icon) 업데이트 문제
        사전설명 : 크롬, 사파리 등 브라우저에서 캐쉬로 이전의 파비콘이 저장되어있어서 나와, 업데이트 된 것이 나오지 않는 경우가 있다.
        1.파비콘의 href의 경로를 full경로로 (ex) http://www.~/favicon.ico")로 해주면 잘 읽어 온다고 하기도 한다.
        [참조링크 : <https://dreamaz.tistory.com/371>]
.        
        2.쿠키,방문기록 삭제하고 다시 접속 및 즐겨찾기 등록
.
    파비콘 변환 사이트
        [-https://icoconvert.com/ - 멀티사이즈 가능]    
        [-https://www.icoconverter.com/ - 멀티사이즈 가능 + GIF가능]
.        
#####(1).전체태그
.
	<link rel="shortcut icon" type="image/x-icon" href="~">
.    
#####(2).기능
.
    파비콘 기능
.
#####(3).사용법
.
	< link rel="shortcut icon" type="~" href="~">
.
#####(4).위치
.
    < link rel="apple-touch-icon-precomposed" href="~">
    < link rel="shortcut icon" type="image/x-icon" href="~">
    < link rel="manifest" href="~.webmanifest">
.

