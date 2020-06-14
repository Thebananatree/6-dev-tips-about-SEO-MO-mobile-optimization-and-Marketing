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
              "theme_color":"#ffffff",
              "background_color":"#ffffff",
              "display":"browser"
           }
            (1).name - 웹 앱의 이름이다.(홈 화면 추가시 지정시킬이름, 안드로이드폰(삼성,크롬 둘다) 아이폰 모두 적용)
            (2).short_name - 웹 앱의 짧은 이름. 공간이 충분하지 않아 full name이 나올 수 없을때 사용된다.
                -but, 아이폰,안드로이드폰(크롬,삼성브라우저) 둘다에서 (1).name이 아닌 (2).short_name을 먼저 적용해서 보여준다.(이 점 알아두기)
            (3).icon - icon은 웹앱을 표시하기 위한 이미지다.(link요소의 rel속성이 icon인것과 동일한 기능)
                    {1}.우선, 이 manifest의 아이콘 이미지를 적용을 안해도(쯕,webmanifest를 아예빼버림) 맥북프로,아이폰,안드로이드폰,안드로이드패드에서
                    아이콘이 전부 제대로 나왔다.(apple-touch-icon 180px만으로도) 192px,512px 크기 자체가 이 부분에 관여하는건 아닌것같다.
                    아래 링크를 보면 Chrome을 설치하려면 최소 192,512 px아이콘을 제공해야한다한다.
                    [링크 : https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp?hl=ko]
                    {2}.더쿠라는 커뮤니티에서는 180보다 큰 192, 512를 명시하고 있는데, 다른 기기에서 웹앱이 적용되는거니 따라가도록 하자.
                    {3}.크기가큰 아이콘이 있으면, 작은아이콘이 필요한곳에서는 아이콘의 크기가 알아서 변경된다.
                    [링크 : https://ldne.tistory.com/80]    
                    [링크 : https://webdir.tistory.com/337]
                1.src - 이미지 위치를 가리킨다.(더쿠는 루트디렉토리,픽은 하위폴더)
                2.type - 아이콘 파일 유형을 명시한다.
                3.sizes - 이미지 크기를 명시한다.
            (5).start_url - 사용자가 웹앱(홈 화면 추가된)을 실행 시켰을때 시작할 url이다. manifest의 상대 경로로 지정한다.
                더쿠는 이 부분이 없는데, 웹페이지의 세부페이지에서 홈 화면 추가할 시에 그 웹앱 클릭하면 세부페이지부터 시작된다.(즉, 저장한 세부주소로 웹앱경로가 저장된다.)
                그러나 픽의 경우, start_url을 지정했는데, 이 경우 어느 세부페이지에서 홈 화면 추가해서 웹앱을 추가하여도, 지정한 start_url에서 시작한다.
                [링크 : https://blog.nundefined.com/48]   
                [링크 : https://joshua1988.github.io/web-development/pwa/webapp-manifest/]
            (6).theme_color - 아니 , theme_color은 webmanifest안의 코드는 의미없고, 바깥의 meta name theme-color만 의미 있는건가.
                              .           
            (7).background_color - 
            (8).display -
            .
            -webmanifest를 쓰는 것의 최소 요구 사항은 name과 적어도 하나
            
.       우선 보면 알겠지만 픽도 fullscreen했는데 아이폰은 상태바 남는다. 즉 아이폰은 제한된게 몇가지 있다.
.
    6.
. 아니 그리고, 더쿠는 theme-color인가 이걸 webmanifest에도 해놓고 그냥 meta태그로도 해놨는데 따로 지정해야하는건가.

#####(1).전체태그
.
	< link rel="manifest" href="/site.webmanifest">
.    
#####(2).기능
.
	    
.
#####(3).사용법
.
	
.
#####(4).위치
.
	
.

1.<meta name="theme-color" content="#000000"> ,2. "theme_color":"#42DE86"
    -우선, 둘다 아이폰에는 아무영향이 없다.
    -1.과 2. 둘다 적혀져있을시에, 안드로이드폰에서는 1.을 따라간다.(삼성브라우저도) + 홈화면추가했을때도 1.을 따라간다.(삼성브라우저도)
    -1.이 없을때, 2.이 적용되는데, 크롬브라우저와 삼성브라우저에는 2.가 적용되지 않고, 홈 화면 추가했을시에만 2.가 적용된다. 즉,
        manifest가 홈 화면 추가 웹앱에서만 적용하는 걸지도.