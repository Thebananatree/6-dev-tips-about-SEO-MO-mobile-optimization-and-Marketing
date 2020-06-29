###[파비콘,아이콘,웹앱]meta name theme-color

#####(0).앞서 알아야 할 내용  
.
    1.< meta name="theme-color" content="#D942DE"> 에 content에는 '색 이름'이나 '#RRGGBB'
        형식을 넣을 수 있다
.
    2.화면의 '상태바'와 '네비게이션바'의 색을 변경할 수 있다. 그러나 지금은 대부분의 브라우저에서 적용되지않고
        안드로이드 크롬, 네이버앱, 삼성인터넷 일부버전, 크롬 일부버전에서 적용된다. - caniuse.com에서 얻는정보
        (pc는 안되고, 모바일이나 패드같은데서만 적용되는것 같다.)
        [링크 : https://blog.naver.com/malloc813/220619007941]   
        [링크 : https://blog.naver.com/dnepdrn/221703694688]
.
    3.적용범위와 효과(탭 여러개 보기 적용은 아래 제시)
        1.아이폰
            (1).사파리 브라우저 - X
            (2).웹앱 - X
        2.안드로이드폰
            (1).크롬 브라우저 - 상태바,네비게이션바 적용
            (2).크롬 브라우저 웹앱 - 상태바, minimal-ui의 다른바 적용
        3.안드로이드폰
            (1).삼성 브라우저 - 상태바,네비게이션바 적용(아래 뒤로가기버튼은 적용x)
            (2).삼성 브라우저 웹앱 - 상태바
        4.엘지 패드
            (1).크롬 브라우저 - X(더쿠도 적용되지 않았다.)
                               [4](최신버전으로 업데이트 하고 이렇게 됬다. 아니면, 업데이트하고 이 패드의 
                               크롬 브라우저 자체를 모바일로 인식안하는건아닐까, 업데이트가 안되는건 아니다. 다른
                               webmanifest의 속성들은 변경된것들이 잘 적용됨)
            (2).크롬 브라우저 웹앱 - 상태바, minimal-ui의 다른바에도 전혀 적용되지않았다.(webmanifest의
                                    theme_color를 덮어씌우는게 아니라, 아예 속성적용이 안된것처럼 보임,
                                    그러나 스플래쉬 화면에서는 webmanifest의 theme_color는 적용됬다.)
                                    [5](최신버전으로 업데이트 하고 이렇게 됬다. 아니면, 업데이트하고 이 패드의 
                                    크롬 브라우저 자체를 모바일로 인식안하는건아닐까, 업데이트가 안되는건 아니다. 다른
                                    webmanifest의 속성들은 변경된것들이 잘 적용됨)
.                                    
    4.탭 여러개 보기 적용
        (1).아이폰
            {1}.사파리 - x
            {2}.사파리 웹앱 - x
        (2).안드로이드 폰
            {1}.크롬 브라우저 - 부분표시
            {2}.크롬 브라우저 웹앱
                1.fullscreen - x
                2.standalone - 적용
                3.minimal-ui - 적용
            {3}.삼성브라우저 - x
            {4}.삼성브라우저 웹앱
                1.fullscreen - 적용
                2.standalone - 적용                       
        (3).엘지패드(크롬)웹앱
            {1}.크롬 브라우저 - x
            {2}.크롬 브라우저 웹앱
                1.fullscreen - x
                2.standalone - x
                3.minimal-ui - x                  
                (theme-color을 적용했음에도, 크롬 브라우저 웹앱은 오히려 theme_color가 적용된 색을
                탭 색으로 적용됬다.)
                [6](최신버전으로 업데이트 하고 이렇게 됬다.)
.                
#####(1).전체태그
.
	< meta name="theme-color" content="#D942DE"> 
.    
#####(2).기능
.
    웹앱 혹은 모바일 브라우저에서 상태바,네비게이션바 등에 색깔적용
.
#####(3).사용법
.
	< meta name="theme-color" content="#D942DE"> 에서 원하는 색을 content 부분에 써 넣는다.
.
#####(4).위치
.
	특별히 어디에 위치해야 한다는 표시는 없었다.(그러나, 다른 태그들은 위치가 조금 상관있다. ex)apple-touch-icon태그)
	ex)
	<meta name="theme-color" content="~">
    .
    .
    .
    .
    .
    <link rel="apple-touch-icon-precomposed" href="~">
    <link rel="shortcut icon" type="image/x-icon" href="~">
    <link rel="manifest" href="~.webmanifest">
.