### [파비콘,아이콘,웹앱] 웹앱 webmanifest

#####(0).앞서 알아야 할 내용  
.
	1.과거에 manifest로 사용되던 몇 가지 흔한 확장자들이 있다. manifest.webapp 은 Firefox OS 웹 manifest로 유명하며, 
	많은 사람들이 JSON 구조로 내용이 구성된 manifest.json을 사용한다. 하지만, .webmanifest 확장자는 W3C manifest 명세에
	명시적으로 언급되고 있으므로 이를 그대로 사용하도록 하겠다.
	[링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
.    
    2.보통 보안(HTTPS) 도메인에서 제공되는 웹사이트가 요구된다고 한다.
    [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
.    
    3.webmanifest 파일은 일반적으로 루트디렉토리에 위치한다. 그래서 href의 경로도 "/site.webmanifest" 이런식 인가보다.
    ex) 더쿠,픽도 이러하다.
    [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
.    
    4.'상태 바'는 스마트폰의 시간,wifi,데이터,충전량을 보여주는 곳은 '상태 바'(status bar)라 하고
    스마트폰 브라우저의 주소검색란 같은것을 '네비게이션 바'(Navigation Bar)라고 한다.
    [링크 : https://brunch.co.kr/@dalgudot/98]
.
    5.webmanifest 파일이 나오게 된 과정
        (1).웹앱 이름 - <meta name="apple-mobile-web-app-title" content="~"> -> ~예시 '인스티즈'
            -태그는 인스티즈에 적용된것인데, 이는 아이폰에서만 작동하고, 안드로이드 폰(크롬, 삼성브라우저 둘다)
            에서는 < title>로 웹앱의 이름을 지정한다.(물론, webmanifest 비활성화했을때다.)
            [인스티즈 코드와 + 내가 직접해보았다.]
        (2).풀 스크린 - <meta name="apple-mobile-web-app-capable" content="~"> -> ~예시 'yes'
            -content를 yes로 적으면, 상태바를 제외한 브라우저의 UI(URL바)를 안보이도록 할 수 있다. 또한 홈 화면추가 된 웹앱을
            클릭시에, 사파리에서 뜨는게 아니라, 사파리와는 별개로 뜨는 창으로 뜬다.(안드로이드 폰의 크롬,삼성브라우저,아이폰의 사파리 모두 적용됬다.) 
            [링크 : https://aboooks.tistory.com/tag/meta%20name%3D%22apple-mobile-web-app-status-bar-style%22]    
            [링크 : https://m.blog.naver.com/PostView.nhn?blogId=bhher&logNo=220788983128&proxyReferer=https:%2F%2Fwww.google.com%2F]
        (3).상태바 색상 - <meta name="aaple-mobile-web-app-status-bar-style" content="~"> -> ~예시 'black'
            -상태바의 색상을 지정할 수 있다. 바탕화면이 검정색인 어플리케이션의 경우 상태바만 회색인 이질감을 줄이기 위해 사용한다.
            단, apple-mobile-web-app-capable 처럼 전체화면 모드를 먼저 지정하지 않으면 효과가 없다.
            content값에 black으로 설정하면, 상태 막대는 검은색배경 black-translucent이면 상태 막대는 검정과 반투명, default는 회색이다.
            (아이폰은 어떤값을 넣든 그냥 배경 검정색이거나, 사파리에서도 본래그대로 아무변화도 없었다. ,  안드로이드폰도 크롬,삼성브라우저나 크롬,삼성 홈 화면에서 어떠한 변화도 없었다. 또한 전체화면 모드였다.)
            [링크 : https://aboooks.tistory.com/tag/meta%20name%3D%22apple-mobile-web-app-status-bar-style%22]   
            [링크 : https://m.blog.naver.com/PostView.nhn?blogId=bhher&logNo=220788983128&proxyReferer=https:%2F%2Fwww.google.com%2F]
        (4).시작화면 - <link rel="apple-touch-startup-image" href="~"> -> ~예시 'loading.png'
            -웹 앱 처음 로딩시 로고화면처럼 로딩될때 스타트업 이미지를 보여줄 수 있다한다.
            (그러나, 실제 해본결과, 아이폰사파리 , 안드로이드폰(크롬브라우저, 삼성브라우저) 아무데서도 작동안한다.) - 글 읽어보면, 기기별 이미지의 크기가
            정확히 맞아야 화면에 표시된다는데, 그냥 안쓰는게 나을 것 같다.
            (webmanifest때문인가 해서, theme_color, background_color 지웠는데도 안됨)  
            [링크 : https://m.blog.naver.com/PostView.nhn?blogId=bhher&logNo=220788983128&proxyReferer=https:%2F%2Fwww.google.com%2F]   
            [링크 : https://itlab.tistory.com/30]   
.        
    6.5.의 종착지가 바로 webmanifest 파일이다.   
        (site.webmanifest파일 내부)    
          {
              "name":"셀럽마인",
              "short_name":"셀럽마인",
              "icons":[{
                      "src":"/192png3x.png",
                      "sizes":"192x192",
                      "type":"image/png"
                  },
                  {
                      "src":"/512png3x.png",
                      "sizes":"512x512",
                      "type":"image/png"
                  }
              ],
              "start_url":"/pwa-examples/index.html",
              "theme_color":"#ffffff",
              "background_color":"#ffffff",
              "display":"browser"
           }
            (1).name - 웹 앱의 이름이다.(홈 화면 추가시 지정시킬이름, 안드로이드폰(삼성,크롬 둘다) 아이폰 모두 적용)
                그러나, 스플래쉬 화면에 뜨는 이름은 이 name이 뜬다.(안드로이드폰(크롬,삼성)의 웹앱, 엘지패드(크롬)웹앱 모두)
            (2).short_name - 웹 앱의 짧은 이름. 공간이 충분하지 않아 full name이 나올 수 없을때 사용된다.
                -but, 아이폰,안드로이드폰(크롬,삼성브라우저),엘지패드(크롬) 홈 화면 추가 이름이 전부 (1).name이 아닌 (2).short_name을 먼저 적용해서 보여준다.(이 점 알아두기)
            (3).icon - icon은 웹앱을 표시하기 위한 이미지다.(link요소의 rel속성이 icon인것과 동일한 기능)
                    {1}.webmanifest의 icons 속성에 관해서는 아이폰과 맥북프로의 적응목록에 어떠한 영향도 주지 않는다. 속성이 적혀있건 안적혀있건(웹앱 등 기타 전부)
                    안드로이드폰,엘지패드에서는 webmanifest파일이 없었어도 스플래쉬 아이콘(안드로이드폰 삼성,크롬 브라우저,엘지패드 크롬 브라우저), 홈 버튼 추가 아이콘(안드로이드폰 삼성,크롬 브라우저,엘지패드 크롬 브라우저)
                    에서 모두 apple-touch-icon이 떳다. 그러나, webmanifest에 192,512px를 각각 디시인 인스티즈 추가하니 몇가지가 변하였다.
                        1.안드로이드(크롬 브라우저) 웹앱
                            (1).홈버튼 추가할때 뜨는 이미지 - icons의 192px 적용
                            (2).홈 화면 추가 아이콘 이미지 - icons의 192px 적용
                            (3).홈 화면 추가 웹앱의 여러탭 - icons의 192px 적용
                            (4).스플래쉬 아이콘 - icons의 512px 적용
                            +
                            그외 적용목록의 (4).크롬 브라우저 탭에는 영향 없다. 
                        2.안드로이드(삼성 브라우저) 웹앱
                            (1).홈버튼 추가할때 뜨는 이미지 - icons의 192px 적용
                            (2).홈 화면 추가 아이콘 이미지 - icons의 192px 적용
                            (3).홈 화면 추가 웹앱의 여러탭 - icons의 192px 적용
                            (4).스플래쉬 아이콘 - icons의 192px 적용           
                            (스플래쉬 아이콘 192px적용이 맞다.)             
                        3.엘지패드(크롬 브라우저) 웹앱
                            (1).홈버튼 추가할때 뜨는 이미지 - icons의 192px 적용
                            (2).홈 화면 추가 아이콘 이미지 - icons의 192px 적용
                            (3).홈 화면 추가 웹앱의 여러탭 - icons의 192px 적용
                            (4).스플래쉬 아이콘 - icons의 512px 적용 
                            (브라우저 버전별, 기기별로 조금 다를 수 있는 부분은 있다.)
                    {2}.아래 링크를 보면 Chrome을 설치하려면 최소 192,512 px아이콘을 제공해야한다한다.
                    [링크 : https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp?hl=ko]
                    또한, 이 링크에도 512X512사이즈가 반드시 지원되야 PWA로 인식된다고 한다.
                    [링크 : https://chaewonkong.github.io/posts/pwa.html]
                    {3}.더쿠라는 커뮤니티에서는 180보다 큰 192, 512를 명시하고 있는데, 다른 기기에서 웹앱이 적용되는거니 따라가도록 하자.
                    {4}.크기가큰 아이콘이 있으면, 작은아이콘이 필요한곳에서는 아이콘의 크기가 알아서 변경된다.
                    [링크 : https://ldne.tistory.com/80]    
                    [링크 : https://webdir.tistory.com/337]
                1.src - 이미지 위치를 가리킨다.(더쿠는 루트디렉토리,픽은 하위폴더)
                2.type - 아이콘 파일 유형을 명시한다.
                3.sizes - 이미지 크기를 명시한다.
            (4).start_url - 사용자가 웹앱(홈 화면 추가된)을 실행 시켰을때 시작할 url이다. manifest의 상대 경로로 지정한다.
                더쿠는 이 부분이 없는데, 웹페이지의 세부페이지에서 홈 화면 추가할 시에 그 웹앱 클릭하면 웹앱을 추가한 해당 현제페이지부터 시작된다.(즉, 저장한 세부주소로 웹앱경로가 저장된다.)
                그러나 픽의 경우, start_url을 지정했는데, 이 경우 어느 세부페이지에서 홈 화면 추가해서 웹앱을 추가하여도, 지정한 start_url에서 시작한다.
                (아이폰 사파리, 안드로이드폰(크롬,삼성),엘지패드 모두 적용됨)
                [링크 : https://blog.nundefined.com/48]   
                [링크 : https://joshua1988.github.io/web-development/pwa/webapp-manifest/]
            (5).theme_color - 홈화면 추가된 웹앱의 상태바와 네비게이션바에 반영되는 색깔이며, 애초에 아래 뒤로가기 바는 색깔이 반영되지 않는다. 
                1.홈 화면 추가 웹앱이 아닌 브라우저에서는 아이폰(사파리 브라우저),안드로이드폰(삼성,크롬),엘지패드(크롬)에서는 전혀 반영되지 않는다.
                2.엘지패드(크롬 브라우저) 에서의 홈 화면 추가해서 웹앱에서 뒤로가기 버튼 부분에도 적용되지않았다.(삼성브라우저는 아예 웹앱의 뒤로가기 버튼이 보이지 않는다.)
                3.기기별 적용되는 요소(탭 여러개 보기는 아래 따로 제시)
                    (1).아이폰
                        {1}.사파리 웹앱 - 적용되지 않는다.
                    (2).안드로이드 폰
                        {1}.크롬 웹앱 
                            1.standalone - 상태바에 적용
                            2.minimal-ui - 상태바와 '조금다른 네비게이션바'에 적용된다.
                        {2}.(삼성브라우저)웹앱 
                            1.fullscreen - 상태바에 적용
                            2.standalone - 상태바에 적용
                    {4}.엘지패드(크롬)웹앱
                            1.fullscreen - 원래 모든ui가 안보이나 위에 내리기(화면 맨위 내리기 하면 잠깐 상태바랑 뒤로가기버튼 보임)해도 해당 보여지는 ui에 대해서는 적용되지않는다.
                            2.standalone - 상태바에 적용된다.(당연히, 뒤로가기 버튼에는 적용안된다.)
                            3.minimal-ui - 상태바, '조금다른 네비게이션바'에 적용된다.(당연히, 뒤로가기 버튼에는 적용안된다.)
                            [1](최신버전으로 업데이트 하고 이렇게 됬다. 아니면, 업데이트하고 이 패드의 
                            크롬 브라우저 자체를 모바일로 인식안하는건아닐까, 업데이트가 안되는건 아니다. 다른
                            webmanifest의 속성들은 변경된것들이 잘 적용됨 스플래쉬화면의 상태바 외에는 위의 1~3이 아무것도 적용되지 않았다. 마치 아무 속성도 안적은것처럼
                            정확히는 meta theme-color적용하고나서부터인데, 이것때문이 아닐 수도 있다. meta theme-color를 지웠는데도 그 이후로 1~3이 적용이안된다.)
                            ([2],[3],[4]meta name theme-color,[5]meta name theme-color,[6]meta name theme-color 와 연관 생각)
                4.탭 여러개 보기 색깔 적용
                    (1).아이폰
                        {1}.사파리 - x
                        {2}.사파리 웹앱 - x
                    (2).안드로이드 폰
                        {1}.크롬 브라우저 - x
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
                            1.fullscreen - 적용
                            2.standalone - 적용
                            3.minimal-ui - 적용
                            [2]
                5.< meta name="theme-color" content="~">의 meta태그와의 상호작용
                    1. meta theme-color와 theme_color가 같이 써있더라도 '스플래쉬화면의 상태바'만 남기고 보일 수 있는 모든 부분(탭 여러개 보기 빼고)은 meta태그를 따라간다. 그러나
                        엘지패드에서는, 크롬브라우저에서도 meta name theme-color가 적용되지않고, 일반 웹앱 화면의
                        상태바나 minimal-ui 부분에서는 전혀 적용되지않았다.(이때 theme_color도 적용되지 않고 아예 두가지 속성(theme_color, theme-color) 모두 적용되지 않는 것처럼
                        보여졌었다.)
                    2.스플래쉬 화면은 theme_color가 적용되는것을 따라갔다.(meta의 theme-color는 이 부분에 영향이 없는것 같다.)
                        안드로이드폰(삼성,크롬 브라우저) 웹앱, 엘지패드(크롬 브라우저) 웹앱 에서는 모두(display 상관없이) theme_color를 따라갔다.(meta theme-color)가 있었음에도
                    3.탭 여러개 보기 색깔 적용에서는, 엘지패드를 제외하고서는, theme-color와 theme_color가 함꼐 쓰여져있는 경우, theme-color을 따라가지만
                        엘지패드의 웹앱에 대한 탭 여러개 보기 색깔은, theme-color와 theme_color가 함께 적혀져있어도 theme_color를 따라갔다.
                        [3]   
                [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
            (6).background_color - 스플래쉬 화면과 설치하는 동안 사용될 배경 색상이다.
                    {1}.아이폰(사파리) 웹앱 - 적용되지 않는다.
                    {2}.안드로이드 폰(크롬) 웹앱 -적용된다.
                    {3}.안드로이드 폰(삼성브라우저)웹앱 - 적용되지 않는다.
                    {4}.엘지패드(크롬)웹앱 - 적용된다.
                [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]    
            (7).display - 웹앱을 표시하는 방식이다.
                1.browser - 브라우저 창에서 뜬다. 아이폰(사파리),안드로이드폰(크롬,삼성),LG패드(크롬) 모두 홈 화면 추가 웹앱이 브라우저에서 떳다.
                2.fullscreen
                    {1}.아이폰(사파리) 웹앱 - '상태바'만 남기고 다 사라진다.(아래 뒤로가기버튼도 사라짐) 그리고 개별적 창에서 뜬다.
                    {2}.안드로이드 폰(크롬)웹앱 - 상태바,네비게이션바 모두 사라지고 개별적 새창에서 뜬다.(내가 쓴 안드로이드폰은 뒤돌기 버튼이 따로있어 크롬에 뒤돌기 버튼이 원래 안뜬다.)
                    {3}.안드로이드 폰(삼성브라우저)웹앱 - 상태바는 보이고, 네비게이션바 그리고 아래에 뒤로가기버튼만 안보인다.(이 안드로이드폰의 삼성브라우저는 아래에 뒤로가기 버튼이 뜬다.) 추가로 개별적창에서 뜬다.
                    {4}.엘지패드(크롬)웹앱 - 상태바,네비게이션바,아래 뒤로가기버튼 모두가 사라져서 보인다.(내가 쓴 엘지패드 크롬브라우저는 뒤로가기버튼이 있다.)
                3.standalone
                    {1}.아이폰(사파리) 웹앱 - '상태바'만 남기고 다 사라진다.(아래 뒤로가기버튼도 사라짐) 그리고 개별적 창에서 뜬다.
                    {2}.안드로이드 폰(크롬)웹앱 - 상태바는 그대로있고,네비게이션바는 사라지고 개별적 새창에서 뜬다.(내가 쓴 안드로이드폰은 뒤돌기 버튼이 따로있어 크롬에 뒤돌기 버튼이 원래 안뜬다.)
                    {3}.안드로이드 폰(삼성브라우저)웹앱 - 상태바는 보이고, 네비게이션바 그리고 아래에 뒤로가기버튼만 안보인다.(이 안드로이드폰의 삼성브라우저는 아래에 뒤로가기 버튼이 뜬다.) 추가로 개별적창에서 뜬다.
                    {4}.엘지패드(크롬)웹앱 - 상태바는 보이고,네비게이션바가 사라졌으며, 아래 뒤로가기버튼은 그대로 보인다.(내가 쓴 엘지패드 크롬브라우저는 뒤로가기버튼이 있다.)
                4.minimal-ui
                    {1},{3}.아이폰(사파리) 웹앱,안드로이드폰(삼성브라우저)웹앱 - 브라우저창에서 뜨고, 
                    {2}.안드로이드 폰(크롬)웹앱 - 상태바는 그대로 나오는데, 네비게이션바가 조금 다르게 나타난다.(안드로이드폰(크롬)은 원래 아래'뒤로가기바'가 없다. 핸드폰 자체가 뒤로가기가 있음)
                    {4}.엘지패드(크롬)웹앱 - 상태바는 있고 네비게이션바가 위 {2}와 똒같이 다르게 나온다.아래 뒤로가기버튼은 그대로 나온다.(엘지패드(크롬)은 자체 뒤로가기 버튼이 없어서 크롬 브라우저 아래에 버튼들이 있다.)
                    4.은 아래 링크에 보면 브라우저마다 많이 상이하다고 나와있긴하다.           
                [링크 : https://developer.mozilla.org/en-US/docs/Web/Manifest/display]  
            (8),(10).description, orientation 등은 필요할 시 알아보기
                [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]    
                [링크 : https://joshua1988.github.io/web-development/pwa/webapp-manifest/]
                추가내용 : webmanifest를 쓰는 것의 최소 요구 사항은 name과 적어도 하나(src,type,size를 포함)의 아이콘이다.
                description, short_name, start_url은 권장사항이다.
                [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
                추가추가내용 : 홈 화면 추가 웹앱이 가끔 사용하는 브라우저나 운영체제에 따라 웹앱 아이콘의 우측 하단에 작은
                브라우저 이미지가 있어 사용자에게 웹 특성에 대한 정보를 주기도 한다.
                [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
.    
    7.홈 화면 추가 웹앱의 스플래쉬 화면은 webmanifest파일의
        (1).name
        (2).icons
        (3).background_color
        로 결정되는거다.
        [링크 : https://developer.mozilla.org/ko/docs/Web/Progressive_web_apps/Installable_PWAs]
.    
    8.webmanifest의 내용(코드)을 바꾸더라도 이전 홈 화면 추가된 웹앱에 대한 적용된 것들은 변화하지 않는다.
        (1).안드로이드(크롬 브라우저) 웹앱 - name(스플래쉬 이름), short_name(웹앱 이름), icons(스플래쉬 아이콘, 웹앱 아이콘),
            theme_color(색상),background_color(색상), display 모두 webmanifest를 변경해도 이전 사항으로 홈 화면 추가된 웹앱은 이 전의
            속성을 따라간다.
        (2).안드로이드(삼성 브라우저) 웹앱 - name(스플래쉬 이름), short_name(웹앱 이름), icons(스플래쉬 아이콘, 웹앱 아이콘),
            theme_color(색상),background_color(색상), display 모두 webmanifest를 변경해도 이전 사항으로 홈 화면 추가된 웹앱은 이 전의
            속성을 따라간다.
        (3).엘지패드(크롬 브라우저) 웹앱 - name(스플래쉬 이름), short_name(웹앱 이름), icons(스플래쉬 아이콘, 웹앱 아이콘),
            theme_color(색상),background_color(색상), display 모두 webmanifest를 변경해도 이전 사항으로 홈 화면 추가된 웹앱은 이 전의
            속성을 따라간다.
        (단, meta theme-color 처럼 html코드는 그때그때마다 이전 웹앱이든 새로운 웹앱이든 새로운 속성값이 적용된다.)
.    
    9.scope이란 webmanifest의 한 속성이 있는데, 웹 앱 유효범위 밖으로 이동하려하면(a 태그 클릭시) 새로운 브라우저에서 실행하냐
        안하냐를 의논하는것인데, 셀럽이나 픽에는 scope 속성을 안넣는데도, 외부url(셀럽은 네이버,픽은 외부 쇼핑몰)을 클릭해도 웹 앱을
        벗어나지 않았다. 나중에 필요해지면 다시 보자
        [링크 : https://joshua1988.github.io/web-development/pwa/webapp-manifest/]
.
    10.또한, IOS에서 즐겨찾기로 추가한 아이콘으로 웹 앱을 실행하면, 웹 앱 내에서 href 태그 접근 시 새로운 브라우저를 띄우면서 scope 이 바뀐다. 라고 한다.
        해결책은 < a href="#">를 없애는 거라한다.
        [링크 : https://joshua1988.github.io/web-development/pwa/webapp-manifest/]
.        
#####(1).전체태그
.
	< link rel="manifest" href="/site.webmanifest">
.    
#####(2).기능
.
    홈 화면 추가 , 웹앱의 기본 정보가 된다.
.
#####(3).위치
.
	shortcut icon, apple-touch-icon, meta theme-color와 함께 쓰자.
.