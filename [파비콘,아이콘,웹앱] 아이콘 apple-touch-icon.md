#### 아이콘 apple-touch-icon
   
#####(0).앞서 알아야 할 내용  
.
	1.apple-touch-icon기능을 m.도메인이 아닌 www.도메인에는 안써주면 맥북 사파리의 즐겨찾기 아이콘에 안뜬다. - 디시인사이드
	    즉, pc html에도 apple-touch-icon을 적어주는게 좋다.
.    
    2.apple-touch-icon의 -precomposed를 붙이는건, 아이콘에 비주얼 효과를 막기 위한 것인데, 사각모서리 테두리, 
        drop shadow, reflective shine인 3가지 효과를 막기 위해 사용한다. 근데 이는 ios7이나 그 이후에는 이 3가지
        효과가 아무것도 적용이 안되기 때문에 ios7이나 그 위의 버전만 고려한다면 precomposed를 적어줄 필요 없다.      
        그리고 안드로이드 2.1버전은 오직 precomposed된 icon만 지원한다 한다.
        (근데, 2011년 글이고 옛날 버전을 고려한거네)  
        [링크 : https://mathiasbynens.be/notes/touch-icons]
        또한, 이렇게 지정한 precomposed 아이콘 이미지는 안드로이드 홈 화면 추가기능에도 지원된다함
        [링크 : https://m.blog.naver.com/PostView.nhn?blogId=bhher&logNo=220788983128&proxyReferer=https:%2F%2Fwww.google.com%2F]
.    
    3.아래 링크에 보면 최신글 타이틀 폰트 사이즈가 작아지는 문제가 있다하니까, 작성자가 CSS파일들을 모두 로딩한 다음에 태그를 적어야
        문제가 발생하지 않는다 한다.
        근데, 이게 바로 픽이나 인스티즈나 맥북 프로 메인즐겨찾기 화면 아이콘이 작게 뜨는거나, 아이폰 사파리 메인즐겨찾기 화면 아이콘이 작게뜨는거랑
        연관지어 생각할 수도 있다. 더쿠는 그런문제가 전혀 없는데, css파일 링크하는 태그가 모두 shortcut icon, apple-touch-icon태그보다 앞에 있다.
        (엣지, 메인 화면 즐겨찾기 아이콘에 인스티즈는 작은 아이콘으로 뜬다. 근데 이건 shortcut icon이 반영되는거다.여기선 아누앤핸도 작게뜨는데, css링크보다 shorcut이 앞에있다.)
        [링크 : https://eyoom.net/bbs/board.php?bo_table=tip&wr_id=14&sst=wr_datetime&sod=desc&sop=and&page=1]
.        
    4.href같은 경로에 /를 맨 앞에 쓰는경우가 있는데, 큰 의미차이는 없는것으로 보인다.
.    
#####(1).전체태그
.
	<link rel="apple-touch-icon-precomposed" href="~">
.    
#####(2).기능
.
	웹앱 밑 기타 아이콘 표시
.
#####(3).위치
.
	<link rel="apple-touch-icon-precomposed" href="~">
    <link rel="shortcut icon" type="image/x-icon" href="~">
    <link rel="manifest" href="~.webmanifest">
.