### [크롤링 & 인덱싱] robots.txt

####(0).앞서 알아야 할 내용  
.
    1.< meta name="robots" content="~">는 주로 인덱싱 제어, robots.txt는 크롤링 제어로 볼 수 있는데,
        크롤링은 사이트와 사이트 사이의 링크를 타고다니며 문서를 수집하는 역활이며, 인덱싱은 수집된 문서를 검색엔진이
        사용자에게 결과물을 좀 더 빠르고 쉽게 제공할 수 있는 색인 또는 인덱스하는 역활을 의미한다. 그러나 robots 메타태그보다
        robots.txt 파일로 크롤링을 제어하는게 일반적이다. 아니면 둘이 같이 쓰기도 하지만, 디시인,더쿠,인스티즈는 모두(모바일,pc둘다) robots.txt
        만 사용하고 있고, 네이버만 robots 메타태그와 robots.txt를 함꼐 사용하고 있다.
        [참조링크 : https://junhobaik.github.io/meta-tag/]   
        [참조링크 : http://www.seo-korea.com/robots-txt-%ED%8C%8C%EC%9D%BC%EA%B3%BC-meta-robots-%ED%83%9C%EA%B7%B8%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90/]
.
    2.기본적으로 robots.txt파일은 사이트의 루트 디렉토리에 저장해 두어야 한다. 예를들면, theqoo.net/robots.txt를 입력 하면 파일을 
        읽을 수 있어야 한다. theqoo.net/myfolder/robots.txt는 유효하지 않으며 제대로 작동하지 않는다.
        [참조링크 : http://www.seo-korea.com/robots-txt-%ED%8C%8C%EC%9D%BC%EA%B3%BC-meta-robots-%ED%83%9C%EA%B7%B8%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90/]
.
    3.검색엔진의 크롤러로 부터 모든 문서수집을 차단하려면 아래와 같은 내용을 robots.txt에 삽입합니다.
        User-agent: *
        Disallow: /
.      
        반대로 모든 문서를 허용하려면
        User-agent: *
        Disallow:
.      
        특정 폴더만을 차단하려면
        User-agent: *
        Disallow: /members/
        Disallow: /search/
        Disallow: /images/
.      
        특정 검색엔진 크롤러를 차단하려면 (구글만 차단)
        User-agent: Googlebot
        Disallow: /
.      
        또는 특정 검색엔진 크롤러만 허용하려면 (구글만 허용)
        User-agent: Google
        Disallow:
        User-agent: *
        Disallow: /
.      
        특정 페이지를 차단하려면
        User-agent: *
        Disallow: /members/personal_info.html
.      
        robots.txt 파일에 사이트맵 명시
        User-agent: *
        Disallow:
        Sitemap: http://www.seo-korea.com/sitemap.xml
.
    4.robots.txt는 검색로봇에게 사이트 및 웹페이지를 수집할 수 있도록 허용하거나 제한하는 국제 권고안이다. robots.txt파일은 항상 사이트의 루트 디렉터리에
        위치해야 하며 로봇 배제 표준을 따르는 일반 텍스트 파일로 작성해야 한다. 간혹 특정 목적을 위하여 개발된 웹 스크랩퍼를 포함하여 일부 불완전한 검색로봇은 robots.txt
        내의 규칙을 준수하지 않을 수 있다.(실제, 검색엔진을 어떻게 짜냐에 따라 무시할 수도 있고 지킬 수도 있는거다.) 그러므로, 개인 정보를 포함하여 외부에 노출되면 안 되는 콘텐츠의 경우
        로그인 기능을 통하여 보호하거나 다른 차단 방법을 사용해야 한다. 즉, 이 robots.txt로 특정 읽어야 하는 컨텐츠를 크롤링 불허한다해도 소용없으니 다른방법으로 보호해야
        한다는 뜻이다.
        예를들어, 관리자페이지, 개인 정보 페이지
        [참조링크 : https://searchadvisor.naver.com/guide/seo-basic-robots]
.    
    5.robots.txt 파일에 작성된 규칙은 같은 호스트,프로토콜 및 포트 번호 하위의 페이지에 대해서만 유효하다. 실제로, m.dcinside.com robots.txt도 따로 있고
    gall.dcinside.com/robots.txt도 따로 있다.
.    1. 도메인은 정확하게 체크됨
      + https://www.hahwul.com 적용 시 www 도메인만 적용됨
     2. 경로의 최상위 디렉토리에만 유효
      + /test/robots.txt는 적용되지 않음
     3. 프로토콜(http, https ,ftp 등..)도 정확하게 따짐
      + http://www.hahwul.com으로 적용 시 https://www.hahwul.com은 적용받지 않음)
     4. 포트도 정확하게 걸러냄
      + https://www.hahwul.com 적용 시 https://www.hahwul.com:8080은 무효
      + 단 80,443 같이 프로토콜의 기본 포트는 예외됨(http://hahwul.com:80 == http://hahwul.com)
.      
    6.robots.txt에 sitemap 설정을 넣는건 옵션이다. 웹 사이트의
.    
    7.마지막에 /를 넣지않으면 폴더로 인식하지않고 파일로 인식하니, 꼭 폴더 경로 넣을때는 마지막에 /붙인다.
####(1).전체태그
.
    ㅁ
.
####(2).기능
.
    ㅁ
.
####(3).위치
.
    ㅁ
.
####(4).타 웹사이트 태그예시    
.
    theqoo.net/robots.txt , instiz.net/robots.txt , dcinside.com/robots.txt , 
.
    1.더쿠
        User-Agent: *
        Disallow:         
    2.인스티즈
        User-agent: bingbot
        Disallow: /
.        
        Disallow: /iframe_scrap.htm
        Disallow: /download.php
        Disallow: /iframe_filter.htm
        Disallow: /delete_ok.php
        Disallow: /bbs/delete_ok.php
        Disallow: /bbs/vote.php
    3.디시인사이드    
        User-agent: *
        Disallow: /
.        
        # Ads
        User-agent: grapeshot
        Allow: /  
.        
        # Search
        User-agent: Googlebot
        Allow : / 
        Crawl-delay: 60
.        
.        
        User-agent: grapeshot
        Allow: /
    4.디시인사이드 갤러리
        User-agent: *
        Disallow: /board/lists/?id=47
        Disallow: /board/lists/?id=singo
        Disallow: /board/lists/?id=stock_new
        Disallow: /board/lists/?id=cat
        Disallow: /board/lists/?id=dog
        Disallow: /board/view/?id=starcraft&no=5179138
        Disallow: /board/view/?id=comedy_new&no=3182480
        Disallow: /board/view/?id=plastic_s&no=118703
        Disallow: /board/view/?id=hajungwoo&no=12995
        Disallow: /board/view/?id=hajungwoo&no=14508
        Disallow: /board/view/?id=hajungwoo&no=14441
        Disallow: /board/view/?id=hajungwoo&no=14977
        Disallow: /board/view/?id=dongbang&no=43265
        Disallow: /board/view/?id=dongbang&no=43265
        Disallow: /board/view/?id=dongbang&no=43265
        Disallow: /board/view/?id=dongbang&no=48008 
        Disallow: /board/view/?id=kimmyungmin&no=57241
        Disallow: /board/view/?id=etc_entertainment1&no=1462322
        Disallow: /board/view/?id=47&no=559394
        Disallow: /board/view/?id=aion&no=231406
        Disallow: /board/view/?id=aoa&no=455310
        Disallow: /board/view/?id=stock_new&no=6151637 
        Disallow: /board/view/?id=stock_new&no=6151418 
        Disallow: /board/view/?id=stock_new&no=6151691 
        Disallow: /board/view/?id=stock_new&no=3763126
        Disallow: /board/view/?id=stock_new&no=3732018 
        Disallow: /board/view/?id=stock_new&no=3729478
        Disallow: /board/view/?id=stock_new&no=3754372
        Disallow: /board/view/?id=dog&no=291214
        Disallow: /board/view/?id=cat&no=490945
        Disallow: /board/view/?id=stock_new&no=3792162
        Disallow: /board/view/?id=dog&no=289858
        Disallow: /board/view/?id=cat&no=492226
        Disallow: /board/view/?id=stock_new&no=3726853
        Disallow: /board/view/?id=stock_new&no=3757604
        Disallow: /board/view/?id=stock_new&no=3757617
        Disallow: /board/view/?id=stock_new&no=3763108
        Disallow: /board/view/?id=stock_new&no=6151691
        Disallow: /board/view/?id=stock_new&no=6151637 
        Disallow: /board/view/?id=stock_new&no=6151418 
        Disallow: /board/view/?id=stock_new&no=6151691 
        Disallow: /board/view/?id=stock_new&no=3763126
        Disallow: /board/view/?id=stock_new&no=3732018 
        Disallow: /board/view/?id=stock_new&no=3729478
        Disallow: /board/view/?id=stock_new&no=3754372
        Disallow: /board/view/?id=aion&no=231406
        Disallow: /board/view/?id=government&no=3795671
        Disallow: /board/view/?id=government&no=3795663
        Disallow: /board/view/?id=government&no=3795664
        Disallow: /board/view/?id=government&no=3795665
        Disallow: /board/view/?id=government&no=3795657
        Disallow: /board/view/?id=government&no=3795641
        Disallow: /board/view/?id=arbeit&no=1781137
        Disallow: /board/view/?id=arbeit&no=1854264
        Disallow: /board/comment_view/?id=arbeit&no=1827137
        Disallow: /board/view/?id=arbeit&no=1902701
        Disallow: /board/view/?id=theaterM&no=1062240
        Disallow: /board/view/?id=immovables&no=1045608
        Disallow: /board/view/?id=admission&no=1591805
        Disallow: /mgallery/board/lists/?id=rezero
        Disallow: /board/view/?id=bigbang&no=107916
        Disallow: /board/view/?id=exam_new&no=3441270
        Disallow: /board/view/?id=immovables&no=827440
        Disallow: /board/lists/?id=baseball_new8
        Disallow: /board/view/?id=baseball_new8
        Disallow: /board/comment_view/?id=baseball_new8
        Disallow: /board/lists/?id=m_entertainer1
        Disallow: /board/view/?id=m_entertainer1
        Disallow: /board/comment_view/?id=m_entertainer1
        Disallow: /board/lists/?id=stock_new2
        Disallow: /board/view/?id=stock_new2
        Disallow: /board/comment_view/?id=stock_new2
        Disallow: /board/lists/?id=ib_new
        Disallow: /board/view/?id=ib_new
        Disallow: /board/comment_view/?id=ib_new
        Disallow: /board/lists/?id=d_fighter_new1
        Disallow: /board/view/?id=d_fighter_new1
        Disallow: /board/comment_view/?id=d_fighter_new1
        Disallow: /board/lists/?id=produce48
        Disallow: /board/view/?id=produce48
        Disallow: /board/comment_view/?id=produce48
        Disallow: /board/lists/?id=sportsseoul
        Disallow: /board/view/?id=sportsseoul
        Disallow: /board/comment_view/?id=sportsseoul
.        
        User-agent: Googlebot
        Allow: /
        Crawl-delay: 60
.       
        User-agent: Daum
        Allow: /
.        
        User-agent: grapeshot
        Allow: /
.       