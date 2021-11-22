###[meta property og] url

#####(0).앞서 알아야 할 내용  
.
    1.og(오픈그래프 태그)는 페이스북에서 만든 태그로, 페이스북의 대부분의 콘텐츠는 url로 공유되는데, url입력시 facebook에 콘텐츠가 표시되는 방식을 관리하기
        위해 정보를 제공하는 meta태그를 만들었다. 이는 현제, 네이버(블로그,지식in),티스토리(블로그)와 카카오, 트위터(일부분)에서도 사용되고 있다.
        [참조링크 : https://blog.naver.com/hightch/221995979923]
.
    2.og:url이라 하면, 단순히 표시하고 싶은 url을 적으라 하는데, 그런것이 아니라, '표준링크(The canonical URL)'을 적는거다.
        표준 링크란, 같은 콘텐츠를 가리키는 여러 개의 URL 중에서 대표 하나의 URL을 말하는거다. 네이버 블로그 글이나, 인스티즈 혹은 더쿠의
        글들 모두 보면, 같은글에 해당하는것의 모바일버전 html과 PC버전 html이 각각 og:url로 PC버전 html을 갖고있는 url을 적는다. 
        즉, pc버전의 url을 기준으로 적는것 같다. 또한, 네이버 글의 https://blog.naver.com/PostView.nhn?blogId=ton0070&logNo=221999067935&from=search&redirect=Log&widgetTypeCall=true&directAccess=false
        도, https://blog.naver.com/ton0070/221999067935의 url을 og:url 값으로 갖고있다.
        [참조링크 : https://brunch.co.kr/@jiyeonsongofnt/11]   
        [참조링크 : http://blog.naver.com/classe82/20198541611]
.    
    3.og:url의 기능은 이것 이외에도 또 있다. 네이버 지식in, 네이버 블로그 글쓰기, 트위터는 입력되는 url을 바탕으로 미리보기가 형성되는데,
        티스토리 글쓰기, 페이스북, 카카오톡은 특정url에 og:url 태그가 적혀있으면, 그 og:url의 content에 해당하는 url을 미리보기로 보여준다.
        (PC,모바일,앱 모두 이와 같다.)
.    
#####(1).전체태그
.
    < meta property="og:url" content="~">
.
#####(2).기능
.
    같은 콘텐츠를 가리키는 여러 개의 URL 중에서 대표 하나의 URL을 가리킨다.
.
#####(3).위치
.
    og태그들과 함께 쓴다.
.
####(4).타 웹사이트 태그예시    
. 
        1.인스티즈
            [참조링크 : https://www.instiz.net/pt/6756991]
                <meta property="og:url" content="https://www.instiz.net/pt/6756991">
            [참조링크 : https://www.instiz.net/name/37227136]
                < meta property="og:url" content="https://www.instiz.net/name/37227136">
        2.더쿠
            [참조링크 : https://theqoo.net/cook/1515298974]
                < meta property="og:url" content="https://theqoo.net/cook/1515298974">
        3.디시인사이드
            [참조링크 : https://gall.dcinside.com/board/view/?id=hit&no=15891]
                < meta property="og:url" content="https://gall.dcinside.com/board/view/?id=hit&amp;no=15891">
        4.네이버
            [참조링크 : https://www.naver.com/]   
                < meta property="og:url" content="https://www.naver.com/">
            [참조링크 : https://blog.naver.com/ton0070/221999067935]
                x(못찾음)
        5.셀럽마인
            [참조링크 : http://www.celebmine.com/]   
                x(안썻었음)
            [참조링크 : http://celebmine.com/hi1/detail.html]
                < meta property="og:url" content="http://www.celebmine.com">
.