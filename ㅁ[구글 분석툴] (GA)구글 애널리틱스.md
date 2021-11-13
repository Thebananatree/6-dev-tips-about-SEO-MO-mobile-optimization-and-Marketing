#### 구글 애널리틱스

https://analyticsmarketing.co.kr/category/digital-analytics/google-analytics-basics/
여기에 다있다.
싹다 처음부터 정리해야해.
1.태그위치
2.유니버셜, 글로벌 GA태그
3.GTM사용방법, 기존 GA태그와의 연동

네이버 애널리틱스와 구글 애널리틱스의 차이 둘다 이용하는게 나을듯
https://polygonstudio.tistory.com/158

-태그 위치
질문3. 추적코드를 헤드 영역에 심으라고 했는데, 꼭 그래야 하나요? 웹사이트 속도에 영향을 미치지는 않나요?
스크립트를 반드시 헤드 영역에 심어야 하는 건 아닙니다. 사실 어느 위치에 추가하건 데이터를 수집하는 데 크게 무리가 없습니다.

다만 헤드 영역을 권장하는 이유는 좀 더 정확한 데이터를 수집하기 위해서 입니다. 방문자가 특정한 웹페이지에 도착하면 페이지는 
위에서부터 아래 방향으로 순차적으로 읽히며 표시됩니다. 따라서 스크립트가 상단에 있으면 그만큼 빨리 하단에 있으면 그만큼 늦게 실행됩니다.

어떤 사용자는 우리 웹사이트에 도착해서 페이지가 다 열리기 전에 떠날 수도 있는데요, 이 때 헤드 영역에 추적코드가 심어져 있다면 사용자가
 방문해서 바로 떠났다는 정보를 수집할 수도 있습니다. 하지만 하단 영역에 있다면 스크립트가 실행되기도 전에 방문자가 떠났기에, 방문 사실 
 자체를 알 수가 없습니다.
 [참조링크 : https://analyticsmarketing.co.kr/digital-analytics/google-analytics-basics/2232/]
 
 
-태그 종류
질문4. 하나의 웹사이트에 두 개의 추적코드를 심어도 되나요?
네, 가능합니다. 하나의 웹페이지에 다수의 추적코드를 추가하여 데이터를 수집할 수 있습니다.

하지만 어떤 태그(글로벌 사이트 태그 vs 유니버설 애널리틱스 태그)를 사용하느냐에 따라 설정 방법에 약간이 차이가 있습니다. 최근에 도입된
 글로벌 사이트 태그(Global Site Tag, gtag.js) 방식에서는 비교적 간단하게 설정(참조: https://developers.google.com/analytics/devguides/collection/gtagjs/sending-data)이 가능합니다.

반면 기존의 유니버설 애널리틱스 태그(Universal Analytics, analytics.js) 방식에서는 각각의 속성을 지정하는 별도의 설정
(참조: https://developers.google.com/analytics/devguides/collection/analyticsjs/creating-trackers)이 필요합니다. 
 
 
 -태그매니저와 기타 내용들이 조금 다르거나 일종의 코드(블로그에서 가려야 한다는)들이
 나는 그대로 들어나고,픽은 다른 문자열로 대체되있다. 근데 이게 위에서 말하던
 글로벌 사이트 태그 던지 유니버설 애널리틱스 태그던지 이거 종류인건가? 왜 다달라?
 
 
 -여러가지 태그 적는 사람들
 GTM - 구글 태그매니저라는것도 있고 여기에 왠만한거 다 나와있는듯.
 https://analyticsmarketing.co.kr/digital-analytics/google-analytics/1850/
 
 
 
<!-- Global site tag (gtag.js) - Google Analytics -->       
~
    < script async src="https://www.googletagmanager.com/gtag/js?id=UA-171536026-1"></script>
    < script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
            gtag('js', new Date());
.     
            gtag('config', 'UA-171536026-1');
    < /script>
    이걸(애널리틱스 추적코드) 추가하고 나면(다른 코드는 안넣었음)
    [1.]
    ~ 부분에
    < script type="text/javascript" async="" src="https://www.google-analytics.com/analytics.js"></script>
    이거하나만 추가되고[이게 전부]   
    [2.] 애드센스 광고 단위 1개만 추가하면
    < script src="https://www.googletagservices.com/activeview/js/current/osd.js?cb=%2Fr20100101"></script>
    < script src="https://partner.googleadservices.com/gampad/cookie.js?domain=www.celebmine.com&amp;callback=_gfp_s_&amp;client=ca-pub-6944617508996548&amp;cookie=ID%3Dc1f4cd133b8da160%3AT%3D1593743253%3AS%3DALNI_MY4rall5d2M-53H2XA4oGATv25cEw"></script>
    < script src="https://pagead2.googlesyndication.com/pagead/js/r20200624/r20190131/show_ads_impl_fy2019.js" id="google_shimpl"></script>
    처럼 3개 줄이 추가되고, 맨 하단에(< /head>바로 위에)
    .
    < link rel="preload" href="https://adservice.google.co.kr/adsid/integrator.js?domain=www.celebmine.com" as="script">
    < script type="text/javascript" src="https://adservice.google.co.kr/adsid/integrator.js?domain=www.celebmine.com"></script>
    <link rel="preload" href="https://adservice.google.com/adsid/integrator.js?domain=www.celebmine.com" as="script">
    < script type="text/javascript" src="https://adservice.google.com/adsid/integrator.js?domain=www.celebmine.com"></script>
    이렇게 4줄이 추가된다.
    .
    body 닫힌 태그 앞에
    <ins class="adsbygoogle adsbygoogle-noablate" data-adsbygoogle-status="done" style="display: none !important;"><ins id="aswift_1_expand" style="display:inline-table;border:none;height:0px;margin:0;padding:0;position:relative;visibility:visible;width:0px;background-color:transparent;"><ins id="aswift_1_anchor" style="display:block;border:none;height:0px;margin:0;padding:0;position:relative;visibility:visible;width:0px;background-color:transparent;"><iframe frameborder="0" marginwidth="0" marginheight="0" vspace="0" hspace="0" allowtransparency="true" scrolling="no" allowfullscreen="true" onload="var i=this.id,s=window.google_iframe_oncopy,H=s&amp;&amp;s.handlers,h=H&amp;&amp;H[i],w=this.contentWindow,d;try{d=w.document}catch(e){}if(h&amp;&amp;d&amp;&amp;(!d.body||!d.body.firstChild)){if(h.call){setTimeout(h,0)}else if(h.match){try{h=s.upd(h,i)}catch(e){}w.location.replace(h)}}" id="aswift_1" name="aswift_1" style="left:0;position:absolute;top:0;border:0px;width:0px;height:0px;"></iframe> <script></script></ins></ins></ins>
    <iframe id="google_osd_static_frame_5793923036396" name="google_osd_static_frame" style="display: none; width: 0px; height: 0px;"></iframe>
    가적혀있고
    .
    body 닫힌 태그 다음에는
    <iframe id="google_esf" name="google_esf" src="https://googleads.g.doubleclick.net/pagead/html/r20200624/r20190131/zrt_lookup.html#" data-ad-client="ca-pub-6944617508996548" style="display: none;"></iframe>
    가 적혀있다.[이게 전부]   
    [3.]
   < script data-ad-client="ca-pub-3596378672158171" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
   이 확인코드만 넣은경우
   위의
   < script src="https://partner.googleadservices.com/gampad/cookie.js?domain=www.celebmine.com&amp;callback=_gfp_s_&amp;client=ca-pub-6944617508996548&amp;cookie=ID%3Dc1f4cd133b8da160%3AT%3D1593743253%3AS%3DALNI_MY4rall5d2M-53H2XA4oGATv25cEw"></script>
   태그 빼고는 [2.]와 똑같이 적혀있다.
   [4.] 구글 태그 매니저 코드 이거 1개 넣었더니
   <!-- Google Tag Manager -->
   <script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
   new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
   j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
   'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
   })(window,document,'script','dataLayer','GTM-PM2F3FG');</script>
   <!-- End Google Tag Manager -->
   이거
   < script async="" src="https://www.googletagmanager.com/gtm.js?id=GTM-PM2F3FG"></script>
   하나가 유일하게 더 생겼다.
   또한
   <!-- Google Tag Manager (noscript) -->
   <noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-PM2F3FG"
   height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
   <!-- End Google Tag Manager (noscript) -->
   이 태그를 추가했는데도 더 추가되는 태그들은 없었다.
   [5.]
   구글 태그 매니저 코드와
   <!-- Google Tag Manager -->
   <script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
   new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
   j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
   'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
   })(window,document,'script','dataLayer','GTM-PM2F3FG');</script>
   <!-- End Google Tag Manager -->
   noscript코드
   <!-- Google Tag Manager (noscript) -->
   <noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-PM2F3FG"
   height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
   <!-- End Google Tag Manager (noscript) -->
   를 넣고
   태그 추가에, 구글 애널리틱스 유니버셜로 넣었더니, 다른 태그는 안변하고
   < script type="text/javascript" async="" src="https://www.google-analytics.com/analytics.js"></script>
   이 태그가 추가되었다.   
   
   
   
   
   모두 pc버전이다.
   1..픽은 구글태그매니저+태그매니저내에 GA 넣고 그 외에 안넣고
   2., 더쿠는 GTM,GA둘다 안넣고 그냥 애드센스만 넣은것같다.(근데,pagead2.태그가 두개인걸 보니 광고단위를 두개 넣으면 이리되나)
   3. 인스티즈는 기존 유니버셜 애널리틱스 코드 넣었다,(GTM통해서가 아닌 그냥 GA만) 
   4. 디시인은 < script type="text/javascript" async="" src="https://ssl.google-analytics.com/ga.js"></script>
   이것만 3개 써져있네;; 그 외에 애널리틱스, 애드센스 쓰지도 않았다.
   
   모두 모바일버전이다.
   1.
   2. 더쿠
   3. 인스티즈
   4. 디시인
   
   네이버 애널리틱스 가입방법
   https://m.blog.naver.com/PostView.nhn?blogId=sjcafe24&logNo=221403420053&proxyReferer=https:%2F%2Fwww.google.com%2F
   
   구글이랑 네이버 애널리틱스 둘다 사용할경우 각각 직접 코드를 넣지말고
   구글 태그 매니저를 이용해서 네이버 애널리틱스 추적코드를 그 안에 넣어라.
    [참조링크 : https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=1060104&docId=295271035&qb=6rWs6riALOuEpOydtOuyhCDslaDrhJDrpqzti7HsiqQg64+Z7Iuc&enc=utf8&section=kin&rank=1&search_sort=0&spq=0]
 
 .
 구글 애드센스 광고하나 태그 설치하니까(다른 GA태그 GTM태그 아예 안넣음)
 헤드태그에
 < link rel="preload" href="https://adservice.google.co.kr/adsid/integrator.js?domain=www.celebmine.com" as="script">
 < script src="https://www.googletagservices.com/activeview/js/current/osd.js?cb=%2Fr20100101"></script>
 < script src="https://partner.googleadservices.com/gampad/cookie.js?domain=www.celebmine.com&amp;callback=_gfp_s_&amp;client=ca-pub-6944617508996548&amp;cookie=ID%3Dc1f4cd133b8da160%3AT%3D1593743253%3AS%3DALNI_MY4rall5d2M-53H2XA4oGATv25cEw"></script>
 < script src="https://pagead2.googlesyndication.com/pagead/js/r20200624/r20190131/show_ads_impl_fy2019.js" id="google_shimpl"></script>
 < script type="text/javascript" src="https://adservice.google.co.kr/adsid/integrator.js?domain=www.celebmine.com"></script>
 < link rel="preload" href="https://adservice.google.com/adsid/integrator.js?domain=www.celebmine.com" as="script">
 < script type="text/javascript" src="https://adservice.google.com/adsid/integrator.js?domain=www.celebmine.com"></script>
 이 뜨고,
 body 닫힌 태그 바로 앞에
 <ins class="adsbygoogle adsbygoogle-noablate" data-adsbygoogle-status="done" style="display: none !important;"><ins id="aswift_1_expand" style="display:inline-table;border:none;height:0px;margin:0;padding:0;position:relative;visibility:visible;width:0px;background-color:transparent;"><ins id="aswift_1_anchor" style="display:block;border:none;height:0px;margin:0;padding:0;position:relative;visibility:visible;width:0px;background-color:transparent;"><iframe id="aswift_1" name="aswift_1" style="left:0;position:absolute;top:0;border:0;width:undefinedpx;height:undefinedpx;" sandbox="allow-forms allow-pointer-lock allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts allow-top-navigation-by-user-activation" frameborder="0" src="https://googleads.g.doubleclick.net/pagead/ads?client=ca-pub-6944617508996548&amp;output=html&amp;adk=1812271804&amp;adf=1573534164&amp;lmt=1593756851&amp;plat=1%3A32776%2C2%3A32776%2C8%3A32768%2C9%3A32776%2C10%3A32%2C11%3A32%2C16%3A8388608%2C17%3A32%2C24%3A32%2C25%3A32%2C30%3A34603008%2C32%3A32%2C40%3A32&amp;guci=2.2.0.0.2.2.0.0&amp;format=0x0&amp;url=http%3A%2F%2Fwww.celebmine.com%2F&amp;ea=0&amp;flash=0&amp;pra=7&amp;wgl=1&amp;dt=1593756851247&amp;bpp=3&amp;bdt=110&amp;idt=61&amp;shv=r20200624&amp;cbv=r20190131&amp;ptt=9&amp;saldr=aa&amp;abxe=1&amp;cookie=ID%3Dc1f4cd133b8da160%3AT%3D1593743253%3AS%3DALNI_MY4rall5d2M-53H2XA4oGATv25cEw&amp;prev_fmts=991x495&amp;nras=1&amp;correlator=7823933172061&amp;frm=20&amp;pv=1&amp;ga_vid=2078071265.1593658737&amp;ga_sid=1593756851&amp;ga_hid=679898098&amp;ga_fc=0&amp;iag=0&amp;icsg=2218&amp;dssz=7&amp;mdo=0&amp;mso=0&amp;u_tz=540&amp;u_his=3&amp;u_java=0&amp;u_h=864&amp;u_w=1536&amp;u_ah=824&amp;u_aw=1536&amp;u_cd=24&amp;u_nplug=3&amp;u_nmime=4&amp;adx=-12245933&amp;ady=-12245933&amp;biw=1007&amp;bih=695&amp;scr_x=0&amp;scr_y=0&amp;eid=42530493%2C42530495%2C42530499%2C42530501&amp;oid=3&amp;pvsid=207224345668863&amp;pem=165&amp;rx=0&amp;eae=2&amp;fc=896&amp;brdim=1%2C5%2C1%2C5%2C1536%2C0%2C1039%2C815%2C1024%2C695&amp;vis=1&amp;rsz=%7C%7Cs%7C&amp;abl=NS&amp;fu=8208&amp;bc=23&amp;ifi=1&amp;uci=a!1&amp;fsb=1&amp;dtd=67" marginwidth="0" marginheight="0" vspace="0" hspace="0" allowtransparency="true" scrolling="no" allowfullscreen="true" data-google-container-id="a!1" data-load-complete="true"></iframe></ins></ins></ins>
 <iframe id="google_osd_static_frame_5463933817047" name="google_osd_static_frame" style="display: none; width: 0px; height: 0px;"></iframe>
 body 닫힌 태그 다음
 <iframe id="google_esf" name="google_esf" src="https://googleads.g.doubleclick.net/pagead/html/r20200624/r20190131/zrt_lookup.html#" data-ad-client="ca-pub-6944617508996548" style="display: none;"></iframe>
 가 적힌다.
 
 
 
 
 
 
 
 
 
 
 
 